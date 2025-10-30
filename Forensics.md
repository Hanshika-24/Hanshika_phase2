# FORENSICS
## trivial flag transfer protocol
### My solve
**Flag** `picoCTF{549698}`
```
Here i first used gdb ./debugger0_a command as instructed in the challenge then i used target exec ./debugger0_a command to give the challenge file as target command and after that i used disassemble main to see the assembly code for main.
There i searched for eax register and found load value 0x86342 (hex) which looked something like this:
  0x0000000000001138 <+15>:	mov    $0x86342,%eax
Next, i converted hex to decimal using python3 -c "print(0x86342) command and got the output 549698 which was my flag.
```
### What I learned
I learned about gdb command.

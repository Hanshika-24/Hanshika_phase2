# REVERSE ENGINEERING
## GDB baby step 1
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



## ARMssembly 1
### My solve
**Flag** `picoCTF{00000715}`
```
Here i first used cat cat chall_1.S command to open the challenge file and after analysing it i found that the program prints "You win!" only if func(argument) returns 0:
func(argument) == 0
> 1813 - argument == 0
> argument == 1813
Then, converting 1813 into 32 bit hex i get 00000715 which is my flag.
```
### What I learned
I learned to interpret basic ARM assembly instructions.



## Vault door 3 
### My solve
**Flag** `picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_79958f}`
```
Here, i used cat VaultDoor3.java to open the challenge file and after analysing it i found the program builds a buffer from the supplied 32-char password using four loops, then checks:
new String(buffer).equals("jU5t_a_sna_3lpm18g947_u_4_m9r54f")
Then, i reversed the index mappings from each loop to recover the original password that produced the 32-char input jU5t_a_s1mpl3_an4gr4m_4_u_79958f which is my flag.
```
### What I learned
I learned string manipulation techniques.

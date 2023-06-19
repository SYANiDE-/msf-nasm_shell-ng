# msf-nasm_shell-ng
A slightly imroved wrapper around msf-nasm_shell

Wraps msf-nasm_shell with pexpect to extend nasm_shell with:
newline delimited commands (already had that capability)
semicolon delimited commands
shell loop interactive terminal (retained)
oneshot piped input
oneshot cli arg input
Helpful formatting: oneline c-style hexstring followed by opcode comments

Example output
```
┌──(notroot㉿Business-End)-[~/repos/msf-nasm_shell-ng]
└─$ msf-nasm_shell-ng "push esp; pop eax; ret"

#[.]  push esp\n pop eax\n ret
# 00000000  54                push esp
# 00000001  58                pop eax
# 00000002  C3                ret
# 3 bytes

"\x54\x58\xc3"  # 54 push esp; 58 pop eax; C3 ret # 3 bytes
```
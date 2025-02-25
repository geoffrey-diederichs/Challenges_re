# [48](https://challenges.re/48/)

We are given this win32 function :

```
main:
    push 0xFFFFFFFF
    call MessageBeep
    xor  eax,eax
    retn
```

In the first two instructions, `MessageBeep` is called with `0xFFFFFFFF` as argument. According to [Micorosoft's documentation](https://learn.microsoft.com/en-us/windows/win32/api/winuser/nf-winuser-messagebeep), this corresponds to a single beep. 
The return code of the function stored in `eax` is then deleted using a `xor` before returning.  


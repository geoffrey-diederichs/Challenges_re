# [49](https://challenges.re/49/)

This x64 code snipet is given :

```assembly
main:
        pushq   %rbp
        movq    %rsp, %rbp
        movl    $2, %edi
        call    sleep
        popq    %rbp
        ret
```

The first two instructions are saving the caller's base pointer onto the stack and setting a new base pointer.
It is then calling the function `sleep` with the value `2` as argument. According to the [man](https://man7.org/linux/man-pages/man3/sleep.3.html), this means the program will sleep for 2 seconds.
It is then restoring the caller's base pointer before returning.


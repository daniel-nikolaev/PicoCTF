#ASM 3
Reverse Engineering, 300 points

Contents of test.S:
```assembly
.intel_syntax noprefix
.global asm3

asm3:
	push   ebp
	mov    ebp,esp
	xor    eax,eax
	mov    ah,BYTE PTR [ebp+0x9]
	shl    ax,0x10
	sub    al,BYTE PTR [ebp+0xd]
	add    ah,BYTE PTR [ebp+0xe]
	xor    ax,WORD PTR [ebp+0x12]
	nop
	pop    ebp
	ret    
```
Contents of main.c:
```assembly
#include <stdio.h>

int asm3(int, int, int);

int main(int argc, char* argv[])
{
    printf("0x%x\n", asm3(0xfe8cf7a4,0xf55018af,0xb8c70926));
    return 0;
}
```
Compiling and running:
```assembly
# gcc -masm=intel -m32 -c test.S -o test.o
```
```assembly
# gcc -m32 -c main.c -o main.o
```
```assembly
# gcc -m32 test.o main.o -o main
```
```assembly
# ./main
```

0xe82f

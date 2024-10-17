```nasm
mov al, [a] ;al=22
mov al, [b] 
mov ax, [b] ;ax=1234
mov ax, [a]
mov eax, [b] ;eax=22_0A_12_34
mov ax, [a+1] ;a+1=b=1234
mov bx, [c-2] ;b=12_34
```

>[!info] `res` instructions
>reserves memory
>
>`resb` - byte
>`resw` - word
>`resd` - double 
>`resq` - quad
>`rest` - tetra - 10 bytes

>[!Example]
>`c resd 3` reserves $4\times3=12\text{ bytes}$ (double type reserved 3 times)


```nasm
a db 22h
b db 22h
c dw 2h
d dw 10h

mov ax, [a];ax=22_22
mov bx, 4;bx=00_04
add bx, ax;bx=22_26
mov ax, [b+1];ax=00_02
add ax, [c+1];ax=10_02
mov [c], ax
```

What value will be in AX register after running the following code, if variable a is a word, b and c are bytes and a=5, b=9,  c=4
```
; 05 00 09 04
;   a    b  c 
mov ax, [a] ;ax=00 05
add ax, 20  ;ax=00 19
mov bx, [b] ;bx=04 09
mov bh, 0   ;bx= 00 09
mov [b], b  ;00 09, [b]=bx
add bx, [c] ;
```

>[!Info] `mul` instructions
> `b*b=>w` AX=AL\*Y
> `w*w=>dw`DX:AX=AX\*Y
> `dw*dw=>qw` EDX:EAX=EAX*Y

>[!Info] `div` instructions
> `div Y`
> y-byte
> `ax:y=>AL,AH`
> y-word\
> `(DX:AX):y=DX,AX`
> (Quotient & Remainder)

```nasm
a dw 1
b dw 13
mov ax, [a]
mul [b]
--------
DX:AX
```

```nasm
a dw 7
b dd 9
mov EAX, 0
mov AX, [a]
mul [b]
```

```
a db 8
b dw 40 h
mov AX, [b]
div [a] ;AH=00, AL=05
```

- [ ] 📅 2024-10-14 Homework Lab 2 (don't open parantheses, homework on computer, look at theory&examples (~vancea) n&n+15 from every problem set, 2&17 from the sets)
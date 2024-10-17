# Memory
- `db` - declare byte (8b)
- `dw` - declare word (16b)
- `dd` - declare doubleword (dword) (32b)
- `dq` - declare quadword (qword) (64b)
```nasm
a db 5
b db 10, 20 ;basically an array with 2 elements
ten equ 10  ;ten is a constant
c dw 0123h, 0ABCDh, 0xAB12 ;if a hexa number starts 
						   ;with a letter 
				   ;you must precede it with a 0,
				   ;the assembler will consider it a
				   ;variable         

```
![[Drawing 2024-10-14 16.34.24.excalidraw.svg]]
`a` isn't a value, it is the address of the data segment plus an offset
`ten` doesn't reserve memory
>[!Important] Endianness
>Intel proccessors are little endian, ![[Drawing 2024-10-14 16.40.52.excalidraw.svg]]=$^{15}0000000100100011^{0}$
> The reason for this is that the least significant bits are put first, because they have a lower index
```nasm
a db 001101b       ;binary number
b db 'a', "abcd",0 ;you have to put the null terminator 
				   ;manually
```
## List of registers
- `EAX,EBX,ECX,EDX,ESI,EDI` - all purpose registers
- `ESP, EBP, EIP, EFLAGS` - control registers, don't use
# Instructions
## `MOV` instruction
`mov destination, source`
`MOV EAX, 2; register, immediate`
`MOV EAX, ten; register immediate; <=> MOV EAX, 10`
>[!Important]
>You cannot have both operands of type *memory*

`MOV BYTE [a], 10`
`MOV [a], 10` is wrong because the assembler must know the size to overwrite.
`MOV a, 10` is wrong because it replaces the address, not the content at that address.
`MOV EAX, [a]` will read 4 bytes starting from `a`, (because it knows how big `EAX` is)
`MOV EAX, BYTE [a]` wrong because operand sizes must be equal
`MOV AL, BYTE [a]` 
## `ADD` instruction
`ADD dest, source <=> dest=dest+source`
## `SUB` instruction
`SUB dest, source <=> dest=dest-source`
## `MUL` instruction
`MUL BX<=>BX\*AX=DX:AX`
## `DIV` instruction
`DIV BX ;DX:AX/BX` AX - quotient, DX - Remainder
## Convert instructions for signed numbers
`CBW`, `CWD`, `CWDE`, `CDQ`  (fill the higher part with the most significant digit)
`CBW` AL$\rightarrow$AX (signed conversion)
`CWS` AX$\rightarrow$DX:AX, AX=$1000\ldots1_{(2)}$
				CWD$\implies$ DX$\implies=1111\ldots1111$
`CWDE` AX$\to$ EAX
`CDQ` EAX$\to$EDX:EAX

# Example
```nasm
a db 5
b dw 320 ;a+b
mov AL, BYTE [a]
mov AH, 0
add AX, WORD [b]
```

$5=00000101_{(2)}$
$-5=11111011_{(2)}=FB_{(16)}$ unsigned 251, signed -5 (2's complement) 
# Exercise 
```nasm
data
a db -10
b dw 325
c db 5
d resw 1 ; d = a+b-c
code 
start:
MOV AL, [a]
MOV AH, 0
CBW
ADD AX, [b]
MOV BX, AX
MOV AL, [c]
CBW
SUB BX, AX
MOV [d], BX
```
>[!info] Definition
>Registers are storage capacities, very small in terms of size 8, 16, 32, or 64 bits, but very fast in terms of access speed used for temporary storage of the operands with which a processor currently works. These can be: 
>- Data
>- Commands codes
>- Addresses
>Everything inside these registers is a number

Any architecture has an _Accumulator register_ (AX) and it is the most use in any architecture, and is used by most of the instructions as one of their operands. Now in 32-bit architectures we work with EAX, which is Extended AX.
BX comes from _Base register_, or EBX in 32-bit architectures, it is used as the starting address of an array.
>[!info] Data types
>A data type is a structure + associated operations.

>[!info] Bits & Bytes
>The bit is the smallest unit of representation and the byte is the smallest accessible or addressable unit of memory

>[!info] Data types in assembly language
>The data type in assembly is the **size** of the representation 
> - byte = 8 bits
> - word = 16 bits
> - doubleword = 32 bits
> - quadword = 64 bits

>[!info] Data definition directives
>``` nasm
>a db 8 ;byte initialized with the value of 8, variable called a
>   dw   ;word
>   dd   ;doubleword
>   dq   ;quadword
>```
>A 32-bit architecture cannot directly work with 64 bits, instead it splits them in two halves.

ECX is the *Counter register* and it is mostly used as the numerical upper limit for instructions that need repetitive runs.
EDX is the *Data register* is frequently used with other registers (mostly with EAX) when the result exceeds a doubleword 
There is a special bit called a *carry flag* which is used when performing additions and subtractions $b\pm b\rightarrow b$, $w\pm w\rightarrow w$ etc.
For multiplications $b\times b\rightarrow w$, $w\times w\rightarrow dd$, $dd\times dd\rightarrow dq$

>[!Important] Explanation for carry flags and why byte times byte result in a word
>In base 10 arithmetic if we have 2 operands, say $a$ and $b$ with $m$ and $n$ digits, for addition we can say that the max number of digits of $a+b$ is $max(m,n)+1$ ($1$ only sometimes, when we go over an order). For multiplication $a\times b$ we have $m+n$ digits.
>For multiplication we will never have overflow because we already have enough space reserved. It will exist in addition, subtraction and division (Explanation in later lectures)

For the multiplication of 2 double words, which results in a quad word, the register __EDX__ is used, the quadword.
>[!info] Multiplication and division
>These two operations have one explicit operand, the divisor and the multiplicator. At a lower level for a quad word we will have EDX:EAX, when dividing by a word we have DX:AX/word and AX/byte

![[Excalidraw/Drawing 2024-10-07 09.20.24.excalidraw.svg]]
ESP - *Stack Pointer* (points to the top of the stack), EBP - *Base Pointer* (points to the bottom of the stack) are the stack registers
The stack, queue and heap are the 3 basic data structures
![[Drawing 2024-10-10 19.33.57.excalidraw.svg]]
SS - *Stack Segment* - Shows the currently active Stack Segment

>[!IMPORTANT] For exam!
>Why do we have 3 (out of 17) registers for the stack but none for queue and heap. Every execution takes place in the runtime stack. The order is always a LIFO order (think child/parent processes). 

At the beginning of the execution EBP and ESP point to the same address. While more data is added to the stack ESP grows bigger. When a new procedure is started EBP is saved and starts pointing to the current location of ESP.

At any given moment there is only 1 given Data segment, 1 Code segment, 1 Stack segment and 1 extra segment.

ESI - *Source index*, EDI - *Destination index*  they are used to keep the index of an "array" (arrays don't exist in assembly). We have 2, source and destination in the case we operate on 2 arrays (think `strcpy` in C++)
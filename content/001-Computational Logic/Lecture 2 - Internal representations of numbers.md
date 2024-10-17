- Integers
	- Unsigned
	- Signed
- Fixed point
- Floating point
# Binary representation of integers
>[!Important] 
>In case of overflow the most significant bits are lost
## Formulas
$$\begin{gathered}
1\underbrace{0\ldots0_{(2)}}_n=2^n\\
\underbrace{1\ldots1}_n=1\underbrace{0\ldots0}_{n}-1=2^n-1\\
0,\underbrace{0\ldots0}_{n-1}1=2^{-n}\\
0,\underbrace{1\ldots1}_{n}=1,\underbrace{0\ldots0}_n-0,\underbrace{0\ldots1}_{n-1}=1-2^{-n}
\end{gathered}

$$
>[!Important]
>Direct codes are the same as inverse and complementary codes for positive numbers, they differ only for negative numbers

The bits in the leftmost square are the sign bits

$[80]_{dir}=[80]_{inv}=[80]_{compl}=$![[Drawing 2024-10-10 14.23.05.excalidraw.svg]]
$[-80]_{dir}$=![[Drawing 2024-10-10 14.17.47.excalidraw.svg]]
$[-80]_{inv}=$![[Drawing 2024-10-10 14.25.07.excalidraw.svg]]
$[-80]_{compl}=$![[Drawing 2024-10-10 14.27.58.excalidraw.svg]]
>[!Important]
> - The formula for inverse codes (for negative numbers) is as follows $2^n-1-|x|$, or just flip all the bits of the direct code
> - The formula for the complementary code (for negative numbers) is as follows $2^n-|x_{(2)}|$, or $[x]_{\text{inv}}+1$

>[!Important]
>You cannot obtain the absolute value from the complementary code 
> To convert from complement form to direct form you have to subtract 1 and flip all the bits (basically you convert to inverse form and then to direct form), or just flip the bits until the least significant active bit (without flipping that last one)
> 
![[Drawing 2024-10-10 14.39.25.excalidraw.svg]]
# Subunitary convention
$$x=\frac{11}{16}=11\times16^{-1}=0,B_{(16)}=0,1011_{(2)}$$
$[\frac{11}{16}]_{\text{dir}}=[\frac{11}{16}]_{\text{inv}}=[\frac{11}{16}]_{\text{compl}}=$![[Drawing 2024-10-10 14.47.28.excalidraw.svg]]
$[\frac{-11}{16}]_{\text{dir}}=$![[Drawing 2024-10-10 14.49.56.excalidraw.svg]]
(same rules as for integers apply for inverse and complementary form)
# Fixed point representation
I is the number of integer bits, F is the number of fractional bits and we also have a sign bit
The minimum absolute value is $2^{-F}$ and the maximum absolute value is $2^I-2^{-F}$
# Floating point representation of real numbers
>[!Important]
>Any real number can be written as $x=\pm 0,m\times b^e$, where $m$ is mantissa, $b$ is the numeration base and $e$ is exponent
## IEEE 754 standard
$e$ is the number of digits in the whole part (in binary)

# Exercise 
$? x \text{ having } C1DE0000_{(16)} \text{as it FP, SP}, m\gt 1$
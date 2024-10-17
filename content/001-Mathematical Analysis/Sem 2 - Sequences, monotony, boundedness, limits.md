# Exercise 1.
Prove using the $\varepsilon$-definition that $\lim\limits_{n\rightarrow\infty}\frac{1}{\sqrt n}$
$$\forall\varepsilon\gt0,\exists N_{\varepsilon}\in\mathbb{N}\text{ s.t. } |\frac{1}{\sqrt n}|\lt\varepsilon,\forall n\geq N_\varepsilon$$
Let $\varepsilon\gt 0$. Take $N_\varepsilon=[\frac{1}{\varepsilon^2}]+1$
$$\frac{1}{\sqrt n}\lt \varepsilon, n\geq N_\varepsilon$$
$$\frac{1}{n}\lt \varepsilon^2, n\gt \frac{1}{\varepsilon^2},\forall n\geq N_\varepsilon$$
$$n\geq N_\varepsilon\gt \frac{1}{\varepsilon^2}$$
# Exercise 2.
## A. $x_n=\sqrt{n+1}-\sqrt n$
$x_n=\sqrt{n+1}-\sqrt n= +\frac{n+1-n}{\sqrt{n+1}+\sqrt n}=\frac{1}{\sqrt{n+1}+\sqrt n}$
$x_n\gt0, x_n\lt x_0=1, n\geq0\implies x_n\in[0,1] (*)$
$\frac{x_n+1}{x_n}=\frac{\sqrt{n+1}+\sqrt{n}}{\sqrt{n+2}+\sqrt{n+1}}\lt 1, \sqrt n\lt\sqrt{n+2}$
$x_{n+1}\lt x_n$ (decreasing) $(**)$
$(*)+(**)\implies (x_n) convergent, x_n\rightarrow0$
## B. $x_n=\frac{1}{1\times2}+\ldots+\frac{1}{n(n+1)}$
$\frac{2-1}{1\times 2}+\frac{3-2}{2\times 3}+\ldots+\frac{(n+1)-n}{n(n+1)}=$
$1-\frac{1}{2}+ \frac{1}{2}-\frac{1}{3}+\ldots+\frac{1}{n}-\frac{1}{n+1}=1-\frac{1}{n+1}\lt1\implies$
$\implies x_n\in (0,1),\text{ bounded} (*)$
$x_{n+1}-x_n=\frac{1}{(n+1)(n+2)}\gt 0, x_{n+1}\gt x_n(**)$
$(*),(**)\implies\text{ convergent}$
## C. $x_n=\frac{2^n}{n!}$
$x_n\gt0$
$\frac{x_{n+1}}{x_n}=\frac{2^{n+1}}{(n+1)!}\times \frac{n!}{2^n}=\frac{2}{n+1}\lt 1$
$x_n\in (0,x_1], x_{n+1}\lt x_n,n\geq2\implies (x_n)\text{ convergent}$
# Exercise 3.
## A. $\sqrt n(\sqrt{n+1}-\sqrt{n})$
$\lim\limits_{n\to\infty}\sqrt n(\sqrt{n+1}-\sqrt{n})\overset{\infty\times0}{=}\lim\limits_{n\to\infty}\frac{\sqrt n}{\sqrt{n+1}+\sqrt n}=\lim\limits_{n\to\infty}\frac{\sqrt n}{\sqrt n\left( \sqrt{1+\frac{1}{n}}+1 \right)}=\frac{1}{2}$
## B. $\frac{2^n+(-1)^n}{3^n}$
$\lim\limits_{n\to\infty}\frac{2^n+(-1)^n}{3^n}=\lim\limits_{n\to\infty}\left( \frac{2}{3} \right)^n+\lim\limits_{n\to\infty}(-\frac{1}{3})^n=0+0=0$
## C. $\sqrt[n]{n}$
 $\lim\limits_{n\to\infty}\sqrt[n]{n}=\lim\limits_{n\to\infty}n^{\frac{1}{n}}\overset{\infty^0}{=}$
 >[!Info] Using $e$ for $\infty^0$
 >$e^{\ln x}=x,\quad f^g=e^{ln f^ g}=e^{g\ln f}$
 
 $n^{\frac{1}{n}}=e^{\frac{\ln n}{n}}\rightarrow e^0=1$
 $\lim\limits_{n\to\infty}\frac{\ln n}{n}\overset{S.C.}{=}\lim\limits_{n\to\infty}\frac{\ln \frac{n+1}{n}}{n+1-n}\ldots$
## E. $(2^n+3^n)^{\frac{1}{n}}=\left( 3^n\left( 1+\left( \frac{2}{3} \right)^n \right) \right)^{\frac{1}{n}}=3\times 1$
$(a_1^n+a_2^n+\ldots+a_k^n)^{\frac{1}{n}}$
$a_i=max\{a_1,\ldots,a_k\}$
$=a_i\left[ \left( \frac{a_1}{a_i} \right)^n+\ldots + \left( \frac{a_k}{a_i} \right)^n \right]^{\frac{1}{n}}$
$(\frac{a_j}{a_i})^n\rightarrow0,j\not=i$
# Exercise 5.
## A. $(\frac{2n+1}{2n-1})^n$
$=[(1+\frac{2}{2n-1})^{\frac{2n-1}{2}}]^{\frac{2n}{2n-1}}$
## B. $n(\ln(n+2)-\ln(n+1)$
$n\ln\frac{n+2}{n+1}=\ln(\frac{n+2}{n+1})^n=\ln\underset{\to 3}{[(1+\frac{1}{n+1})^{n+1}]^{\frac{n}{n+1}\to1}}\to \ln e=1$
# Exercise 6. 
## A.
$\lim\limits_{n\to\infty}\frac{x_1+\ldots+x_n}{n}\overset{S.C.}{=}\lim\limits_{n\to\infty}\frac{x_{n+1}}{n+1-n}=\lim\limits_{n\to\infty}x_n$
$\exists \lim\limits_{n\to\infty}\frac{x_1+\ldots+x_n}{b}, \text{ but}\nexists\lim\limits_{n\to\infty}x_n$
$x_n=(-1)^n,\nexists\lim\limits_{n\to\infty}x_n$
$$

\frac{x_1+x_2+\ldots+x_n}{n}=\begin{cases}
0,\text{n even}\\
-\frac{1}{n},\text{ n odd}
\end{cases}
\implies\lim\limits\frac{x_1+\ldots x_n}{n}=0
$$
## B.
$\lim\limits_{n\to\infty}\frac{1+\frac{1}{2}+\ldots+\frac{1}{n}}{n}\overset{S.C.}{=}\lim\limits_{n\to\infty}\frac{\frac{1}{n+1}}{1}=0$
$\lim\limits_{n\to\infty}\frac{1+\frac{1}{2}+\ldots+\frac{1}{n}}{\ln n}\overset{S.C.}{=}\lim\limits_{n\to\infty}\frac{\frac{1}{n+1}}{\ln \frac{n+1}{n}}=\lim\limits_{n\to\infty}\frac{}{n\ln\frac{n+1}{n}}\times\frac{n}{n+1}=\lim\frac{1}{\ln\left( 1+\frac{1}{n} \right)^n}\times \frac{n}{n+1}=1\times1=1$
# Exercise 7.
$l=\lim\limits_{n\to\infty}\frac{x_{n+1}}{x_n}$
$\sqrt[n]{x_n}=x_n^{\frac{1}{n}}=e^{\frac{1}{n}\ln x_n}=e^{\frac{\ln x_n}{n}}\to e^{\ln e}=e$
$\lim\limits_{n\to\infty}\frac{\ln x_n}{n}\overset{S.C.}{=}\lim\limits_{n\to\infty}\frac{\ln x_{n+1}-\ln x_n}{n+1-n}=\lim\limits_{n\to\infty}\ln\frac{x_{n+1}}{x_n}=\ln \lim\limits_{n\to\infty}\frac{x_{n+1}}{x_n}=\ln e$
# Exercise 8.
## A. 
$\frac{n}{\sqrt[n]{n!}}=\sqrt[n]{\frac{n^n}{n!}}=\sqrt[n]{x_n}\implies \lim\limits_{n\to\infty}\sqrt[n]{x_n}=\lim\limits_{n\to\infty}\frac{x_{n+1}}{x_n}=e$
$\lim\limits_{n\to\infty}\frac{x_{n+1}}{x_n}=\lim\limits_{n\to\infty}\frac{(n+1)^{n+1}}{(n+1)!}\times\frac{n!}{n^n}$
$\lim\limits_{n\to\infty}\frac{(n+1)^n}{n^n}=\lim\limits_{n\to\infty}\left( \frac{n+1}{n} \right)^n=\lim\limits_{n\to\infty}(1+\frac{1}{n})^n=e$

A sequence is a set $\{x_n|n\in\mathbb{N}\}$, denoted by $(x_n)_{n\in\mathbb{N}}$ or simply $(x_n)$. A sequence $(x_n)$ is:
- bounded (above or below) if the set $\{x_n|n\in\mathbb{N}\}$ is bounded
- increasing if $x_{n+1}\geq x_n,\forall n \in\mathbb{N}$
- monotone if it is either increasing pr decreasing
A sequence $(x_n)$ has a limit $l\in\overline{\mathbb{R}}$, and we write $\lim\limits_{n\rightarrow\infty}=l$ or $x_n\rightarrow l$
$$\forall V\in \mathcal V(l),$$
- [ ] 🔼  Finish completing this using lecture notes

> [!info] Proposition
> Any convergent sequence is bounded

>[!note] Proof
> Let $(x_n) \text{ convergent to }l\in mathbb{R}$. Let $\varepsilon=1$. Then since $x_n\rightarrow l, \exists N_1\in \mathbb{N}$, 
> $|x_n-l|\lt 1,\forall n\geq N_1$
> $x_n\in(l-1,l+1)\forall n\geq N_1\implies \text{ bounded (starting from } N_1\text{)}$
> $M=max|x_n|, n=\overline{1,N_1}$ 
> $(x_n)$ is bounded by max $\{l+1, M\}$

>[!info] Theorem (Weierstrass)
>Any monotone and bounded sequence is convergent 

>[!note] Proof
>let $(x_n)$ increasing and bounded. 
>$$x_1\leq x_2\leq\ldots\leq x_n\leq x_{n+1}\leq \ldots$$
>$A=\{x_n|n\in\mathbb{N}\}=(x_n)$, bounded
>$\forall\varepsilon\gt 0, \exists N\in\mathbb{N} \text{ s.t. }: sup(A)-\varepsilon\leq x_N\leq sup(A)$
>$sup(A)-\varepsilon\lt x_N\leq x_n\leq sup(A),\forall n\geq N$
>$|x_n|-sup(A)\lt\varepsilon, \forall n\in \mathbb{N}\implies sup(A)=\lim\limits_{n\rightarrow\infty} x_n$

>[!info] Proposition
>Any monotone sequence has a limit in $\overline{\mathbb{R}}$.

>[!note] Proof
>$(x_n)$ monotone
>a. $(x_n)$ is bounded $\overset{\text{Weierstrass}}{\implies}{} (x_n) \text{ is convergent}$
>b. $(x_n)$ is unbounded $\implies x_n\rightarrow\{\pm\infty\}$

>[!info] Theorem (Squeeze/Sandwich theorem)
>Let $(x_n), (y_n), (z_n)$ be sequences fpr which there exists $n_0\in\mathbb{N}$ such that $$x_n\leq y_n \leq z_n\forall n\geq n_0$$
>and $$\lim\limits_{n\rightarrow\infty}x_n=\lim\limits_{n\rightarrow \infty}z_n$$ Then
>$$\lim\limits_{n\rightarrow\infty}x_n=\lim\limits_{n\rightarrow\infty}y_n=\lim\limits_{n\rightarrow \infty}z_n$$


>[!Note] Proof
>$x_n\rightarrow l:\quad \exists N_1\in\mathbb{N}:\ |x_n-l|\lt\varepsilon,\forall n\geq N_1, x_n\in(l-\varepsilon,l+\varepsilon)$
>$z_n\rightarrow l:\quad \exists N_w\in\mathbb{N}:\ |z_n-l|\lt\varepsilon,\forall n\geq N_2, z_n\in(l-\varepsilon,l+\varepsilon)$
>$\implies x_n,z_n\in (l-\varepsilon,l+\varepsilon)\forall n\geq max\{N_1,N_2\}=N$
>$\implies y_n\in (l-\varepsilon,l+\varepsilon),\forall n\geq N, |y_n-l|\lt\varepsilon$

>[!info] Theorem (Cantor's nested intervals)
>Let $(a_n)$ be increasing and $(b_n)$ be decreasing such that $$a_n\leq a_{n+1}\leq b_{n+1}\leq b_n,\forall n\in\mathbb{N}.$$ Consider the closed intervals $$I_n\coloneqq [a_n,b_n],\ with I_{n+1}\subseteq I_n.$$ If $\lim\limits_{n\rightarrow\infty}(b_n-a_n)=0$, then there exists $x\in\mathbb{R}$ such that $$\bigcap\limits_{n=1}^{\infty} I_n=\{x\}$$

^8f48cc

>[!note] Proof
>Found in lecture notes

>[!note] Theorem (Bolzano-Weierstrass)
>Any bounded sequence has a *convergent subsequence*

>[!info]  Subsequences
>For any sequence $(x_n)_{n\in\mathbb{N}}$, subsequences are basically a rule, i.e. $(x_{2n}), (x_{2n+1}), (x_{n^2})$. $(x_i)_{i\in I},\  I\leq\mathbb{N}\text{ infinite}$.  It is sometimes written as $(x_{n_k}), k\in \mathbb{N}$

Hint for proof: [[Divide et Impera]] + [[#^8f48cc|Cantor's nested intervals]], $x_{n_1}\in [a_1,b_1], x_{n_2}\in [a_2,b_2], \ldots, x_{n_k}\in[a_k,b_k]$

>[!note] Proof
>$(x_n)$ is bounded $\implies inf(x_n), sup(x_n)\in\mathbb{R}$
>Let $a_1=inf(x_n), b_1=sup(x_n)$
>$x_n\in [a_1,b_1],\forall n\in \mathbb{N}$
>Divide $[a_1,b_1]$ into 2 equal intervals
>Choose the one that contains an infinity of terms $(x_n)$.
>$[a_2,b_2], b_2-a_2=\frac{b_1-a_1}{2}, [a_2,b_2]\subseteq[a_1,b_1]$
>Iteration $[a_k,b_k], b_k-a_k=\frac{b_1-a_1}{2^{k-1}}\rightarrow 0, \text{ as } k\rightarrow \infty$
>$\lim\limits_{k\rightarrow\infty}x_{n_k}=\{x\}=\bigcap\limits_{k=1}^\infty[a_k,b_k]$

>[!info] Definition
>For a sequence $(x_n)$ we define the set of its *limit points* by $$LIM(x_n)\coloneqq\{x\in\overline{\mathbb{R}}|\text{ there exists a subsequence }(x_{n_k})\text{ s.t. } x_{n_k}\rightarrow x\}$$ and 
>$$\begin{gathered}
>\lim_{n\rightarrow\infty} inf\ x_n\coloneqq inf(LIM(x_n)),\\
>\lim_{n\rightarrow\infty} sup\ x_n\coloneqq sup(LIM(x_n)),\\
>\end{gathered}$$

>[!Example]
> $x_n=\frac{(-1)^n n}{n+1},\quad -\frac{1}{2},\frac{2}{3},-\frac{3}{4},\frac{4}{5},\ldots$ $$x_{2n}=\frac{2n}{2n+1}\rightarrow 1,\ x_{2n+1}=-\frac{2n+1}{2n+2}\rightarrow -1$$
> 
> $$LIM(x_n)=\{-1,1\},\lim\limits_{n\rightarrow\infty}inf\ x_n=-1, \lim\limits_{n\rightarrow\infty}sup\ x_n=1$$

>[!info] Definition (Cauchy sequence)
>A sequence $(x_n)$ is called *Cauchy (or fundamental)* if $$\forall\varepsilon\gt0,\exists N_\varepsilon\in\mathbb{R}\text{ such that } |x_m-x_n|\lt\varepsilon,\forall m,n\geq N_\varepsilon$$

>[!note] Proposition
>Any *Cauchy sequence is bounded*

>[!note] Proof
> Let $\varepsilon=1: \exists N_1\in\mathbb{N}\text{ s.t. } |x_n-x_m|\lt 1,\forall n,m\geq N_1$
> In particalular $|x_n-x_{N_1}|\lt 1,\forall n\geq N_1\implies (x_n)\text{ is bounded. } x_n\in (x_{N_1}-1,x_{N_1}+1)$

>[!info] Theorem
>A *sequence is convergent* if and only if it is *Cauchy*

>[!note] Proof
>$A\Leftrightarrow B: A\implies B, B\implies A$
> Convergent $\implies$ Cauchy
> Let $l=\lim\limits_{n\rightarrow\infty}x_n$
> $$\forall \varepsilon\gt0, \exists N_\varepsilon\in\mathbb{N}\text{ s.t. } |x_n-l|\lt\frac{\varepsilon}{2},\forall n\geq N_\varepsilon$$
> $$|x_n-x_m|=|x_n-l+l-x_m|\leq \underbrace{|x_n-l|}_{\lt\frac{\varepsilon}{2}}+\underbrace{|x_m-l|}_{\lt\frac{\varepsilon}{2}}\lt \varepsilon, \forall n,m\geq N_\varepsilon\implies (x_n) \text{ is Cauchy }$$
\3.  Proof 1
$$\begin{align}
-S\coloneqq\{-x|x\in S\}
 \text{Let } d=sup(S)\Leftrightarrow d&\geq x,\forall x\in S\\
 d&=min(ub(S))\\
 &\text{if } u\gt x,\forall x\in S \text{ then } u\geq d\Leftrightarrow -u\leq-d (3)\\
 d\geq x\leftrightarrow-d\leq-x\\
 -d\in lb(-S) (1)
 u\geq x\Leftrightarrow-u\leq-x\implies-u\in lb(-S) (2)\\
 (1),(2),(3)\implies -d=inf(-S)
 \end{align}
$$Proof 2 (less rigorous)
$$
\begin{align}
ub(S)=[sup(S),\infty)\\
lb(-s)=[-\infty, -sup(S)]\\
\implies inf(-s)=-sup(S)
\end{align}
$$4. Let $f : D → \mathbb{R}$ and $g : D → \mathbb{R}$ be two functions defined on a nonempty set $D$. Prove that
$$\underset{x\in D}{inf} (f(x)+g(x)\geq \underset{x\in D}{inf}f(x)+\underset{x\in D}{inf}g(x)$$
and
$$sup_{x\in D}(f(x)+g(x)\leq sup_{x\in D}f(x)+sup_{x\in D}g(x)$$Give examples where the above inequalities are strict.
Solution: 
$$\begin{align}
f(x)\leq \underset{x\in D}{sup\ f(x)}=F, \forall x\in D\\
g(x)\leq \underset{x\in D}{sup\ g(x)}=G, \forall x\in D\\
f(x)+g(x)\leq F+G\forall x\in D\implies sup(f(x)+g(x))\leq F+G\\
\\
D=[0,1], x\in D\\ 
f(x)=x, sup\ f(x)=1\\
g(x)=-x, sup\ g(x)=0
f(x)+g(x)=0
\end{align}
$$
>[!info] Definition
>$V$ is a neighborhood of $x\in R$ if $\exists\varepsilon\gt 0 \text{ s.t. } (x-\varepsilon,x+varepsilon)\subseteq V$
 
 6.  Which of the following sets are neighborhoods of 0?
	 a. $[-1,1]\cup\{2\}$
	 $$\begin{align}
	 \varepsilon= \frac{1}{2},\ (-\frac{1}{2},\frac{1}{2})\subseteq[-1,1]\cup\{2\}\\
	 \end{align}
	 $$ 
	 b. $(-1,2)\cup\mathbb{Q}$
	 $$\begin{align}
	\nexists\varepsilon\text{ s.t. } (-\varepsilon,\varepsilon)\subseteq(-1,1)\cup\mathbb{Q}
	 \end{align}
	 $$
	 c.  $\bigcap_{n=1}^\infty[-\frac{1}{n},\frac{1}{n}]$
	 $$\begin{align}
	 \bigcap_{n=1}^\infty[-\frac{1}{n},\frac{1}{n}]=0\\
	 0\in[-\frac{1}{n},\frac{1}{n}], \forall n\geq1
	 \end{align}$$
	7. Let $x \in \mathbb{R}$ and $U, V \in \mathcal{V}(x)$. Prove that $U \cup V \in \mathcal{V}(x)$.
			$$\begin{align}
			U \cup V \in \mathcal{V}(x),&\exists\varepsilon_1,\text{ s.t. } (x-\varepsilon_1, x+\varepsilon_1)\subset\mathcal{V}\\
			&\exists\varepsilon_2,\text{ s.t. } (x-\varepsilon_2, x+\varepsilon_2)\subset\mathcal{V}\\
			Let\ \varepsilon=min(\varepsilon_1,\varepsilon_2)\\
			(x-\varepsilon,x+\varepsilon)\subset U,V\implies\\
			\implies (x-\varepsilon, x+\varepsilon)\subset U\cup V\implies U\cup V\in\mathcal{V}(X)
			\end{align}
			$$$
- [ ] 📅 2024-10-14 ⏫ exercises 5,8,10
>[!info] Interiors & Closures
>$$int(A)=\{x\in\mathbb{R}:\exists V\in\mathcal{V}(x), V\subseteq A\}$$
>If you take any number in the interior you can find a neighborhood inside the set A
>$$(0,1], 0\notin int(A), 1\notin int(A), int(A)=(0,1)$$
>$$cl(A)=\{x\in\mathbb{R}:\exists V\in\mathcal{V}(x), V\cup A\not=0\}$$
>So an element is in the closure if any neighborhood will intersect the set A
>$$cl(0,1]=[0,1], o\in(0,1]$$

1. Find the interior and the closure for each of the following sets:
	a. $(1,2]=A$
		$$int(A)=(1,2),\ cl(A)=[1,2]$$
		b. $[-3,2)\cup\{3\}=B$
		$$int(B)=(-3,2),\ cl(B)=(-3,3)$$
		c. $(-1,1]\cup(2,\infty)=C$
		$$int(C)=(-1,1)\cup(2,\infty),\ cl(A)=[-1,1]\cup[2,\infty)$$
		d. $(-5,5)\cup\mathbb{Z}=D=\{-4,-3,\ldots,3,4\}$
		Since for any interval that we take there will always be neighborhoods that aren't subsets of $D$ (because we have only whole numbers) $int(A)=\emptyset$
		$$cl(D)=D$$
		
# Syllabus
- Real numbers 
- Sequences
- Series of real numbers
- Power series
- Functions of one variable: limits, continuity, differentiability
- Higher Order derivatives
- Taylor series
- Riemann integrals
- Improper integrals
# Real numbers
>[!info] Definition
>Let $A\subseteq \mathbb{R}$. We define $x\in \mathbb{R}$ to be
>		- a *lower bound* for $A$ if $x\leq a,\ \forall a\in A$
>		- an *upper bound* for $A$ if $x\geq a,\  \forall a\in A$
>	- $lb(A)\coloneqq\{x\in\mathbb{R}|x\leq a,\forall a\in A\}$, the set of lower bounds of A.
>	- $ub(A)\coloneqq\{x\in\mathbb{R}|x\geq a,\forall a\in A\}$, the set of upper bounds of A.

>[!info] Definition
>A set $A\subseteq\mathbb{R}$ is defined to be
>	- bounded (from) below if $lb(A)\not = \emptyset$
>	- bounded (from) above if $ub(A)\not = \emptyset$

>[!info] Definition
>We say that $x\in\mathbb{R}$ is the *supremum* of $A\subseteq\mathbb{R},\ x\coloneqq sup(A)$, if and only if 
>	1. $x\geq a,\forall a\in A$, that is $x\in ub(A)$ 
>	2. if $u$ is an upper bound for $A$, then $x\leq u$
>The supremum is the *least upper bound*, i.e. $sup(A)\coloneqq min(ub(A))$

>[!info] Definition
>We say that $x\in\mathbb{R}$ is the *infimum* of $A\subseteq\mathbb{R},\ x\coloneqq inf(A)$, if and only if 
>	1. $x\leq a,\forall a\in A$, that is $x\in lb(A)$ 
>	2. if $u$ is an lower bound for $A$, then $x\geq u$
>The supremum is the *greatest lower bound*, i.e. $inf(A)\coloneqq max(lb(A))$

>[!Example]
>Find $sup(A), max(A), inf(A), min(A)$ for the following:
>1. $A=\{\frac{1}{n} | n\in\mathbb{N}\}$
>2. $A=\{x\in\mathbb{Q}|x^2\leq 2\}$
>>>[!note] Solution
>>1. $A=\{\frac{1}{n} | n\in\mathbb{N}\}=\{1,\frac{1}{2},\frac{1}{3},\frac{1}{4}\dots\}$
>> 	1. $sup(A)=1=max(A)$
>> 	2. $inf(A)=0$
>>	1. $lb(A)=(-\infty,0]$
>>	2. $\nexists\ min(A)$
>>2. $A=\{x\in\mathbb{Q}|x^2\leq 2\}=[-\sqrt{2},\sqrt{2}]\cap\mathbb{Q}$
	>>	1. $sup(A)=\sqrt 2,\ \nexists\ max(A)$
	>>	2. $inf(A) = -\sqrt{2},\ \nexists min(A)$



>[!info] Definition 
>*Completeness Axiom*
>Every set $A\subseteq\mathbb{R}$ that is bounded above has a supremum. Similarly, every set $A\subseteq\mathbb{R}$ that is bounded below has an infimum.

>[!info] Theorem
>Let $A\subseteq\mathbb{R}$ be a *bounded* set. For $sup(A)$ and $inf(A)$ the *following* are true:
>$$\forall\varepsilon\gt 0,\ \exists x\in A\ \text{ such that } sup(A)-\epsilon\lt x$$
>$$\forall\varepsilon\gt 0,\ \exists x\in A\ \text{ such that } x<inf(A)+\epsilon$$
>>[!Proof]
>> By definition, for any $y < sup(A)$, say $y = sup(A) − \varepsilon$ with $\varepsilon > 0$, we have that
$y \notin ub(A)$. Hence there exists $x\in A$ such that $y < x$. Similar proof for $inf(A)$.

> [!info] Proposition
>
> Let $A\subseteq B\subseteq\mathbb{R}$ be *(nonempty) bounded sets*. Then 
> $$inf(B)\leq inf(A)\leq sup(A)\leq sup(B)$$  
> 	and $$\begin{aligned}
> 	sup(A\cup B)=max\{sup(A),sup(B)\} \\ inf(A\cup B)=min\{inf(A),inf(B)\}\end{aligned}$$

>[!info] Definition
>Define the *extended real line* $\overline{\mathbb{R}} \coloneqq\mathbb{R}\cup\{-\infty,\infty\}$ where $\infty$ and $-\infty$ are such that $$\forall x\in \mathbb{R}, -\infty\lt x\lt \infty$$
>If a set $A$ is not bounded above, we define $sup(A)\coloneqq\infty$
>If a set $A$ is not bounded below, we define $inf(A)\coloneqq-\infty$

>[!info] Definition
>A set $V\subseteq\mathbb{R}$ is a *neighborhood (vecinity)* of $x\in\mathbb{R}$ if $$\exists\varepsilon\gt 0\ \text{ such that }\ (x-\varepsilon,x+\varepsilon)\subseteq V$$
>A set $V\subseteq\mathbb{R}$ is a neighborhood of $\infty$ if $\exists a\in\mathbb{R}\text{ such that }\ (a,\infty)\subseteq V$
>
>A set $V\subseteq\mathbb{R}$ is a neighborhood of $-\infty$ if $\exists a\in\mathbb{R}\text{ such that }\ (-\infty,a)\subseteq V$
>$$\mathcal{V}(x)\coloneqq\{V\subseteq\mathbb{R}|\text{V is a neighborhood of x}\}$$

>[!info] Definition
>Let $A\subseteq\mathbb{R}$. the following set is called the *interior* of $A$
>$$int(A)\coloneqq\{x\in\mathbb{R}|\exists V\in \mathcal{V}(x)\text{ such that } V\subseteq A\}$$
>and the following set is called the *closure*
>$$cl(A)\coloneqq\{x\in\mathbb{R}|\forall V\in\mathcal{V}(x)\text{ such that } V\cap A\not = 0\}$$

>[!info] Proposition
> For any $A\subseteq\mathbb{R}$, it holds that $int(A)\subseteq A\subseteq cl(A)$.
> >[!note] Proof
> >To prove that $int(A) \subseteq A$  we prove that if $x \in int(A)$, then $x \in A$. Let $x \in int(A)$,
then $\exists \varepsilon \gt 0$ such that $(x − \varepsilon, x + \varepsilon) \subseteq A$. Since $x \in (x − \varepsilon, x + \varepsilon)$, we have that $x \in A$.
To prove that $A \subseteq cl(A)$ we show that if $x \in A$, then $x \in cl(A)$. Let $x \in A$. Then for any $V \in \mathcal{V}(x)$ it holds that $x \in V$, giving that $x \in V \cup A$. Hence $x \in cl(A)$ since $V\in A \not= \emptyset$.

>[!info] Definition
> If $A=int(A)$ then $A$ is called *open*. If $A=cl(A)$, then $A$ is called *closed*.

>[!hint] Remark
>To prove that a set $A$ is open, it is sufficient to prove that $A\subseteq int(A)$. To prove that a set $A$ is closed, it is sufficient to prove that $cl(A)\subseteq A$.


>[!info] Proposition
>The following statements are true
 >- The complement of an open set is closed.
 >- The complement of a closed set is open.
 >>[!note] Proof
 >>Let us prove the first statement, the other one being similar. Consider $A$ an open
set, i.e. $A = int(A)$, and denote by $A^c = \{x \in \mathbb{R} | x \notin A\}$ its complement. To prove that
$A^c$ is closed, we prove that $cl(A^c) \subseteq A^c$. Consider $x \in cl(A^c)$ and let’s assume that $x \notin A^c$,
i.e. $x \in A$, aiming to obtain a contradiction. Since $A$ is open, there exists $V \in \mathcal{V}(x)$ such
that $V \subseteq A$, giving that $V \cup A^c = \emptyset$: contradiction with $x \in cl(A^c)$. Hence the assumption
$x\in A^c$ is false, and we have that if $x \in cl(A^c)$, then $x \in A^c$. In other words, $cl(A^c) \subseteq A^c$

>[!Proposition]
>Any union of open sets is open. Any intersection of closed sets is closed. Any finite intersection of open sets is open. Any finite union of closed sets is closed.


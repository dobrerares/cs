# Theory Recap
$(G,*)$ group if:
- Associative
- has identity element
- all elements have a symmetric
$(R,+,\cdot)$ ring if:
- $(R, +)$ Abelian group
- $(R^*,\cdot)$ semigroup
- Distributivity holds


>[!info] Distributivity
>$$
>\begin{align}
>\forall x,y,z\in R: &x(y+z)=xy+xz\\
>			&(y+z)x=yz+zx
>\end {align}
>			$$

$(H,+)$ subgroup of $(G,+)$ if 
- H stable part of $(G,+)$
- $(H,+)$ Group
>[!info] Characterization theorem of a subgroup
>$H\not=\emptyset$
>$$
>\begin{rcases}
>\forall x,y\in H:&\in H\\
>\forall x\in H:& -x\in H
>\end {rcases}\implies\forall x,y\in H:x-y\in H
>$$

$f:(G_1, *)\to (G_2,\circ)$ gr. homomorphism
$\forall x,y\in G_1:f(x*y)=f(x)\circ f(y)$


f group isomorphism if 
- f - homomorphism
- f - bijective (inj+surj) ($\exists f^{-1}$)


# Exercises
## Exercise 1.
$M\not=\emptyset$
$S_M=\{f:M\to M|f\text{ bijective}\}$
Show that $(S_M,\circ$) is a group
Associativity: $\forall f,g,x\in S_M;f\circ(g\circ h)=(f\circ g)\circ h$
Let $x\in M\implies (f\circ(g\circ h))(x)=f\circ(g(h(x))=f(g(h(x)))$
$((f\circ g)\circ h)(x)=f(g(x))\circ h=f(g(h(x)))\implies \text{ assoc}$

Identitiy element: Let $e\in S_m$ be the identity element 
$\forall f\in S_M\quad f\circ e=f\text{ and } e\circ f=f$
$e=1_{S_M};\ e(x)=x$
$(f\circ e)(x)=f(e(x))=f(x)$
$(e\circ$

## Exercise 2.
$M\not=\emptyset$
$(R,+,\cdot)$ ring
$R^M=\{f|f:M\to R\}$
$$\begin{align}
\forall f,g\in R^M:&(f+g)(x)=f(x)+g(x)\\ \\
	 &(f\cdot g)(x)=f(x)\cdot g(x)

\end{align}$$
Show that $(R^M,+,\cdot)$ is a ring. If R is comm or has id, does $R^M$ have the same property
Associativity
$$\begin {gathered}
\forall f,g,h\in R^M:(f+g)+h=f+(g+h) \\
\end {gathered}
$$$$
\begin{rcases}
((f+g)+h)(x)=(f+g)(x)+h(x)=f(x)+g(x)+h(x)\\
 (f+(g+h))(x)=f(x)+(g+h)(x)=f(x)+g(x)+h(x)\\
 \end{rcases}\implies \checkmark
$$
Commutativity: 
$$
\forall f,g\in R^M:f+g=g+f
$$
$$\begin{rcases}
(f+g)(x)=f(x)+g(x)\\
(g+f)(x)=g(x)+f(x)\\
\end{rcases}\implies \checkmark$$
Identity element: 
$$\begin{gathered}
\exists e\in R^M \text{ s.t. } \forall f\in R^M:e+f=f+e=f\\
\theta\\
(e+f)(x)=f(x)\Leftrightarrow e(x)+f(x)=f(x)\Leftrightarrow e(x)=0=\theta(x)
\end{gathered}
$$
Symmetrical element:


Subgroup Associativity
$\forall f,g,h\in R^M: (f\cdot g)\cdot h=f\cdot(g\cdot h)$
$$
\begin{rcases}
((f\cdot g)\cdot h)(x)=(f\cdot g)(x)\cdot h(x)=f(x)\cdot g(x)\cdot g(x)\\
(f\cdot(g\cdot h))(x)=f(x)\cdot(g\cdot h)(x)= f(x)\cdot g(x)\cdot h(x)\\
\end{rcases}\implies (R^{M*}, \cdot) \text{ semigroup} 
$$
Distributivity:
$\forall f,g,h\in R^M: f\cdot(g+h)=(f\cdot g)+(f\cdot h)$

## Exercise 3
$H=\{z\in\mathbb{C}|\ |z|=1\}$
Prove that $h\leq(\mathbb{C^*},\cdot)$, $H\not\leq(\mathbb{C},+)$
$$
H\leq (\mathbb{C^*}, \cdot)\Leftrightarrow\begin{cases}H\not=\emptyset \\
 \forall x,y\in H: x\cdot y\in H\\
\end{cases}\\
$$
Let $z=1\in H\implies |z|=1\in M$
$$
\begin{gathered}
\forall x,y\in M: x+y\in M\\
|x\cdot y|=|x|\cdot|y|=1\in M\\
\end{gathered}
$$
Symmetrical elements: $\forall$

## Exercise 5
$n\in\mathbb{N},n\geq2$
1. $GL_n(\mathbb{C})=\{A\in M_n(\mathbb{C}|det A\not = 0\}$ stable subset of $(M_n(\mathbb{C}),\cdot)$
2. $GL_n(\mathbb{C},\cdot)$ group
3. $SL_n(\mathbb{C})=\{A\in M_n(\mathbb{C})|det A=1\}$ subgroup of $(GL_n(\mathbb{C}),\cdot)$

1. $\forall A,V\in GL_n(\mathbb{C}): A\cdot B\in GL_n(\mathbb{C})$
$$\begin{rcases}
det A\not= 0, det B\not = 0\\
det(A\cdot B)=det A\cdot det B\not = 0\\
\end{rcases}\implies GL_n(\mathbb{C}) \text{ stable subset}
$$
2. "$\cdot$" on $M_n(\mathbb{C})\text { is associative}$
	Let $I_n$ identity element for $(M_n(\mathbb{C}),\cdot)$
	$det I_n=1\not=0\implies I_n\in GL_n(\mathbb{C})$
	$\forall A\in M_n{\mathbb{(C)}}\exists A^{-1}\in M_n(\mathbb{C})$
	$det A^{-1}\not = 0$
	$det I_N=1=det$
3. SL
>[!important]
>The first exercise in algebra exams is giving definitions and examples

## Exercise 7
## Exercise 9 
$n\in\mathbb{N},n\geq2$
$(\mathbb{Z}_n,+,\cdot)$ ring 
$\hat a\in \mathbb{Z}_n^*$
i. $\hat a$ invertible $\Leftrightarrow (a,n)=1$
ii. $(\mathbb{Z}_n,+,\cdot)$ field $\leftrightarrow$ n prime\


i.  $\hat a$ inv. $\Leftrightarrow \exists \hat a^{-1}\text{ s.t. }\hat a \cdot\hat a ^{-1}\Leftrightarrow\exists \hat a^{-1}\in \mathbb{Z}_n^*\text{ s.t. }\hat a\cdot \hat a^{-1}-\hat 1=\hat 0$
$\exists \hat a^{-1}\in \mathbb{Z}_n^* n| a\cdot a^{-1}-1$

Homogenous relations $\varphi: M \rightarrow M$
An equivalence relation must be Reflexive $\forall x\in M\Rightarrow x\varphi x$, Transitive $\forall x,y,z, \text{ if } x\varphi y, y\varphi z$,
Graph of a relation $G=\{x,y\in M|x\varphi y\}$. A relation is given by its graph
A partition of a relation $$(A_i)_{i\in I}\text{ s.t. } \bigcup_{i\in I} A_i=M,\forall i,j\in I A_i\cap A_j=\emptyset$$
Exercise 1.
$M=\{2,3,4,5,6\}$
$$\begin{align}
R=x\ r\ y \Leftrightarrow x\lt y\\
S=x\ s\ y \Leftrightarrow x/y\\
T=x\ t\ y \Leftrightarrow gcd(x,y)=1\\
V=x\ v\ y \Leftrightarrow x\equiv y\pmod 3
\end{align}$$
Write the graphs R,S,T,V $$R=\{(2,3),(2,4),(2,5),(2,6),(3,4),(3,6),(4,5),(4,6),(5,6)\}$$$$S=\{(2,4),(2,2),(2,6),(3,6),(3,3),(4,4),(5,5),(6,6)$$
$$T=\{(2,3),(2,5), (3,4),(3,5),(4,5),(5,6),(3,2),(5,2),(5,3),(5,6),(6,5)\}$$
$$V=\{(5,2),(2,5),(6,3),(3,6),(3,3),(2,2),(4,4),(5,5),(6,6)\}$$
Exercise 2.
$$\begin{gathered}
|A|=n\in\mathbb{N}^*\\
|B|=m\in\mathbb{N}^*\\
\text{Find the no. of }\\
i. \varphi: A\rightarrow B (2^{nm})\\ 
ii. \varphi: A\rightarrow A (2^{n^2})\\
\text{the formula is: } 2^{|Domain\times codomain|}
\end{gathered}$$
Exercise 4.
$$\begin{gathered}
(\mathbb{R},\lt)\rightarrow T\\
(\mathbb{N}, |)\rightarrow R,T\\
(\mathbb{Z},|)\rightarrow R,T\\
(\mathbb{R}^2,\perp)\rightarrow S\\
(\mathbb{R}^3,\parallel)\rightarrow R,T,S\\
(\mathbb{R}^3,\equiv_\Delta)\rightarrow R,T,S\\
(\mathbb{R}^3, \backsimeq_\Delta)\rightarrow R,T,S
\end{gathered}$$
Exercise 5.
$$\begin{gathered}
M=\{1,2,3,4\}\\
r_1,r_2 - \text{relations}\\
\pi_2,\pi_2 -\text{partitions}\\
R_1=\Delta_M\cup\{(1,2),(2,1),(1,3),(3,1),(2,3),(3,2)\}- R,S,T\Rightarrow \text{equiv}\\
R_2=\Delta_M\cup\{(1,2),(1,3)\}- \Rightarrow\text{not equiv}\\
\pi_1=\{\{1\},\{2\},\{3,4\}\}- \text{yes}\\
\pi_2=\{\{1\},\{1,2\},\{3,4\}\}- \{1\}\cup\{1,2\}=\emptyset, \text{ no }\\
i. r_1,r_2, relations\\
ii. \pi_2,\pi_2 partitions
\end {gathered}$$
Exercise 6.
$$\begin{gathered}
(\mathbb{C},r),(\mathbb{C},s)\\
z_1\ r\ z_2 \Leftrightarrow |z_1|=|z_2|\\
z_1\ s\ z_2\Leftrightarrow arg\ z_1= arg\ z_2\text{ or } z_1=z_2=0\\
\\
i. r,s- equiv.\ R,T,S\Rightarrow \text{equiv.}\\
ii.  \mathbb{C}_{/r}\ , \mathbb{C}_{/s}\\
\\
\mathbb{C}_{/r}=\{x\in \mathbb{C}| \ |x|=y\}\\
\\
s - R, T, S \Rightarrow \text{equiv.} \\
\mathbb{C}_{/s}=\{x\in\mathbb{C}| arg\ x=y \text{ or } x=0\}
\end{gathered}$$
Exercise 7.
$$\begin{gathered}
n\in\mathbb{N}\\
(\mathbb{Z},\rho_n)\\
x\ \rho_n\ y\Leftrightarrow n|(x-y)\\
\\
1. \rho_n - \text{equiv.}\\
2. \mathbb{Z}/\rho_n=? (n=0,n=1)\\
\\
\begin{align}
\forall x,y,z\in\mathbb{Z}, x\ \rho_n\ y, z\ \rho_n\ y\\
x\ \rho_n\ y= &n |(x-y)\\
y\ \rho_n\ z= &n|(y-z)\\
&+\\
&n|(x-z)\\
\end{align}\\
n|(x-z)\\
\forall x,y\in \mathbb{Z}, x\rho_n y, y\rho_nx?\\
x\ \rho_n\ y
\end{gathered}$$
TBC^
$$\begin{gathered}\mathbb{Z}\rho_n=\{x\in\mathbb{Z}|n|(x-y),y\in\mathbb{Z}\}\\
=\{x\in\mathbb{Z}|2|(x-y),y\in\mathbb{Z}\}=\{x,y\in\mathbb{Z}|x\equiv y\pmod 2\}\\
=\{\hat0, \hat1\}=\mathbb{Z}_2\\
\mathbb{Z}/\rho_n=\mathbb{Z}_n=\{\hat0,\hat1,\ldots,\hat{n-1}\}\\
n=0\Rightarrow \mathbb{Z}/\rho_0=\emptyset\\
x\rho_0 y\Rightarrow0|(x-y) \text{Not}\\
n=1\Rightarrow\mathbb{Z}/\rho_1=\mathbb{Z}\\
x\rho_1y\Rightarrow 1|(x-y)
\end{gathered}$$
>[!info] What is a function
>$|h<x>|=1,\forall x\in M$
> Translation : $\exists !y\in M\text{ s.t. } h(x)=y$


Exercise 9. 

- [ ] 🔼 write problem sentence
$$\begin{align}
h<x>&=\{y\in M|h(x)=y\}\\
&=\{y\in M|x=4k+y, k\in \mathbb{Z}\}\\
&=\{y\in M|x\equiv y\pmod 4\}\\
x=1\implies y=1\text{ unique}\\
x=2\implies y=2\text{ unique}\\
\ldots
M=\{0,1,2,3\}\implies \exists!\in M\text{ s.t. } h(x)=y\\
\implies |h<x>|=1\\
\implies h - \text{function}\
\end{align}
$$
$$
R..
$$
# Relations
>[!definition]
A triple $r=(A,B,R)$, where $A,B$ are sets and 
$$R \subseteq A \times B = \{(a,b)|a\in A, b\in B\}$$
is called a binary relation.
The set $A$ is called the *domain*, the set $B$ is called the *codomain* and the set $R$ is called the *graph* of the relation $r$.
If $A=B$, then the relation $r$ is called *homogeneous*
If $(a,b)\in R$, then we sometimes write $a\ r\ b$ and we say that *a has the relation r to b* or *a and b are related with respect to the relation r*.

>[!Definition]
>Let $r=(A, B, R)$ be a relation and let $X\subseteq A$. Then the set
$$r(X) = \{b\in B\ |\ \exists\ x\in X: x\ r\ b\}$$ is called the relation class of X with respect to r. 
If $x\in X$, then we denote $$r< x >= r(\{x\}) = \{b\in B\ |x\ r\ b\}$$

Notice that $$r(X) = \bigcup_{x\in X} r< x >$$
If A,B are finite sets, then $r=(A,\ B,\ R)$ may be represented by a diagram consisting of two sets with elements and connecting arrows. For instance, let $r=(A,\ B,\ R)$ where $A=\{1,2,3\}$, $B=\{1,2\}$ and $R=\{(1,1), (1,2), (3,1)\}$
![[Pasted image 20241003085050.png]]
	Figure: Diagram of a relation.
Also note that $r<1>=\{1,2\}=r(A)$
## Examples of relations
a. Let $C$ be the set of all children and let $P$ be the set of all parents. Then we may define the relation $r = (C, P, R)$, where $$R=\{(c,p)\in C \times P\ |\ c\ \text{is a child of}\ p\}$$
b. The triple $r = (\mathbb{R},\mathbb{R},R)$, where $$R=\{(x,y)\in\mathbb{R}\times\mathbb{R}|x\leq y\}$$
is a homogeneous relation, called the *inequality relation* on $\mathbb{R}$. We have $$r<1>=[1,\infty)=r([1,2])$$ 
c. There are several examples from Number Theory, such as divisibility on $\mathbb{N}$ or on $\mathbb{Z}$, and Geometry, such as parallelism of lines, perpendicularity of lines, congruence of triangles, similarity of triangles
d. Let $A$ and $B$ be two sets. Then the triples $$o=(A,B,\emptyset),\quad u=(A,B,A\times B)$$
are relations, called the *void relation* and the *universal relation* respectively.
e. Let $A$ be a set. Then the triple $\delta _A=(A,A,\Delta _A)$, where $$\Delta _A = \{(a,a)|a\in A\}$$ is called the *equality relation* on $A$.
f. Every function called is a relation. Indeed, a function $f : A \rightarrow B$ is determined by its domain $A$, its codomain $B$ and its graph $$G_f=\{(x,y)\in A\times B|\ y\ =\ f(x)\}$$
Then the triple $(A,B,G_f)$ is a relation.
g. Every directed graph is a relation.
For instance the directed graph 
![[Pasted image 20241003091247.png]]
may be seen as a relation $(A,\ A,\ R)$, where $A=\{1,2,3,4\}$ and $$R=\{(1,2),(1,3),(2,4),(3,4),(4,1)\}$$
# Functions
>[!definition]
>A relation $r=(A,\ B,\ R)$ is called a *function* if 
$$\forall a\in A,\ |r < a > | =1 $$
that is, the relation class with respect to r of every $a\in A$ consist of exactly one element.

In what follows, if $f = (A,B,F)$ is a function, we will mainly use the classical notation for a function, namely $f : A → B$ or sometimes $A \overset{f}\rightarrow B$. The unique element of the set $f < a >$ will be denoted by $f(a)$. Then we have $$(a,b)\in F \iff f(a)=b$$
## Related notions
From relations we get the following notions.
>[!Definition]
>Let $f:A\rightarrow B$ be a function. Then A is called the *domain*, $B$ is called the *codomain* and $$F=\{(a,f(a)) | a\in A\}$$ is called the *graph* of the function f.
## Examples of functions and relations
a.
b.
# Equivalence relations
Recall that a relation $r = (A,B,R)$ is called homogeneous if $A =B$.

>[!Definition] 
>A homogeneous relation $r=(A,A,R)$ on $A$ is called :
>1. reflexive (r) if: $\forall x \in A, x\ r\ x$
>2. transitive (t) if: $x,y,x\in A, x\ r\ y\ \text{and}\ y\ r\ z\implies x\ r\ z$
>3. symmetric (s) if: $x,y\in A,\ x\ r\ y \implies y\ r\ x$
>
>A homogeneous relation $r=(A,A,R)$ is called an *equivalence relation* if $r$ has the properties (r), (t), (s).
## Examples of equivalence relations
# Partitions
## Definition
Let $A$ be a non-empty set. Then a family $(A_i)_{i\in I}$ of non-empty subsets of $A$ is called a partition of $A$ if:
 1. The family $(A_i)_{i\in I}$ covers $A$, that is, $$\bigcup_{i\in I} A_i = A$$
 2. The $A_i$'s are pairwise disjoint, that is, $$i,j \in I, i\not =  j \implies A_i\ \cap\ A_j = \emptyset$$
## Examples of partitions
(a) Let $A = {1,2,3,4,5}$ and $A_1 = \{1,2,3\},\ A_2 = \{4\},\ A_3 = \{5\}$. Then $\{A_1,A_2,A_3\}$ is a partition of $A$. 
(b) Let $A$ be a set. Then $\{\{a\}\ | a \in A\}$ and $\{A\}$ are partitions of $A$. 
(c) Let $A_1$ be the set of even integers and $A_2$ the set of odd integers. Then $\{A_1,A_2\}$ is a partition of $\mathbb{Z}$. 
(d) Consider the intervals $$A_n = [n,n+1)$$
for every $n\in \mathbb{Z}$. then the family $(A_n)_{n\in\mathbb{Z}}$ is a partition of $\mathbb{R}$.
# Quotient set
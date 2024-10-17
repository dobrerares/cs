# Connectives
-  $\lnot$ - negation (not)
- $\land$ - conjunction (and)
- $\lor$ - disjunction (or)
- $\to$ - implication
- $\leftrightarrow$ - equivalence
The *negation* is a unary connective and all the others are binary connectives.
>[!Important] Decreasing order of precedence
> $\lnot\ \land\ \lor\ \to\ \leftrightarrow$
## New connectives
 - $\uparrow$ - nand - $\lnot(p\land q)$
 - $\downarrow$ - nor - $\lnot(p\lor q)$
 - $\oplus$ - xor (exclusive or) $\lnot(p\leftrightarrow q)$
![[Drawing 2024-10-17 14.40.42.excalidraw.svg]]
>[!info] Logical equivalence
>The formulas *U* and *V* are *logically equivalent*, if they have identical truth tables: $U\equiv V$

# Exercise 
$X=(p\land q\to r)\to (p\to r)\land q\equiv(\lnot(p\land q)\lor r)\to(\lnot p \lor r)\land q\equiv$
$\equiv \lnot(\lnot(p\land q)\lor r)\land(\lnot p \lor r)\land q\equiv(p\land q\land\lnot r)\lor(\lnot p\lor r)\land q\equiv$
$(p\land q\land \lnot r)\lor(\lnot p \land q)\lor(r\land q)$

# Homework 

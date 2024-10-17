>[!Important] Type limits of `int` in python
>Python automatically implements big int, so there are no proper limits
# The stack
Programming languages are stack based, python has a stack limit of 1000, that means a recursive function can only call itself 1000 times. The stack contains the functions, their variables. 
## Tail call optimization
Tail call optimization makes a recursive function iterative. In C(++) tail call optimization is used to avoid overflowing the stack, but in python TCO is not implemented (because the focus is on understandability not speed). To allow a compiler to make this optimization, the return should only call a function, without making additional optimization. This allows the compiler to remove the current call from the stack and replace it with another.
# Caching
To optimize branching recursive values you can use a cache, usually in the form of a dictionary (to make your job easier you can also use `lru_cache` which does this automatically)

# Complexity
>[!Important]
>You cannot restrict input size when analyzing for the best case (e.g., n=1 is not best case, it's just a particulat input size)

>[!Important]
>When talking about runtime complexity we only care about the highest order term, for example, $T(n)=13\times n^3+n^2$ we say it has $O(n^3)$ time complexity

Technically $O(n^2)$ is also an upper bound for an algorithm that has $O(\log n)$ complexity, (admissions exam ahem ahem) but in real life we care about the least upper bound, i.e. the smallest upper bound

>[!Important]
>- Big $O$ is worst case, higher bound
>- Big $\Omega$ is the best case, or lower bound
>- Big $\Theta$ is the average case, or tight bound (hard to determine but very useful)


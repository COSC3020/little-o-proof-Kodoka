# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

# Proof

By definition Little-o is:  
$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$  
Meaning for all values of $c > 0$, there exists some value, $n_0$, where, for all  
$n\ge n_0$, it is true that $f(n) < c g(n)$  
  
By definition Big-O is:  
$f(n)\in O(g(n)) \iff \exists c>0, \exists n_0, \forall n\ge n_0: f(n) \le c g(n)$  
Meaning there is at least one value of $c > 0$, where there exists some value,  
$n_0$, where, for all $n\ge n_0$, it is true that $f(n) \le c g(n)$  

Assume that:  
$f(n)\in o(g(n))$,  
which means, by definition:  
$\forall c>0, \exists n_0 \in \mathbb{N}, \forall n\ge n_0: |f(n)| < c|g(n)|$  
Let $c=1$, which guarantees there exists some $n_0 \in \mathbb{N}$ such that:  
$\forall n\ge n_0: |f(n)| < 1\cdot |g(n)| \equiv \forall n\ge n_0: |f(n)| < |g(n)|$  
As:  
$|f(n)| < |g(n)| \implies |f(n)| \le |g(n)|$  
A value of $c=1$ of little-o satisfies the definition of big-O, thus:  
$f(n)\in o(g(n)) \implies f(n)\in O(g(n))$

# Sources

For my definition of Big-O/general information:  
https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/

General information regarding asymptotic notation of Big/Little-O:  
https://stackoverflow.com/questions/1364444/difference-between-big-o-and-little-o-notation

# Plagirism Notice

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

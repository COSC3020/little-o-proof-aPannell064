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



Defintions: 

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$  //Definition of o

$f(n)\in O(g(n)) \iff \exists c>0, \exists n_0, \forall n\ge n_0: f(n) <= c g(n)$  //Defintion of O

Proof:

$f(n)\in o(g(n)) \implies f(n)\in O(g(n))$

$\forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n) \implies \exists c>0, \exists n_0, \forall n\ge n_0: f(n) \le c g(n)$ //Defintions of o and O

$\forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n) \implies \exists c_0>0, \exists n_1, \forall n\ge n_1: f(n) \le c_0 g(n)$ //Rename second c to $c_0$ and second $n_0$ to $n_1$

$\forall n_0, \exists c>0, \exists n: c>0 \and n\ge \and n_0 f(n) < c g(n) \implies \exists c_0>0, \exists n_1, \forall n\ge n_1: f(n) \le c_0 g(n)$

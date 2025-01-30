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


Note: I found any additional notation through https://en.wikibooks.org/wiki/LaTeX/Mathematics

##### Defintions: 

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$  //Definition of o

$f(n)\in O(g(n)) \iff \exists c>0, \exists n_0, \forall n\ge n_0: f(n) <= c g(n)$  //Defintion of O

##### Proof:

$f(n)\in o(g(n)) \implies f(n)\in O(g(n))$

$\forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n) \implies \exists c>0, \exists n_0, \forall n\ge n_0: f(n) \le c g(n)$ //Defintions of o and O

$\forall c>0, \exists n_0, \forall n*\ge n_0: f(n*) < c g(n*) \implies \exists c_0>0, \exists n_1, \forall n\ge n_1: f(n) \le c_0 g(n)$ //Rename second c to $c_0$, first n to n* and second $n_0$ to $n_1$

$\forall n_0, \forall n, \exists c, \exists n*, \exists c_0, \exists n_1: (c>0 \land n*\ge n_0 \land f(n*) < c g(n*) \implies c_0>0 \land n\ge n_1 \land f(n) \le c_0 g(n))$ //Migrate Quantifiers

$\exists c, \exists n*, \exists c_0, \exists n_1: (c>0 \land n*\ge n_0 \land f(n*) < c g(n*) \implies c_0>0 \land n\ge n_1 \land f(n) \le c_0 g(n))$ //Remove Forall Quantifiers

$(c>0 \land n\ge n_0 \land f(n) < c g(n) \implies c>0 \land n\ge n_0 \land f(n) \le c g(n))$ //Remove exists quantifiers, replacing c with c, n* with n, $c_0$ with c, and $n_1$ with $n_0$

$c>0 \land n\ge n_0 \land f(n) < c g(n) \implies c>0 \land n\ge n_0 \land f(n) < c g(n) \lor f(n) = c g(n)$ //Definition of $\le$

$True \lor f(n) = c g(n)$  //Self-implication

$True$  // $\lor$ null

Q.E.D.

"I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. 
All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that 
if plagiarism is suspected, charges may be filed against me without prior notice."

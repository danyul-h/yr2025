> divisibility, proof writing, cases, EDA, Euclidean algorithm w/ gcd, induction
### sets
$$
\begin{eqnarray}
A &=& \{1, 2\} \\
B &=& \{a, b, c\} \\ \\
\text{Two sets C and D are disjoint iff} &:& C \cap D = \varnothing \\ \\ 
\text{Complement of a set} &:& \bar{A} : A' : \text{All elements in universal set that is not in set A} \\ \\
\text{Intersection of all sets} &:& \bigcap_{i}{S_i} = \{s \mid s \in S_j \text{ for all j}\} \\
\text{Union of all sets} &:& \bigcup_{i}{S_i} = \{s \mid s \in S_j \text{ for some j}\} \\ \\
\text{Cartesian Product} &:& A \times B = \{(x,y) \mid x \in A \land x \in B\}\\ 
&& A \times B = \{(1,a), (1,b), (1,c), (2, a), (2,b), (2,c)\}\\ 
&& \mathbb{R} \times \mathbb{R} = \mathbb{R}^2\\ \\
\text{Power Set, the set of all subsets} &:& P(A) = \{\varnothing, \{1\}, \{2\}, \{1, 2\}\} \\ \\
\text{Cardinality, number of vals in a set} &:& |A| = 2, |A \times B| = |A| \times |B|, |P(A)| = 2^{|A|}\\ \\
\text{Symmetric Difference of Sets} &:& A \Delta B = (A-B) \cup(B-A) \\ \\
\text{Improper Subset} &:& C \subseteq D \iff \forall x(x \in A \implies x \in B)\\
\text{Proper Subset} &:& C \subset D \iff C \subseteq D \land C \neq D
\end{eqnarray}
$$
* **partitions** are a way of splitting up a set into non overlapping subsets
### propositional logic
$$
\begin{eqnarray}
P \implies Q &\Leftrightarrow& \lnot P \lor Q \\
\text{Law of Addition} : P \implies (P \lor Q) &\Leftrightarrow& T \\
\text{Law of Simplification} : (P \land Q) \implies P &\Leftrightarrow& T \\
\end{eqnarray}
$$
* something is **vacuously true** when it is true because the **antecedent** is false
* conditional (p -> q) = contrapositive (~q -> ~p)
* converse (q -> p) = inverse (~p -> ~q) 
* when p implies q
	* p is the antecedent
	* q is the consequent
* something is a **tautology** if it is true no matter what
### predicate logic
* quantifiers indicate we're in predicate logic
* our domain of discourse can change results
	* something may be true under the domain of complex numbers 
	* while the same thing is false under real numbers

$$
\begin{eqnarray}
\exists &:& \text{There exists...} \\
\forall &:& \text{For all...}\\ \\
\exists x P(x) &\Leftrightarrow& P(a_1) \lor P(a_2) \lor ...\lor P(a_n) \lor... \\
\forall x P(x) &\Leftrightarrow& P(a_1) \land P(a_2) \land ...\land P(a_n) \land... \\ \\
\lnot \exists x P(x) &\Leftrightarrow& \forall x \lnot P(x) \\
\lnot \forall x P(x) &\Leftrightarrow& \exists x \lnot P(x)
\end{eqnarray}
$$
### divisibility
$$ 
\begin{eqnarray}
\text{"b divides a"} &:& b \mid a \iff a=b*c \text{, for some c} \in \mathbb{Z} 
\end{eqnarray}
$$
* by our definition, 0 divides 0
### gcd
$$
\begin{eqnarray}
gcd(a, b) =  d > 0 \iff&& \\ 
\text{d divides both a, b...} && d \mid a \land d \mid b \\
\text{any other c that divides a, b also divides d...} && (c \mid a \land c\mid b) \implies c \mid d
\end{eqnarray}
$$
### lcm
$$
\begin{eqnarray}
lcm(a, b) =  m \geq 0 \iff&& \\ 
\text{m is a multiple of a, b...} && a \mid m \land b \mid m \\
\text{any other n that is a multiple of a, b is also a multiple of m...} && (a \mid n \land b\mid n) \implies m \mid n
\end{eqnarray}
$$
### parity
* odd vs. even
* odd = 2k+1
* even = 2k
###  well ordering principle
* every nonempty subset of natural numbers {0, 1, 2, ...} has a least element
* this is our axiom in the class
* proves that **there is no infinite decreasing sequence of positive integers**
	* so we can solve a **proof by infinite descent** via **descending chain condition**
* also proves the euclidean division algorithm...
### euclidean division algorithm
$$
\begin{eqnarray}
\text{for a, b} \in \mathbb{Z}, \text{ }b \neq 0 \\
\exists \text{ a unique } q, r &&\text{ s.t.} \\
\text{i.} && a = qb + r, \text{ }r \in \mathbb{Z} \\
\text{ii.} && 0 \leq r < |b|
\end{eqnarray}
$$
* essentially states given a, b there exists unique q, r representing quotient and remainder
* to prove...
	* start with set that ignores condition ii but follows condition i
	* s is non empty so apply wop
		* get least element, this should be our unique r
	* now we need to prove that r follows condition ii
		* suppose it doesn't
		* run into a contradiction with the wop
	* now for uniqueness
		* suppose there are two q's, so it isn't unique
		* solve a system of eq.
		* sub in values in condition ii
		* find that the difference of the two q's has to be 0, so they are equal
### equivalence relation
* given some set S, every equivalence relation R on that set induces a partition of S into "equivalence classes"
	* in each class, all objects are equivalent based on the relations
* any equivalence relation R is...
	* reflexive, a R a
	* symmetric, a R b -> b R a
	* transitive, a R b and b R c -> a R c
### bezout's identity
$$
\begin{eqnarray}
gcd(a,b) &=& sa+tb \\
&& \text{for some } s,t \in \mathbb{Z} \\
\text{example} : 
gcd(3,5) &=& 1 = (2)(3) + (-1)(5) \\
&& s = 2, t = -1
\end{eqnarray}
$$
* based off example, imagine jumper frogs
	* one can only jump a distance of 3, while the other only a distance of 5
	* by bezout, the gcd of 3, 5 is a linear combination of each other
### euclidean algorithm
* way to find gcd
* long way
	* gcd(260, 110)
	* gcd(150, 110)
	* gcd(110, 40)
	* gcd(70, 40)
	* gcd(40, 30)
	* gcd(30, 10)
	* gcd(20, 10)
	* gcd(10, 10) = 10
	* subtracting over and over again
* short way
	* apply EDA
	* 260 = 2 * 110 + 40
	* 110 = 2 * 40 + 30
	* 40 = 1 * 30 + 10
	* 30 = 3 * 10  + 0
	* gcd(260, 110) = 10
	* keep replacing a with b, and b with r
	* stop once r is 0, your gcd will be b
### prime divisibility property
* for prime p, p | ab -> p | a and p | b
### weak / mathematical induction
$$
\forall P([P(0) \land \forall k(P(k) \implies P(k+1))] \implies \forall n P(n))
$$
* for any property p,
* if p(0), meaning the property is true for the first case
* and if p(k) implies p(k+1),
* then for all n after base case, p(n)
### strong / complete induction
$$
\forall P([P(0) \land \forall k((P(0) \land P(1) \land ... \land P(k)) \implies P(k+1))] \implies \forall n P(n))
$$
* when mathematical induction isn't enough, use strong induction
* rather than just p(k), you assume that all cases from base case to k have property p
* and use that to imply p(k+1)
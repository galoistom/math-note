>in the following notes all ring will be assumed to be commutative with unit(unless stated otherwise)

**Definition 1.1**: Let $A$ be a ring, a abilian group $M$ is said to be an $A-module$ if $A$ acts on $M$ linearly (i.e. there is a ring homomorphism $A \rightarrow End(M)$)
**Example**:
1. every abilian group $G$ is naturally a $\mathbb{Z}-module$.
2. Let $A$ be a field, then an $A-module$ is actually an $A-v.s.$
3. Let $G$ be a finite group, and $A=k[G]$ be a group ring, then an $A-module$ is a linear representation of $G$ (c.f. [[Basic Definitions of representation]])
4. $A$ and the ideals of $A$ is also modules of $A$, with the multiplication as the action over it.

**Definition**: Let $Mod_A$ be a category whose elements is the modules of $A$, and morphism is the homomorphism between $M,N$ preserving the module structure.
We have a natural isomorphism $Hom(A,M) \simeq M$ by sending $f \mapsto f(1)$.

**Definition**: Let $N \leq M$ be a sub group of $M$, stable under $A$, then $N$ is called the submodule of $M$, one should note that $M/N$ also inherit the structure of $A-module$.
**Example**: Let $f: M \rightarrow N$ be an homomorphism, then $ker(f),Im(f),coker(f),coIm(f)$ are all $A-module$

Let $f: A \rightarrow B$ be a ring homomorphism, then $B$ is an $A-module$, and $ker(f)$ is an ideal, $Im(f)$ is a $B-submodule$ but not an ideal of $B$.

**Definition**: an $A-module$ M who can be represented by $\sum Ax_i$ with $x_i \in A$, then we say that $(x_i)$ is the set of generator of $M$. Let $N,P \subset M$, let $(N:P):=\{a \in A : aP \subset N\}$ is an ideal. Specifically, $(0,M)$ is called the annihilator $Ann(M)$ of $M$.

**Definition**: a ring is integral domain if it has no zero divsor (i.e. $\not\exists ab=0,a \neq0, b\neq0$), a ring is a field if $1 \neq 0$ and every element is a unit. Let $\mathfrak{p}$ be an ideal, consider $A/\mathfrak{p}$, we say $\mathfrak{p}$ is prime if $A/\mathfrak{p}$ is integral domain, and maximal if there is no bigger nontrivial ideal containing $\mathfrak{p}$, which can also be expressed as $A/\mathfrak{p}$ is a field.

Let A be a ring, we let $spec(A)$ be a topological space with elements $\mathfrak{p}$ and the close sets look like $V(E)=\{\mathfrak{p} \in spec(A):E \subset\mathfrak{p}\}$, for an element $f \in A$, let $V(f)=\{\mathfrak{p} \in spec(A):f \in \mathfrak{p}\}$.
Basic example: let k be an algebraicly closed field, $f \in k[x]$, then for any $\alpha \in k$, $(x-\alpha)$ is a maximum ideal of $k[x]$ and $(x-\alpha)$ is a closed point of $spec(k[x])$ then $f(\alpha)=0$ is equvalient to $(x-\alpha) \in V(f)$.

**Theorem(Hochster)**: let $X$ be a topological space then the TFAE:
1. there is a ring $A$ such that $X \simeq spec(A)$.
2. $X$ is an inverse limit of finite $T_0-spaces$.
3. $X$ is spectrial, i.e. $X$ is quasi compact, has a bisis of quasi-compact open sub sets stable under finite intersections, and every irr closed subsets has a unique generic point(sober)

**Construction 1.14** $f:A \rightarrow B$ is a ring homomorphism. then it defines a map $^af:Spec(B) \rightarrow Spec(A)$ which maps $\mathfrak{q} \mapsto f^{-1}(\mathfrak{q})=\mathfrak{q} \cap A$. It is eqsy to check that it is well defined. One should note that for a maximal $\mathfrak{m} \subset B$ its image $^af(\mathfrak{m})$ is not necessarily maximal.

**Theorem 1.16** Let $A \neq 0$ be a commutative ring, then $A$ has at least one maximal ideal (i.e. $Spec(A)$ is a closed point)
Proof:(applying zorn's lemma) Let $\Sigma:=\{I \subset A: I \neq (1)\}$, ordered by inclusion. since $(0) \in \Sigma$ we have $\Sigma\neq0$. We show: Every chain $(I_\alpha)$ in $\Sigma$ has an upper bound. Indeed, $I= \cup I_\alpha$ is an upper bound. Using zorn's lemma, $\Sigma$ has an maximal element.#
Cor1.18 if $I$ is an ideal of $A$, then there is a maximal ideal ideal $\mathfrak{m}$ s.t. $I \subset \mathfrak{m}$.

**Definition 1.20** If $A$ has exactly one maximal ideal $\mathfrak{m}$, then we call $A$ a local ring. We call $k:=A/\mathfrak{m}$ the residue field of $A$.
Localization $A_{\mathfrak{p}}$ is some how looking at the functions at the small area around the spot $\mathfrak{p}$.

**Prop 1.21** If $\mathfrak{m} \subset A$ is a maximal ideal, such that every $x\in A\backslash \mathfrak{m}$ is a unit, then A is a local ring.
Proof:every ideal $I \neq (1)$ consists only non-units have $I \subset \mathfrak{m}$, hence $\mathfrak{m}$ is the only maximal ideal.#
**Prop 1.22** If $\mathfrak{m} \subset A$ is a maximal ideal such that all elements in $1+\mathfrak{m}$  are units, then $A$ is a local ring
Proof:all we need to show is that elements in $A \backslash\mathfrak{m}$ are units. For $x \in A \backslash\mathfrak{m}$, we have $\mathfrak{m} \subset (x)+\mathfrak{m}$, so there is a $y \in A$ such that $y+tx=1$, thus $xy=1-m$ is a unit, hence $x$ is a unit.

**Ideal's geometrical motive**. let $k$ be a field, and $Y \subset k^n$, then $I(Y)=\{f \in k[x_1,\cdots,x_n]: \forall p\in Y,f(p)=0\}$ is a tipical ideal for $k^n$.
We consider when $I(Y)$ is prime?

**Definition 1.23** Let $n=\{a \in A:\exists n \in \mathbb{N},a^n=0\}$, is called the nilradical of $A$. It is an ideal, specifically the intersection of all prime ideals in $A$. And $R=\bigcap \mathfrak{m}$ the intersection of all maximal ideal, we have $R=\{x \in A: \forall y \in A, 1-xy \text{ is a unit in } A\}$.
Lemma Suppose $f \in A-\mathfrak{m}$ is not a nilpotet, then there is a prime ideal $\mathfrak{p}$ with $f \notin \mathfrak{p}$. Let $\Sigma:=\{\mathfrak{a}:\forall n \in \mathbb{N},f^n \notin \mathfrak{a}\}$. Using Zorn's lemma, take the masimal element $\mathfrak{p}$ of $\Sigma$, it is easy to see that $\mathfrak{p}$ is prime. 

**Definition 1.25** Let $S \subset A$ as a set, with $1\in S$ and $\forall x,y \in S$, we have $xy\in S$, the $S$ is called the multiplicative subset. Let $I$ be a ideal, then radical $\sqrt{I}:=\{a:\exists n\in\mathbb{N},a^n\in I\}$, similiar definition can be used on multiplicative subset.
Lemma: if $S$ is a radical multiplicative subset, and $0 \notin S$, then there is a prime ideal $\mathfrak{p} \cap S=0$.
Motive: We have that $V(I)=V(\sqrt{I})$, so $\sqrt{I}$ is the largest ideal with the close set $V(I)$.

---


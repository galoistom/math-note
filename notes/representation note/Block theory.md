We extend the ideal of [[Basic Definitions of representation]] to the modules of group algebra $k[G]$.

# Definitions
>[!note] Definition
>Let $G$ be a group. A representation of $G$ over $k$ is a pair $(V,\rho)$ consisting of a $k-module$ $V$ and a group homomorphism $\rho:G \rightarrow GL(V)$, where $GL(V)=Aut_k(V)$ is the group of $k-linear$ automorphism.

Morphism between two representations are simple, just preserve the module structure and the $G$ action over it.

# Twisted group algebra
We want to construct different pultiplication for $k[G]$. Let $\alpha:G \times G \rightarrow k^\times$ be a max, and multiplication be $x \cdot y=\alpha(x,y) xy$, then the multiplication is associative if and only if $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)\alpha(y,z)$. We extend this definition to general abilian group $Z$, thus we get the definition of the 2-cocycle $Z^2(G;Z)$, i.e. all $\alpha:G \times G \rightarrow Z$ such that, $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)(^x\alpha(y,z))$. But one might notice that when viewing $k_\alpha[G],k_\beta[G]$ with multiplication $\alpha,\beta$, if there is a scalar $\gamma:G \rightarrow k^\times$ s.t.$\alpha(x,y)=\beta(x,y)\gamma(x)\gamma(y)\gamma(xy)^{-1}$(i.e. there is an isomorphism between $k_\alpha[G] \simeq k_\beta[G]$ by sending $x \mapsto \gamma(x)x$), then there is no much different between the multiplications, and note that $\alpha(x,y)=\gamma(x)(^x\gamma(y))\gamma(xy)^{-1}$ where $\gamma(x)=(^xz)z^{-1}$ for some $z \in Z$ forms a subgroup of $Z^2(G;Z)$, we shall denote it by $B^2(G;Z)$. Now, by lowering the dimension one get $Z^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that $\gamma(xy)=\gamma(x)(^x\gamma(y))$, and $B^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that there is a $z \in Z$ s.t. $\gamma(x)=(^xz)z^{-1}$. Using quotient, we get the [[Cohomology on groups]] $H^1(G;Z)=Z^1(G;Z)/B^1(G;Z)$ and $H^2(G;Z)=Z^2(G;Z)/B^1(G;Z)$.
**Remark**: Using the above interpretation, one get a natural link between $H^i(G;Z)$ and $Ext_{\mathbb{Z}[G]}^i(\mathbb{Z},Z)$ through the extension of group $G$:
$$1 \longrightarrow Z \stackrel{l}{\longrightarrow} \widehat{G} \stackrel{\pi}{\longrightarrow} G \longrightarrow 1$$
where the multiplication $\widehat{x}\cdot\widehat{y}=\alpha(x,y)\widehat{xy}$.

# G-algebras
We already have $G-module$, so it is natural to consider the concept of $G-algebra$. The definition is straightforward: simply giving an algebra $A$ a $G-action$ over it, specificly, the homomorphism between $G \rightarrow A^\times$ is called the *structural homomorphism of the interior G-algebra A*. Moreover, the algebraic morphism $A \rightarrow B$ preserving the $G-action$ is called the homomorphism of $G-algebra$. 

# Category algebra
One might now that a group $G$ is a special monoid category. So we extend the idea of group algebra to category algebra, where the morphism between objects take the place of group action. This lead to the quiver algebra, which is the quotient $A=k\mathcal{C}/I$, where $I$ is an ideal of the algebra. 

# Center and commutator subspace
It is well known that the center $Z(k[G])$ of the group algebra $k[G]$ is spanned by the conjugacy classes of $G$, i.e. let $\mathcal{K}$ be the set of conjugacy classes of $G$, and for each conjugacy classes $C \subset G$, set $\overline{C}=\sum_{c\in C}c$, then every $z \in Z(k[G])$ can be uniquely expressed by $\sum_{C \in \mathcal{K}}\lambda_C\overline{C}$. 

**Theorem**: 
Let A,B be k-algebras. Suppose that $A$ and $Z(B)$ are free as k-modules, ans that $Z(B)$ us a direct summand of $B$ as k-module. Then the centralizer of the subalgebra $1 \otimes B$ of $A \otimes_k B$ is $A \otimes_k Z(B)$, and we have $Z(A \otimes_k B)= Z(A) \otimes_k Z(B)$.
*Proof*: 
One side of the inclusion is clear, we shall proof the other side. Taking a k-basis $\{a_i\}_{i \in I}$ for $A$, and $\{z_j\}_{j \in J}$ for $Z(B)$. Then the set $\{a_i \otimes 1_B\}_{i \in I},\{1_A \otimes z_j\}_{j \in J}$ are basis for $A \otimes_k B,A \otimes_k Z(B)$ as a $B,A$ module. Thus $z \in A \otimes_k B$ can be written in the from $z=\sum_{i \in I}a_i \otimes b_i$ where $b_i$ are uniquely determined and almost all equal to 0. Now suppose $z$ centralises $1 \otimes_k B$, then we have $\sum_{i \in I}a_i \otimes bb_i=\sum_{i \in I}a_i \otimes b_ib$, using the uniquness, one gets $b_i \in Z(B)$ for all $i \in I$, so $z \in A \otimes_k Z(B)$. Suppose now that $z \in Z(A \otimes_k B)$, then $z \in A \otimes_k Z(B)$, so $z=\sum_{j \in J}c_j \otimes z_j$ is unique up to $c_j$. Using the same argument above, one proof he theorem.

Using the above theorem, one easily know that $Z(k[G \times H])=Z(k[G]) \otimes Z(k[H])$ if $H \leq G$. But in general, the twisted group algebra does not have the silimiar properties. In fact, the certer $Z(k_{\alpha}[G])$ may not be free as k-module since the multiplicative inverse of a group element $x$ is not necessarily $x^{-1}$. But there is another way to measure how far it is to be commutative is using the commutator space $[A,A]$ which is generated by $ab-ba$, $a,b \in A$. One might notice that $[A,A]$ is a $Z(A)$ module, so $A/[A,A]$ is also a $Z[A]$ module. 

**Proposition**:
1. the commutator space $[k[G],k[G]]$ is spanned by $[x,y]=xy-yx,\  x,y \in G$.
2. If $x,x'$ are conjugate, then $x-x' \in [k[G],k[G]]$, in fact, those sets of $[x,x']$ span the space $[k[G],k[G]]$.
3. We have an isomorphism of k-module $k[G]/[k[G],k[G]] \simeq Z(k[G])^*$, sending $x+[k[G],k[G]] \mapsto \sigma$ where $\sigma \in Z(k[G])^*$ is the maps that sent the conjugacy class sum of $x^{-1}$ to 1, and other classes to 0. 
4. We have an isomorphism of k-module $(k[G]/[k[G],k[G]])^* \simeq Z(k[G])$, sending $\phi \in (k[G]/[k[G],k[G]])^*$ to $\sum_{g \in G} \phi(g^{-1})g$.
5. Let $A,B$ be k-algebras. We have $[A \otimes_k B,A \otimes_k B]=A \otimes [B,B]+[A,A] \otimes B$.

We extend the commutator operator to modules: Let $A$ be a k-algebra, and $M$ an $A-A$ bimodule. We set $M^A=\{m \in M | am=ma, \forall a \in A\}$ and denote by $[A,M]$ be k-submodule of $M$ generated by $am-ma$.
*Remark*: note that $End_k(U)$ is also an $A-A$ bimodule for an A-module $U$, and $End_k(U)^A=End_A(U)$.
# The Hopf algebra structure of group algebra
The main idea here is that we want to generalize the group algebra, but close enough to preserve many properties.

**Definition**: 
Let $G$ be a group. The argumentation homomorphism of $k[G]$ is the unique k-algebra homomorphism $\epsilon:k[G] \rightarrow k$ sending every element of $G$ to $1_K$. Set $I(k[G])=ker(\epsilon)= \{\sum_{g \in G} \lambda_g g: \sum_{g \in G} \lambda_g=0\}$.

**Proposition**: 
LEt $G,H$ be finite groups. Let $\phi:G \rightarrow H$ be a group homomorphism an let $\alpha:k[G] \rightarrow k[H]$ be the induced algebra homomorphism. Set $N=ker(\alpha)$, then we have $ker(\alpha)=k[G] \cdot I(k[G])=I(k[N])k[G]$. 

Recall that for any k-algebra $A$, there is a natural map $\mu:A \otimes_k A \rightarrow A$, such that $\mu(a \otimes b)=ab$. $\mu$ is naturaly a morphism as $A-A$ bimodule, but not as algebra in general. However, in the case of group algebra, there is always a *comultiplication* map $\Delta:k[G] \rightarrow k[G] \otimes_k k[G] \simeq k[G \times G]$ induced from $\Delta:G \rightarrow G \times G$, sending $g \mapsto (g,g)$. 

Another property is that there is an *antipode* $l:k[G] \simeq k[G]^{op}$ sending $g \rightarrow g^{-1}$, and one also have $l \circ l =id_{k[G]}$. Moreover, a *unit* map $\eta:k \rightarrow k[G]$ sending $1_k \mapsto 1$.

Then we have the following **theorem**:
1. $\mu \circ (id \otimes eta)=id=\mu \circ (\eta \otimes id)$.
2. $\mu \circ (\mu \otimes id)=\mu \circ (if \otimes \mu):k[G] \otimes_k k[G] \otimes_k k[G] \rightarrow k[G]$.
3. $(id \otimes \epsilon) \circ \delta = id = (\epsilon \otimes id) \circ \Delta$.
4. $(\Delta \otimes id) \circ \Delta = (id \otimes \Delta) \circ \Delta: k[G] \rightarrow k[G] \otimes_k k[G] \otimes_k k[G]$.
5. $\mu \circ (id \otimes l) \circ \Delta=\eta \circ \epsilon=\mu \circ (l \otimes id) \circ \Delta:k[G] \rightarrow k[G]$.

The algebra satisfying the above theorem are called *Hopf algebra*. the second equation is the associativity of $\mu$, the third and the forth correspond to $A$ being a *coalgebra* with the last one being the *coassociativity*. The antipode ensures that the category of left and right modules are the equivalent. The comultiplication meusres that a tensor product over $k$ of two A-module is again a A-module. 

We want some how extend these maps to the twisted group algebra, then we get that the map sending $g \mapsto \alpha(g,g^{-1})g^{-1}$ where $g \in G$ induced an isomorphism $(k_\alpha[G])^{op} \simeq k_{\alpha^{-1}}G$, and that if $\gamma=\alpha\beta$ then there is a natural injective k-algebra homomorphism $k_\gamma[G] \rightarrow k_\alpha[G] \otimes_k k_\beta[G]$, and $k_\gamma[G]$ is a direct summand of $k_\alpha[G] \otimes_k k_\beta[G]$ as a $k_\gamma[G]-k_\gamma[G]$ bimodule.

# Blocks and indempotent
Given two k-algebra $B,C$, set the carstesian product $B \times C$ with the componentwise sum ans multiplication, together with the canonical projections onto $B$ ans $C$, is the direct product of $B,C$ in the category of k-algebra. Let $A$ be an k-algebra, a subalgebra $B$ is a direct factor if there is a split surjective $A-A$ bimodule homomorphism $\tau:A \rightarrow B$.

Let $A$ be a k-algebra, and $b \in Z(A)$ be an indempotent, then $Ab:=\{ab:a \in A\}$ is a k-algebra with unit $b$. one  immediately know that $A(1-b)$ is also a k-algebra, and that $A=Ab \times A(1-b)$ as k-algebra. The following theorem bridge the connection between the two concept above.

**Theorem**:
Let $A$ be a k-algebra, $B$ a k-submodule of $A$, then the following are equivalent:
1. $B$ is a direct summand of $A$ as an $A-A$ bimodule.
2. B is a direct factor of A as a k-algebra.
3. B=Ab for sum idempotent b in Z(A).
*Proof*:
Suppose (1) holds, let $A=B \oplus N$ as an A-A-bimodule. Notice that $BN \subset B \cap N \{0\}$, and write $1_A=b+n$, then $b=b \cdot 1_A=b^2+bn=b^2$ so $b$ is an indempotent, the same argument shows that $n$ is indempotent, so they are orthogonal. Write $a=c+r$ for some $c \in B,r \in N$, and $a=ab+an=ba+na$, so $b,n \in Z(A)$, and $B=Ab,N=An$.
Suppose (2) holds, let $A=B \times C$, then $1_A=(1_B,0)+(0,1_C)$ and $(1_B,0),(0,1_C)$ are orthogonal indempotent in $Z(A)$. Setting $b=(1_B,0)$, then $B=Ab$.
Suppose (3) holds, let $B=Ab$, and $C=A(1-b)$, then $A=B \oplus C$ as A-A-bimodule, and $A=B \times C$ as k-algebra.

**Definition**:
Let $A$ be a k-algebra. A *block* of $A$ is a primitive indempotent $b$ in $Z(A)$; the algebra $Ab$ is called a *block algebra* of $A$.

**Theorem**:
Suppose that k is noetherian. Let $A$ be a k-algebra such that $Z(A)$ is finitly generated as a k-module. Then $Z(A)$ is noetherian, and the following hold.
1. The set of Blocks $\mathcal{B}$ of $A$ is the unique primitive decomposition of $1_A$ in $Z(A)$. In particular, $\mathcal{B}$ is finite, and they are pairwise orthogonal blocks of $A$.
2. $A=\prod_{b \in \mathcal{B}} Ab$ is the uniuqe decomposition of $A$ as a direct product of indecomposable k-algebras.
3. $A=\oplus_{b \in \mathcal{B}}Ab$ is the unique decomposition of $A$ as direct sum of indecomposable A-A-bimodule.
*Proof*:
Since $k$ is noetherian and $Z(A)$ is finitly generated as k-module, so $Z(A)$ is noetherian. Let $b \in \mathcal{B}$, and $c \in Z(A)$ is another primitive indempotent such that $bc \neq 0$. Then one have $b=bc+b(1-c)$, where $bc,b(1-c)$ are indempotent in $Z(A)$ but $b$ is primitive, so one must have $b(1-c)=0,b=bc$, the same agrument shows that $c=cb=bc=b$. The rest it then clear.

In view of abilian category, there is no much difference between direct product and direct sum, and coproduct coincides with tensor product. That's why the decomposition of $A$ to its block yealds a direct sum and a direct product.

**Definition**:
Let $A$ be a k-algebra and $b$ be a block. We say that an A-module $M$ belongs to the block $b$ if $M=bM$.

**Proposition**:
Suppose that k is noetherian. Let $A$ be a k-algebra such that $A$ is finitl generated as a k-module, let $\mathcal{B}$ be the set of blocks of $A$.
1. for any A-module $M$ we have $M=\oplus_{b \in \mathcal{B}}\,bM$.
2. for any indecomposable A-module $M$ there is a unique block $b$ if $A$ such that $M=bM$.
3. for any two A-module belonging to two different blocks $b,c$. We have $Hom_A(M,N)=\{0\}$.

Using this proposition, we can study the category $Mod(A)$ by studying the category $Mod(Ab)$ where $b$ runs through the set of blocks of $A$.

# Composition series and Grothendieck groups
c.f.[[Grothendieck group]]

**Definition**:Let $A$ be a k-algebra. A *composition series* of A-module $M$ is a finite chain $M= M_0 \supset_1 M_1 \supset \cdots \supset M_n=\{0\}$ of submoduels $M_i$ in $M$ such that $M_{i+1}$ is a maximal submoduels, the module $M_i/M_{i+1}$ be the composition factors, and $n$ is the length of the series. Two composition series of A-modules $M$ and $M'$ are called *equivalent* if they have the same length $n$ and if there is a bijection between the sets of composition factors of each of these series such that corresponding composition factors are isomorphic.

**Theorem**(Hordan-Holder):
Let $A$ be a k-algebra, and let $M$ be an A-module. Then $M$ has a comspostion series if and only if $M$ is both Artinian and noetherian. In the case, any composition series of $M$ are equivalent.
*Proof*: 
Using induction, one get that $M$ is noetherian and artinian. Take two decomposition series $M=M_0 \supset M_1 \supset \cdots \supset M_n=\{0\}$ and $M=N_0 \supset N_1 \supset \cdots \supset N_k=\{0\}$, and suppose that $n >1$. Set $N=N_1$, consider 
$$M=M_0+N \supset M_1+N \supset \cdots \supset M_n+N=N=M_0 \cap N \supset M_1 \cap N \supset \cdots \supset M_n \cap N=\{0\}$$
Since $N$ is maximal, we know that there is a $i$ such that $M=M_i+N \supset M_{i+1}+N=N$, then we have $M/N \simeq (M_i+N)/(M_{i+1}+N) \simeq M_i/M_{i+1}$, and using induction, one get that $N_j/N_{j+1} \simeq (M_k \cap N)/(M_{k+1} \cap N) \simeq M_k/M_{k+1}$.

**Proposition**:
Let $U$ be a submodule of $M$, then there is a composition series with $U=M_i$.

**Definition**: 
Let $A$ be a k-algebra. The *Grothendieck group* of $A$ is the abelian group denoted $R(A)$ which is generated by the set pf isomorphism classes of finitly generated A-modules $U$, subject to the relation $[U]+[V]=[W]$ whenever there is a [[Short exact sequence]] for A-modules of the form $0 \longrightarrow U \longrightarrow V \longrightarrow W \longrightarrow 0$. We denote by $[U]$ the image of $U$ in $R(A)$. 
For a finite-dimensional algebra over a field has a particular simple structure: $[U]=\sum_{S}d(U,S)[S]$ where $S$ runs over a set of representatives of isomorphism classes of simple A-module and $d(U,S)$ is the number of $S$ in the composition factors of $U$.

# Semisimple modules
**Definition**:
Let $A$ be a k-algebra. An A-module $M$ is called *semisimple* if $M$ is the sum of its simple submoduels.

**Theorem**([[Schur's lemma]]): 
Let $A$ be a k-algebra. For any simple A-module $S$ the k-algebra $End_A(S)$ is a division algebra. For any two nonisomorphic simple A-module S,T we have $Hom_A(S,T)=\{0\}$.
*proof*:
Let $S,T$ be simple A-modules, and suppose there is a nonzero A-homomorphism $\phi:S \rightarrow T$. Then $ker(\phi) \neq S$, hence $ker(\phi)=\{0\}$ because $S$ is simple. Thus $\phi$ is injective. In particular, $im(\phi) \neq \{0\}$. Since $T$ is simple this implies $im(\phi)=T$. Thus $\phi$ is an isomorphism. The result follows.
*Remark*: 
This lemma leads to the following corollary: If $k$ is algebraically closed, and $A$ a k-algebra, then for a simple A-module $S$ of finite dimension over k, one has that $End_A(S)= \{\lambda id_S:\lambda \in K\}$.

**Theorem**:
Let $A$ be a k-algebra and let $M$ be an A-module. If $M$ is semisimple, so every quotient and every submoduel of $M$. Moreover, the following are equivalent:
1. $M$ is semisimple.
2. $M$ is a direct sum of simple modules.
3. Every submoduel $U$ has a compliment.
*Proof*: not difficult (will use zorn's lemma).

**Theorem**(Clifford):
Let $G$ be a finite group, let $N$ be a  normal subgroup of $G$ and suppose that k is a field. For any simple $k[G]$ module $S$, the restriction $Res_{N}^G(S)$ to $k[N]$ is a semisimple $k[N]$ module. Moreover, if $T,T'$ are simple $k[N]$-submodules of $Res_N^G(S)$ then there is an element $x \in G$ such that $T' \simeq xT$. In other words, the isomorphism classes of simple $k[N]$-submodules of $Res_N^G(S)$ are permuted transitively by the action of $G$.
*Proof*:
Let $T$ be a simple $k[N]$-submodules of $S$. Then using $nxT=x(x^{-1}nx)T \subseteq xT$, we know that $xT$ is also a submoduels of $S$ in $k[G]$. Then the sum of $xT$ is a $k[G]$-submodules of $S$, hence it is $S$ itself. 
*Remark*: 
This is just saying that every $S$ can be written in the from of $Ind_N^G(T)$ for some simple $k[N]$-module $T$.

# The Jacobson radical
**Definition**: The *Jacobson radical* $J(A)$ of a k-algebra $A$ is the intersection of the annihilators of all simple left A-modules. More explicitly, $J(A)$ is equal to the set of all $a \in A$ satisfying $aS=\{0\}$ for every simple A-module $S$.


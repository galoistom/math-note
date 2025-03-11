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
One side of the inclusion is clear, we shall proof the other side. Taking a k-basis $\{a_i\}_{i \in I}$ for $A$, and $\{z_j\}_{j \in J}$ for $Z(B)$. Then the set $\{a_i \otimes 1_B\}_{i \in I},\{1_A \otimes z_j\}_{j \in J}$ are basis for $A \otimes_k B,A \otimes_k Z(B)$ as a $B,A$ module. Thus $z \in A \otimes_k B$ can be writtne in the from $z=\sum_{i \in I}a_i \otimes b_i$ where $b_i$ are uniquely determined and almost all equal to 0. Now suppose $z$ centralises $1 \otimes_k B$, then we have $\sum_{i \in I}a_i \otimes bb_i=\sum_{i \in I}a_i \otimes b_ib$, using the uniquness, one gets $b_i \in Z(B)$ for all $i \in I$, so $z \in A \otimes_k Z(B)$. Suppose now that $z \in Z(A \otimes_k B)$, then $z \in A \otimes_k Z(B)$, so $z=\sum_{j \in J}c_j \otimes z_j$ is unique up to $c_j$. Using the same argument above, one proof he theorem.

Using the above theorem, one easily know that $Z(k[G \times H])=Z(k[G]) \otimes Z(k[H])$ if $H \leq G$. But in general, the twisted group algebra does not have the silimiar properties. In fact, the certer $Z(k_{\alpha}[G])$ may not be free as k-module since the multiplicative inverse of a group element $x$ is not necessarily $x^{-1}$. But there is another way to measure how far it is to be commutative is using the commutator space $[A,A]$ which is generated by $ab-ba$, $a,b \in A$. One might notice that $[A,A]$ is a $Z(A)$ module, so $A/[A,A]$ is also a $Z[A]$ moudle. 

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
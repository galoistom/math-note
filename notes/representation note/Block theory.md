We extend the ideal of [[Basic Definitions of representation]] to the modules of group algebra $k[G]$.

# Definitions
>[!note] Definition
>Let $G$ be a group. A representation of $G$ over $k$ is a pair $(V,\rho)$ consisting of a $k-module$ $V$ and a group homomorphism $\rho:G \rightarrow GL(V)$, where $GL(V)=Aut_k(V)$ is the group of $k-linear$ automorphism.

Morphism between two representations are simple, just preserve the module structure and the $G$ action over it.

# Twisted group algebra
We want to construct different pultiplication for $k[G]$. Let $\alpha:G \times G \rightarrow k^\times$ be a max, and multiplication be $x \cdot y=\alpha(x,y) xy$, then the multiplication is associative if and only if $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)\alpha(y,z)$. We extend this definition to general abilian group $Z$, thus we get the definition of the 2-cocycle $Z^2(G;Z)$, i.e. all $\alpha:G \times G \rightarrow Z$ such that, $\alpha(xy,z)\alpha(x,y)=\alpha(x,yz)(^x\alpha(y,z))$. But one might notice that when viewing $k_\alpha[G],k_\beta[G]$ with multiplication $\alpha,\beta$, if there is a scalar $\gamma:G \rightarrow k^\times$ s.t.$\alpha(x,y)=\beta(x,y)\gamma(x)\gamma(y)\gamma(xy)^{-1}$(i.e. there is an isomorphism between $k_\alpha[G] \simeq k_\beta[G]$ by sending $x \mapsto \gamma(x)x$), then there is no much different between the multiplications, and note that $\alpha(x,y)=\gamma(x)(^x\gamma(y))\gamma(xy)^{-1}$ where $\gamma(x)=(^xz)z^{-1}$ for some $z \in Z$ forms a subgroup of $Z^2(G;Z)$, we shall denote it by $B^2(G;Z)$. Now, by lowering the dimension one get $Z^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that $\gamma(xy)=\gamma(x)(^x\gamma(y))$, and $B^1(G;Z)$, the set of $\gamma:G \rightarrow Z$ such that there is a $z \in Z$ s.t. $\gamma(x)=(^xz)z^{-1}$. Using quotient, we get the [[Cohomology on groups]] $H^1(G;Z)=Z^1(G;Z)/B^1(G;Z)$ and $H^2(G;Z)=Z^2(G;Z)/B^1(G;Z)$.
**Remark**: Using the above interpretation, one get a natural link between $H^i(G;Z)$ and $Ext_{\mathbb{Z}[G]}^i(\mathbb{Z},Z)$ through the extension of group $G$:
$$1 \longrightarrow Z \stackrel{l}{\longrightarrow} \widehat{G} \stackrel{\pi}{\longrightarrow} G \longrightarrow 1$$where the multiplication $\widehat{x}\cdot\widehat{y}=\alpha(x,y)\widehat{xy}$.

# G-algebras
We already have $G-module$, so it is natural to consider the concept of $G-algebra$. The definition is straightforward: simply giving an algebra $A$ a $G-action$ over it, specificly, the homomorphism between $G \rightarrow A^\times$ is called the *structural homomorphism of the interior G-algebra A*. Moreover, the algebraic morphism $A \rightarrow B$ preserving the $G-action$ is called the homomorphism of $G-algebra$. 

# Category algebra
One might now that a group $G$ is a special monoid category. So we extend the idea of group algebra to category algebra, where the morphism between objects take the place of group action. This lead to the quiver algebra, which is the quotient $A=k\mathcal{C}/I$, where $I$ is an ideal of the algebra. 
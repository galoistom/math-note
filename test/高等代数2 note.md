# adjoint function
Let $T:V \rightarrow W$ be a linear transformation and $V$ has a symmetric bilinear mesures, then $T^*:W \rightarrow V$ is called the adjoint function if and only if $(Tv_1|v_2)=(v_1|T^*v_2)$ for all $v_1,v_2 \in V$.
Recall that $ker(T)=ker(T^*T:V \rightarrow V)$, and that $T^*T \in End(V),TT^* \in End(W)$, both are self-adjoint and positive semidefinite.

# SVD
Let $T:V \rightarrow W$ be linear transformation and $n=dim(V),m=dim(W)$, then there is a ONB(单位正交基) $v_1,v_2, \cdots,v_n$ and $w_1,w_2,\cdots,w_m$ and $\sigma_1\geq\sigma_2\geq\cdots\geq\sigma_q$, $q=\min\{m,n\}$, such that $Tv_i=\sigma_i w_i$ if $1 \leq i \leq p$ and $Tv_i=0$ if not. The $(\sigma_i)$ are uniquely determined by $T$ which is called the sigular value of $T$. Using the language of matrix, then it is that for any $A \in M_{n \times m}(\mathbb{R})$, then there is $P \in SO(m),Q\in SO(n)$ such that $Q^{-1}AP$ is sort of "diagonal".
**We proof the uniqueness**: We claim that $T^*w_j=\sigma_jv_j$ if $j \leq p$. We let $S$ to satisfy the condition, then $(v_i|Sv_j)=\sigma_j \delta_{ij}$, note that $(Tv_i|v_j)=\sigma_i\delta_{ij}$, then we have $(T|\cdot)=(\cdot|S)$, hence $S=T^*$. After that, we note that $\sigma_i^2$ is the eigenvalue of $T^*T$, so the $\sigma_i$ are uniquely determined.(Using the above result, we can easily construct the $P,Q$, so existence is clear)

# MP inverse
Let $T:V \rightarrow W$ and $S:W \rightarrow V$, we say $S$ is the MP inverse of $T$ if and only if:1.$STS=S$ 2.$TST=T$ 3.$(ST)^*=ST$ 4.$(TS)^*=TS$. We will proof that this inverse is unique.
**The existence:** Let $v \in V, w \in W, v' \in ker(T), v'' \in ker(T)^{\perp}, w' \in im(T), W'' \in im(T)^\perp$ with $v=v'+v'',w=w'+w''$ and $Tv=w'$ we set $Sw:=v''$. It is easy to check that $S$ is well defined. As to the uniquess, suppose $S,R$ are both MP inverse of $T$, then we have 
$$
S=STS=S(TS)^*=SS^*T^*=SS^*(TRT)^*=SS^*T^*R^*T^*=S(TS)^*(TR)*=STSTR=STR
$$
Hence $S=STR=R$.

# proposition1:
Let $T:V \rightarrow W$ be a linear transformation, $r:=rank(T)$
Using SVD, we have ONBs: $v_1,v_2, \cdots, v_m$ of V, and $w_1,w_2, \cdots, w_n$ of W, and singular values $\sigma_1\geq\sigma_2\geq\cdots$.
Define $S:W \rightarrow V$, with $Sw_j=\frac{1}{\sigma_J}v_i$ if $1 \leq j \leq r$ and 0 if not.
then $S$ is the MP inverse of $T$.

we proof this using the explicit construction of MP inverse. for any $w \in W$, $w=\sum\limits_{j=1}^{n}a_jw_j$, and $imT=<w_1,w_2, \cdots, w_r>$, hence $w'=\sum\limits_{j=1}^{r}a_jw_j$, and $v=\sum\limits_{i=1}^{r}\frac{a_j}{\sigma_J}v_j \in V$, then $v \in ker(T)^{\perp}$, hence the projection of $v''$ to $ker(T)^{\perp}$ is v. hence $Sw=v''$ agrees with the construction above.

# Min-Max principle:
Let V be a vector space with natural inner product and $B:V\times V \rightarrow \mathbb{R}$ be a symmetric bilinear form. then there is a unique $S \in End(V)$ such that $B(v_1,v_2)=(v_1|Sv_2)$. giving it a corodinates, then we get there is a unqiue $A \in M_{n \times n}(\mathbb{R})$ such that $B(v_1,v_2)=v_1^{T}Av_2$, moreover, if B is symmetric, we have $A^T=A$,i.e. $S=S^*$. Take $v_1,v_2,\cdots,v_n$ of V, s.t. $Sv_i=\lambda_iv_i$ for all i, $\lambda_1\geq\cdots\geq\lambda_n$.
Simple observation:$\lambda_1=\max\limits_{\lVert v \rVert=1} B(v,v), \lambda_n=\min\limits_{\lVert v \rVert=1} B(v,v)$.
Using this fact, we can give another proof of 正交对角化定理: note that $S^n$ is compact, hence $\max\limits_{\lVert v \rVert=1} (v,Sv)$ exists, and using the fact that $S=S^*$, then we get the max point $v$ is an eigenvector of S (Langrange multiples).
Theorem(Coueant-fischer)
Given B, for a $k<1<n=dim(V)$, we have $\lambda_k=\min\limits_{dim(U)=n-k+1}(\max\limits_{\lVert v \rVert=1 \in U}B(v,v))$, and $\lambda_k=\max\limits_{dim(U)=k}(\min\limits_{\lVert v \rVert=1 \in U}B(v,v))$.
*Proof*: we only need to proof the frist one. Assume $U \subset V, dim(U)=n-k+1$, then $dim(U \cap <v_1,\cdots,v_k>)=dimU+k-dim(U+<v_1,\cdots,v_k>)\geq 1$. We can then take $v=\sum\limits_{i=1}^{k}a_iv_i, \lVert v \rVert=1$, then $B(v,v)=\sum\limits_{i=1}^{k}\lambda_ia_i^2 \geq\lambda_k$, we now check that the maximum exists: Take $U=<v_k,\cdots,v_n>$, then for any v, we have $B(v,v) \leq \lambda_l$, hence the inf is attained.

*This is also related to SVD:* 
proposition2: Let V,W be finite dimensional vector space with inner product. and $T:V\rightarrow W$ be linear transformation and $\sigma_1\geq\cdots$ be its singular values of T. Let $\sigma_i=0$ if i>min(dimV,dimW). Then $\sigma_1=\max\limits_{v \neq 0} \frac{\lVert Tv \rVert}{\lVert v \rVert}$, $\sigma_i=\min\max\frac{\lVert Tv \rVert}{\lVert v \rVert}$, and $\sigma_{dimV}=\min\limits_{V\neq0}\frac{\lVert Tv \rVert}{\lVert v \rVert}$. We proof this by taking $S=T^*T$, and $B(v_1,v_2)=(v_1|T^*Tv_2)=(Tv_1|Tv_2)$, hence $B(v,v)=\frac{\lVert Tv \rVert^2}{\lVert v \rVert^2}$, recall that $\sigma_i^2$ is the eigenvalue of $S$, using the theorem above and take square root, then we are done.

# Positive matrix:
We define $A \geq B$ if $a_{ij}\geq b_{i,j}$. Then $A>0,A\geq0$ make sense. Then we have the following lemma: if $A \in M_{m \times n}(\mathbb{R})>0, x \in \mathbb{R}^n\geq0$, then $Ax>0$. To study eigenvalues and eigenvector of $A>0$. Define the spectral radius $S(A)=\max\limits_{\lambda}|\lambda|$, where $\lambda$ runs through A' eigenvalues.
Theorem: Let $A>0$
1. if S(A)>0, then there is a $v>0$ such that $Av=S(A)v$.
2. if $\mu$ is a eigenvalue of A $\neq S(A)$, then $|\mu|<S(A)$. 
3. the S(A)-eigenspace has dim 1.
4. S(A) is a simple root of A 的特征多项式.
(More general version for $A\geq0$(+conditions) "Perron-Frobenius Theorem")

**we proof the frist statement**: Let $S:=\{x\in \mathbb{R}^n:\lVert x \rVert=1,x\geq0\}$, which is compact. Consider the continuous map $\mathcal{L}:S \rightarrow \mathbb{R}_{\geq0}$, $x \mapsto \min\{\frac{(Ax)_i}{x_i}:1 \leq i \leq n, x_i \neq 0\}$. So there is a $v \in S$ that attains the maximum $S>0$ at v. We claim that $Av=S(A)v$. $\mathcal{L}(v)=S$ hence $Av \geq Sv$ if $Av\neq Sv$, then $Av-Sv>0$, so we get $A(Av-Sv)>0$. For a small $\epsilon>0$ $A(Av-Sv)>\epsilon Av$, thus $Aw>(S+\epsilon)w$, where $w=t\cdot Av$, which is to say $\mathcal{L} \geq S+\epsilon$. the contradiction shows that $Av=Sv$. We also have $S \leq S(A)$, to show $S=S(A)$, we take $\mu\in\mathbb{C}, w\in \mathbb{C}^n-{0}, Aw=\mu w$,then for any i, $|(\mu w)_i|=|\mu||W_i|$, so $|\sum a_{ij}w_j| \leq \sum a_{ij}|w_j|$, we now take $w'\in\mathbb{C}^n$ whose i-th value is $|w_i|$, scaling it to have absoluate value 1. Hence $S(A) \geq S \geq \mathcal{L}(w') \geq |\mu|$ for all eigenvalue $\mu$, thus we have $S=S(A)$.

**We now proof (2)**: what we need is to show that $|\mu|=S(A)$ leads to $\mu=S(A)$. The consiquence is that $|\mu|=S(A)$ shows that $\mathcal{L}(w')=\max \mathcal{L}$, hence $\sum\limits_{j}a_{ij}|w_j|=|\sum\limits_j a_{ij}w_j|$, so $w_i$ are all on the same ray in $\mathbb{C}$. Take a $c \in \mathbb{C}$ such that $c^{-1}w_i \in \mathbb{R}_{\geq0}$, then we have $A(c^{-1}w)=\mu(c^{-1}w)$, hence $\mu \in \mathbb{R}_{\geq 0}$, so we have $\mu=S(A)$.

**Proof of (3)**: Suppose $v,v' \in \mathbb{R}^n$, $Av=S(A)v,Av'=S(A)v'$, and $v>0$, we want to show that $v' \in \mathbb{R}v$. If not, we may choose $\epsilon>0$ s.t. $v-\epsilon v'>0$, but $\exists i,(v-\epsilon v')_i=0$. Then $(v-\epsilon v')=S(A)^{-1}A(v-\epsilon v')>0$, a contradictiom.

**Proof of (4)**: May assume $n \geq 2$. Fix $v>0$, $Av=S(A)v$, $S(A)=S(A^T)$. Then $\exists u\in\mathbb{R}^n,u>0,s.t.A^Tu=S(A)u$, let $\langle u \rangle:=\mathbb{R}u, \langle u \rangle^{\perp}:=\{x\in\mathbb{R}:u^{\perp}x=0\}$ is A-invariant. Note that $\langle u \rangle^{\perp}$ has dimension n-1 and $u^Tv=0$, we have $\mathbb{R}^n=\langle v\rangle \oplus \langle u \rangle^{\perp}$, so $Char_A=Char_{A|_{\langle v \rangle}} \cdot Char_{A|_{\langle u \rangle^{\perp}}}$. If $(x-S(A))^2|Char_A$, then $Char_{A|_{\langle u \rangle^{\perp}}}(S(A))=0$, so we get a $S(A)-eigenvector$ $v'$ in $\langle u \rangle^{\perp}$, contradicting (3).#
**More general version**: Forbenius-perron Theorem for $A \geq 0$.
**Application**: Page rank algorithm.

# Complex inner product
**Recall**: real IRS=$\mathbb{R}$-v.s V + symmetric bilinear form which is positive definite.
Idea: complex $\times$ IPS=$\mathbb{C}$- v.s. V form $(\cdot|\cdot):V\times V \rightarrow \mathbb{C}$ with pisitive definite.

**Definition**: Let $T:V\rightarrow W$ be a map between $\mathbb{C}-v.s.$ If $T(v_1+v_2)=Tv_1+Tv_2$ and $T(zv_1)=\bar{z}\,Tv_1$, we say that it is a semi-linear(半线性)
A cplx IPS:=$\mathbb{C} -v.s.$ V + map $(\cdot|\cdot):V\times V \rightarrow \mathbb{C}$, linear in $v_2$ and semi-linear in $v_1$, then $(v_1|v_2)=(v_2|v_1),(v|v)+0$. 

**Construction**: given a $\mathbb{C}-v.s.$ V, consider the same set V ans the same $+:V\times V\rightarrow V$, but with $\odot:\mathbb{C}\times V\rightarrow V$ that $(z,v) \mapsto \bar{z} v$. Then $(V,+,\odot)$ forms a $\mathbb{C}-v.s.$, we denote it as $\overline{V}$. Then we have $\overline{\overline{V}}=V$, and are additive under direct sum, mean while, by sending $z\mapsto \bar{z}$, we get an isomorphism between $\mathbb{C}$ and $\overline{\mathbb{C}}$. Moreover, semi-linear map $T:V\rightarrow W$ is the linear map $\overline{V} \rightarrow W$ or $V \rightarrow \overline{W}$, thus $Hom(\overline{V},W)=Hom(V,\overline{W})$. We also notice that $\overline{Hom(V_1,V_2)}=Hom(\overline{V_1},\overline{V_2})$. Recall that $V^*=Hom(V,\mathbb{C})$, then we have $\overline{V}^*=\overline{Hom(V,\overline{\mathbb{C}})}$ and is isomorphic to $\overline{Hom(V,\mathbb{C})}=\overline{V^*}$. 

**Definition**: Let $V,W,X$ be $\mathbb{C}-v.s.$ We asy a map $B:V\times W\rightarrow X$  is a sesquilinear(半双线性) if $B$ is semi-linear in $V$ and linear in $W$. All sesquilinear $V\times W \rightarrow X$ form a $\mathbb{C}-v.s$ by $(B_1+zB_2)(v,w)=B_1(v,w)+zB_2(v,w)$, where $B_i$ sesquilinear and $z \in \mathbb{C},v\in V,w\in W$. Specially, let $X=\mathbb{C}$, then we get the definition of sesquilinear form.

**Definition**: Let $B:V\times W \rightarrow \mathbb{C}$ be sesquilinear, then the left radical is $ker(B(\cdot,W))$, similiarly, right radical is $ker(B(V,\cdot))$. When $dimV,dimW<\infty$, if let and right radical are both $\{0\}$, then we say $B$ is nondegenerated. Similiar to real bilinear form, we have that when $dimV=dimW$ then $B$ is nondegenerated $\Longleftrightarrow$ Left rad = $\{0\}$ $\Longleftrightarrow$ Right rad = $\{0\}$. We can also get that if $B$ is nondegenerated, we induces $W\simeq \overline{V}^*,\overline{V}\simeq W^*$.
Sesquilinear forms and maxraices: Let $V=\mathbb{C}^n,W=\mathbb{C}^m$, the $B$ takes the form of $A\in M_{m\times n}(\mathbb{C})$. 

Definition: Let $V:\mathbb{C}-v.s.$ $\epsilon\in \{1,-1\}$, $B:V\times V\rightarrow \mathbb{C}$ is a sesquilinear, we say that $B$ is $\epsilon-Hermitian$ if $\overline{B(v,w)}=\epsilon B(v,w)$ 

# Adjoint linear maps
**Def-prop** Let $B_1:V_1\times V_1' \rightarrow \mathbb{C}$ and $B_2:V_2\times V_2' \rightarrow \mathbb{C}$ be nondegenerated sesquilinear forms, then there is a semi-linear map $Hom(V_1,V_2) \rightarrow Hom(V_1',V_2'),T\mapsto T^*$, characterized by $B_2(T(v_1),v_2')=B_1(v_2,T^*(v_1'))$, there is also a $Hom(V_1',V_2')\rightarrow Hom(V_1,V_2)$ such that $B_2(v_2, T(v_1'))=B_1(^*T(v_1),v_1')$. There are three ways to proof this:
1. Repeat the proof in the bilinear case
2. Reduce to the bilinear case by passing $\overline{V_1},\overline{V_2}$.
3. Look at the matrices: $V_i,V_i'$ can be written in the form of $\mathbb{C}^{m_i},\mathbb{C}^{m_i'}$ up tp isomorphism, which maps $B_i$ to invertible matrix $A_i \in M_{m_i\times m_i'}(\mathbb{C})$, then $$B_2(Tv_1,v_2')=(Tv_1)^tA_2v_2=v_1^tT^tA_2v_2=v_1^tA_1A_1^{-1}T^tA_2v_2=v_1^tA_1T^*v_2$$the other one is similiear
**Observation**: 1.$(ST)^*=T^*S^*,^*(ST)=^*T^*S$ 2. $^*(T^*)=T=(^*T)^*$ 3. If $\epsilon=\pm 1$ both $B_1,B_2$ are $\epsilon-Hermitian$, then $^*T=T^*.

**Definition**: Given a nondegenerated $\epsilon-Hermitian$ form ($\epsilon=\pm1$) $B:V\times V\rightarrow \mathbb{C}$, and $T\in End(V)$, then $T=T^*$ is self-adjoint, $T^*=-T$ is anti-adjoint.
**Remark**: Let $c\in i\mathbb{R}-{0}$, then $B:V\times V \rightarrow \mathbb{C}$ is Hermitian $\Longleftrightarrow$ $cB$ is anti-Hermitian, $T \in End(V)$ is self-adjoint $\Longleftrightarrow$ $cT$ is anti-adjoint.

**Definition**: $dimV<\infty, B:V\times V\rightarrow \mathbb{C}$ be $\epsilon-Hermitian$, Then $T\in End(V)$ is normal if and only if $T^*T=TT^*$.

# Hermitian forms
Recall the quadratic forms say over $\mathbb{R}$. Then a $\sum\limits_{1\leq i,j\leq n}a_{ij}x_ix_j$, where $a_{ij}=a_{ji}$, is equvalient to a $A\in M_{n\times n}(\mathbb{R})$ where $A^T=A$, and a bilinear form $B:\mathbb{R}^n\times\mathbb{R}^n\rightarrow\mathbb{R}$.
We usie the similiar notions. Let $\sum\limits_{1\leq i,j\leq n}a_{ij}\overline{x_i}x_j$ be hermitian form, then it is equvalient to $A\in M_{n\times n}(\mathbb{C}): \epsilon-hermintian$ and $B:\mathbb{C}^n\times\mathbb{C}^n\rightarrow\mathbb{C}$ a $\epsilon-hermintian\}$.
To classify them, we can reduce to the quadratic forms over $\mathbb{C}$, or using "spectral theorem" for self-adjoint matrices, or copy the arguments for quadratic forms.

Using the third way: 
1. 对角化, we state that for any $f=\sum\limits_{1\leq i,j\leq n}a_{ij}\overline{x_i}x_j$ is $\simeq$ to a "diagonal" $f'=\sum a_i |x_i|^2,a_i\in \mathbb{R}$. 配方即可
2. 伸缩, let $x_i'=|a_i|^{\frac{1}{2}}x_i$, then we reduce to the case where $a_i\in\{1,0,-1\}$, so it can be expressed as $|x_1|^2+\cdots+|x_p|^2-|x_{p+1}|^2-\cdots-|x_{p+q}|^2$, where $p,q\in \mathbb{Z}_{\geq 0},\,p+q\leq n$.
Thus we get the following proposition: Given $n\in \mathbb{Z}_{\geq 1}$, then the hermitian form $\{f:\mathbb{C}^n \rightarrow \mathbb{R}\}$ has a one-to-one morphism to $\{(p,q)\in\mathbb{Z}_{\geq0}:p+q\leq n\}$.

**Definition:** Given $V:\mathbb{C}-v.s.$ and $B:V\times V\rightarrow \mathbb{C}$ be hermitian form, we say that $B$ is positive semi-definite if an only if $B(v,v)\in \mathbb{R}$, and positive definite if $B(v,v)\geq 0$ for all $v$. Those notion is only related to the isomorphism class of $(v,B)$, hance is determined by the pair $(p,q)$, and the first case is that $q=0$, the second is $p=n$, for other notion similiar to quadratic forms, we won't write that down specifically.

**Definition:** If an Hermitian form $(|):V \times V \rightarrow \mathbb{C}$ which has positive definite, then it is called a Hermitian IPS. Then for all $v\in V$, we define $\Vert v \Vert := \sqrt{(v \vert v)}$. If $\Vert v \Vert =1$, then we sety that $v$ is a unit vector. Let $S \subset V$, we say that $S$ is orthogonal if $\forall v\neq w \in S, (v \vert w)=0$, and $S$ is orthonormal if $S$ is orthogonal and $\forall v\in S, \Vert v \Vert =1$. It is easy to see that if $S$ is orthogonal, then it is linearly independent.

**Definition:** $V:IPS/\mathbb{C}$, let $V_0,V_1 \subset V$ be subspaces, then $V_0 \perp V_1$ means that $\forall v_0 \in V_0, v_1 \in V_1, (v_0 \vert v_1)=0$. Given a family of $(V_i)_{i \in I} \in V$, if $V = \bigoplus V_i$, and $V_i \perp V_j$ then we say that $V$ is orthogonal direCT sum of $(V_i)_{i \in I}$.
**Fact**: If $V:IPS/\mathbb{C}$, and $V_0 \subset V$,be a subspaces, $dimV_0<\infty$, then $V_0^\perp :=\{v \in V: (v_0 \vert v)=0, \forall v_0 \in V_0 \}$ has the property of $V=V_0 \oplus V_0^\perp$.

**Theorem**(Caushy-Bunyakousky-Schwary): In a $V:IPS/\mathbb{C}$, we have 
$$\vert (v | w) \vert^2  \leq (v | v) \cdot (w|w),\forall v,w \in V$$
Proof: For all $t \in \mathbb{C}$, we have $0 \leq \Vert v+tw \Vert^2 = \Vert v \Vert^2 + 2Re(v|tw) + \Vert tw \Vert^2$, put $t=\frac{-(w|v)}{(w,w)}$, to get $0 \leq \Vert v \Vert^2 - \frac{|(v|w)|^2}{(w|w)}$, the equality holds if and only if there is a $t \in \mathbb{C}$ such that $v+tw=0$. This theorem leads to the triangle inequality $\Vert v+w \Vert \leq \Vert v \Vert + \Vert w \Vert$. #

**Theorem**(Gram-Schmidt):  Let $V:IPS/\mathbb{C}$ and $v_1,v_2, \cdots$ be linearly independent in $V$, define inductively, let $w_1=v_1$ and $w_k=v_k-\sum\limits_{i=1}^{k-1} \frac{(w_i|v_k)}{(w_i|w_i)}w_i$, then $(w_i)$ are orthogonal and $\langle v_1, \cdots, v_k \rangle=\langle w_1, \cdots, w_k \rangle$.
Proof: trivial.#
Using this theorem, we can extend a set of orthogonal elements to a orthogonal basis of a finite dimensional $IPS/\mathbb{C}$. Moreover, there will always be an orthonormal basis for finite dimensional $V:IPS/\mathbb{C}$.

Examples: 
1. standard inner product on $\mathbb{C}^n$, the standard basis is an ONB.
2. Function space: Let $a<b \mathbb{R}$ and $C[a,b]:=\{f:[a,b] \rightarrow \mathbb{C},\, continuous\}$ be a $\mathbb{C}-v.s.$ by $(f+cg)(x)=f(x)+cg(x)$, and $(f|g):= \int_a^b \bar{f}g dx$. Then $\mathbb{C}[x]$ restric to $[a,b]$ forms an ONB in $C[a,b]$.

Notions of isomorphism: Let $V,W:IPS/\mathbb{C}$ If $T\in Hom(V,W)$, $\Vert Tv \Vert_W= \Vert v \Vert_V$, then we say that $T$ is isometry. Notice that $T$ is isometry $\Longleftrightarrow$ $T$ preserve the inner product. Moreover $T$ is an isomorphism between $IPS/\mathbb{C}$. Suppose $dimV=n \in \mathbb{Z}_{\geq1}$, then the isomorphism $\mathbb{C} \rightarrow V$ has a bijection with the ordered ONB of $V$.

**Definition**: the unitary operator on an $IPS/\mathbb{C}$ is the isomorphism $T:(V,(|)) \rightarrow (V,(|))$,  such that $T^*=-T$, a matrix is unitary if and only if $^\dagger A=-A$. We can see that $P$ unitary $\Longleftrightarrow$ $^\dagger PP=I_n$. On the other hand, it is also equvalient to $P \cdot (^ \dagger P)=I_n$. 

# Spectral theorem for normal operators
Recall: $T \in End(V)$, is said to be normal if $TT^*=T^*T$.

**Theorem**: The following are equvalient for $T \in End(V)$:
1. there is an $ONB$ $v_1, \cdots v_n$ of $V$ and $\lambda_1 \cdots \lambda_n \in \mathbb{C}$ s.t. $Tv_i=\lambda_iv_i$ for all $i$.
2. $T$ is normal.
Taking $V=\mathbb{C} + std.IP$, then 1 says: $T$ unitary such that $P^{-1}AP$ is diagonal matrix when $A \leftrightarrow T$. 

Proof: 
1. ($1 \rightarrow 2$) Choosing $ONB$ of $V$, one may assume $V=\mathbb{C}^n,\,T \leftrightarrow A\in M_{n\times n}(\mathbb{C})$, then $P^{-1}AP=diag(\lambda_1, \cdots, \lambda_n)$, so we have $T^* \leftrightarrow \,^\dagger P^{-1}diag(\overline{\lambda_1}, \cdots, \overline{\lambda_n})\,^\dagger P=Pdiag(\overline{\lambda_1}, \cdots, \overline{\lambda_n})P^{-1}$ hence $T$ is normal.
2. ($2 \rightarrow 1$) Any $T \in End(V)$, decomposes uniquely as $T'+T''$, with $(T')^*=T',\,(T'')^*=-T''$. If $T$ is normal, then $T'T''=T''T'$.  One should also noteice that if $V_0 \subset T$ is a $T-invariant$ subspace, then $V_0^{\perp}$ is $T^*-invariant$. 
3. The first case is when $T^*=T$, we proof that  there is a $v_1 \in V,\lVert v_1 \rVert =1$ and $\lambda_1 \in \mathbb{R}\, s.t.\, Tv_1=\lambda_1v_1$.  Just consider any eigenvalue $\lambda$ we have $(Tv_1|v_1)=\lambda(v_1|v_1)$ hence $\overline{\lambda}=\lambda$. Using the facts mentioned above, we now that we can split $V=\langle v_1 \rangle \oplus \langle v_1 \rangle^{\perp}$ and use induction. Thus we proof the case.
4. The second case s when $T^*=-T$, one might notice that multiplying $\sqrt{-1}$, one get the case of 3.
5. Third case is the general case. Let $T=T'+T''$, then $T'T''=T''T'$,  同步正交对角化 $V=V_{\mu_1} \oplus \cdots \oplus V_{\mu_m}$ where $\mu_1, \cdots, \mu_n$ are the distinct eigenvalue of $T'$ and $V_{\mu_i} \perp V_{\mu_j}$ if $i \neq j$, where $V_{\mu_i}$ is the eigenspace of $\mu_i$. Notice that $T'T''=T''T'$, so $V_{\mu_i}$ is stable under $T''$, and $(T''|_{V_{\mu_i}})^*=-(T''|_{V_{\mu_i}})$, so $V_{\mu_i}$ has an $ONB$ consisting of eigenvectors of $T''$, so we get an $ONB$ of $V$. Both $T',T''$ acts on it as a scalers and so does $T=T'+T''$.

# Facts for $IPS/\mathbb{R}$ carry over to $\mathbb{C}$
**Theorem**: Let $f:\mathbb{C}^n \rightarrow \mathbb{R}$ be an hermitian form corresponding $A \in M_{n \times n}(\mathbb{C})$ then $f$ is positive definite if and only if all the eigenvalues of $A$ are positive. 
Proof: Using the spectral theorem, there is a unitary $C$ s.t. $^\dagger CAC=diag(\lambda_1, \cdots, \lambda_n)$, where $\lambda_i \in \mathbb{R}$, hence $f \simeq \sum\limits_{i=1}^n \lambda_i|x_i|^2$ as hermitian form on $\mathbb{C}^n$, so every $\lambda_i \geq 0$.

Let $T \in End(V),\,^*T=T$, then $(v_1,v_2) \mapsto (Tv_1|v_2)=(v_1|Tv_2)$ is Hermitian. We say $T$ is positive definite if this Hermitian form is. Let $V,W$ be $IPS/\mathbb{C}$ ans $Hom(V,W)$ $\Rightarrow$ $T^*T \in End(V),\,TT^* \in End(W)$ are both simi-definite as $(T^*Tv|v)=(Tv|Tv) \geq 0$, in fact $kerT^*=(imT)^\perp$, noticing that $(T^*w|v)_W=(w|Tv)_V$.

**Def-prop**: If $T\in End(V)$  is positive definite, then there is a unique $S \in End(V)$ such that $T$ is positive definite and $S^2=T$, we denote $S$ as $\sqrt{T}$. (The proof is the same as the case in $\mathbb{R}$ using spectral therorem.)

**Theorem**(极分解/polar decomposition): Let $T \in End(V)$ be invertable, then there is a unique pair of $R,U \in End(V)$ s.t. $T=RU$ and $R$ is opsitive definite $R^*=R$ and $U$ unitary. (Special case is when $V=\mathbb{C}$, the theorem is simply $z=r \cdot\exp(i\pi \theta)$)
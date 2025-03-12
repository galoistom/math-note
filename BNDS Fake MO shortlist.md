# N
1. 给定$n \in \mathbb{N}^+$, 求能写成为 $\sum\limits_{i=1}^{n} \frac{a_i}{b_i}$ 的最小正数, 其中$a_i,b_i$为绝对值不超过$n$的非零整数.(DHY)
2. $A \subset \mathbb{N}$ 为一个无穷集合, 且满足 $\sum\limits_{a \in A} \frac{1}{a}$ 收敛, 对任一正整数$n$定义 $\Delta(n):=\sum\limits_{d|n,d \in A} d$, 以及$B:=\{n \in \mathbb{Z}: \Delta(n) \geq n\}$. 问:$\sum\limits_{b \in B} \frac{1}{b}$ 是否收敛?(LXY)
3. 甲乙二人玩一个游戏, 两人已知一个多项式$P \in \mathbb{Z}[x]$, 两人每次从$\mathbb{N}$中各取出一个数, 分别放入集合$A,B$, 不能重复选取, 要求
	- 甲先选, $A$中的元素不相邻, 且甲所选数不能为当时剩下数中最小的那个.
	- 乙每次选一个比甲这次选的数小的数.
	若存在某个时刻使得甲选取$a_1,\cdots, a_k \in A,\ b_1,\cdots, b_k\in B$ (可重), 使得 $P|\sum\limits_{i=1}^{k}a_ix^{b_i}$,则甲胜, 若乙可以保证甲无法获胜则乙胜. 求所有$n$次无实根的$P$使甲有必胜策略.
4. 对于$P \in \mathbb{Z}[x]$, 定义$T_P:=\{k \in \mathbb{Z}_{\geq 2}: P(x)|P(x^k)\}$, 求证:若$T_P \neq \emptyset$, 则$T_P$为无穷集.(LHB)
5. 给定$n,k \in \mathbb{N}^+$, 设$a_1, \cdots, a_k,b_1, \cdots, b_k$为$2k$个绝对值不大于$n$的非零整数, 记$L$为$1, \cdots, n$中$k$个两两互素的质数之积, 若不存在则$L=lcm(1,\cdots,n)$, 证明:$\sum\limits_{i=1}^{n} \frac{a_i}{b_i}$的最小正取值为$\frac{1}{L}$.(LHB,DHY)
6. 给定$n$次首一整系数多项式$P$以及$T_P:=\{k \in \mathbb{Z}_{\geq 2}: P(x)|P(x^k)\}$, $f(k):=\# \{t \in T_P: 1<t \leq k\}$, 已知$f(x)\neq0$能成立, 证明:对$\forall c>0$, 存在$N \in \mathbb{N}$使$\lim\limits_{k \rightarrow \infty}\frac{f(k)}{k} \geq c \cdot \sqrt{\frac{\ln n}{n}}$ 对任意$n\geq N$成立.(LHB)
7. 求所有$(x,y) \in \mathbb{Z}^2$满足$y^2=x^3-19$.(LZM)

# C 
1. 一个圆盘上顺时针依次有$n$个可以放置箱子的位置, 现在Bmoer将$n$个箱子任意摆放在这$n$个位置上, 可以有位置为空, 也可以有位置叠了若干层($\leq 3$)之后每次做如下操作
	- 将第一层的箱子顺时针移动一个位置
	-  不动第二层的箱子
	- 逆时针移动第三层的箱子一个位置
	称以上操作为一轮, 问:最少操作多少多少轮可以使所有箱子均在第一层?(DNY)
2.  现有$n$个不同的盒子和$n$种不同的小球各$k$个, 在每个盒子中随意放入$k$个小球, 小明每次可以
	- 在某个盒子中取出或放入$p$个相同的小球
	- 将$n$个不同种类的小球各放一个进不同的箱子
	问:小明是否可以在有限步之内清空盒子(LZM)
3. 在一张无穷大的方格表上已选出了$n$个方格, 求最小的正整数$S$使得总可以找到若干两两不相邻的的方格表矩阵覆盖所有$n$个方格(其中两个矩形被称为是相邻的若他们有公共边).(LXY)

# A
1. 求所有的$x_1,\cdots,x_n\in\mathbb{R}$,满足$\sum\limits_{i=1}^nx_i=0,\,\sum\limits_{i=1}^nx_i^2=n-1,\,(\max\limits_{1 \leq i \leq n}x_i-\min\limits_{1 \leq i \leq n}x_i)^2=\frac{n^2+n}{3}$.(LHB)
2. 已知$a_1,\cdots,a_n \in\mathbb{R}^+$在下表$mod\, n$的前体下定义$b_i=\frac{a_{i-1}a_{t+1}}{a_i}\ c_i=a_{i-1}+a_{i+1}$, 证明:$\sum\limits_{i=1}^nc_i \geq \sum\limits_{i=1}^n \frac{a_i^2(a_i+b_i+c_i)}{(a_i-b_i)^2+(b_i-c_i)^2+(c_i-a_i)^2}$. (LHB)

# G
1. 在$\triangle ABC$中$I$为内心, $O$为外心, $P$为$\odot O$上$\widehat{BC}$上终点, $T$为$\odot O$上一点使得$\angle PTI=\frac{\pi}{2}$, $\omega$为过$I,T且切$$AP$于$I$的圆, $\omega$与$IO$交于另一点$K$. 证明:$\cdot (AIK)$且切$IT$于$I$.(LHB)
2. $\triangle ABC$中$I$为内心, $T$为$A$所对的伪内切圆切点, $S=IT \cap BC$, $ID \perp BC$于$D$.求证:$\angle AID=\angle ACT \Longleftrightarrow ST=SD$.(LHB)
3. $\odot ABE$与$\odot ACD$均与$BC$相切, $DE \parallel BC$ 作$\triangle ADE$中$D,E$所对旁心$I_D,I_E$. 证明:$I_DI_E$为$\odot ADE$和$\odot ABC$的跟轴.(LZM)
4. $\triangle ABC$中$M$为$BC$中点, $O$为外心, $G$为重心, $AM$交$\odot O$于另一点$D$, $CD,CG$交$B$处切线于$C_1,C_2$, 做$C_3$满足$C_3B\perp BC,\,C_3C_2=C_3G$同理定义$B_1,B_2,B_3$. 求证:$C_1M \perp CC_3 \Longleftrightarrow B_1M \perp BB_3$.(LSX)
5. $\triangle ABC$外心为$O$, 垂心为$H$, 三边上的垂足分别为$D,F,E$. 设$AO$与$\odot(BOC)$交于另一点$X$, $\odot(ADX)$与$\odot(FHE)$交于另一点$T$. 设$A$关于$EF,DX$的对称点分别为$P,Q$. 证明:$X,P,T,Q$共圆.(HY)
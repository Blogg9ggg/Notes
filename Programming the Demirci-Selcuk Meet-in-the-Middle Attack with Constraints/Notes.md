### Programming the Demirci-Selcuk Meet-in-the-Middle Attack with Constraints
1. Introduction\
   略.
2. Notations(符号声明)
   1. n 比特的 state($n=cn_c$) 表示成一个序列($state[0],state[1],...,state[n_c-1]$), 序列中有 $n_c$ 个 $c$ 比特的 word.
   2. $\mathcal{A}=[j_0,j_1,...,j_{s-1}]$ 是一个有序的整数集合 (满足 $0 \leqslant j_0 < ... < j_{s-1} < n_c$). 则 $state[\mathcal{A}]$ 代表 $state[j_0]||...||state[j_{s-1}]$, 其中 $state[j]$ 是第 $j$ 个 $c$ 比特状态字 (word of state), "||" 代表比特串连结操作.
   3. <font color=#00FF00>定义1</font>: 集合 $\{P^0,...,P^{N-1}\} \subseteq \mathbb{F}_{2}^{cn_c} = \mathbb{F}_{2}^{n}$ 代表状态 $state[\mathcal{A}]$ 的所有 $N=2^{sc}$ 种不同的取值方式 (每个 $P^i$ 都是一种 $n=cs$ 比特的状态值). 我们称集合 $\{P^0,...,P^{N-1}\}$ 为 $state[\mathcal{A}]$(其中 $\mathcal{A}=[k_0,k_1,...,k_{s-1}]$) 的一个 $\delta(\mathcal{A})-set$, 若它满足如下条件:
      1. $P^{0}[\mathcal{A}] \oplus P^{j}[\mathcal{A}] = j, 1 \leqslant j < N$;
      2. $\forall i,j \in \{0,...,N-1\}, k \notin \mathcal{A}$, 有 $P^i[k] = P^j[k]$;
   
      <font color=#FF0000>实际意义: $\{P^0,...,P^{N-1}\}$ traverse the $s c-bit$ words specified by $\mathcal{A}$ while share the same value in other word positions.</font>
   4. 将一个 $r$ 轮的分组密码 $E$ 分成 3 部分, 即 $r=r_0+r_1+r_2$, 如图 1 所示:\
   ![Fig.1](./assets/Fig1.PNG)
   $$图1$$
   可以看到, 图中将分组密码每一轮的操作分为线性和非线性两种, 图中的 $state_{2k}$ 是第 $k$ 轮的输入状态, $state_{2k+1}$ 是第 $k$ 轮非线性操作的输出状态, $state_{2(k+1)}$ 是第 $k$ 轮的输出 (或者说是第 $k+1$ 轮的输入), $k \in \{0,...,r_0+r_1+r_2-1\}$.\
   5. 123
   
3. 123
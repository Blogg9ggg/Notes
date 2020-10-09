1. **Introduction**  
   这篇论文重点关注在 $\mathbb{F}_{2^8}$ 上的乘法逆操作 (和它的等价仿射). AES 的 S 盒 (等价于一个 $\mathbb{F}_{2^8}$ 求逆器) 是目前已知的 <font color=#0000FF>关于局部安全性质["in terms of local security properties(*i.e.*, non-linearity, differential uniformity, algebraic degree, etc.)"]</font> 最强的 $8 \times 8$ S 盒. 目前, AES 最紧凑的 S 盒专用集成电路实现是基于塔域架构 (tower field architecture) 的. 在塔域结构中, $\mathbb{F}_{2^{2k}}$ 上的操作被递归地表示成 $\mathbb{F}_{2^k}$ 上的操作.  
   而且, AES 的许多成本效益好的 S 盒 (抗[旁路攻击](./Side-channel_Attack.md)) 实现都是建立在塔域架构的顶层.  
   在塔域实现中, 一系列域扩展从 $\mathbb{F}_2$ 开始, 在 $\mathbb{F}_{2^8}$ 结束. 在各级域扩展中, 都要有 $\mathbb{F}_{2^k}$ 上的一个不可约多项式和 <font color=#FF0000>a corresponding basis of $\mathbb{F}_{(2^k)^{2^l}}$ over $\mathbb{F}_{2^k}$ (一组XXX的基?). The irreducible polynomials and bases induce a basis of $\mathbb{F}_{2^8}$ over $\mathbb{F}_2$.</font> 塔域架构是在新基 (这个新基是有合适的基变换获得的) 的基础上获得原始的域表示来实现 S 盒. 因此, 域扩展中的选择, 即相应的不可约多项式和基的选择, 决定了实现中的总体开销.  
   **Contributions.** 测试了由不可约多项式引入的正规基的所有塔域表示 (总共 720 种), 发现了能实现更紧凑的 S 盒的参数设置.
2. 123
   
3. 123
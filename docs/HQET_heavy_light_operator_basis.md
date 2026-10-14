# NNLP 重轻流算符基及 B→γℓν 专门化边界

- **日期：** 2026-10-14
- **目标：** 从已发表文献确定 HQET 重轻弱流的二阶局域算符和时间有序乘积的系统母基，连接 NNLP 项目的树级重夸克展开，区分尚未闭合的过程专门化。
- **状态：** 文献中的 26+26 母基 [文献已核对]；下文从重夸克小分量消元得到的 7 类树级贡献 [形式代数已核对]；质量为零的 u 夸克进一步求极小基及完整 B→γℓν SCET/电磁基 [待完成]。

## A. 范围与约定

针对 `B^-=(b\bar u)` 和 `\bar u\gamma^\mu(1-\gamma_5)b=2\bar u_L\gamma^\mu b`，取 `\bar u_L\equiv\bar u P_R`，`P_\pm=(1\pm\!\not v)/2`，`P_+h_v=h_v`，`D_\alpha=\partial_\alpha-ig_s A_\alpha`，`\sigma^{\alpha\beta}=i[\gamma^\alpha,\gamma^\beta]/2`。引入**有序**左右作用导数

$$L_\alpha=i\overleftarrow D_\alpha,\qquad R_\alpha=i\overrightarrow D_\alpha,\qquad L_v=v\cdot L,\quad R_v=v\cdot R,\quad \not L=\gamma^\alpha L_\alpha,\quad \not R=\gamma^\alpha R_\alpha.$$

所有下列 `\mathcal Q_i^\mu` 都代表 `\bar u_L (\cdots)h_v`；不同箭头和非对易导数的次序不允许私自交换。对重轻局域流不能随意把总导数丢掉：电流传递四动量。

**来源：** C. Balzereit, T. Ohl, *Heavy Quark Effective Field Theory at O(1/m_Q^2). II. QCD Corrections to the Currents*, [arXiv:hep-ph/9612339](https://arxiv.org/pdf/hep-ph/9612339), §2.1, Eqs. (3)–(9). 原文采用 `\bar c_L` 和带质量的 c 夸克，本文将该约定中的轻夸克符号暂换成 u；这一步只是写下**完备母基**，不能自动证明在 `m_u=0` 下仍是严格独立的极小基。

## B. 维数 3 与 4 的底层局域流

$$\mathcal J^{(0)\mu}_1=\bar u_L v^\mu h_v,\qquad \mathcal J^{(0)\mu}_2=\bar u_L\gamma^\mu h_v.$$

原文的八个维数 4 流（按 i=1,...,8）：

| i | `\mathcal J_i^{(1)\mu}/(\bar u_L\;\cdot\;h_v)` |
|---|---|
| 1 | $-L^\mu$ |
| 2 | $R^\mu$ |
| 3 | $-L_vv^\mu$ |
| 4 | $-\not L\,v^\mu$ |
| 5 | $\not R\,v^\mu$ |
| 6 | $-L_v\gamma^\mu$ |
| 7 | $-L_\alpha i\sigma^{\alpha\mu}$ |
| 8 | $R_\alpha i\sigma^{\alpha\mu}$ |

`m_u=0` 的轻夸克 EOM 使其中有冗余，例如 `\mathcal J_4^{(1)}=0`，并在给定矩阵/箭头次序下给出 `\mathcal J_7^{(1)}=\mathcal J_1^{(1)}`。因此 **8 是文献的中间维数-4 母基数目，而不是无质量 u 的极小数目**。

## C. 二阶 26 个局域算符（维数 5 母基）

定义 `\mathcal Q_i^\mu=\bar u_L\,X_i^\mu h_v`。按照原文 Eq. (5) 的顺序：

| i | `X_i^\mu` | i | `X_i^\mu` |
|---:|---|---:|---|
| 1 | $L_v^2 v^\mu$ | 2 | $(L\cdot L)v^\mu$ |
| 3 | $-(L\cdot R)v^\mu$ | 4 | $(R\cdot R)v^\mu$ |
| 5 | $-L_v\not R\,v^\mu$ | 6 | $R_v\not R\,v^\mu$ |
| 7 | $L_v\not L\,v^\mu$ | 8 | $-L_\alpha R_\beta\sigma^{\alpha\beta}v^\mu$ |
| 9 | $R_\alpha R_\beta\sigma^{\alpha\beta}v^\mu$ | 10 | $-L_vR^\mu$ |
| 11 | $R_v R^\mu$ | 12 | $L^\mu L_v$ |
| 13 | $L_v^2\gamma^\mu$ | 14 | $(L\cdot L)\gamma^\mu$ |
| 15 | $-(L\cdot R)\gamma^\mu$ | 16 | $(R\cdot R)\gamma^\mu$ |
| 17 | $-\not L R^\mu$ | 18 | $\not R R^\mu$ |
| 19 | $-L^\mu\not R$ | 20 | $R^\mu\not R$ |
| 21 | $L^\mu\not L$ | 22 | $-L_v R_\alpha\sigma^{\alpha\mu}$ |
| 23 | $R_vR_\alpha\sigma^{\alpha\mu}$ | 24 | $L_vL_\alpha\sigma^{\alpha\mu}$ |
| 25 | $-i\epsilon^{\alpha\beta\gamma\mu}L_\alpha R_\beta v_\gamma$ | 26 | $i\epsilon^{\alpha\beta\gamma\mu}R_\alpha R_\beta v_\gamma$ |

该 26 的来源是原文将 56 个候选二阶局域流利用 heavy-quark EOM 和其 arrow identities 化简而得。记号 `(L·R)` 是明确的 Lorentz 指标收缩，但保留算符箭头作用的顺序。符号/epsilon 约定若用于环图应按原文及统一 gamma5 方案重新核对。

**无质量极限警告：** `\bar u_L i\overleftarrow{\not D}=0` 可以使本母基中的一些局域组合消失或等价，例 `\mathcal Q_{17}=0`（使用最低阶轻夸克 EOM、在通常的分离箭头导数约定下）。再考虑 QCD 轻夸克 EOM、四维 Schouten/手征 gamma 恒等式、total derivatives/contact terms 和特定外态后，`26` 未必是 `b→u` 过程独立数目。我们**尚未独立计算出相应秩**，故不以 `26` 冒充最终无质量极小基。

## D. HQET 拉氏量算符

取文献未重定义约定（`M=2m_b`）：

$$\mathcal K_1=\bar h_v (iD)^2h_v,\qquad \mathcal K_2=\frac{g_s}{2}\bar h_v\sigma_{\alpha\beta}G^{\alpha\beta}h_v,$$

$$\mathcal D_1=\bar h_v iD_\alpha(iv\cdot D)iD^\alpha h_v,\quad \mathcal D_2=\bar h_v i\sigma_{\alpha\beta}iD^\alpha(iv\cdot D)iD^\beta h_v.$$

依据严格保留导数次序的小分量消元：

$$\mathcal L_{\rm HQET}=\bar h_vVh_v+\frac{1}{M}(\mathcal K_1+\mathcal K_2)-\frac1{M^2}(\mathcal D_1-\mathcal D_2)+O(M^{-3}),\qquad V=iv\cdot D,$$

其中 `\mathcal D_{1,2}` 与 `\bar h KVK h` 的关系可能需要去掉最低阶 EOM 类项，必须在**同一场重定义约定**下一起变换流与接触项。等价的 Darwin 和 spin–orbit 基是另一个选项；不能当作第三、第四个独立贡献额外再加。把 Darwin 用胶子 EOM 改写时会出现重轻四费米接触结构，需要一并追踪。

## E. 26 个非局域二阶时间有序乘积

按原文 Eqs. (7)–(9) 的索引集合，明确地写作：

### E1. 双一阶拉氏量插入：6 个

$$\mathcal T_{i;jk}^{(011)\mu}=\frac{i^2}{1+\delta_{jk}}\int d^4x\,d^4y\;T\{\mathcal J_i^{(0)\mu}(0),\mathcal K_j(x),\mathcal K_k(y)\},\qquad i=1,2,\quad (j,k)=(1,1),(1,2),(2,2).$$

这里分母 `1+δ_jk` 表示同类插入除以 2，混合插入不除以 2；此处 `i^2` 来自 Dyson 积分，不是算符索引。

### E2. 单二阶拉氏量插入：4 个

$$\mathcal T_{i;j}^{(02)\mu}=i\int d^4x\;T\{\mathcal J_i^{(0)\mu}(0),\mathcal D_j(x)\},\qquad i=1,2,\ j=1,2.$$

### E3. 一阶电流 × 一阶拉氏量插入：16 个

$$\mathcal T_{a;j}^{(11)\mu}=i\int d^4x\;T\{\mathcal J_a^{(1)\mu}(0),\mathcal K_j(x)\},\qquad a=1,\ldots,8,\quad j=1,2.$$

于是母基恰好 `6+4+16=26`。这里以统一的 Dyson 规范化表示；原论文 Eq. (7)–(9) 在 `T` 的总体相位、同类插入对称因子上选择了不同的符号记法，做 Wilson 系数对照时须换算。**非局域的算符插入不等同于另一个局域维数-5 双线性算符**。

## F. 与此前树级 H1–H7 的严格对应

小分量树级形式解：

$$b=e^{-im_bv\cdot x}\left[1+\frac K M-\frac {VK}{M^2}+O(M^{-3})\right]h_v,\qquad K=i\not D_\perp,$$

给出弱流与作用量：

$$J^\mu=\bar u\Gamma^\mu h_v+\frac1M\bar u\Gamma^\mu Kh_v-\frac1{M^2}\bar u\Gamma^\mu VKh_v+\cdots,\qquad \Gamma^\mu=\gamma^\mu(1-\gamma_5).$$

将 Dyson 展开到 `M^{-2}`，仅在此树级原始场方案中得到七类：

| H | 结构 | 树级展开中的系数（采用有序 `T`） |
|---|---|---|
| H1 | $\bar u\Gamma^\mu VK h_v$ | $-1/M^2$ |
| H2 | $i\int T\{\bar u\Gamma^\mu K h_v,\mathcal K_1\}$ | $+1/M^2$ |
| H3 | $i\int T\{\bar u\Gamma^\mu K h_v,\mathcal K_2\}$ | $+1/M^2$ |
| H4 | $i\int T\{\bar u\Gamma^\mu h_v,\mathcal D_1-\mathcal D_2\}$ | $-1/M^2$ |
| H5 | $(i^2/2)\iint T\{J_0,\mathcal K_1,\mathcal K_1\}$ | $+1/M^2$ |
| H6 | $i^2\iint T\{J_0,\mathcal K_1,\mathcal K_2\}$ | $+1/M^2$ |
| H7 | $(i^2/2)\iint T\{J_0,\mathcal K_2,\mathcal K_2\}$ | $+1/M^2$ |

注：H6 已是**合并两个互换位置后的混合乘积**，故若采用统一的 `(i^2/2)` 定义，则它的系数改为 `+2/M^2`。这七类是 **HQET 树级重夸克匹配在 52 母基中的特定线性组合**，而不是 52 个算符各自独立的已计算 Wilson 系数。

在局域流中，取最低阶重夸克 EOM `Vh_v=0` 并保持有序算符，形式地有

$$J_0^\mu=2\mathcal J_2^{(0)\mu},\quad J_1^\mu=2(\mathcal J_2^{(1)\mu}+\mathcal J_8^{(1)\mu}),\quad J_2^\mu=2(\mathcal Q_{11}^\mu+i\mathcal Q_{23}^\mu).$$

最后一个等式中的 `i` 来自 `\gamma^\mu\gamma^\alpha=g^{\mu\alpha}+i\sigma^{\alpha\mu}`。这些是 **EOM 商空间内的形式代数表示**；离壳背景场、双胶子、接触项、复相位和 renormalized Wilson coefficient 的匹配尚待核对，不标作已完成的通用系数表。

## G. 为什么还不能称为完整 B→γℓν NNLP 过程基

全强子张量定义为

$$T^{\mu\nu}(p)=i\int d^4x\,e^{ip\cdot x}\langle0|T\{j_{\rm em}^\nu(x),J^\mu(0)\}|B^-\rangle.$$

其 `O(\Lambda_{\rm QCD}^2/m_b^2)` 过程展开还应包括：

1. 轻夸克发硬光子时的 hard-collinear 传播子到二阶，含背景软胶子的协变展开；
2. 由 `D_\mu`、胶子场强和非局域 Wilson 线产生的二、三、四粒子及更高 twist B 介子分布振幅，需逐项判定计数；
3. 重夸克发射 **硬** 光子的 QCD→(H)SCET 局域/非局域硬匹配，不能用软 HQET 重夸克最小耦合直接代替；
4. 真实光子强子结构（resolved photon）与可能的端点/软重叠贡献，在指定因子化方案内判断是否同阶；
5. QED Ward 恒等式对应的接触项，以及为整体物理衰变振幅所需的轻子辐射；
6. 软、hard-collinear、hard 尺度的模式分离、减重计数以及 `F_V,F_A` 的规范投影。

参阅 [Beneke et al., arXiv:1804.04962](https://arxiv.org/abs/1804.04962) 与 [Cui et al., EPJC 85 (2025) 1052](https://link.springer.com/article/10.1140/epjc/s10052-025-14772-z)。这两篇主要研究 LP/NLP 项，不能直接用作 NNLP 过程完备性的证明。

## H. 研究状态与下一步任务

**[文献已验证]** 26+26 的 HQET 重轻流系统母基及其分组，文献 §2.1。**[形式代数已核对]** HQET 非重定义场方案的 J0/J1/J2、L1/L2 和 H1–H7 的 Dyson 组合；结合母基的局部表达仍需背景场检验。**[未解决]** 无质量 u 的二阶局域/非局域独立秩；SCET×HQET×QED 的 NNLP 全模式算符基；完整树级 Wilson 系数、Ward 核查及非微扰函数的独立性；`F_V^{NNLP}`、`F_A^{NNLP}`、分支比。

**具体下一步：** (1) 设定 `m_u=0`，把 26 维数-5 流和 26 个 T 产品连同 EOM/箭头恒等式输入符号线性代数，求极小维数及变换矩阵；(2) 用零/一/二背景胶子外态复核软 HQET Wilson 系数；(3) 建立硬光子 QCD→SCET 匹配基并逐项核对 `p_\nu T^{\mu\nu}` Ward 恒等式；(4) 按独立多粒子 LCDAs 分类所有 NNLP 核和端点区域；(5) 完成 `F_V,F_A` 后再计算分支比。

**归档状态：** 本文件随经审核的研究同步进入仓库；文献母基已归档不代表物理 NNLP 完备性、极小化或匹配系数已完成。

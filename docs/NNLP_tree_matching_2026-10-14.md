# $B\to\gamma\ell\nu$ 研究：二阶重轻弱流的 QCD/HQET 树级匹配

- 日期：2026-10-14
- 目标：在固定场定义、导数顺序、归一化和算符基的情况下，计算重轻弱流的 $1/m_b^2$ 树级系数，逐级核对自由外态、单背景胶子与二胶子接触结构，并给出作用量插入。
- 本笔记范围：**HQET 重夸克展开的 $1/m_b^2$ 子集**；**不是**完整 $B\to\gamma\ell\nu$ 物理 NNLP 的所有 SCET/QED 匹配系数。
- 研究状态：小分量消元及有序展开 **[树级形式代数已核对]**；单背景胶子顶点与纵向恒等式 **[代数检查通过]**；二胶子**局域接触项** **[已写出形式表达式，完整 QCD 振幅未验]**；无质量 $u$ 的 $26+26$ 母基极小化与完整离壳背景场树图 **[未完成]**。不把形式检查冒充全部匹配的独立验证。

## 1. 固定约定，区分两套场基底

$$
 g^{\mu\nu}=\operatorname{diag}(1,-1,-1,-1),\quad D_\mu=\partial_\mu-ig_s A_\mu^aT^a,
\quad v^2=1,\quad P_\pm=\frac{1\pm\slashed v}{2}.
$$

$$
M\equiv2m_b,\qquad V\equiv iv\cdot D,\qquad K\equiv i\slashed D_\perp,
\qquad D_\perp^\mu=D^\mu-v^\mu(v\cdot D),\quad
\Gamma^\mu\equiv\gamma^\mu(1-\gamma_5).
$$

**原始场**记 $h_v$，消去小分量 $H_v$ 后未另作高阶场重定义。**规范化场**记 $h_v^c$，采用第 4 节的显式局域重定义。不同场基底的系数不能不加转换地比较；$M^{-n}$ 单独提取时，表格中列的是无量纲系数。

## 2. 从 QCD 二次重夸克拉氏量消去小分量

以

$$\mathcal L_b=\bar b(i\slashed D-m_b)b,\quad
 b(x)=e^{-im_b v\cdot x}[h_v(x)+H_v(x)],\quad P_+h_v=h_v,\;P_-H_v=H_v$$

为起点。投影后的双线性拉氏量为

$$
\mathcal L_b=\bar h_v Vh_v-\bar H_v(M+V)H_v+\bar h_v K H_v+\bar H_v K h_v.
$$

对 $\bar H_v$ 变分，得到 $(M+V)H_v=Kh_v$，因此

$$
\boxed{H_v=(M+V)^{-1}K h_v.}
$$

令逆算符在其左侧作用，**不可**预先交换 $V$ 与 $K$：

$$
(M+V)^{-1}=M^{-1}-M^{-2}V+O(M^{-3}),
\quad H_v=\bigl(M^{-1}K-M^{-2}VK\bigr)h_v+O(M^{-3}).
$$

得到 QCD 场的有序重构

$$
\boxed{b=e^{-im_bv\cdot x}[1+K/M-VK/M^2]h_v+O(M^{-3}).}
$$

消去 $H_v$ 后的有效作用量（忽略此处不参与树级双线性匹配的量子行列式项）为

$$
\mathcal L_{\mathrm{raw}}=\bar h_v\left[V+K(M+V)^{-1}K\right]h_v
=\bar h_v\left[V+K^2/M-KVK/M^2\right]h_v+O(M^{-3}).
$$

## 3. 原始场基底：局域弱流及其树级系数

代入 $J_{\rm QCD}^\mu=\bar u\Gamma^\mu b$，得

$$
\boxed{
J_{\rm QCD}^\mu\doteq e^{-im_bv\cdot x}
\left[J_0^\mu+\frac{J_1^\mu}{M}-\frac{J_b^\mu}{M^2}\right]+O(M^{-3})
}
$$

其中（这里 $\doteq$ 指固定原始场下的树级有效算符表示）

$$
J_0^\mu=\bar u\Gamma^\mu h_v,\quad
J_1^\mu=\bar u\Gamma^\mu K h_v,\quad
J_b^\mu=\bar u\Gamma^\mu VK h_v.
$$

因此，在 $1,M^{-1},M^{-2}$ 分别外提的约定中：

| 算符 | 阶数 | 树级系数 | 范围 |
|---|---|---:|---|
| $J_0^\mu$ | $M^0$ | $+1$ | 原始场 |
| $J_1^\mu$ | $M^{-1}$ | $+1$ | 原始场 |
| $J_b^\mu$ | $M^{-2}$ | $-1$ | 原始场，保留 $VK$ 次序 |

**判定：**这是由树级精确小分量消元获得的有序系数，并非所有独立的二阶流的通用 Wilson 系数向量。

## 4. 规范化场重定义及系数 $1/2,-1$

选择 $h_v$ 和 $h_v^c$ 的局域重定义

$$
\boxed{h_v=\left(1+\frac{K^2}{2M^2}\right)h_v^c+O(M^{-3}).}
$$

对作用量中的 $\bar h_v$ 同时实施 Dirac 共轭及相应的积分分部（使微分算符最终右作用），得到

$$
\begin{aligned}
\mathcal L_c
&=\bar h_v^c\left[V+\frac{K^2}{M}
+\frac{1}{M^2}\Bigl(\frac12 K^2V+\frac12VK^2-KVK\Bigr)\right]h_v^c+O(M^{-3})\\
&=\boxed{\bar h_v^c\left[V+\frac{K^2}{M}-\frac{1}{2M^2}[K,[V,K]]\right]h_v^c+O(M^{-3})},
\end{aligned}
$$

因为 $[K,[V,K]]=2KVK-K^2V-VK^2$。弱流在同一场基底下变为

$$
\boxed{
J_{\rm QCD}^\mu\doteq e^{-im_bv\cdot x}\bar u\Gamma^\mu
\left[1+\frac{K}{M}+\frac{1}{M^2}\left(\frac12K^2-VK\right)\right]h_v^c+O(M^{-3}).
}
$$

定义 $J_a^\mu\equiv\bar u\Gamma^\mu K^2h_v^c$、$J_b^\mu\equiv\bar u\Gamma^\mu VKh_v^c$，则

$$\boxed{C_{J_a}^{(0)}=+\tfrac12,\qquad C_{J_b}^{(0)}=-1,}$$

树级记号上标 $(0)$ 为 $\alpha_s^0$，不是 LP；整体 $M^{-2}=1/(4m_b^2)$ 已提到系数之外。$+1/2$ 是**场基底相关**的系数，不能再独立地加上原始场基底的 H1–H7，避免重复计数。

## 5. 自由夸克外态核验及其可区分性限制

取 $p_b=m_bv+k$，$\omega=v\cdot k$、$k_\perp=k-\omega v$，分解 $u_b=u_++u_-$。从 $P_-$ 投影 QCD Dirac 方程得到

$$
-(M+\omega)u_-+\slashed k_\perp u_+=0,\quad
\boxed{u_-=(M+\omega)^{-1}\slashed k_\perp u_+.}
$$

从而 QCD 自由弱流为

$$
\begin{aligned}
\mathcal M_{\rm QCD}^\mu&=\bar u(p_u)\Gamma^\mu
\left(1+\frac{\slashed k_\perp}{M+\omega}\right)u_+\\
&=\bar u(p_u)\Gamma^\mu
\left(1+\frac{\slashed k_\perp}{M}-\frac{\omega\slashed k_\perp}{M^2}\right)u_++O(M^{-3}).
\end{aligned}
$$

将 $K\mapsto\slashed k_\perp$、$VK\mapsto\omega\slashed k_\perp$，与**原始场**的局域流结构吻合。因此得到独立于重夸克场形式消元之外的自由旋量一致性检查。

**限制：** 在壳条件 $M\omega+\omega^2+k_\perp^2=0$ 使张量结构不完全独立；该检验不能区分全部 EOM 冗余算符与场强算符。对 $h_v^c$ 的外态比较还要同步变换外态归一化，不能把原始 $u_+$ 直接当规范化场的全部外态检验。

## 6. 单背景胶子：局域流重构顶点及纵向恒等式

取一个流入重夸克线的背景胶子动量 $q$，令 $k'=k+q$，$d=M+v\cdot k$、$d'=M+v\cdot k'$。对精确重构 $\mathcal R=1+(M+V)^{-1}K$ 求一阶场变分，利用

$$
\delta K=g_sT^a\gamma_\perp^\rho A_\rho^a,\qquad
\delta V=g_sT^a v^\rho A_\rho^a,\qquad
\delta X^{-1}=-X^{-1}(\delta X)X^{-1},
$$

得到（剥去 $\bar u\Gamma^\mu$、外部场及总体 Feynman $i$ 因子）

$$
\boxed{\mathcal R_g^{a\rho}
=g_sT^a\left[\frac{\gamma_\perp^\rho}{d'}-\frac{v^\rho\slashed k_\perp}{d'd}\right].}
$$

按 $M^{-1}$ 展开：

$$
\mathcal R_g^{a\rho}=g_sT^a\left[
\frac{\gamma_\perp^\rho}{M}
-\frac{(v\cdot k')\gamma_\perp^\rho+v^\rho\slashed k_\perp}{M^2}
\right]+O(M^{-3}).
$$

直接变分 $K/M-VK/M^2$ 得同式；进一步按 $q$ 收缩，

$$
\boxed{q_\rho\mathcal R_g^{a\rho}
=g_sT^a\left[\frac{\slashed k'_\perp}{d'}-\frac{\slashed k_\perp}{d}\right].}
$$

这是**场重构核**的树级纵向差分关系；不是完整含重夸克传播和拉氏量顶点的 QCD/HQET 振幅 Ward 验证，更不是 QED 实光子 Ward 恒等式。

规范化场基底产生额外 $K^2/2M^2$ 的变分，得到

$$
\boxed{\begin{aligned}
\mathcal R_{g,c}^{a\rho}=g_sT^a\Bigg[&\frac{\gamma_\perp^\rho}{M}
+\frac{1}{M^2}\Big\{\frac12(\slashed k'_\perp\gamma_\perp^\rho+\gamma_\perp^\rho\slashed k_\perp)\\
&-(v\cdot k')\gamma_\perp^\rho-v^\rho\slashed k_\perp\Big\}\Bigg]+O(M^{-3}).
\end{aligned}}
$$

其 $q$ 收缩与 $\mathcal R_c(k')-\mathcal R_c(k)$ 一致，其中

$$\mathcal R_c(k)=1+\frac{\slashed k_\perp}{M}
+\frac{\frac12k_\perp^2-(v\cdot k)\slashed k_\perp}{M^2}. $$

**状态：**上述为协变重构算符的**代数**及纵向检验，尚需显式组装独立的 QCD 一胶子 Green 函数与 HQET 作用量插入图，统一离壳外态、相位及 EOM 接触项。

## 7. 两个背景胶子的局域接触项

在规范化局域流中，二次背景场来自 $(K^2/2-VK)/M^2$：

$$
\left.K^2\right|_{A^2}=g_s^2\gamma_\perp^\rho A_\rho\gamma_\perp^\sigma A_\sigma,
\qquad \left.VK\right|_{A^2}=g_s^2(v\cdot A)\gamma_\perp^\sigma A_\sigma,
$$

$A_\rho=A_\rho^aT^a$，不可交换颜色矩阵，故

$$
\boxed{
\left.J_{2g}^\mu\right|_{\rm local,contact}=
\frac{g_s^2}{M^2}\bar u\Gamma^\mu
\left[\frac12\gamma_\perp^\rho A_\rho\gamma_\perp^\sigma A_\sigma
-(v\cdot A)\gamma_\perp^\sigma A_\sigma\right]h_v^c.
}
$$

提取外部两个胶子腿时必须包括 $1\leftrightarrow2$ 对称、颜色排序、所有一胶子迭代图与 HQET 拉氏量插入图。这是**局域接触项**，不是完成了独立 QCD/HQET 的双胶子振幅匹配。

## 8. Dyson 展开：规范化场基底的全部二阶重夸克插入类别

定义 $O_1=\bar h_v^cK^2h_v^c$、$O_2=\bar h_v^c[K,[V,K]]h_v^c$，并约定

$$
\mathcal T_1[A,B]=i\int d^4x\,T\{A(0),B(x)\},\quad
\mathcal T_2[A,B,B]=\frac{i^2}{2}\int d^4x\,d^4y\,T\{A(0),B(x),B(y)\}.
$$

将 $1/M^2$ 整体提取后：

$$
\boxed{\mathbb J_{\rm HQET,c}^{(2)\mu}
=\frac12J_a^\mu-J_b^\mu
+\mathcal T_1[J_1^\mu,O_1]
-\frac12\mathcal T_1[J_0^\mu,O_2]
+\mathcal T_2[J_0^\mu,O_1,O_1].}
$$

| 结构（去掉共同 $1/M^2$） | 树级组合系数 |
|---|---:|
| $J_a^\mu$ | $+\tfrac12$ |
| $J_b^\mu$ | $-1$ |
| $\mathcal T_1[J_1^\mu,O_1]$ | $+1$ |
| $\mathcal T_1[J_0^\mu,O_2]$ | $-\tfrac12$ |
| $\mathcal T_2[J_0^\mu,O_1,O_1]$ | $+1$ |

后三项是同一有效作用量的 **Dyson 组合因子**，不应描述成对每个独立非局域母基重新求出的硬 Wilson 系数。若取原始场，$O_1=O_{\rm kin}+O_{\rm mag}$、$O_T=\bar h_vKVKh_v$，上式回到

$$
\mathbb J_{\rm raw}^{(2)\mu}=-J_b^\mu
+\mathcal T_1[J_1^\mu,O_1]
-\mathcal T_1[J_0^\mu,O_T]
+\mathcal T_2[J_0^\mu,O_1,O_1],
$$

将 $O_1$ 展开即可重现现有 `docs/power_corrections.md` 的 H1–H7；这两套表达**二选一**，不能相加。

## 9. 与 26 局域 + 26 非局域母基的关系及 EOM 陷阱

用 $\bar u_L=\bar uP_R$ 与 $R_\mu=i\overrightarrow D_\mu$（母基记号），保持矩阵次序，

$$
J_1^\mu=2\left(\mathcal J_2^{(1)\mu}+\mathcal J_8^{(1)\mu}\right)
-2\bar u_L\gamma^\mu Vh_v,
$$

$$
J_b^\mu=2\left(\mathcal Q_{11}^\mu+i\mathcal Q_{23}^\mu\right)
-2\bar u_L\gamma^\mu V^2h_v.
$$

其中 $\gamma^\mu\gamma^\alpha=g^{\mu\alpha}+i\sigma^{\alpha\mu}$。

**警告：** 首式中的最低阶 EOM 项 $\bar u_L\gamma^\mu Vh_v$ 本身在 $J_1/M$ 里是 $O(M^{-1})$，但使用包含首个次阶修正的 HQET EOM $Vh_v=-K^2 h_v/M+O(M^{-2})$，会在 $M^{-2}$ 产生新的局域项。时间有序积中的 EOM 使用另可能引起接触项。因此不能在 NNLP 上将母基的低阶 EOM 等价关系无条件当作强等式。

**未完成：** $m_u=0$ 条件下的 EOM/分部积分/Dirac 约束矩阵和独立秩，全部 $52$ 母基的约化矩阵与规范化系数向量，以及 QCD/QED 硬光子过程的独立匹配。

## 10. 与物理 $B\to\gamma\ell\nu$ NNLP 的边界

该弱流匹配**不包括**：真实硬光子从轻夸克传播子产生的二阶 hard-collinear 展开和背景软胶子场；重夸克硬光子辐射的 QCD→(H)SCET 过程硬系数；非微扰 LCDAs 与端点/软重叠；电磁 Ward 接触项及轻子辐射；$F_V,F_A$ 的全体 NNLP 投影。这些是单独任务。

## 11. 待执行的可复现核验

1. 以 $m_u=0$ 的 $26+26$ 母基建立 EOM、箭头导数、Dirac/Schouten 恒等式约束矩阵，求独立秩并保存变换矩阵。
2. 分离 EOM 冗余项，检查 $J_1/M$ 经次阶 EOM 产生的二阶接触贡献。
3. 组装独立 QCD 与 HQET 的 0/1/2 背景胶子 Green 函数，连同拉氏量图、外态归一化和 Ward 恒等式检验，不仅验证局域重构顶点。
4. 在相同场基底下显式做 RPI 变换，核对局域系数与插入系数的相关性。
5. 再进入带真实光子外态的过程级 (H)SCET/QED 匹配和 $F_V,F_A$ 的 NNLP 投影。

**既有研究资料：** `docs/HQET_expansion.md`、`docs/QCD_HQET_matching.md`、`docs/HQET_heavy_light_operator_basis.md`、`docs/power_corrections.md`。本笔记是 2026-10-14 本轮对话中**新增的详细推导**，与原始历史记录并存。


---

## 12. 2026-10-14 — 无背景胶子 QCD/HQET 树级匹配核对 [新增]

对于明确限定为**树图阶**的 NNLP 物理目标，我们在原始场定义 $M=2m_b$ 下分别计算 QCD 截肢自由夸克振幅和 QCD 投影重夸克传播 Green 函数，并与 HQET $J_0+J_1/M-J_2/M^2$ 以及 $\mathcal L_0+O_K/M-O_T/M^2$ 的单/双时间有序插入逐项比较。完整推导与所有图的动量核载于 [无胶子逐项匹配新文档](zero_gluon_QCD_HQET_tree_matching_2026-10-14.md)。

在固定非零 $\omega=v\cdot k$ 的离壳比较中，QCD 与 HQET 的 LP、NLP、NNLP 核逐项相同；NNLP 四项依次为 $-K_0,-K_0z/\omega^2,+z/\omega,+z^2/\omega^3$，其中 $K_0=\slashed k_\perp,z=k_\perp^2$。

**重要限制：** 在壳重夸克满足 $\omega=-z/M+O(M^{-3})$，单个无胶子在壳振幅不能独立测定带 $VK$ 的二阶流系数；其 $-1$ 是所选**原始场**的树级消元系数。零胶子检验无法确定普适 26+26 母基 Wilson 系数，也没有计算任何真实硬光子图。

# QCD $\to$ HQET 电流匹配

**状态：[计算方法已讨论；独立匹配尚待核验]。**

## 1. 匹配要回答的问题

QCD 中的重轻电流在固定的重整化方案和算符基下写为

$$
J_{\rm QCD}=\sum_i C_i(m_b,\mu)\,O_i^{\rm HQET}(\mu),
$$

上式示意包含按 $1/m_b$ 分类的算符；真实的物理矩阵元还应加入有效理论作用量的时间有序插入。$C_i$ 描述短距离差异，$\langle O_i\rangle$ 是后续要处理的长距离信息，**两者不可混为一谈**。

## 2. 为什么树图可以匹配树图？

若目标是给定算符基下的 **树级匹配系数**，先把 QCD 与 HQET 的适当外态振幅都计算到相同的 $1/m_b^2$ 阶并逐个张量结构比较，即可在可区分的算符结构上匹配树级系数。并不要求 QCD 必须先计算一个圈图。

若要得到 $O(\alpha_s)$ 的匹配修正，则需要比较相应的 QCD/HQET 圈图，并指定重整化与红外处理。

## 3. 推荐的实际计算顺序

1. 固定 $m_b$ 定义、$v$、外部残余动量 $k$、$\Gamma$、导数记号和算符规范化。
2. 写全到 $1/m_b^2$ 的独立局域流算符及所有必要的作用量插入；记录可能的 EOM 等价关系。
3. 计算 QCD 侧外态矩阵元，按残余动量及外部极化张量展开。
4. 计算 HQET 侧相同外态的矩阵元，连同应有的时间有序插入一起保留。
5. 按独立 Lorentz/Dirac/颜色结构逐项比较，解出系数并做重定义一致性检验。
6. 对自由外部夸克态无法区分的含 $[D_\mu,D_\nu]$ 结构，增加一个背景胶子外态检验。

## 4. NNLP 的 EOM 陷阱

设最低阶 EOM 是 $iv\cdot D h_v=0$。一个表面上带 $1/m_b$ 的 EOM 正比项，若用**包含 $1/m_b$ 修正的运动方程**替换，可能在 $1/m_b^2$ 阶产生非零贡献。因此，不能在计算 NNLP 时照搬较低阶的算符删减，而不同时追踪系数、场重定义及接触项。

相反，一个已带 $1/m_b^2$ 的纯最低阶 EOM 项，其相关重定义效应在合适条件下可能从更高阶才开始；具体仍取决于是否存在接触项及算符混合。最终以一致的有效作用量和可观测量为准。

## 5. 尚未确认的事项

- 未定稿算符基，故不在这里列出通用数值系数。
- 过去对话曾探讨特定归一化下的候选系数；在未附上其完整算符定义和背景场检验前，一律保持 **[待核验]**。
- Neubert 1994 讨论的是重轻流在 $1/m_Q$ 阶的短距离展开，不能直接当成 $1/m_Q^2$ 全部结果的依据。


---

## 6. 2026-10-14：树级自由外态检验 [部分已核对]

采用 $M=2m_b$、$p_b=m_bv+k$、$k_\perp=k-v(v\cdot k)$。
QCD 重夸克传播子投影给出

$$
P_+S_{\rm QCD}(m_bv+k)P_+
=\frac{iP_+}{v\cdot k+k_\perp^2/(M+v\cdot k)+i0}.
$$

按 $M^{-1}$ 展开，其逆传播核为

$$
v\cdot k+\frac{k_\perp^2}{M}
-\frac{(v\cdot k)k_\perp^2}{M^2}+O(M^{-3}),
$$

与未重定义 HQET 的 $\bar h_v[V+M^{-1}K^2-M^{-2}KVK]h_v$ 的自由核一致。
自由在壳重夸克旋量满足

$$
u_-=\frac{\not k_\perp}{M+v\cdot k}u_+.
$$

这核对了树级场重构的 Dirac 结构，但在壳自由外态**不足以独立确定 EOM 冗余或含场强的系数**。

## 7. 单个背景胶子顶点 [候选解析式；完整匹配待复核]

令背景胶子流入重夸克线，$k'=k+q$，并定义
$d=M+v\cdot k$、$d'=M+v\cdot k'$。在 $D=\partial-ig_sA$ 约定下，对小分量精确树级表达式做一次背景场变分，得到不含总体 Feynman 相位的候选顶点

$$
\mathcal R_g^{a\rho}
=g_sT^a\left[
\frac{\gamma_\perp^\rho}{d'}
-\frac{v^\rho\not k_\perp}{d'd}\right],
$$

$$
\mathcal V_g^{a\rho}
=g_sT^a\left[
v^\rho+\frac{\not k'_\perp\gamma_\perp^\rho}{d'}
+\frac{\gamma_\perp^\rho\not k_\perp}{d}
-\frac{\not k'_\perp v^\rho\not k_\perp}{d'd}
\right].
$$

$\mathcal R_g$ 来自弱流重构；$\mathcal V_g$ 来自 HQET 作用量。按 $M^{-1}$ 和 $M^{-2}$ 展开分别生成 $J_1,J_2$ 接触顶点与 $\mathcal L_1,\mathcal L_2$ 顶点。**[待核验]** 须再次检查外态归一化、离壳 Ward 恒等式、相位、双胶子接触顶点及 EOM/场重定义的一致性，不能声称已完成通用 NNLP 重轻流匹配。

## 8. 硬光子从重夸克线发射 [QCD 核已写出；协变 NNLP 匹配待核验]

令 $p^2=0$、$E=v\cdot p\sim m_b$，QCD 树级核为

$$
\mathcal K_b^{\mu\nu}
=Q_b\Gamma^\mu\frac{\not p_b-\not p+m_b}{(p_b-p)^2-m_b^2+i0}\gamma^\nu.
$$

在 $k=0$、$p\cdot\epsilon=v\cdot\epsilon=0$ 以及 $P_+$ 外态下，
领先非零核为

$$
\mathcal K_b^{[0]\mu}
=\frac{Q_b}{ME}\Gamma^\mu\not p\not\epsilon^*P_+.
$$

此前讨论给出的相对一阶软动量候选核为

$$
\begin{aligned}
\mathcal K_b^{[1]\mu}=\frac{Q_b}{ME}\Gamma^\mu\Big[
&(v\cdot k)\not\epsilon^*-2(\epsilon^*\cdot k_\perp)
+\frac{\not p}{M}\not\epsilon^*\not k_\perp\\
&+\not p\not\epsilon^*\left(\frac{v\cdot k}{E}
-\frac{2p\cdot k}{ME}\right)
\Big]P_+.
\end{aligned}
$$

**[待核验]** 上式仅作为此前对话的自由外态推导记录；还未完成独立 Dirac 检验、软背景场的协变匹配、接触项和 RPI 检查。不能将它视为最终 NNLP Wilson 系数。硬光子携带 $O(m_b)$ 动量，不能以软 HQET 胶子顶点简单替代这一步。

# 从 HQET/QCD 树级匹配到 $B\to\gamma\ell\nu$ 的 NNLP 分支比：为什么中间还有计算

- 日期：2026-10-14
- 目标：完整保留本轮对话中“HQET 拉氏量与弱流已经展开，匹配系数求出后为何不能直接算分支比”的问题、数学推理、与后续任务。
- 状态：匹配/强子矩阵元区别与振幅平方的幂次代数 **[概念及代数已核对]**；LP 例式 **[文献常用的约定性形式，具体 $F_A$ 接触项及尺度需统一]**；完整的 NNLP 因子化与分支比 **[待计算]**。

## 1. 原始疑问与关键区分

研究者提出：既然 HQET 拉氏量和弱流都已经展开到 $1/m_b^2$，是否只需逐阶比较 QCD/HQET 树级矩阵元以得到匹配系数，然后做 RG 跑动，便得到 $B\to\gamma\ell\nu$ 的 NNLP 分支比？

**回答：** 比较外部夸克/胶子矩阵元得到的是短距离系数，但分支比需要含物理 $B$ 介子和真实光子的**强子矩阵元**，以及过程本身的 hard/hard-collinear/soft 幂次展开。局域弱流的 HQET 展开仅是 NNLP 振幅的一部分，RG 也不能替代非微扰输入。

用两个不同等式展示不能混同的外态：

$$
\underbrace{\langle u+({\rm gluons})|J_{\rm QCD}^\mu|b\rangle}_{\text{匹配用微扰外态}}
=\sum_i C_i^{\rm tree}\underbrace{\langle u+({\rm gluons})|O_i^\mu|h_v\rangle}_{\text{用于比较 Dirac/Lorentz/color 张量结构}}
$$

（应同时包含选择的有效作用量插入、外线规范化与 EOM 接触项）；而衰变振幅需要

$$
\underbrace{\langle \gamma|J_{\rm QCD}^\mu|B\rangle}_{\text{真实强子外态}}
=\sum_i C_i\underbrace{\langle\gamma|O_i^\mu|B\rangle}_{\text{未知非微扰/过程相关矩阵元}}
$$

（此处 $O_i$ 为含所需时间有序插入的广义结构，并非仅局域流）。前一个等式决定短距离 Wilson 系数；后一个等式才进入形状因子，但右侧矩阵元不是由 $C_i$ 决定的。

## 2. $1/m_b^2$ 的有效流与作用量四类组合

记 $M=2m_b$，按固定原始场定义

$$
J=J_0+\frac{J_1}{M}+\frac{J_2}{M^2}+\cdots,\quad
\mathcal L=\mathcal L_0+\frac{\mathcal L_1}{M}+\frac{\mathcal L_2}{M^2}+\cdots
$$

（这里 $J_2$ **已经包括自身符号**，与 `HQET_expansion.md` 将 $-VK$ 记作 $-J_b$ 的写法只差标签）。固定最低阶有效理论矩阵元，到二阶包含

$$
\begin{aligned}
\mathcal A^{(2)}\sim{}&\langle J_2\rangle_0
+i\!\int d^4x\,\langle T\{J_1(0),\mathcal L_1(x)\}\rangle_0\\
&+i\!\int d^4x\,\langle T\{J_0(0),\mathcal L_2(x)\}\rangle_0\\
&+\frac{i^2}{2}\!\int d^4x\,d^4y\,\langle T\{J_0(0),\mathcal L_1(x),\mathcal L_1(y)\}\rangle_0.
\end{aligned}
$$

该式省略共同 $M^{-2}$，还未包括外态、归一化及光子过程其他幂次项。故不能只求一个 $J_2$ 系数便当作全部 NNLP。

## 3. 即便 LP 树图已知，仍需要 $B$ 介子 LCDA

在 $E_\gamma\sim m_b$ 的高能光子区域，一种常见 LP 因子化表达式写为

$$
F_V^{\rm LP}(E_\gamma)=F_A^{\rm LP}(E_\gamma)
=\frac{Q_u m_B}{2E_\gamma}\,\widetilde f_B(\mu)
\int_0^\infty \frac{d\omega}{\omega}\,T(E_\gamma,\omega,\mu)\phi_+(\omega,\mu)
$$

（此式需与所选的 $F_A$ 轻子辐射/接触项定义一致；$T$ 的规范化也依赖因子化方案）。最低树级硬核取 $T^{(0)}=1$ 时有

$$
\boxed{F_{V,A}^{\rm LP,tree}\simeq\frac{Q_u m_B\widetilde f_B}{2E_\gamma\lambda_B},\qquad
\lambda_B^{-1}=\int_0^\infty\frac{d\omega}{\omega}\phi_+(\omega).}
$$

已完成树图仍不能预测 $\lambda_B$，因为它是 $B$ 介子分布振幅的非微扰逆矩。NNLP 更可能涉及新的二、三及多粒子 LCDAs/局域矩阵元，不应假设都能化为 $\lambda_B$。

## 4. 真实硬光子引入额外的传播子幂次展开

轻 $u$ 夸克发射光子时，内部传播子取软夸克动量 $k\sim\Lambda_{\rm QCD}$、真实光子动量 $q$（$q^2=0$，$v\cdot q=E_\gamma\sim m_b$）为

$$
S_u(k-q)=\frac{i(\slashed k-\slashed q)}{(k-q)^2+i0},\quad
(k-q)^2=-2q\cdot k+k^2.
$$

若 $|k^2/(2q\cdot k)|\ll1$，则

$$
\frac1{(k-q)^2}=-\frac1{2q\cdot k}
\left[1+\frac{k^2}{2q\cdot k}+\left(\frac{k^2}{2q\cdot k}\right)^2+\cdots\right].
$$

由于 $k^2/(2q\cdot k)\sim\Lambda_{\rm QCD}/m_b$，第二、第三项相对领先传播子分别是 NLP、NNLP。传播子分子 $\slashed k-\slashed q$ 也必须按一致的功率计数展开。**即使暂时不改变 HQET 重夸克拉氏量，这些 NLP/NNLP 传播子修正也存在。**

记自由传播子三阶系数为 $S_0,S_1,S_2$，各阶重夸克软矩阵元为 $\Phi_0,\Phi_1,\Phi_2$，则二阶乘积形式上包含

$$
\boxed{S_0\frac{\Phi_2}{M^2}+S_1\frac{\Phi_1}{M}+S_2\Phi_0.}
$$

这是**自由传播子部分的代数计数**，不等于完整规范不变的 NNLP 因子化核。还需软胶子传播子、Wilson 线和多粒子 LCDAs、重夸克硬光子辐射、resolved-photon/端点与 QED Ward 接触项等，逐项判断其在所选物理幂次计数中是否同阶。

## 5. 物理电磁时间有序乘积与形状因子

强子张量可定义为

$$
T^{\mu\nu}(q)=i\int d^4x\,e^{iq\cdot x}
\langle0|T\{j_{\rm em}^\nu(x),J_{\rm weak}^\mu(0)\}|B^-\rangle,
$$

需要同时考虑轻夸克、重夸克的光子发射以及 QED Ward 联系的接触项；完整衰变的轻子辐射应按同一 $F_A$ 定义及实验切割计入。对轻夸克流作 Wick 收缩时出现**背景场传播子** $S_u(x,0;A)$，剩余 $B$ 介子软矩阵元仍需独立非微扰输入。这解释了为何比较微扰夸克外态不足以得到形状因子的数值。

## 6. $\alpha_s$ 微扰展开、RG 和 $\Lambda/m_b$ 幂次展开各自解决什么

$$
\frac{\Lambda_{\rm QCD}}{m_b}\quad\text{(幂次)}\qquad\ne\qquad
\alpha_s(\mu)\quad\text{(微扰)}.
$$

本轮树级 NNLP 针对 $\alpha_s^0(\Lambda_{\rm QCD}/m_b)^2$ 中由指定 HQET 子集贡献的系数。RG 演化可能重求和 $\ln(m_b/\mu)$，需要相应反常维数/算符混合，不能从单一树级匹配系数自动算出；即使 RG 已知，仍不能决定 $\phi_+$、$\lambda_B$ 或 NNLP 软矩阵元的非微扰初始条件。

## 7. 由 $F_V,F_A$ 走向分支比：不能只平方 NNLP 形状因子

按相对 LP 的阶次展开

$$F_i=F_i^{(0)}+F_i^{(1)}+F_i^{(2)}+\cdots,\qquad i=V,A.$$

则

$$
\begin{aligned}
|F_i|^2={}&|F_i^{(0)}|^2
+2\operatorname{Re}[F_i^{(0)*}F_i^{(1)}]\\
&+\underbrace{2\operatorname{Re}[F_i^{(0)*}F_i^{(2)}]+|F_i^{(1)}|^2}_{\text{相对 NNLP}}
+O(\lambda^3).
\end{aligned}
$$

在质量可忽略的轻子、常见 $F_{V/A}$ 归一化且适当处理轻子辐射的情况下，结构依赖贡献可写作

$$
\frac{d\Gamma}{dE_\gamma}=
\frac{\alpha_{\rm em}G_F^2|V_{ub}|^2}{6\pi^2}
 m_BE_\gamma^3\left(1-\frac{2E_\gamma}{m_B}\right)
\bigl(|F_V|^2+|F_A|^2\bigr).
$$

此式的**精确适用范围依赖 $F_A$、接触项和内辐射约定**；若进行严格的重夸克展开，还需要同步展开运动学因子、质量/衰变常数转换等，不能从上式孤立截取完整物理 NNLP。积分还要指定 $E_\gamma>E_{\rm cut}$、过程电荷态、$\ell$ 的味及数值输入：

$$\mathcal B(E_\gamma>E_{\rm cut})=\tau_B\int_{E_{\rm cut}}^{E_{\rm max}}dE_\gamma\,\frac{d\Gamma}{dE_\gamma}.$$

## 8. 完整工作顺序与输出边界

1. HQET 重夸克拉氏量与重轻弱流展开到 $1/m_b^2$，保留场重定义和有序算符（本轮有新结果）。
2. QCD/HQET 夸克及背景胶子外态树级匹配，确定指定算符基中的系数（已有固定基底结果；通用 $26+26$ 系数未完成）。
3. 构造 $T\{j_{\rm em},J\}$，包括轻夸克、重夸克和必要接触拓扑。
4. 完成传播子/SCET 模式幂次展开与规范因子化；确定新的二阶 hard-collinear 核与软非局域算符。
5. 给出非微扰矩阵元、LCDAs 的定义、模型/格点/QCD 和规则等输入，以及尺度/端点处理，得到 $F_V^{(2)},F_A^{(2)}$。
6. 将 LP、NLP、NNLP 的干涉项全部计入衰变率，按实验切割积分，再做误差预算与适当 RG 改进。

**结论：** “HQET 拉氏量和流展开 + 树级匹配”完成的是物理 NNLP 的必要基础，并不是完整 NNLP 分支比。误把两个不同外态的矩阵元等同，会遗漏非微扰强子结构与真实光子过程硬核。

## 9. 与既有项目文档的分工

- `NNLP_tree_matching_2026-10-14.md`：本轮固定场基底树级匹配系数及背景场检验的详细计算。
- `HQET_heavy_light_operator_basis.md`：文献的 26+26 系统母基、EOM/arrow 恒等式及未完成的 $m_u=0$ 独立秩。
- `form_factors.md`：强子张量、光子发射和非微扰软矩阵元。
- `branching_ratio.md`：能量切割、积分及 NNLP 阶振幅平方。

本笔记不包含未经验证的数值形状因子与分支比，也不声称已构造完整 NNLP 因子化定理。
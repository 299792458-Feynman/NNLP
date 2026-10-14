# 二阶幂次修正的组织方式

**状态：[框架已讨论，完整算符列表和矩阵元待计算]。**

## 1. 统一计数

在此文中暂用 $\lambda=1/m_b$ 表示重夸克展开参数，$J=J^{(0)}+J^{(1)}+J^{(2)}+\cdots$，$\mathcal L=\mathcal L^{(0)}+\mathcal L^{(1)}+\mathcal L^{(2)}+\cdots$，其中上标表示相对于最低阶的 $1/m_b$ 幂次，相关因子已包含在各项内。

## 2. 二阶的四类贡献

对最低阶 HQET 理论的矩阵元做 Dyson 展开，形式上在二阶出现：

$$
\begin{aligned}
\mathcal A^{(2)} \supset{}& \langle J^{(2)}\rangle_0
+i\!\int d^4x\,\langle T\{J^{(1)}\mathcal L^{(1)}(x)\}\rangle_0\\
&+i\!\int d^4x\,\langle T\{J^{(0)}\mathcal L^{(2)}(x)\}\rangle_0\\
&+\frac{i^2}{2!}\!\int d^4x\,d^4y\,
\langle T\{J^{(0)}\mathcal L^{(1)}(x)\mathcal L^{(1)}(y)\}\rangle_0.
\end{aligned}
$$

这里只表示**形式上的贡献类别**；真正规范化的矩阵元要处理外态修正、真空图抵消、场重定义、接触项和所选过程的其他功率修正。不能只算 $J^{(2)}$ 就宣称得到物理过程的 NNLP。

## 3. 过程相关的补充

对于 $B\to\gamma\ell\nu$，还需确认电磁流插入、软/共线模与必要的 SCET 匹配，识别光子从轻夸克、重夸克或轻子线辐射的不同贡献和对应功率计数。HQET 重夸克展开只能提供完整框架的一部分。

## 4. 待计算列表

- [ ] 对每个独立算符列出量子数、质量维度和 $1/m_b$ 抑制。
- [ ] EOM、RPI 和积分分部约化后选取完备算符基。
- [ ] 对每类时间有序乘积建立树级 Feynman 规则。
- [ ] 识别 UV/IR 分离及后续非微扰矩阵元定义。
- [ ] 在完整计数下检查是否遗漏电磁或 SCET 次领先贡献。


---

## 5. 2026-10-14：HQET 二阶算符及树级组合系数

**状态：[Dyson 展开组合因子已确定；不等同于完整衰变 NNLP 的独立算符基]。**
采用 docs/HQET_expansion.md 第 5 节的 $M=2m_b$、$J_0,J_1,J_2,O_{\rm kin},O_{\rm mag},O_T$ 定义，并约定

$$
\mathcal T_1[A,B]=i\int d^4x\,T\{A(0)B(x)\},\quad
\mathcal T_2[A,B,C]=\frac{i^2}{2!}\int d^4x\,d^4y\,
T\{A(0)B(x)C(y)\}.
$$

| 编号 | 二阶算符结构 | 系数 |
|:--:|---|---:|
| H1 | $J_2^\mu$ | $-1/M^2$ |
| H2 | $\mathcal T_1[J_1^\mu,O_{\rm kin}]$ | $+1/M^2$ |
| H3 | $\mathcal T_1[J_1^\mu,O_{\rm mag}]$ | $+1/M^2$ |
| H4 | $\mathcal T_1[J_0^\mu,O_T]$ | $-1/M^2$ |
| H5 | $\mathcal T_2[J_0^\mu,O_{\rm kin},O_{\rm kin}]$ | $+1/M^2$ |
| H6 | $\mathcal T_2[J_0^\mu,O_{\rm kin},O_{\rm mag}]$ | $+2/M^2$ |
| H7 | $\mathcal T_2[J_0^\mu,O_{\rm mag},O_{\rm mag}]$ | $+1/M^2$ |

H6 已把两个混合顺序合并，因此相对于含 $1/2!$ 的 $\mathcal T_2$ 定义有系数 2。
这些是 *七类树级重夸克二阶组合*，不是完整独立局域算符表。若采用 Darwin、spin-orbit 等场重定义后的算符基，必须同时变换电流及插入，不能把它们额外叠加在 H4 上。

## 6. 完整衰变的联合功率计数

除 HQET 二阶组合以外，对轻夸克发射真实硬光子的自由传播子
$S_u(p-\ell)$ 还需按软动量展开。
若 $\Phi_r$ 代表含适当 HQET 插入的 $M^{-r}$ 阶软矩阵元，二阶自由传播子贡献形式上由

$$
S_0\Gamma^\mu\frac{\Phi_2}{M^2}
+S_1\Gamma^\mu\frac{\Phi_1}{M}
+S_2\Gamma^\mu\Phi_0
$$

组成。同阶还需分析软背景胶子、多粒子 LCDA、重夸克硬光子发射、端点/重叠扣除、电磁接触项及可能的光子强子结构。该式是**自由传播子分量的计数恒等式**，不是完整 NNLP 因子化定理。未给出完整物理 NNLP Wilson 系数。

---

## 7. H1–H7 与二阶重轻流系统母基的关系（2026-10-14）

**[文献输入/形式代数；极小化待计算]** Balzereit–Ohl §2.1 提供 26 个维数 5 局域重轻流和 $6+4+16=26$ 个非局域 $T$-积，共 52 个 HQET 二阶重轻流系统母基元素。原有 H1–H7 是在 $M=2m_b$、未重定义 HQET 场下的树级 Dyson 组合，**既不是需额外叠加的七个独立算符，也不是 52 个系数的完整匹配**。

算符定义、左/右作用导数及混合插入对称因子详见 [`HQET_heavy_light_operator_basis.md`](HQET_heavy_light_operator_basis.md)。$m_u=0$ 下的极小独立基和完整 $B\to\gamma\ell\nu$ 的 NNLP 过程基均 **[待计算]**。

---

## 8. 2026-10-14：规范化场基底的二阶 Dyson 组合

原有 H1–H7 采用未重定义场。本节**改用另一基底，不与 H1–H7 相加**：$h_v=(1+K^2/2M^2)h_v^c$，定义 $O_1=\bar h_v^cK^2h_v^c$、$O_2=\bar h_v^c[K,[V,K]]h_v^c$；$J_a=\bar u\Gamma^\mu K^2h_v^c$、$J_b=\bar u\Gamma^\mu VKh_v^c$、$J_{0,1}$ 亦改用 $h_v^c$。

$$
\boxed{
\mathbb J_c^{(2)\mu}
=\frac12J_a^\mu-J_b^\mu
+\mathcal T_1[J_1^\mu,O_1]
-\frac12\mathcal T_1[J_0^\mu,O_2]
+\mathcal T_2[J_0^\mu,O_1,O_1] .}
$$

这里已外提共同的 $1/M^2$，$\mathcal T_1=i\int T$、$\mathcal T_2=i^2/2!\iint T$ 保持第 5 节的规范。**系数**依次为 $+1/2,-1,+1,-1/2,+1$；后面三个是树级作用量展开的 Dyson 组合因子，不是每个独立非局域母基的通用硬系数。推导、场重定义和背景场检查见 [`NNLP_tree_matching_2026-10-14.md`](NNLP_tree_matching_2026-10-14.md)。

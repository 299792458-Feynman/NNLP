# 分支比计算路线

**状态：[计算计划；尚无 NNLP 分支比数值]。**

## 1. 从形状因子到振幅

给定 $F_V(E_\gamma)$ 和 $F_A(E_\gamma)$ 的一致定义后，构造弱衰变振幅。示意地：

$$
\mathcal M_{\rm SD}=\frac{G_F V_{ub}}{\sqrt 2}\,
[\bar u_\ell\gamma^\mu(1-\gamma_5)v_\nu]\,H_\mu^{\rm SD},
$$

其中 $H_\mu^{\rm SD}=\langle\gamma|\bar u\gamma_\mu(1-\gamma_5)b|B\rangle_{\rm SD}$，电磁耦合已包含在所选形状因子参数化中。具体电荷共轭过程与符号应在实际计算时统一。

如果计算完整物理衰变率，还要检验内部辐射（IB）等贡献及其与结构依赖部分的干涉，视轻子质量和能量切割决定是否可近似忽略。

## 2. 相空间与可观测量

$$
\Gamma(E_\gamma>E_{\rm cut})=
\frac{1}{2m_B}\int_{E_\gamma>E_{\rm cut}}d\Phi_3\,
\sum_{\rm spins,pol.}|\mathcal M|^2,
\qquad
\mathcal B(E_\gamma>E_{\rm cut})=\tau_B\Gamma(E_\gamma>E_{\rm cut}).
$$

这只是通用相空间定义，并不是已经完成的解析谱或数值积分。积分前应指定 $B^\pm$ 电荷态、轻子味、实验定义的相空间切割与辐射修正方案；软光子区域可能涉及红外敏感性。

## 3. 计算所需输入

| 类别 | 待确定项目 |
| --- | --- |
| 运动学 | $m_B,m_\ell,E_{\rm cut}$、积分区间 |
| 标准模型 | $G_F$, $V_{ub}$, $\alpha_{\rm em}$, $\tau_B$ |
| 扰动部分 | 匹配系数、尺度、可能的重求和及理论误差 |
| 非微扰部分 | $F_V,F_A$ 所需的 B 介子分布振幅或其他矩阵元参数 |
| 校验 | Ward 恒等式、维度、极限行为、切割依赖、误差传播 |

## 4. 数值计算之前的门槛

- [ ] 取得一组自洽的形状因子函数及其误差，不能只有算符展开。
- [ ] 明确“NNLP”覆盖哪些功率项，避免遗漏同阶贡献。
- [ ] 实现差分衰变率并用已知极限或参考结果核验。
- [ ] 再进行数值积分和误差预算，记录参数版本与引用来源。

---

## 5. 2026-10-14：微扰匹配、RG 与 NNLP 衰变率的区别

树级重轻弱流系数是 $\alpha_s^0$ 的短距离信息，并非 $F_V,F_A$ 的非微扰输入。RG 需要反常维数及算符混合，不能仅由树级系数确定 $\lambda_B$ 等输入。$\Lambda_{\rm QCD}/m_b$ 的幂次展开和 $\alpha_s$ 微扰展开应独立计数；NNLP 不等于 NNLL。

设 $F_i=F_i^{(0)}+F_i^{(1)}+F_i^{(2)}+\cdots$（此处上标为**相对幂次**），则衰变率中相对 NNLP 的模平方结构为

$$
\boxed{\bigl.|F_i|^2\bigr|_{\rm NNLP}=2\operatorname{Re}[F_i^{(0)*}F_i^{(2)}]+|F_i^{(1)}|^2,\quad i=V,A.}
$$

如果再重夸克展开相空间/运动学因子，还需计入它们的二阶系数。质量可忽略的轻子及某种统一的轴矢/内辐射约定下，常见结构依赖光子谱为

$$
\frac{d\Gamma}{dE_\gamma}=\frac{\alpha_{\rm em}G_F^2|V_{ub}|^2}{6\pi^2}
 m_BE_\gamma^3(1-2E_\gamma/m_B)(|F_V|^2+|F_A|^2).
$$

需先核对具体规范和 $E_{\rm cut}$，不把此示意关系当作已算出 NNLP 谱。完整讨论见 [`from_matching_to_branching_ratio_2026-10-14.md`](from_matching_to_branching_ratio_2026-10-14.md)。

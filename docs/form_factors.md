# $B\to\gamma\ell\nu$ 的形状因子

**状态：[定义与计算路线；尚无 NNLP 数值预测]。**

## 1. 两个结构依赖形状因子

对真实光子动量 $k$、极化 $\epsilon$ 和 $B$ 介子动量 $p$，可用两个与电磁规范不变性兼容的 Lorentz 结构参数化结构依赖的强子电流，例如

$$
\begin{aligned}
\langle \gamma(k,\epsilon)|\bar u\gamma_\mu b|\bar B(p)\rangle
&=\frac{e}{m_B}\,\varepsilon_{\mu\nu\alpha\beta}\epsilon^{*\nu}p^\alpha k^\beta\,F_V(E_\gamma),\\
\langle \gamma(k,\epsilon)|\bar u\gamma_\mu\gamma_5 b|\bar B(p)\rangle_{\rm SD}
&=\frac{ie}{m_B}\,[\epsilon^*_\mu(p\cdot k)-k_\mu(\epsilon^*\cdot p)]\,F_A(E_\gamma).
\end{aligned}
$$

这里仅给出一种**约定性定义**，尤其要明确 $\varepsilon_{0123}$、总体相位、$B$ 介子电荷及轴矢 Ward 恒等式可能引入的接触项。与参考文献比较之前不能直接比较符号。

## 2. 从算符到形状因子

1. 先完成 `QCD_HQET_matching.md` 的短距离算符系数。
2. 为各局域算符与时间有序乘积定义 $\langle\gamma|\mathcal O|B\rangle$ 的非微扰矩阵元。
3. 用 Lorentz 投影和 Ward 恒等式提取 $F_V,F_A$；明确 $E_\gamma=v\cdot k$ 的参考系。
4. 在一致的功率计数下相加各项，区分可微扰算的硬核与模型/格点/QCD sum rules 等输入。
5. 若采用光锥方法，需另外定义分布振幅、卷积核、尺度及端点问题，不可仅由 HQET 电流展开替代。

## 3. 待核验/待计算

- [ ] 决定 $F_A$ 中接触项与内部辐射部分的约定。
- [ ] 明确重夸克辐射、电磁流插入与轻夸克辐射的分解方式。
- [ ] 确定 NNLP 非微扰矩阵元是否可用已有参数表达，还是需要新的独立函数。
- [ ] 检查能量依赖、尺度演化、强子输入及不确定性传播。


---

## 4. 2026-10-14：电磁流 Wick 收缩后的四类 NNLP 软矩阵元

采用
$T^{\mu\nu}(p)=i\int d^4x\,e^{ipx}
\langle0|T\{j_{\rm em}^\nu(x),J^\mu(0)\}|B^-\rangle$。
对轻夸克电磁流 $j_{{\rm em},u}^\nu=Q_u\bar u\gamma^\nu u$，
将 $u(x)$ 与弱流中 $\bar u(0)$ 做 Wick 收缩，产生固定背景场传播子
$S_u(x,0;A)=\langle T u(x)\bar u(0)\rangle_A$。以下仅列留下的软场结构；
整体相位、费米符号及不相连部分仍须按统一的 Fourier/外态约定核对。

| 来源 | Wick 收缩后的剩余强子结构 |
|---|---|
| $J_2$ | $\bar u(x)\gamma^\nu S_u(x,0;A)\Gamma^\mu VKh_v(0)$ |
| $J_1\mathcal L_1$ | $\bar u(x)\gamma^\nu S_u(x,0;A)\Gamma^\mu Kh_v(0)$，并插入 $O_K(y)$ |
| $J_0\mathcal L_2$ | $\bar u(x)\gamma^\nu S_u(x,0;A)\Gamma^\mu h_v(0)$，并插入 $O_T(y)$ |
| $J_0(\mathcal L_1)^2$ | 最低阶弱流结构，并插入 $O_K(y)O_K(z)$ |

这些非局域算符需要相应 Wilson 线、剩余时间排序及非微扰矩阵元定义，不能仅由领先 $\phi_+(\omega)$ 代替。

## 5. 自由轻夸克传播子与 NNLP 的三种联合组合

在 $p^2=0$、$d=2p\cdot\ell$ 时，

$$
S_u(p-\ell)=\frac{i(\not p-\not\ell)}{-d+\ell^2+i0}.
$$

沿 $|\ell^2/d|\ll1$ 区域展开：

$$
S_0=-\frac{i\not p}{d},\quad
S_1=\frac{i\not\ell}{d}-\frac{i\not p\,\ell^2}{d^2},\quad
S_2=\frac{i\not\ell\,\ell^2}{d^2}
-\frac{i\not p\,(\ell^2)^2}{d^3}.
$$

以 $\Phi_r$ 表示含第 $r$ 阶 HQET 插入的软矩阵元，
**自由传播子部分**在二阶要求全部三组：

$$
\boxed{\quad
T_{u,\mathrm{free}}^{\mu\nu}\big|_{\lambda^2}
\ \propto\
\int d^4\ell\,\mathrm{Tr}
\left[\gamma^\nu\left(
S_0\Gamma^\mu\frac{\Phi_2}{M^2}
+S_1\Gamma^\mu\frac{\Phi_1}{M}
+S_2\Gamma^\mu\Phi_0
\right)\right].\quad}
$$

比例号表明整体 $i$、归一化、Fourier 测度和 Ward 接触项尚待统一。
这里的 $\Phi_1,\Phi_2$ 是时间有序的非局域软矩阵元，不是已知数值输入。
含背景软胶子的传播子展开还需规范不变的三粒子或更高多粒子 LCDA；
将 $\ell^2$ 转成协变导数时需考虑 EOM 和端点重叠。

## 6. 硬光子、Ward 检验与形状因子状态

重夸克硬光子发射的树级 QCD 核及候选 NNLP 动量展开见
docs/QCD_HQET_matching.md 第 8 节。**[待核验]**
电磁流 Ward 恒等式中的接触项必须和轻、重夸克及轻子辐射一起核对。
不能将自由传播子三组直接称为完整物理 $F_V^{\rm NNLP},F_A^{\rm NNLP}$。

若 $F=F^{(0)}+F^{(1)}+F^{(2)}+\cdots$，相对二阶的模平方包括

$$
\left.|F|^2\right|_{\mathrm{NNLP}}
=2\mathrm{Re}[F^{(0)*}F^{(2)}]+|F^{(1)}|^2.
$$

这是纯代数关系，不代表本项目已求出形状因子或分支比。

---

## 7. 2026-10-14：为什么树级系数仍不足以得到 $F_V,F_A$

QCD/HQET 匹配时的 $\langle u|J|b\rangle$ 使用微扰外态，而衰变需要 $\langle\gamma|J|B\rangle$。后者在高能光子 LP 已包含 $B$ 介子 LCDA 的逆矩 $\lambda_B^{-1}=\int_0^\infty d\omega\,\phi_+(\omega)/\omega$，不能由树级 Wilson 系数求出。作为**约定性 LP 示例**，树级常见形式 $F_{V,A}^{\rm LP}\sim Q_um_B\widetilde f_B/(2E_\gamma\lambda_B)$；轴矢接触项和辐射定义须另行统一。

此外，轻夸克发射硬光子时 $S_u(k-q)=i(\not k-\not q)/[-2q\cdot k+k^2+i0]$，即使重夸克 HQET 场不做更高阶展开，其分母的 $[k^2/(2q\cdot k)]^2$ 项也在相对 NNLP 量级。真实光子的过程匹配、软背景胶子、多粒子 LCDAs、硬核与规范 Ward 检查均不能由本轮重轻弱流系数表直接替代。推理及幂次组合详见 [`from_matching_to_branching_ratio_2026-10-14.md`](from_matching_to_branching_ratio_2026-10-14.md)。

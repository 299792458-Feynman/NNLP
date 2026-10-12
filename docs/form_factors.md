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

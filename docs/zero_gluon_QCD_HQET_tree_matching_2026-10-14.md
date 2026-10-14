# 无背景胶子的 QCD/HQET 树级匹配：到 NNLP 的完整推导

**日期：** 2026-10-14  
**任务范围：** $B^-\to\gamma\ell^-\bar\nu$ 项目中的重夸克弱流 **QCD $\to$ HQET 树图**匹配，先只考虑**零背景胶子**。该子任务不等于真实硬光子的完整 NNLP 衰变振幅。

## 1. 出发点：为什么比较两种矩阵元？

QCD 弱流是 $J_{\rm QCD}^\mu=\bar u\Gamma^\mu b$，其中 $\Gamma^\mu=\gamma^\mu(1-\gamma_5)$。希望在固定重夸克场基底中，让 HQET 的局域弱流及拉氏量插入重现 QCD 的树级重夸克低能传播及弱流振幅，到 $1/m_b^2$ 精度。

比较两个**不同用途**的对象：
- **在壳截肢振幅** $\mathcal M_{\rm QCD}^\mu=\langle u(p')|\bar u\Gamma^\mu b|b(p_b)\rangle_{\rm tree}$，用于看到 Dirac 旋量的场重构。
- **离壳投影 Green 函数**：轻夸克线截肢，重夸克源取 $P_+$，保留它到弱流顶点之间的重夸克传播子，用于检查有效作用量的一阶、二阶插入。

单一在壳无胶子矩阵元不一定能独立确定所有 EOM 冗余系数；离壳 Green 函数的算符分解也依赖场定义与源约定。

## 2. 场与动量约定

$$
M=2m_b,\quad p_b=m_bv+k,\quad v^2=1,\quad \omega=v\cdot k,\quad
k_\perp^\mu=k^\mu-\omega v^\mu,\quad P_\pm=\frac{1\pm\slashed v}{2},
$$
$$
V=iv\cdot D,\qquad K=i\slashed D_\perp,\qquad D_\mu=\partial_\mu-ig_sA_\mu^aT^a.
$$

固定**原始、未额外重定义**的 HQET 场：
$$
b(x)=e^{-im_bv\cdot x}[h_v(x)+H_v(x)],\quad
P_+h_v=h_v,\quad P_-H_v=H_v.
$$
从 QCD 重夸克二次作用量精确消去小分量：
$$
H_v=(M+V)^{-1}Kh_v.
$$
因此严格保留 $V,K$ 的有序次序，
$$
\boxed{b=e^{-im_bv\cdot x}
\left(1+\frac{K}{M}-\frac{VK}{M^2}\right)h_v+O(M^{-3}).}
$$

## 3. QCD 无胶子在壳截肢振幅

树级 QCD 图只有一个弱流顶点：
$$
\boxed{\mathcal M_{\rm QCD}^\mu=\bar u_u(p')\Gamma^\mu u_b(p_b).}
$$
将 $u_b=u_++u_-$，其中 $u_\pm=P_\pm u_b$。QCD Dirac 方程给出
$$
\boxed{u_-=\frac{\slashed k_\perp}{M+\omega}u_+.}
$$
于是
$$
\begin{aligned}
\mathcal M_{\rm QCD}^\mu
&=\bar u_u\Gamma^\mu\left(1+\frac{\slashed k_\perp}{M+\omega}\right)u_+\\
&=\bar u_u\Gamma^\mu
\left(1+\frac{\slashed k_\perp}{M}
-\frac{\omega\slashed k_\perp}{M^2}\right)u_+ +O(M^{-3}).
\end{aligned}
$$
这里约定 $u_+$ 是用于两边比较的共同投影外态；不应未经转换拿它代表规范化 HQET 场的外态。

## 4. HQET 局域弱流：所有直接出现的树级算符与系数

直接将上一节的 QCD 场展开代入弱流，去掉共同的快速相位：
$$
\boxed{J_{\rm tree}^\mu
=J_0^\mu+\frac{J_1^\mu}{M}-\frac{J_2^\mu}{M^2}+O(M^{-3}),}
$$
$$
J_0^\mu=\bar u\Gamma^\mu h_v,\quad
J_1^\mu=\bar u\Gamma^\mu Kh_v,\quad
J_2^\mu=\bar u\Gamma^\mu VKh_v.
$$

| 阶数 | 局域算符 | 外提 $M$ 因子 | 固定原始场的树级系数 |
|---|---|---|---:|
| LP | $J_0^\mu$ | $1$ | $+1$ |
| NLP | $J_1^\mu$ | $1/M$ | $+1$ |
| NNLP | $J_2^\mu$ | $1/M^2$ | $-1$ |

无胶子自由场取 $K\mapsto\slashed k_\perp$、$V\mapsto\omega$，得到
$$
\mathcal M_{\rm HQET,current}^\mu
=\bar u_u\Gamma^\mu\left(
1+\frac{\slashed k_\perp}{M}
-\frac{\omega\slashed k_\perp}{M^2}\right)u_+,
$$
与 QCD 旋量展开相容。**注意：这是固定场重构的系数，不表示可由这一个在壳过程独立解出所有 NNLP Wilson 系数。**

## 5. HQET 拉氏量：为何必须插入

弱流的局域展开不自动包含在弱流顶点之前的重夸克传播修正。由同一次树级小分量消元得到
$$
\boxed{\mathcal L_{\rm HQET}
=\bar h_v\left[V+\frac{K^2}{M}-\frac{KVK}{M^2}\right]h_v+O(M^{-3}).}
$$
定义
$$
O_K=\bar h_vK^2h_v,\qquad O_T=\bar h_vKVKh_v.
$$
在所定义的 $M$ 幂次外提后，拉氏量的**树级系数**为 $C_{O_K}=+1$、$C_{O_T}=-1$。

完整协变作用量中 $O_K=O_{\rm kin}+O_{\rm mag}$，但**无胶子**自由外态不能独立检测 $O_{\rm mag}$ 的场强部分；不能把零胶子下看不到它误解为磁算符树级系数为零。

## 6. QCD 带重夸克传播子的离壳 Green 函数

将轻夸克腿截肢、重夸克源取 $P_+$，剥去共同的传播子 $i$ 因子：
$$
\boxed{
\mathcal G_{\rm QCD}^\mu
=\bar u_u(p')\Gamma^\mu\,
\frac{M+\omega+\slashed k_\perp}
{M\omega+\omega^2+k_\perp^2}\,P_+.
}
$$
实际因果传播子含 $+i0$；为比较远离极点的离壳幂次系数，以下略去该记号。记
$$
K_0=\slashed k_\perp,\qquad z=k_\perp^2=K_0^2.
$$
在**固定非零 $\omega$ 的离壳展开**中：
$$
\boxed{\begin{aligned}
\mathcal G_{\rm QCD}^\mu
=\bar u_u\Gamma^\mu\Bigg[
&\frac1\omega+
\frac1M\left(\frac{K_0}{\omega}-\frac{z}{\omega^2}\right)\\
&+\frac1{M^2}\left(-K_0-\frac{K_0z}{\omega^2}
+\frac z\omega+\frac{z^2}{\omega^3}\right)
\Bigg]P_++O(M^{-3}).
\end{aligned}}
$$
这就是 HQET 必须重现的、带流与传播修正的目标，而不是只要求传播子极点相同。

## 7. HQET Green 函数与时间有序插入

无胶子下 $V\mapsto\omega,K\mapsto K_0,K^2\mapsto z,KVK\mapsto\omega z$，于是
$$
R_h=1+\frac{K_0}{M}-\frac{\omega K_0}{M^2},\qquad
S_h^{-1}=\omega+\frac zM-\frac{\omega z}{M^2},
$$
$$
\boxed{\mathcal G_{\rm HQET}^\mu
=\bar u_u\Gamma^\mu R_h(S_h^{-1})^{-1}P_+.}
$$
展开重夸克传播子：
$$
(S_h^{-1})^{-1}
=\frac1\omega-\frac z{M\omega^2}
+\frac1{M^2}\left(\frac z\omega+\frac{z^2}{\omega^3}\right)
+O(M^{-3}).
$$

各阶的**全部自由无胶子树图核**如下（表中已剥去该阶的整体 $1/M^n$）：

| 阶数 | HQET 算符或 Dyson 插入 | 在 Green 函数中的动量核 |
|---|---|---|
| LP | $J_0$、$\mathcal L_0$ 自由传播 | $1/\omega$ |
| NLP | $J_1$ | $K_0/\omega$ |
| NLP | $i\int T\{J_0,O_K\}$ | $-z/\omega^2$ |
| NNLP | $-J_2$ | $-K_0$ |
| NNLP | $i\int T\{J_1,O_K\}$ | $-K_0z/\omega^2$ |
| NNLP | $-i\int T\{J_0,O_T\}$ | $+z/\omega$ |
| NNLP | $\frac{i^2}{2}\iint T\{J_0,O_K,O_K\}$ | $+z^2/\omega^3$ |

这里的时间有序积定义包括相应积分与 Dyson $i$、$1/2!$ 因子。**弱流/拉氏量中的 Wilson 展开系数的符号，与把它插入传播子后出现的动量核符号，并不一定相同**，后者还包含逆传播子的负号。

将这些图同阶相加：
$$
\boxed{\begin{aligned}
\mathcal G_{\rm HQET}^\mu
=\bar u_u\Gamma^\mu\Bigg[
&\frac1\omega+
\frac1M\left(\frac{K_0}{\omega}-\frac{z}{\omega^2}\right)\\
&+\frac1{M^2}\left(-K_0-\frac{K_0z}{\omega^2}
+\frac z\omega+\frac{z^2}{\omega^3}\right)
\Bigg]P_++O(M^{-3}).
\end{aligned}}
$$
与 QCD 式逐项相同：
$$
\boxed{\mathcal G_{\rm QCD}^{(n)\mu}=\mathcal G_{\rm HQET}^{(n)\mu},\qquad n=0,1,2.}
$$

无需另猜系数：在没有截断 $1/M$ 的自由理论中，**精确代数恒等式**就是
$$
\boxed{
\frac{M+\omega+K_0}{M\omega+\omega^2+z}
=\left(1+\frac{K_0}{M+\omega}\right)
\left(\omega+\frac{z}{M+\omega}\right)^{-1}.
}
$$
QCD 分子来自完整重夸克传播子；右侧两个因子分别来自弱流场重构与 HQET 作用量。这是在同一重夸克 $P_+$ 源规范下的等式。

## 8. 所有树级系数应如何称呼

**固定原始场、外提 $1,M^{-1},M^{-2}$ 的局域流系数：**
$$
C_{J_0}^{(0)}=1,\quad C_{J_1}^{(0)}=+1,\quad C_{J_2}^{(0)}=-1.
$$
上标 $(0)$ 指 $\alpha_s^0$，不是 LP。

**固定原始场的 HQET 拉氏量系数：**
$$
C_{O_K}^{(0)}=+1,\qquad C_{O_T}^{(0)}=-1.
$$

**时间有序积的组合因子**（采用 $i\int T$ 和 $\frac{i^2}{2}\iint T$ 规范化）：
$$
\begin{array}{c|c}
i\int T\{J_0,O_K\}\quad(\mathrm{NLP}) & +1\\
i\int T\{J_1,O_K\}\quad(\mathrm{NNLP}) & +1\\
i\int T\{J_0,O_T\}\quad(\mathrm{NNLP}) & -1\\
\frac{i^2}{2}\iint T\{J_0,O_K,O_K\}\quad(\mathrm{NNLP}) & +1
\end{array}
$$
这些不是四个新的、各自独立的短程 Wilson 系数。

## 9. 在壳限制与不能擅自下的结论

重夸克在壳：
$$
p_b^2=m_b^2\quad\Longrightarrow\quad
M\omega+\omega^2+z=0,\qquad
\omega=-\frac zM+O(M^{-3}).
$$
因此 $-\omega K_0/M^2=O(M^{-3})$；**仅一个无胶子、在壳两夸克振幅，在 NNLP 精度下不能独立确定 $J_2$ 的 $-1$**。这一系数来自固定原始场小分量消元和离壳投影 Green 核的场重构约定，不应冒充可观测的独立匹配系数。

同理，无胶子外态不能独立确定含 $G_{\mu\nu}$ 的算符系数；对 EOM 冗余项做重定义会改变局域系数与时间有序接触项的分配。采用规范化场
$$
h_v=\left(1+\frac{K^2}{2M^2}\right)h_v^c
$$
时，会出现 $+\frac12\bar u\Gamma^\mu K^2h_v^c/M^2$，必须连同作用量和外态一起换基，绝不可与本原始场表重复相加。

## 10. 与 NNLP 树图物理主线的承接

**已在本记录中解析验证：** 无胶子、指定 $P_+$ 外部源的 QCD/HQET 自由 Green 函数中，弱流重构及作用量单、双插入共同匹配到 $1/M^2$；完整自由旋量结构相容。

**未由此验证：** 一、二软背景胶子的全部独立图和接触项；含真实硬光子的发射核、QED Ward 恒等式、EOM/RPI 全套检验；非微扰 $B$ 介子矩阵元，$F_{V/A}^{(2)}$ 与分支比。

**下一步：** 不去求 26+26 母基的通用独立秩作为树级工作的前提，而是直接计算真实硬光子分别从轻旁观夸克和重夸克辐射的 QCD 树图，并建立对应的 HQET/SCET 展开及完整幂次计数。

相关文件：[NNLP 树级流与作用量](NNLP_tree_matching_2026-10-14.md)、[QCD/HQET 匹配](QCD_HQET_matching.md)、[树级物理流程](tree_level_NNLP_workflow_2026-10-14.md)。

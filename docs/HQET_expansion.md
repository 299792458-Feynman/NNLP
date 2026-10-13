# HQET 重夸克场展开（至 $1/m_b^2$）

**状态：[形式推导/待核验]。** 本文记录计算起点；尚未对所有导数排序、重定义和规范约定进行最终校验。

## 1. 固定约定

令 $v^2=1$，$P_\pm=(1\pm\!\not v)/2$，$D_\perp^\mu=D^\mu-v^\mu(v\cdot D)$。约定中的 $D_\mu$ 符号与度规必须在匹配计算前固定。把 QCD 重夸克场写为

$$
b(x)=e^{-im_b v\cdot x}\bigl[h_v(x)+H_v(x)\bigr],\qquad
P_+h_v=h_v,\quad P_-H_v=H_v.
$$

## 2. 小分量消元（树级经典关系）

从重夸克作用量得到形式解

$$
H_v=\frac{1}{2m_b+i v\cdot D}\,i\!\not\!D_\perp\,h_v.
$$

按逆算符的有序乘积展开：

$$
H_v=\frac{1}{2m_b}i\!\not\!D_\perp h_v
-\frac{1}{(2m_b)^2}(i v\cdot D)(i\!\not\!D_\perp)h_v
+O(m_b^{-3}).
$$

这里的导数是算符，**次序不可随意交换**；改写时会产生协变导数对易子和胶子场强项。

## 3. 电流与有效作用量

对示意的重轻电流 $J_{\rm QCD}=\bar q\,\Gamma b$，代入上式并按幂次分组：

$$
J_{\rm QCD}=e^{-im_b v\cdot x}\bigl[J^{(0)}+J^{(1)}+J^{(2)}+O(m_b^{-3})\bigr],
$$

其中 $J^{(n)}$ 含对应的 $1/m_b^n$ 抑制因子。通过消去 $H_v$，重夸克作用量形式上成为

$$
\mathcal L_{\rm HQET}=
\bar h_v i v\cdot D h_v+
\bar h_v i\!\not\!D_\perp\frac{1}{2m_b+i v\cdot D}
 i\!\not\!D_\perp h_v,
$$

随后按 $1/m_b$ 展开为 $\mathcal L^{(0)}+\mathcal L^{(1)}+\mathcal L^{(2)}+\cdots$。这只是给出一种场变量约定下的形式表示，不能直接当作所有重整化后局域算符系数。

## 4. 必查问题

- 二阶项中 $i v\cdot D$ 是否能使用**最低阶** EOM 消去？消去后作用量、流和时间有序乘积如何一起变化？
- $D_\perp$ 和 $v\cdot D$ 的次序改变产生哪些 $[D_\mu,D_\nu]$？
- 选取的 HQET 场是否做过额外重定义？是否应对照 RPI 约束？
- 完整衰变 NNLP 与单纯重夸克 $1/m_b^2$ 子问题的关系是什么？

**下一步：** 固定明确的二阶独立算符基，再到 `QCD_HQET_matching.md` 做外态匹配。


---

## 5. 2026-10-14 补充：统一的树级未约化算符定义

**状态：[树级形式代数已核对；未构造完整独立重整化算符基]。**
固定度规 $g^{\mu\nu}=\mathrm{diag}(1,-1,-1,-1)$、$D_\mu=\partial_\mu-ig_sA_\mu^aT^a$，
$P_\pm=(1\pm\not v)/2$，并记

$$
M=2m_b,\quad V=iv\cdot D,\quad K=i\not D_\perp,\quad
\Gamma^\mu=\gamma^\mu(1-\gamma_5).
$$

重夸克大/小分量的树级消元与局域有序展开为

$$
H_v=(M+V)^{-1}Kh_v,\qquad
b=e^{-im_bv\cdot x}[1+M^{-1}K-M^{-2}VK+O(M^{-3})]h_v.
$$

这给出 **未额外进行高阶场重定义** 的弱流

$$
J^\mu=J_0^\mu+M^{-1}J_1^\mu-M^{-2}J_2^\mu+O(M^{-3}),
$$

$$
J_0^\mu=\bar u\Gamma^\mu h_v,\quad
J_1^\mu=\bar u\Gamma^\mu Kh_v,\quad
J_2^\mu=\bar u\Gamma^\mu VKh_v.
$$

同一场定义中的拉氏量为

$$
\mathcal L_{\rm HQET}
=\bar h_vVh_v+M^{-1}O_K-M^{-2}O_T+O(M^{-3}),
$$

$$
O_K=\bar h_vK^2h_v
=O_{\rm kin}+O_{\rm mag},\qquad
O_T=\bar h_vKVKh_v,
$$

$$
O_{\rm kin}=\bar h_v(iD_\perp)^2h_v,\qquad
O_{\rm mag}=\frac{g_s}{2}\bar h_v\sigma_{\alpha\beta}G^{\alpha\beta}h_v.
$$

**导数次序不得交换**：$VK=KV+[V,K]$，在本约定下
$[V,K]=ig_s\gamma_\perp^\rho v^\alpha G_{\alpha\rho}$。
利用最低阶 EOM 改写时必须同时追踪场重定义、时间有序乘积及接触项。
Darwin/spin-orbit 基是另一种约化表示，不可与原始 $O_T$ 重复相加。

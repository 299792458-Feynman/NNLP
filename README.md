# NNLP — $B\to\gamma\ell\nu$ 的幂次修正研究

> **状态：研究笔记初稿；尚未完成可用于数值预测的 NNLP 计算。**

## 研究目标

研究辐射轻子衰变 $B\to\gamma\ell\nu$ 的结构依赖振幅、形状因子 $F_V(E_\gamma)$ 与 $F_A(E_\gamma)$，以及含光子能量切割的分支比。当前重点是 **重夸克 HQET 展开中的 $1/m_b^2$ 项**，检查其电流匹配、拉氏量插入和非微扰矩阵元。

**范围提醒：**“HQET 中的 $1/m_b^2$”不自动等于衰变振幅完整的 NNLP（相对于 $\Lambda_{\rm QCD}/E_\gamma$ 等变量的幂次展开）。必须明确所采用的功率计数；完整结果可能还需 SCET 次领先算符、光子从不同夸克线发射的贡献等。

## 文档导航

| 路径 | 内容 |
| --- | --- |
| [`docs/HQET_expansion.md`](docs/HQET_expansion.md) | 重夸克场分解及 $1/m_b^2$ 展开 |
| [`docs/HQET_heavy_light_operator_basis.md`](docs/HQET_heavy_light_operator_basis.md) | 二阶重轻流 26+26 系统母基、H1–H7 映射及尚未完成的无质量/过程级约化 |
| [`docs/QCD_HQET_matching.md`](docs/QCD_HQET_matching.md) | 全理论/有效理论的匹配流程与 EOM 陷阱 |
| [`docs/power_corrections.md`](docs/power_corrections.md) | NNLP 算符和时间有序插入清单 |
| [`docs/form_factors.md`](docs/form_factors.md) | $F_V,F_A$ 的定义及提取 |
| [`docs/branching_ratio.md`](docs/branching_ratio.md) | 相空间积分、输入参数与分支比 |
| [`progress/CURRENT_STATUS.md`](progress/CURRENT_STATUS.md) | 当前进度、阻塞点及下一步 |
| [`progress/research_log.md`](progress/research_log.md) | 按日期记录讨论和验证 |
| [`references/bibliography.md`](references/bibliography.md) | 文献及待核查信息 |
| [`AGENTS.md`](AGENTS.md) | AI / Codex 修改仓库的规则 |

## 研究标准

每个物理陈述区分：**[已推导并核验]、[形式推导/待核验]、[待计算]、[外部输入]**。讨论过的表达式不是自动成立的最终结果。写出算符基、场重定义、运动方程和归一化约定后，才允许比较匹配系数。

已按 Balzereit–Ohl §2.1 整理 HQET 重轻流二阶 26 个局域算符和 26 个非局域时间有序乘积的**系统母基**。该数目不代表无质量 $u$ 夸克的最终极小基，也不等于含真实硬光子的完整 $B\to\gamma\ell\nu$ NNLP 过程基。

## 同步流程

在 ChatGPT 中讨论后，明确发出“同步 NNLP”指令，先预览改动，再经确认提交 GitHub。项目指令不会自行监听每条对话并自动推送。GitHub 本仓库当前为 **Public**：不要提交凭据、私人聊天记录、未获许可传播的文献全文。

## 下一步

先固定功率计数与算符基，再复核到 $1/m_b^2$ 的重夸克场展开、电流与作用量插入；对可能被低阶 EOM 消去的算符逐一检查，完成带背景胶子振幅的树级匹配，最后转向衰变矩阵元与数值输入。

---

## 2026-10-14 本轮详细研究笔记（待审核新增）

- [`docs/NNLP_tree_matching_2026-10-14.md`](docs/NNLP_tree_matching_2026-10-14.md)：固定未重定义及规范化重夸克场基底；完整小分量消元、树级系数 $C_{K^2}=+1/2,C_{VK}=-1$、自由外态、单背景胶子 Ward 差分、二胶子局域接触项、Dyson 插入系数及 EOM 陷阱。
- [`docs/from_matching_to_branching_ratio_2026-10-14.md`](docs/from_matching_to_branching_ratio_2026-10-14.md)：匹配夸克外态与物理 $B$ 矩阵元的区别；LP 的 $\lambda_B$ 非微扰输入；硬光子传播子 NNLP 幂次；RG/幂次展开；衰变率的 NNLP 干涉项与未完成清单。

**范围：** 此两篇仅新增固定基底 HQET 树级子集与物理计算路线，不能解释为已完成完整 $m_u=0$ 极小算符基、全部 QCD/HQET/SCET/QED 匹配或数值分支比。

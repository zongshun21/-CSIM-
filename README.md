<div align="center">

# 科研论文写作规范

### 实验室新人论文写作与汇报手册

把科研经验沉淀成一份能直接查、直接用、能反复自检的写作规范。

![Writing Logic](https://img.shields.io/badge/Writing-Story%20First-b91c1c)
![Evidence](https://img.shields.io/badge/Core-Claim%20Evidence-2f4858)
![Reference](https://img.shields.io/badge/Reference-GB%2FT%207714%20%2B%20Submission%20Style-5f7f71)
![Notation](https://img.shields.io/badge/Notation-Consistent%20Symbols-8a6f4d)

</div>

---

## 目录

| 一级模块 | 二级目录 | 入口 |
|---|---|---|
| **0. 写作总纲** | 核心原则与判断标准 | [进入](#0-写作总纲先判断再表达) |
| **1. 从项目到论文** | [1.1 一篇论文的主线](#11-一篇论文的主线) · [1.2 推荐写作顺序](#12-推荐写作顺序) · [1.3 截稿前一个月倒排](#13-截稿前一个月倒排) | [进入](#1-从项目到论文先搭-story-再写正文) |
| **2. 论文正文写法** | [2.1 总原则](#21-正文写作总原则) · [2.2 Title 和 Abstract](#22-title-和-abstract) · [2.3 Introduction](#23-introduction) · [2.4 Method](#24-method) · [2.5 Implementation Details](#25-implementation-details) · [2.6 Experiments](#26-experiments) · [2.7 Related Work](#27-related-work) · [2.8 Conclusion](#28-conclusion) · [2.9 自审修改](#29-自审修改) | [进入](#2-论文正文写法每一节都要回答固定问题) |
| **3. 组会汇报** | [3.1 推荐汇报结构](#31-推荐汇报结构) · [3.2 每一页只讲一个判断](#32-每一页只讲一个判断) | [进入](#3-组会汇报不要只报结果要报判断) |
| **4. 参考文献规范** | [4.1 完整字段](#41-完整参考文献应包含什么) · [4.2 会议论文](#42-会议论文示例) · [4.3 期刊论文](#43-期刊论文示例) · [4.4 特殊情况](#44-特殊情况) · [4.5 BibTeX](#45-bibtex-建议) | [进入](#4-参考文献规范真实完整可追溯) |
| **5. 符号与字母规范** | [5.1 字体约定](#51-字体约定) | [进入](#5-符号与字母规范让公式可读) |
| **6. 投稿前检查** | story、claim、method、experiments、figures、references、notation、submission 自查 | [进入](#6-投稿前检查少犯低级错误) |

---

![科研论文写作飞轮](assets/paper_writing_flywheel.svg)

## 0. 写作总纲：先判断，再表达

> [!IMPORTANT]
> 写论文不是把实验结果翻译成英文，而是让读者相信：问题值得研究，方法有必要，证据能支撑结论。

| 原则 | 一句话解释 | 常见错误 |
|---|---|---|
| 先搭 story | 先讲清 Task、Gap、Insight、Method、Evidence | 一上来写 Method，论文没有主线 |
| 每个 claim 都要有证据 | 强结论必须能追到实验、图表、引用或分析 | Abstract 写得很强，实验撑不住 |
| 图表也是论证 | 图、表、caption 要帮助读者理解贡献 | 图表只是装饰，没有结论 |
| 失败结果要解释 | failure case 用来说明边界和下一步 | 只报“失败了”，不说明原因 |
| 格式服务可读性 | 引用、符号、公式统一，减少读者理解成本 | 同一变量前后换符号、换含义 |

---

## 1. 从项目到论文：先搭 story，再写正文

### 1.1 一篇论文的主线

写正文前，先用下面 8 个问题检查项目是否已经能讲成论文。

| 问题 | 你必须能回答 |
|---|---|
| Task 是什么 | 输入、输出、目标是什么 |
| Application 是什么 | 这个任务为什么重要 |
| Existing methods 怎么做 | 现有路线是什么 |
| Gap 在哪里 | 旧方法在哪些条件下失败 |
| Insight 是什么 | 你观察到的关键事实是什么 |
| Method 怎么利用 insight | 方法如何把观察变成设计 |
| Contribution 是什么 | 相比已有工作新增了什么 |
| Evidence 是什么 | 哪些实验支撑上述贡献 |

> [!TIP]
> 判断 story 是否成熟：不用图、不看代码，3 分钟能否讲清“问题为什么重要、旧方法为什么不够、我们为什么有效”。

### 1.2 推荐写作顺序

| 顺序 | 任务 | 目的 |
|---|---|---|
| 1 | 画 pipeline 草图 | 检查方法能否被清楚解释 |
| 2 | 梳理 Introduction 主线 | 确定卖点和实验需求 |
| 3 | 设计 comparison / ablation | 避免写完才发现 claim 没证据 |
| 4 | 写 Method 初稿 | 讲清模块动机、设计和优势 |
| 5 | 写 Experiments | 用证据回答 reviewer 质疑 |
| 6 | 写 Related Work | 定位本文贡献，而不是罗列文献 |
| 7 | 写 Title / Abstract | 最后浓缩整篇论文 |
| 8 | 自审和导师 review | 提前暴露拒稿风险 |

### 1.3 截稿前一个月倒排

| 时间 | 核心目标 | 必须产出 |
|---|---|---|
| T-30 到 T-24 | story 成型 | pipeline 草图、Introduction 大纲、实验矩阵 |
| T-23 到 T-18 | 方法成型 | Method v1、主结果表、初版消融 |
| T-17 到 T-12 | 证据成型 | comparison、ablation、analysis、failure cases |
| T-11 到 T-7 | 初稿完整 | Related Work、Abstract、Title、完整 PDF |
| T-6 到 T-3 | 集中修改 | review issue list、v2/v3/v4 |
| T-2 到 T-0 | 投稿检查 | 匿名版、supp、代码/项目页、引用检查 |

---

## 2. 论文正文写法：每一节都要回答固定问题

本章参考你给的论文写作资料的核心逻辑：先画清楚 pipeline，先搭 story，再写 Introduction / Method / Experiments，最后写 Abstract 和 Title；写完后要像 reviewer 一样反复审自己。这里不照搬模板，而是整理成组内可以直接使用的正文写作规范。

> [!IMPORTANT]
> 正文写作最重要的不是英文华丽，而是每一节都有明确任务：读者读完这一节，应该更相信你的问题、方法或证据。

### 2.1 正文写作总原则

| 原则 | 具体含义 | 写作重点 |
|---|---|---|
| 先让 reader 读懂 | 每一段只解决一个问题 | 段首说明目的，段尾给出结论 |
| 先让 reviewer 信服 | 每个强 claim 都要有实验或分析支撑 | Abstract 和 Introduction 的 claim 最危险 |
| 先让图表讲故事 | teaser、pipeline、表格、可视化决定第一印象 | 图题和 caption 要直接写结论 |
| 先自我 review | 写完后主动问 reviewer 会质疑什么 | 把可能被拒的点提前修掉 |
| 反复打磨 | 初稿只负责讲清楚，后续再追求漂亮 | 不要在 story 不清楚时过早润色句子 |

### 2.2 Title 和 Abstract

Title 和 Abstract 是读者的第一判断入口。Title 要让人一眼知道任务、方法和关键条件；Abstract 要在很短时间里讲清任务、困难、方法、证据和结论边界。

| 需要回答的问题 | 重点是什么 | 常见误区 |
|---|---|---|
| 研究什么任务 | 明确输入、输出、场景 | 标题太大，只写 “A Novel Framework” |
| 为什么难 | 写具体技术困难，不只写 challenging | gap 写得空泛，和方法没关系 |
| 方法核心是什么 | 写方法机制，不堆模块名 | 只说用了 diffusion / transformer / NeRF |
| 证据是什么 | 说明在哪些数据和实验上验证 | 只写 SOTA，不写证据范围 |
| 边界在哪里 | 不夸大实验不能证明的结论 | 把局部提升写成普遍解决 |

| 以 `Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination` 为例 | 可以学习什么 |
|---|---|
| `Under Unknown Illumination` 放在标题里 | 标题直接突出关键难点，而不是泛泛写 inverse rendering |
| 从 posed images 恢复 object materials | 摘要先讲输入输出，让任务清楚 |
| geometry、material、lighting 耦合 | 难点具体，不是空泛说任务很难 |
| albedo / specular diffusion priors | 方法和困难直接对应：用材质先验缓解歧义 |

**检查问题**：读完 Abstract，读者能否回答“你解决什么、为什么难、你怎么做、凭什么信、适用边界是什么”。

### 2.3 Introduction

Introduction 的任务是制造“必要性”：让 reviewer 觉得这篇论文不是可有可无，而是自然地从已有问题中长出来的。

| 段落 | 核心任务 | 重点 |
|---|---|---|
| 背景段 | 说明任务和应用价值 | 不要从大而空的领域历史开始 |
| 现有方法段 | 概括主流路线 | 按技术路线讲，不按论文年份罗列 |
| Gap 段 | 指出现有方法的具体失败模式 | gap 要能被实验或图像现象验证 |
| Insight 段 | 给出自己的关键观察 | insight 要能自然引出方法设计 |
| Method 段 | 简要说明方法如何利用 insight | 不展开细节，只讲核心机制 |
| Contribution 段 | 列贡献 | 每条贡献都要能追到证据 |

| 重点判断 | 好写法 | 不好写法 |
|---|---|---|
| gap 是否具体 | 未知光照下，材质颜色和阴影容易混淆 | Existing methods are inaccurate |
| insight 是否有用 | 材质分布可以作为先验约束反演过程 | We observe diffusion models are powerful |
| contribution 是否可验证 | 提出 albedo/specular priors，并通过 ablation 验证 | We propose a novel framework |

> [!IMPORTANT]
> Introduction 里的每一个强 claim 都要提前问：后文有没有实验、图或引用支撑？如果没有，就降级表述或补证据。

### 2.4 Method

Method 不是代码说明书，而是设计论证。读者关心的不是你代码怎么写，而是每个模块为什么必要、如何解决前文 gap、是否能被实验验证。

| 内容 | 需要讲清楚 | 重点 |
|---|---|---|
| Problem formulation | 输入、输出、符号、目标 | 先让读者知道问题被如何数学化 |
| Overview | pipeline 和信息流 | 一张图能否说明整体方法 |
| Module motivation | 为什么需要这个模块 | 每个模块都要对应一个困难或 insight |
| Module design | 模块如何工作 | 讲机制，不按代码函数顺序写 |
| Objective | loss 每项的作用 | 每个 loss 都要有语义和必要性 |
| Training / inference | 训练和测试流程 | 只写复现所需的关键步骤 |

| Method 写作检查 | 应该能回答 |
|---|---|
| 这个模块解决哪个问题 | 对应 Introduction 中哪个 gap |
| 为什么不用更简单方法 | 设计是否有必要 |
| 输入输出是什么 | 符号是否定义清楚 |
| 怎么证明它有用 | 是否有 ablation 或 analysis |

**常见误区**：把代码流程当 Method；堆公式但不解释每项作用；模块名很高级但没有动机；pipeline 图和正文符号不一致。

### 2.5 Implementation Details

Implementation Details 的任务是保证别人能复现你的实验，不是把所有代码细节都倒出来。

| 应该写 | 重点 |
|---|---|
| 网络结构关键参数 | 只写影响结果和复现的设置 |
| 训练配置 | optimizer、learning rate、batch size、iterations、hardware |
| 数据处理 | 分辨率、crop、mask、augmentation、采样策略 |
| 推理设置 | 测试时间、采样步数、后处理 |
| 公平性设置 | baseline 是否使用同样输入、同样数据、同样评价协议 |

**检查问题**：别人看到这节，能否复现主要实验？reviewer 能否判断 comparison 是公平的？

### 2.6 Experiments

Experiments 的任务不是展示“我做了很多实验”，而是用证据回答 reviewer 的疑问。

| 实验类型 | 回答的问题 | 重点 |
|---|---|---|
| Comparison | 是否比已有方法好 | 说明提升来自什么场景、什么指标 |
| Ablation | 每个模块是否必要 | 每个 ablation 对应一个 claim |
| Analysis | 方法为什么有效 | 用可视化、分场景、误差分析解释现象 |
| Failure cases | 方法边界在哪里 | 主动暴露失败，不要藏问题 |
| Efficiency | 代价是否可接受 | 时间、显存、参数量、推理速度 |

| 写实验段落时 | 应该这样组织 |
|---|---|
| 段首 | 这个实验想验证什么 claim |
| 中间 | 实验设置、对比对象、关键变量 |
| 结果 | 不只报数字，要解释数字说明什么 |
| 段尾 | 得出判断，并连接到下一组实验 |

> [!IMPORTANT]
> 表格不是结果解释。表格只呈现证据，正文必须告诉读者：最重要的数字是哪一个，为什么重要，支持了哪个 claim。

### 2.7 Related Work

Related Work 的任务是定位本文贡献，而不是证明自己读了很多论文。

| 写法 | 重点 |
|---|---|
| 按技术路线组织 | 每一类工作对应一种解决思路 |
| 先承认已有贡献 | 不要把相关工作写成“别人都不行” |
| 再说明本文区别 | 区别要和 gap / insight 对齐 |
| 少按年份罗列 | 年份不是逻辑，技术路线才是逻辑 |

**检查问题**：读完 Related Work，读者是否知道本文站在哪几条路线的交叉处，以及本文和每条路线的关键差异。

### 2.8 Conclusion

Conclusion 不是简单重复 Abstract，而是收束全文：本文解决了什么、靠什么解决、证据说明什么、还有什么边界。

| 应该写 | 不应该写 |
|---|---|
| 回到任务和核心 gap | 只说 proposed a novel method |
| 总结核心机制 | 重新罗列所有模块 |
| 概括主要证据 | 夸大没有验证的结论 |
| 说明局限和未来方向 | 写空泛 future work |

**好结论的感觉**：读者读完会觉得“这篇论文的贡献、证据和边界都收住了”。

### 2.9 自审修改

写完初稿后，要用 adversarial writing 的方式审自己：假设 reviewer 正在挑毛病，提前把问题修掉。

| 自审对象 | 必问问题 |
|---|---|
| Story | 读者能否顺着 Task-Gap-Insight-Method-Evidence 读下来 |
| Claim | 每个强 claim 是否都有证据 |
| Figure | teaser、pipeline、表格是否第一眼清楚 |
| Paragraph | 每段是否只讲一个问题 |
| Experiment | comparison / ablation / analysis 是否支撑主线 |
| Writing | 是否有空泛形容词，如 significant、effective、robust 但没有证据 |

> [!TIP]
> 好论文通常不是一次写出来的，而是反复 review、反复改出来的。导师和同学指出的问题越多，投稿后 reviewer 能抓住的问题通常越少。

---

## 3. 组会汇报：不要只报结果，要报判断

组会不是证明“我这周很忙”，而是让大家快速判断项目下一步怎么走。

低效汇报：

> 我试了 A，不 work；试了 B，好一点。

有效汇报：

> 我想验证 claim X，所以做了实验 A。结果说明模块 M 对数据集 D 有帮助，但在场景 S 失败。我目前判断失败原因是输入噪声破坏了假设 H，下一步要做实验 B 来确认。

### 3.1 推荐汇报结构

| 顺序 | 内容 | 必须回答 |
|---|---|---|
| 1 | 本周核心问题 | 这周最想验证什么 |
| 2 | 当前判断 | 现在相信什么，不确定什么 |
| 3 | 关键实验 | 为什么做这个实验 |
| 4 | 结果解释 | 结果支持还是反驳假设 |
| 5 | 失败与风险 | 失败说明了什么 |
| 6 | 下周计划 | 下一步优先做什么 |

### 3.2 每一页只讲一个判断

| 不推荐标题 | 推荐标题 |
|---|---|
| Experiment 1 | 模块 M 主要提升低光照场景 |
| Ablation Results | 去掉 specular prior 会导致高光估计不稳定 |
| Failure Cases | 几何误差会传播到材质恢复 |
| Next Week Plan | 下一步优先验证噪声是否破坏输入假设 |

> [!IMPORTANT]
> 每一页最好回答一个问题：为什么做这个实验、结果说明什么、下一步该怎么决策。

---

## 4. 参考文献规范：真实、完整、可追溯

![一条完整参考文献的结构](assets/reference_anatomy.svg)

> [!IMPORTANT]
> 本章示例均使用真实存在的文献。作者姓名可按目标格式缩写，作者过多时可使用 `et al.` 或“等”；会议名、期刊名、出版社、论文集名称等来源信息尽量写全。

### 4.1 完整参考文献应包含什么

| 字段 | 是否常用 | 说明 |
|---|---|---|
| 作者 | 必需 | 按目标格式列全、缩写、`et al.` 或“等” |
| 年份 | 必需 | 使用正式发表年份 |
| 题名 | 必需 | 论文、书、网页或数据集标题 |
| 来源 | 必需 | 期刊、会议、论文集、网站或预印本平台 |
| 卷号 / 期号 | 期刊常见 | 会议论文通常没有卷号 |
| 页码 / 文章编号 | 有则写 | 电子期刊可能只有文章编号 |
| DOI / URL | 强烈建议 | DOI 优先，网页保留访问日期 |

### 4.2 会议论文示例

IEEE / ACM 数字制：

`[1] A. Vaswani et al., "Attention Is All You Need," in Advances in Neural Information Processing Systems, 2017, pages 5998-6008.`

GB/T 7714 组内推荐：

`[2] MILDENHALL B, SRINIVASAN P P, TANCIK M, 等. NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis[C]//European Conference on Computer Vision. 2020: 405-421.`

### 4.3 期刊论文示例

IEEE / 数字制：

`[3] J. Jumper et al., "Highly accurate protein structure prediction with AlphaFold," Nature, volume 596, number 7873, pages 583-589, 2021, DOI: 10.1038/s41586-021-03819-2.`

APA 7：

`LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. Nature, 521(7553), 436-444. https://doi.org/10.1038/nature14539`

### 4.4 特殊情况

| 情况 | 处理方式 |
|---|---|
| 会议论文没有卷号 | 不写卷号；写会议全称、年份、页码或论文编号 |
| 期刊没有期号 | 有卷号写卷号，无期号可省略 |
| 没有页码 | 写文章编号，如 `aac4716` |
| 预印本 | 若已有正式版，优先引用正式版 |
| 数据集 | 优先引用数据集论文，不只写网址 |
| 软件 | 有论文引用论文；必要时补版本和 URL |
| 网页 | 写作者/机构、标题、网站名、URL、访问日期 |

### 4.5 BibTeX 建议

```bibtex
@inproceedings{mildenhall2020nerf,
  author    = {Mildenhall, Ben and Srinivasan, Pratul P. and Tancik, Matthew and Barron, Jonathan T. and Ramamoorthi, Ravi and Ng, Ren},
  title     = {NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis},
  booktitle = {European Conference on Computer Vision},
  year      = {2020},
  pages     = {405--421},
  doi       = {10.1007/978-3-030-58452-8_24}
}
```

> [!TIP]
> Zotero / BibTeX 中尽量保存完整作者信息，最终显示 `et al.` 交给模板、`.bst` 或 CSL 样式处理。

---

## 5. 符号与字母规范：让公式可读

### 5.1 字体约定

| 对象 | 推荐写法 | 示例 |
|---|---|---|
| 标量 | 小写斜体 | $x, y, t, \lambda$ |
| 向量 | 小写粗体 | $\mathbf{x}, \mathbf{v}, \mathbf{n}$ |
| 矩阵 | 大写粗体 | $\mathbf{K}, \mathbf{R}, \mathbf{T}$ |
| 图像 / 张量 | 粗体大写 | $\mathbf{I}, \mathbf{F}$ |
| 集合 | 花体 | $\mathcal{D}, \mathcal{P}$ |
| 损失函数 | 花体 L | $\mathcal{L}_{\mathrm{rec}}$ |
| 网络参数 | 希腊字母 | $\theta, \phi$ |

---

## 6. 投稿前检查：少犯低级错误

| 检查项 | 问题 |
|---|---|
| Story | 3 分钟能否讲清任务、gap、insight、method、evidence |
| Claim | Abstract / Introduction 中的强 claim 是否都有证据 |
| Method | 每个模块是否说明动机、设计、优势和验证方式 |
| Experiments | comparison、ablation、analysis、failure cases 是否完整 |
| Figures | 图和 caption 是否能独立传达结论 |
| References | 文献是否真实、完整、格式统一 |
| Notation | 符号是否第一次出现即定义，全文一致 |
| Submission | 匿名、页数、模板、supp、代码链接是否合规 |

---

## 来源与参考

- 彭思达老师 Learning Research 仓库：<https://github.com/pengsida/learning_research>
- 论文写作参考资料：<https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e>
- Research Paper Writing Skills 结构化仓库：<https://github.com/Master-cai/Research-Paper-Writing-Skills>
- APA Style 官方参考文献指南：<https://apastyle.apa.org/style-grammar-guidelines/references>
- IntrinsicAnything / Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination：<https://arxiv.org/abs/2404.11593>
- Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination, IEEE Transactions on Pattern Analysis and Machine Intelligence：<https://doi.org/10.1109/TPAMI.2026.3650770>
- Attention Is All You Need 论文页：<https://proceedings.neurips.cc/paper/7181-attention-is-all-you-need>
- NeRF 论文记录：<https://par.nsf.gov/biblio/10301170-nerf-representing-scenes-neural-radiance-fields-view-synthesis>
- AlphaFold 期刊论文：<https://www.nature.com/articles/s41586-021-03819-2>

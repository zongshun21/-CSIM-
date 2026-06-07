<div align="center">

# 科研论文写作与参考文献规范

### 实验室新人科研写作训练手册

把科研经验从“口口相传”沉淀为可复用、可检查、可迭代的书面规范。

![Knowledge Base](https://img.shields.io/badge/Knowledge%20Base-Research%20Writing-2f4858)
![Reference Standard](https://img.shields.io/badge/Reference%20Style-GB%2FT%207714%20%2B%20Submission%20Style-5f7f71)
![For Lab Training](https://img.shields.io/badge/Audience-Lab%20Newcomers-8a6f4d)

</div>

---

## 目录

> [!TIP]
> 目录对齐到二级内容：先定位五个主模块，再直接跳到每个模块下最常用的小节。组内培训、开题、中期、组会、投稿前自查都可以从这里进入。

| 主模块 | 二级内容 | 跳转 |
|---|---|---|
| **1. 手册总览** | 科研写作训练什么；核心读者；最重要的写作原则 | [进入](#1-手册总览科研写作到底在训练什么) |
| **2. 从项目到论文** | [先讲 story](#21-先讲-story再写句子) · [推荐写作顺序](#22-推荐写作顺序) · [一个月倒排计划](#23-截稿前一个月倒排计划) · [组会汇报](#24-组会时不要只报结果要报判断) | [进入](#2-从项目到论文少走弯路的完整工作流) |
| **3. 论文正文写法** | [Title 和 Abstract](#31-title-和-abstract最后写但决定第一印象) · [Introduction](#32-introduction把-reviewer-带到这篇论文必须存在的位置) · [Method](#33-method不是代码说明书而是设计论证) · [Experiments](#34-experiments用证据回答质疑) · [Related Work 和 Conclusion](#35-related-work-和-conclusion定位贡献收束边界) | [进入](#3-论文正文怎么写title-到-conclusion-的统一方法) |
| **4. 参考文献规范** | [完整字段](#41-完整参考文献应该包含什么) · [会议论文](#42-会议论文标准实例) · [期刊论文](#43-期刊论文标准实例) · [组内 GB/T 7714](#44-组内参考文献规范中文-gbt-7714-风格) · [特殊情况](#45-特殊情况怎么处理) · [BibTeX](#46-bibtex-字段建议) · [最终检查](#47-参考文献最终检查) | [进入](#4-参考文献规范字段格式实例与特殊情况) |
| **5. 知识库落地** | [页面结构](#51-推荐页面结构) · [推荐数据库](#52-推荐数据库) · [可复制模板](#53-可复制模板) · [新人训练路径](#54-新人训练路径) | [进入](#5-知识库落地方式数据库模板和检查清单) |

---

![科研论文写作飞轮](assets/paper_writing_flywheel.svg)

## 1. 手册总览：科研写作到底在训练什么

科研写作不是把实验结果翻译成英文，也不是把所有工作细节堆进 PDF。科研写作的本质是：让读者相信你发现了一个值得解决的问题，并且你提出的方法确实带来了可靠的新知识。

一篇论文至少要讲清四件事：

| 核心问题 | 新人常见误区 | 正确写法 |
|---|---|---|
| 研究什么 | 只说技术名，不说任务和场景 | 先定义任务，再说明应用价值 |
| 为什么重要 | 用大而空的背景铺垫 | 说明旧方法在具体场景下哪里失败 |
| 你做了什么 | 按代码顺序介绍模块 | 按“问题-动机-设计-优势”介绍方法 |
| 凭什么相信 | 只放一张主结果表 | 用 comparison、ablation、analysis、failure cases 支撑 claim |

> [!IMPORTANT]
> 新人写作优先级：先让 story 成立，再让段落清楚，最后才是润色句子。不要在 story 还没讲通时过早打磨英文。

写论文时要一直记住两类读者：快速浏览的 reviewer 和认真追问的 reviewer。前者用标题、摘要、teaser、表格判断论文是否清楚可信；后者会追问每个 claim 是否有证据、方法是否必要、实验是否公平。

![Claim 与 Evidence 对齐图](assets/claim_evidence_alignment.svg)

---

## 2. 从项目到论文：少走弯路的完整工作流

### 2.1 先讲 story，再写句子

很多新人写论文会从 Method 开始，因为 Method 看起来最像“我实际做了什么”。但真正高效的写作顺序是：先把论文 story 梳理清楚，再写各部分。

| 问题 | 你需要写出的答案 |
|---|---|
| Task 是什么 | 我们研究的问题是什么，输入输出是什么 |
| Application 是什么 | 这个问题为什么在真实应用或科学问题中重要 |
| Existing methods 怎么做 | 现有方法的主要路线是什么 |
| Gap 在哪里 | 现有方法在什么条件下不够好 |
| Insight 是什么 | 我们观察到了什么关键事实或结构 |
| Method 怎么利用 insight | 我们的方法如何把 insight 变成技术方案 |
| Contribution 是什么 | 相比已有工作，新增价值是什么 |
| Evidence 是什么 | 哪些实验或分析支撑上述贡献 |

> [!TIP]
> 判断 story 是否成熟的简单方法：不看图、不看代码，只用 3 分钟能否讲清“问题为什么重要、旧方法为什么不够、我们为什么有效”。

### 2.2 推荐写作顺序

| 顺序 | 任务 | 为什么先做 |
|---|---|---|
| 1 | 画 pipeline 草图 | 先验证方法能否被清楚解释 |
| 2 | 梳理 Introduction 思路 | 确定论文卖点和实验需求 |
| 3 | 设计 comparison 和 ablation | 避免写完才发现 claim 没证据 |
| 4 | 写 Method 初稿 | 把模块动机、设计和优势讲清 |
| 5 | 同步补实验和改 Method | 方法描述和实验结果互相校准 |
| 6 | 写 Experiments | 用证据回答 reviewer 问题 |
| 7 | 美化 teaser、pipeline、表格 | 强化第一印象和可读性 |
| 8 | 写 Related Work | 根据 story 组织相关工作 |
| 9 | 写 Abstract 和 Title | 最后浓缩整篇论文 |
| 10 | 自审和导师 review | 提前暴露拒稿风险 |

### 2.3 截稿前一个月倒排计划

| 时间 | 核心目标 | 必须产出 | 负责人应检查 |
|---|---|---|---|
| T-30 到 T-24 | story 成型 | pipeline 草图、Introduction 大纲、实验矩阵 | 3 分钟能否讲清贡献 |
| T-23 到 T-18 | 方法成型 | Method v1、核心结果表、初版消融 | 每个模块是否必要 |
| T-17 到 T-12 | 证据成型 | comparison、ablation、analysis、可视化 | claim 是否都有证据 |
| T-11 到 T-7 | 初稿完整 | Related Work、Abstract、Title、完整 PDF | 读者是否能顺着故事读 |
| T-6 到 T-3 | 反复修改 | review issue list、v2/v3/v4 | 高风险问题是否已修复 |
| T-2 到 T-0 | 投稿检查 | 匿名版、supp、代码/项目页、引用检查 | 格式、页数、引用、图表是否合规 |

### 2.4 组会时不要只报结果，要报判断

低效汇报：“我试了 A，不 work；试了 B，好一点。”

有效汇报：“我想验证 claim X，所以做了实验 A。结果说明模块 M 对数据集 D 有帮助，但在场景 S 失败。我目前判断失败原因是输入噪声破坏了假设 H，下一步要做实验 B 来确认。”

> [!IMPORTANT]
> 组会汇报不是流水账，而是训练科研判断。每一页最好回答一个问题：我为什么做这个实验、结果说明什么、下一步该怎么决策。

---

## 3. 论文正文怎么写：Title 到 Conclusion 的统一方法

> [!IMPORTANT]
> 本章的“反例”不是批评原论文质量。很多经典论文因为时代、领域、期刊类型或作者声誉不同，可以使用非常简洁或非常宏观的写法；但实验室新人投稿时，不能直接模仿这些写法。我们要学习的是：什么写法适合自己的论文，什么写法只适合特定语境。

### 3.1 Title 和 Abstract：最后写，但决定第一印象

Title 的任务是让读者一眼知道任务和贡献。标题不要只有模型名字，也不要为了高级感牺牲可理解性。Abstract 的任务不是“压缩全文”，而是让 reviewer 在 30 秒内知道：研究对象、现有问题、核心方法、主要证据和结论边界。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 标题是否说明任务 | 读者只看标题，是否知道研究对象是什么 |
| 标题是否说明贡献 | 标题里是否能看到方法、机制、性质或目标 |
| 摘要是否有证据 | 摘要里的性能、效率、鲁棒性 claim 是否能在实验中找到对应结果 |
| 摘要是否过度承诺 | 是否用了 revolutionary、universal、always、solves 等过强表达 |

#### 真实合格例子

| 论文 | 可学习之处 | 为什么符合条件 |
|---|---|---|
| Vaswani et al., **Attention Is All You Need**, 2017 | 标题短，但直接点出核心论点：用 attention 替代循环结构 | 标题不是模型名堆砌，而是把论文最强的设计主张写出来；摘要进一步交代 Transformer、机器翻译任务和 BLEU 证据 |
| Mildenhall et al., **NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis**, 2020 | 标题包含方法名、表示方式和任务 | 新人可以直接学习这种结构：`方法名: 核心表示/机制 for 任务`，读者一眼知道论文做 view synthesis |
| Ioffe and Szegedy, **Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift**, 2015 | 标题同时说明技术、目标和假设 | 不是只写 “Batch Normalization”，而是说明它要加速训练，并给出作者认为的机制解释 |

#### 不宜直接模仿的真实例子

| 论文 | 为什么不宜直接模仿 | 新人应如何改 |
|---|---|---|
| LeCun, Bengio and Hinton, **Deep Learning**, 2015 | 这是 Nature 综述文章，标题可以极其宏观；普通方法论文如果也叫 “Deep Learning for X”，会显得贡献模糊 | 改成 `具体任务 + 具体方法 + 具体贡献`，例如 `Robust [Task] via [Mechanism]` |
| Shannon, **A Mathematical Theory of Communication**, 1948 | 这是奠基性理论论文，标题宏大但历史语境特殊；新人论文不能轻易使用 “A Theory of ...” 这种范围很大的标题 | 如果只是提出一个模型或算法，应写清应用边界，如 `A [Specific] Model for [Specific Task]` |

> [!TIP]
> 好标题不是越短越好，而是“短到没有废词，清楚到不会误解”。如果标题删掉任务名以后仍然像口号，就需要重写。

#### 摘要写法示例

以 `Attention Is All You Need` 为例，它的摘要可以拆成：旧路线依赖 recurrence/convolution → 提出完全基于 attention 的 Transformer → 在机器翻译任务上给出结果 → 说明训练成本和效果。这个结构值得学，因为它不是先讲实现细节，而是先说明为什么需要新架构，再给证据。

反例模式是：摘要第一句写大背景，第二句说“现有方法存在不足”，第三句突然说“本文提出一种新方法”，但不说明不足具体是什么，也不给核心证据。这样的摘要即使语法正确，也会让 reviewer 觉得 claim 没落地。

### 3.2 Introduction：把 reviewer 带到“这篇论文必须存在”的位置

Introduction 的核心不是“介绍背景”，而是“制造必要性”。读者读完 Introduction 后，应该自然接受三个判断：这个问题重要，旧方法确实不够，本文方法正好解决这个缺口。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 第一段是否定义了任务 | 是否说清输入、输出、场景和评价目标 |
| 背景是否服务于 gap | 每一句背景是否都在把读者推向本文问题 |
| gap 是否具体 | 是否能指出旧方法在什么数据、假设、场景或限制下失败 |
| contribution 是否可验证 | 每条贡献是否能对应到方法设计或实验结果 |

#### 真实合格例子

| 论文 | Introduction 可学习点 | 解释 |
|---|---|---|
| **NeRF**, 2020 | 从新视角合成任务出发，逐步引出传统表示和神经表示的限制，再提出连续 5D radiance field 表示 | 它没有先堆所有 3D 视觉背景，而是围绕“如何从多张图合成新视角”组织问题 |
| **Highly accurate protein structure prediction with AlphaFold**, 2021 | 先说明蛋白质结构预测的科学重要性，再用 CASP14 等评测语境说明突破性证据 | 它的必要性来自长期科学问题和清晰 benchmark，不是空泛地说“这个方向很重要” |
| **Batch Normalization**, 2015 | 先指出深层网络训练困难，再把 internal covariate shift 作为具体假设和切入点 | 它把“训练难”变成一个可讨论、可设计、可实验验证的问题 |

#### 不宜直接模仿的真实例子

| 论文 | 为什么不宜直接模仿 | 新人应如何处理 |
|---|---|---|
| **Deep Learning**, 2015 | 作为综述，它需要从很大范围介绍 representation learning；但普通投稿如果也从整个人工智能历史写起，会显得铺垫过宽 | 背景只写到足以解释你的 gap，不要把 Introduction 写成领域综述 |
| **A Mathematical Theory of Communication**, 1948 | 理论奠基论文可以从非常基础的概念定义开始；应用型或方法型论文如果这样写，容易迟迟不进入问题 | 新人论文第一段应尽快进入任务、应用场景和现有方法限制 |

#### 推荐段落骨架

| 段落 | 目标 | 常用句子功能 |
|---|---|---|
| 第 1 段 | 定义任务和价值 | 这个任务是什么；为什么值得研究 |
| 第 2 段 | 说明已有路线 | 现有方法大致分成哪几类 |
| 第 3 段 | 提出具体缺口 | 它们在什么条件下失败，为什么失败 |
| 第 4 段 | 引出本文 insight | 我们观察到什么，为什么它能解决 gap |
| 第 5 段 | 总结方法和贡献 | 本文提出什么，实验证明什么 |

> [!WARNING]
> Introduction 最常见的问题不是英文差，而是 gap 太虚。`existing methods are limited` 不是 gap；`existing methods fail under sparse-view input because ...` 才是 gap。

### 3.3 Method：不是代码说明书，而是设计论证

Method 的读者不是来复现每一行代码的，而是来判断你的设计是否合理、必要、可复现。写 Method 时不要按代码文件顺序写，而要按“设计问题”组织。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 模块是否都有动机 | 每个模块前是否解释它解决什么问题 |
| 公式是否服务于理解 | 公式后是否解释变量、输入输出和直觉 |
| pipeline 是否闭环 | 读者是否能从输入一路跟到输出 |
| 实现细节是否分层 | 关键设计在正文；超参数、网络层数、训练细节可放 implementation details |

#### 真实合格例子

| 论文 | Method 可学习点 | 解释 |
|---|---|---|
| **NeRF**, 2020 | 把场景表示成连续 5D 函数：输入位置和视角，输出密度和颜色，再通过体渲染得到图像 | 这是非常清晰的“输入-表示-渲染-监督”闭环，新人可以学习它如何把复杂方法讲成一条链 |
| **Attention Is All You Need**, 2017 | 先给整体 Transformer 架构，再分别解释 self-attention、multi-head attention、position-wise feed-forward 和 positional encoding | 它不是从代码类名开始写，而是从架构功能块开始写 |
| **Adam: A Method for Stochastic Optimization**, 2014 | 先定义优化目标和矩估计，再给算法步骤和性质说明 | 对算法论文来说，它把核心更新规则、变量意义和使用方式放在中心位置 |

#### 不宜直接模仿的真实例子

| 论文 | 为什么不宜直接模仿 | 新人应如何处理 |
|---|---|---|
| **Adam**, 2014 | 这类算法论文可以用很紧凑的数学定义推进；如果你的工作是系统、视觉或生物交叉任务，照搬这种高密度公式写法会让读者看不到设计动机 | 每个公式前先写“为什么需要这个量”，公式后写“它改变了什么行为” |
| **A Mathematical Theory of Communication**, 1948 | 理论论文可以长时间停留在定义和定理；方法论文如果这样写，reviewer 会找不到系统如何运行 | 方法论文应先给 pipeline，再展开必要的数学细节 |

#### 合格写法模板

| 层次 | 写法 |
|---|---|
| Overview | 先用一段话说明输入、输出、总流程和核心模块 |
| Module motivation | 每个模块开头先说明它为什么存在 |
| Module design | 解释计算过程、公式、网络结构或算法步骤 |
| Connection | 说明模块之间如何传递信息 |
| Complexity / implementation | 给出训练设置、复杂度、超参数或复现关键点 |

> [!TIP]
> Method 的好坏可以用一句话测试：读者不看代码，能不能画出你的 pipeline？如果画不出来，说明写法还没有闭环。

### 3.4 Experiments：用证据回答质疑

Experiments 的目标不是“展示我们做了很多实验”，而是回答 reviewer 最可能问的问题。每个实验都应该对应一个 claim：有效性、必要性、泛化性、鲁棒性、效率或边界。

#### 写前反思

| Reviewer 可能问什么 | 需要的证据 |
|---|---|
| 你真的比已有方法好吗 | 与强 baseline 的公平 comparison |
| 提出的模块真的必要吗 | ablation study |
| 方法什么时候失败 | failure cases 和边界分析 |
| 提升是否只是调参 | 同等训练预算、相同数据、相同评价协议 |
| 是否有实际代价 | 参数量、训练时间、推理速度、显存或计算量 |

#### 真实合格例子

| 论文 | Experiments 可学习点 | 解释 |
|---|---|---|
| **Attention Is All You Need**, 2017 | 用机器翻译结果证明主效果，并用模型变体分析 attention head、模型规模等因素 | 主结果回答“是否有效”，消融回答“为什么有效/哪些设计重要” |
| **NeRF**, 2020 | 在 synthetic 和 real forward-facing scenes 上与已有方法比较，并展示 view-dependent appearance、positional encoding 等分析 | 它不只给一张主表，还用可视化和消融解释核心设计为什么重要 |
| **Batch Normalization**, 2015 | 报告训练步数、准确率和不同模型设置下的表现 | 它把“加速训练”这个 claim 转化为可量化指标，而不只是说训练更稳定 |

#### 不宜直接模仿的真实例子

| 论文 | 为什么不宜直接模仿 | 新人应如何处理 |
|---|---|---|
| **Deep Learning**, 2015 | 综述文章主要综合已有证据，不承担单篇方法论文的实验验证任务 | 方法论文不能用综述式叙述替代自己的 comparison、ablation 和 analysis |
| **A Mathematical Theory of Communication**, 1948 | 理论论文的证据形式是定义、推导和定理，不一定有现代机器学习式实验 | 如果你的论文是实验驱动，就必须把 claim 落到数据集、指标和对照实验上 |

#### 实验组织模板

| 小节 | 作用 | 必须回答 |
|---|---|---|
| Experimental Setup | 说明数据、指标、baseline、实现细节 | 比较是否公平 |
| Main Results | 展示核心性能 | 方法是否有效 |
| Ablation Study | 去掉或替换关键模块 | 每个模块是否必要 |
| Analysis | 分析机制、鲁棒性、效率、泛化 | 为什么有效，边界在哪里 |
| Failure Cases | 展示失败样例 | 方法不能解决什么 |

> [!IMPORTANT]
> 不要让实验表格孤立存在。每张表后至少写一句“这张表支持了哪个 claim”。如果找不到对应 claim，这个实验可能不该放在正文。

### 3.5 Related Work 和 Conclusion：定位贡献，收束边界

Related Work 的任务不是证明你读了很多论文，而是把你的工作放到正确坐标系里。Conclusion 的任务也不是重复摘要，而是收束贡献、承认边界、指出下一步。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| Related Work 是否按问题组织 | 小节标题是否是技术路线或问题，而不是年份顺序 |
| 是否说明本文位置 | 每类工作后是否说明本文与它们的关系 |
| 是否避免贬低前人 | 是否把前人工作写成“都不行”，而没有具体条件 |
| Conclusion 是否有边界 | 是否说明方法适用范围和失败情况 |

#### 真实合格例子

| 论文 | 可学习点 | 解释 |
|---|---|---|
| **NeRF**, 2020 | Related Work 围绕 neural rendering、view synthesis、scene representation 等路线组织 | 它让读者知道本文在多个相关方向中的位置，而不是按年份罗列论文 |
| **Attention Is All You Need**, 2017 | 相关工作聚焦 sequence transduction、attention 和并行化训练背景 | 它把本文贡献定位为架构替代，而不只是又一个翻译模型 |
| **AlphaFold**, 2021 | Discussion/Conclusion 承认蛋白复合物、动态构象等边界，同时说明结构预测的科学意义 | 高水平论文不会假装解决所有问题，而是清楚说明能力边界 |

#### 不宜直接模仿的真实例子

| 论文 | 为什么不宜直接模仿 | 新人应如何处理 |
|---|---|---|
| **Deep Learning**, 2015 | 综述文章天然会覆盖大量历史脉络；普通方法论文如果这样写 Related Work，会挤占贡献和实验空间 | Related Work 只写与 gap 直接相关的路线，并解释差异 |
| **A Mathematical Theory of Communication**, 1948 | 奠基理论论文的结尾可以非常宏观；普通论文如果结尾只写愿景，会显得没有边界 | Conclusion 要回到本文证据：本文证明了什么，没有证明什么 |

#### 推荐写法

| 部分 | 建议 |
|---|---|
| Related Work 开头 | 说明本节按哪几条技术路线组织 |
| 每类工作 | 先概括共同思想，再列代表文献，最后说明和本文差异 |
| Conclusion 第一段 | 一句话回到任务和方法 |
| Conclusion 第二段 | 总结最重要的实验证据 |
| Conclusion 最后一段 | 说明局限、边界和未来方向 |

> [!WARNING]
> Related Work 最危险的写法是“张三做了 A，李四做了 B，王五做了 C”。这不是 related work，而是文献流水账。真正的 related work 要回答：这些工作共同解决什么问题，本文为什么仍然必要。

---

## 4. 参考文献规范：字段、格式、实例与特殊情况

![一条完整参考文献的结构](assets/reference_anatomy.svg)

> [!IMPORTANT]
> 本章所有示例均使用真实存在的文献。作者姓名按目标格式处理：可以缩写，作者过多时可以使用 `et al.` 或中文“等”。但文献题名、会议名称、期刊名称、出版社、论文集名称等来源信息尽量写全，不使用期刊或会议缩写。

### 4.1 完整参考文献应该包含什么

| 字段 | 含义 | 是否通常必需 | 说明 |
|---|---|---|---|
| 作者 | 谁写的 | 必需 | 按目标格式处理：列全、缩写、`et al.` 或“等” |
| 年份 | 何时发表 | 必需 | 在线优先和正式发表年份不同时，按目标格式处理 |
| 题名 | 文献标题 | 必需 | 论文题名、书名、数据集名、网页标题 |
| 来源 | 发表在哪里 | 必需 | 期刊名称、会议名称、论文集名称、书名、网站、预印本平台 |
| 卷号 volume | 期刊卷 | 期刊常见 | 会议论文通常没有卷号；不要为了整齐伪造卷号 |
| 期号 issue 或 number | 期刊期 | 期刊常见 | 有些期刊没有期号，可省略 |
| 页码 pages | 起止页 | 有则写 | 电子期刊可能使用文章编号而非页码 |
| 文章编号 article number | 替代页码 | 部分期刊常见 | 如 `aac4716`、`e105432`、Article 105432 |
| DOI | 持久标识符 | 强烈建议 | 有 DOI 时优先写 DOI |
| URL | 网页地址 | 网页、预印本、软件常见 | 无 DOI 时尤其重要 |
| 访问日期 | 何时访问网页 | 网页常见 | 稳定出版物通常不需要 |

### 4.2 会议论文标准实例

#### IEEE/ACM 数字制示例（作者较多时使用 et al.）

正文引用：

`The Transformer architecture replaces recurrence with self-attention mechanisms [1].`

参考文献：

`[1] A. Vaswani et al., "Attention Is All You Need," in Advances in Neural Information Processing Systems, 2017, pages 5998-6008.`

| 部分 | 内容 | 解释 |
|---|---|---|
| 作者 | A. Vaswani et al. | 作者较多时，IEEE/ACM 数字制中常用 `et al.` 截断 |
| 题名 | Attention Is All You Need | 论文题名完整保留 |
| 来源 | Advances in Neural Information Processing Systems | 会议论文集名称写全；组内规范中不写成 NeurIPS，也不把 “30” 当作会议名的一部分 |
| 年份 | 2017 | 正式发表年份 |
| 页码 | pages 5998-6008 | 有页码必须写 |

#### APA 7 示例（参考文献列表按 APA 规则列作者）

`Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017). Attention is all you need. In Advances in Neural Information Processing Systems (pp. 5998-6008).`

> [!NOTE]
> APA 7 的正文引用和参考文献列表规则不同。正文引用通常可写 `Vaswani et al. (2017)`；参考文献列表中，作者不超过 20 位时通常列出全部作者，超过 20 位时列前 19 位、加省略号、再列最后一位作者。

### 4.3 期刊论文标准实例

#### IEEE/数字制示例（作者很多时使用 et al.）

正文引用：

`AlphaFold demonstrates that deep learning can predict protein structures with high accuracy [2].`

参考文献：

`[2] J. Jumper et al., "Highly accurate protein structure prediction with AlphaFold," Nature, volume 596, number 7873, pages 583-589, 2021, DOI: 10.1038/s41586-021-03819-2.`

| 部分 | 内容 | 解释 |
|---|---|---|
| 作者 | J. Jumper et al. | 作者很多时使用 `et al.`，避免参考文献过长 |
| 期刊名称 | Nature | 期刊名称写全，不使用缩写 |
| 卷号 | volume 596 | 期刊卷号 |
| 期号 | number 7873 | 期刊期号；若期刊无期号则省略 |
| 页码 | pages 583-589 | 有页码必须写 |
| DOI | 10.1038/s41586-021-03819-2 | 真实 DOI，优先保留 |

#### APA 7 示例（作者较少的期刊论文）

`LeCun, Y., Bengio, Y., & Hinton, G. (2015). Deep learning. Nature, 521(7553), 436-444. https://doi.org/10.1038/nature14539`

### 4.4 组内参考文献规范（中文 GB/T 7714 风格）

> [!IMPORTANT]
> 组内开题、中期、结题、组会汇报、项目文档等场合，建议统一使用本节的 GB/T 7714 风格规范，便于中文语境下阅读和管理。正式投稿时必须以目标会议、期刊、学校或出版社模板要求为准，不要用组内规范替代投稿格式。

顺序编码制常见写法：

`[序号] 作者. 题名[文献类型标识]. 来源, 年, 卷(期): 起止页码.`

真实期刊示例：

`[1] JUMPER J, EVANS R, PRITZEL A, 等. Highly accurate protein structure prediction with AlphaFold[J]. Nature, 2021, 596(7873): 583-589.`

真实会议示例（组内汇报推荐写法）：

`[2] MILDENHALL B, SRINIVASAN P P, TANCIK M, 等. NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis[C]//European Conference on Computer Vision. 2020: 405-421.`

字段解释：

| 字段 | 示例 | 说明 |
|---|---|---|
| `[2]` | 文献序号 | 正文中用 `[2]` 对应引用 |
| 作者 | `MILDENHALL B, SRINIVASAN P P, TANCIK M, 等` | 中文 GB/T 风格常用姓在前、名缩写；作者多时用“等” |
| 题名 | `NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis` | 题名完整保留 |
| 类型标识 | `[C]` | conference paper，会议论文 |
| 会议名称 | `European Conference on Computer Vision` | 组内规范写会议全称，不写 ECCV 缩写 |
| 年份 | `2020` | 会议论文正式发表年份 |
| 页码 | `405-421` | 有起止页码时必须写；没有页码时写文章编号或 DOI |

### 4.5 特殊情况怎么处理

| 情况 | 处理方式 | 真实示例 |
|---|---|---|
| 会议论文没有卷号 | 不写卷号；写完整会议名称、年份、页码或论文编号 | Mildenhall 等的 NeRF 会议论文写 `European Conference on Computer Vision. 2020: 405-421`，不写 volume |
| 期刊有卷号和期号 | 写期刊名称、volume、number、pages、DOI | Jumper et al. 的 Nature 论文：volume 596, number 7873, pages 583-589 |
| 期刊有文章编号而非页码 | 用文章编号替代页码，不要伪造页码 | Open Science Collaboration, “Estimating the reproducibility of psychological science,” Science, volume 349, number 6251, article aac4716, 2015, DOI: 10.1126/science.aac4716 |
| 预印本 | 写预印本平台和编号；若已有正式发表版本，优先引用正式版本 | Pumarola et al., “D-NeRF: Neural Radiance Fields for Dynamic Scenes,” arXiv preprint arXiv:2011.13961, 2020 |
| 数据集论文 | 按会议或期刊论文引用，不能只写数据集网址 | Lin et al., “Microsoft COCO: Common Objects in Context,” in European Conference on Computer Vision, 2014, pages 740-755 |
| 软件论文 | 如果软件有论文，优先引用论文；必要时同时给版本和网址 | Harris et al., “Array programming with NumPy,” Nature, volume 585, number 7825, pages 357-362, 2020, DOI: 10.1038/s41586-020-2649-2 |
| 网页 | 写机构或作者、网页标题、网站名、URL、访问日期 | American Psychological Association, “References,” APA Style, https://apastyle.apa.org/style-grammar-guidelines/references, accessed 2026-06-07 |
| 标准 | 写发布机构、标准号、标准名、年份 | National Information Standards Organization, ANSI/NISO Z39.29-2005, Bibliographic References, 2005 |

### 4.6 BibTeX 字段建议

> [!IMPORTANT]
> BibTeX / Zotero / EndNote 中建议尽量保存完整作者数据；真正显示在论文里的作者截断规则，应交给期刊模板、会议模板、`.bst` 文件或 CSL 样式处理。不要为了显示 `et al.` 就随意删除数据库中的作者字段。

会议论文真实示例：

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

文章编号真实示例：

```bibtex
@article{openScienceCollaboration2015estimating,
  author  = {{Open Science Collaboration}},
  title   = {Estimating the reproducibility of psychological science},
  journal = {Science},
  year    = {2015},
  volume  = {349},
  number  = {6251},
  pages   = {aac4716},
  doi     = {10.1126/science.aac4716}
}
```

### 4.7 参考文献最终检查

- 正文引用和参考文献列表是否一一对应。
- 是否引用了数据集、baseline、评价指标、工具库和理论来源。
- 是否优先引用正式发表版本，而不是只引用预印本。
- 作者名是否按目标格式处理；来源信息是否写全。
- DOI、URL、页码、文章编号、卷期号是否放在正确字段。
- 组内开题、中期、组会文档是否使用统一 GB/T 7714 风格；正式投稿是否切换为目标模板要求。

---

## 5. 知识库落地方式：数据库、模板和检查清单

建议把这个手册作为实验室“科研训练”或“论文写作规范”的首页。页面不要拆得太碎，采用一个主页面加几个数据库即可。

### 5.1 推荐页面结构

| 模块 | 内容 |
|---|---|
| 顶部说明 | 手册目的、适用对象、核心原则 |
| 目录 | 5 个大章节，支持点击跳转 |
| 图示区 | 写作飞轮、claim-evidence 图、参考文献结构图 |
| 正文区 | 本手册主体 |
| 模板区 | Paper Card、Story Outline、Claim-Evidence Map |
| 数据库区 | 项目、文献、实验、review issue |

### 5.2 推荐数据库

| 数据库 | 字段 |
|---|---|
| Paper Projects | 项目名、负责人、阶段、目标会议、deadline、当前版本、风险等级 |
| Literature Bank | 标题、作者、年份、类型、方向、BibTeX、精读状态、与项目关系 |
| Experiment Log | 日期、实验目的、配置、结果、结论、失败原因、下一步 |
| Claim-Evidence Map | claim、出现位置、证据、状态、负责人、处理方式 |
| Review Issues | 问题、来源、严重程度、对应章节、解决状态、修改记录 |

### 5.3 可复制模板

| 模板 | 用途 |
|---|---|
| Paper Card | 记录论文问题、方法、实验、局限和可借鉴写法 |
| Story Outline | 记录 Task、Application、Gap、Insight、Method、Contribution、Evidence |
| Claim-Evidence Map | 检查每个 claim 是否有实验、引用、理论或分析支撑 |
| Reviewer 自审清单 | 投稿前从 contribution、writing、experiments、method、references、presentation 六个维度自查 |

### 5.4 新人训练路径

| 周次 | 训练目标 | 交付物 |
|---|---|---|
| Week 1 | 学会读论文 | 3 篇 Paper Card |
| Week 2 | 学会看方法 | 1 张 pipeline 重画图 |
| Week 3 | 学会组织 story | 1 份 Introduction reverse outline |
| Week 4 | 学会做证据表 | 1 份 Claim-Evidence Map |
| Week 5 | 学会自审 | 1 份 reviewer-style review |
| Week 6 | 学会写 mini paper | 4 页项目短论文 |

---

## 来源与参考

- 彭思达老师 Learning Research 仓库：<https://github.com/pengsida/learning_research>
- 原始论文写作模板：<https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e>
- Research Paper Writing Skills 结构化仓库：<https://github.com/Master-cai/Research-Paper-Writing-Skills>
- APA Style 官方参考文献指南：<https://apastyle.apa.org/style-grammar-guidelines/references>
- Attention Is All You Need 论文页：<https://proceedings.neurips.cc/paper/7181-attention-is-all-you-need>
- NeRF 论文记录：<https://par.nsf.gov/biblio/10301170-nerf-representing-scenes-neural-radiance-fields-view-synthesis>
- AlphaFold 期刊论文：<https://www.nature.com/articles/s41586-021-03819-2>
- Deep Learning 综述论文：<https://www.nature.com/articles/nature14539>
- Batch Normalization 论文页：<https://proceedings.mlr.press/v37/ioffe15>
- Adam 论文页：<https://arxiv.org/abs/1412.6980>
- A Mathematical Theory of Communication 论文页：<https://onlinelibrary.wiley.com/doi/abs/10.1002/j.1538-7305.1948.tb01338.x>

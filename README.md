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
> 本章的正例以 `Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination` / `IntrinsicAnything` 的论文内容为主要分析对象。反例不是来自某篇真实论文，而是根据正例反推出的常见错误写法，目的是帮助新人理解“同一个研究点写好和写坏的差别”。

### 3.1 Title 和 Abstract：最后写，但决定第一印象

Title 的任务是让读者一眼知道任务、核心方法和关键条件。Abstract 的任务不是“压缩全文”，而是让 reviewer 在 30 秒内知道：研究对象、现有问题、核心方法、主要证据和结论边界。

#### 从 IntrinsicAnything 学到的正例

| 写作点 | 正例做法 | 为什么好 |
|---|---|---|
| 标题同时给任务和条件 | `Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination` | 标题不只说 inverse rendering，还强调 unknown illumination，这是论文困难来源和卖点所在 |
| 摘要先定义任务 | 任务是从未知静态光照下拍摄的 posed images 中恢复 object materials | 读者一开始就知道输入、输出和问题场景 |
| 摘要给出具体 gap | 困难来自 geometry、materials、environment lighting 的耦合，导致 inverse rendering 存在歧义 | gap 不是“现有方法不好”，而是解释了为什么问题本质上 ill-posed |
| 摘要给出方法核心 | 用 generative model 学习 material prior，并把 albedo 和 specular 分别建模为 diffusion priors | 方法不是泛泛的“提出网络”，而是和物理分解、材质歧义直接对应 |
| 摘要给出证据范围 | 在 real-world 和 synthetic datasets 上验证 material recovery 性能 | claim 有实验范围，不是无边界承诺 |

#### 由正例反推的反例

| 不推荐写法 | 问题 | 如何改 |
|---|---|---|
| `A Novel Diffusion Framework for 3D Vision` | 标题太宽，读者不知道是 inverse rendering、material recovery、relighting 还是 reconstruction | 写清任务和条件：`Diffusion Material Priors for Inverse Rendering under Unknown Illumination` |
| `Existing inverse rendering methods are inaccurate. We propose a diffusion model.` | gap 没有解释为什么不准，方法也没有和问题建立关系 | 写成：由于材质、几何和光照耦合，优化会把 shading 或 shadow 错当成 albedo，因此需要 material prior 约束 |
| `Experiments show our method is state-of-the-art.` | 没有说明在哪些数据、哪些任务、哪些指标上成立 | 写清 real/synthetic datasets、material recovery、ablation 或 relighting 证据 |

> [!TIP]
> 好摘要不是把所有模块都列出来，而是让“问题为什么难”和“方法为什么正好解决它”连起来。IntrinsicAnything 的关键优点就在于 gap 和 method 是扣在一起的：歧义来自材质/光照/几何耦合，因此用材质先验来正则化优化。

### 3.2 Introduction：把 reviewer 带到“这篇论文必须存在”的位置

Introduction 的核心不是介绍背景，而是制造必要性。读者读完 Introduction 后，应该自然接受三个判断：这个问题重要，旧方法确实不够，本文方法正好解决这个缺口。

#### 从 IntrinsicAnything 学到的正例

| Introduction 层次 | 正例内容 | 写作作用 |
|---|---|---|
| 任务价值 | inverse rendering 要从图像中恢复 geometry、material、lighting，这对 VR/AR、电影制作、游戏等应用重要 | 先说明任务不是孤立技术，而是有明确应用价值 |
| 现实限制 | 早期方法依赖复杂采集系统、特殊硬件或受控环境 | 把读者带到更现实的问题：普通捕获条件下怎么做 |
| 现有路线 | 近期方法用 differentiable physically based rendering 和 neural scene representations 优化材质、几何、光照 | 说明作者理解当前主流技术路线 |
| 核心 gap | 单靠 rendering loss 不足，因为 diffuse shading 与 albedo、shadow 与 albedo 之间存在歧义 | gap 具体、可视化、可验证，不是泛泛说“精度不高” |
| 方法动机 | 学习 albedo 和 specular 的 generative priors，用来约束反演优化 | 方法从 gap 自然生长出来，不是突然出现 |

#### 由正例反推的反例

| 反例写法 | 为什么不好 | 正确思路 |
|---|---|---|
| “Inverse rendering is an important problem in computer vision and graphics. Recently, neural rendering has achieved great success.” | 太泛，无法解释本文为什么必须存在 | 应该尽快进入 unknown illumination 和 material ambiguity |
| “Previous methods cannot recover accurate materials.” | 没有说清失败机制 | 应该指出两类具体歧义：shading-albedo ambiguity 和 shadow-albedo ambiguity |
| “We use diffusion models because they are powerful generative models.” | 方法动机跟问题没扣紧 | 应该说明 diffusion priors 学到的 material distribution 如何帮助优化摆脱错误分解 |

#### 可复用写法模板

| 段落 | 写法 |
|---|---|
| 第 1 段 | 定义 inverse rendering 任务：输入 posed RGB images，目标恢复 materials / lighting / geometry，并说明应用价值 |
| 第 2 段 | 说明受控采集方法的限制，再引出现实场景 unknown illumination 的难度 |
| 第 3 段 | 概括 differentiable PBR 优化路线，并指出只靠 rendering loss 容易陷入歧义 |
| 第 4 段 | 用具体例子解释歧义：黄色光照会被误分解进 albedo，自遮挡阴影会被 baked into albedo |
| 第 5 段 | 引出 material diffusion priors、albedo/specular 分解和 coarse-to-fine training |

> [!WARNING]
> Introduction 里最重要的不是“背景大”，而是“缺口准”。如果缺口能被画成 Fig. 1 那样的具体失败模式，reviewer 会更容易相信方法设计是必要的。

### 3.3 Method：不是代码说明书，而是设计论证

Method 的读者不是来复现每一行代码的，而是来判断你的设计是否合理、必要、可复现。写 Method 时不要按代码文件顺序写，而要按“设计问题”组织。

#### 从 IntrinsicAnything 学到的正例

| Method 设计 | 正例逻辑 | 为什么好 |
|---|---|---|
| 先解释为什么需要 prior | inverse rendering 是 ill-posed，仅靠 rendering loss 会出现错误材质分解 | 模块不是凭空加的，而是服务于歧义消解 |
| prior 与物理分解对应 | 根据 rendering equation 可拆成 diffuse 和 specular shading，分别学习 albedo/specular diffusion priors | 方法设计和物理模型对齐，增强可信度 |
| 训练数据来源合理 | 使用大量 3D object data 构造 albedo/specular 训练数据 | 回答 diffusion prior 从哪里学、为什么能学 |
| 优化过程有闭环 | diffusion prior regularizes inverse rendering optimization，并通过 guided sampling 对齐 multi-view observations | 读者能看到 prior 如何进入任务，而不是只知道“用了 diffusion” |
| coarse-to-fine 训练有明确目的 | 先估计粗材质，再用它引导 diffusion models 满足多视角一致性 | 训练策略解决稳定性和一致性问题，不是单纯技巧堆叠 |

#### 由正例反推的反例

| 不推荐写法 | 问题 | 如何改 |
|---|---|---|
| “Our method contains a renderer, a diffusion model, and an optimizer.” | 像模块清单，没有说明模块为什么存在 | 按问题组织：渲染损失导致歧义，因此引入 material prior；prior 通过 albedo/specular diffusion 建模 |
| “We use a diffusion model to improve material recovery.” | diffusion model 的对象不清楚：学图像、光照、材质还是 residual？ | 写清楚 prior 学的是 albedo 和 specular 的分布，并解释它们和 rendering equation 的关系 |
| “We design a two-stage training scheme for better results.” | better results 太空，读者不知道为什么需要 two-stage | 写成 coarse material estimates 用来 guide diffusion，使 samples 满足 multi-view consistency |

#### Method 写作模板

| 层次 | 建议写法 |
|---|---|
| Overview | 先画出输入 posed images、geometry/material/light optimization、diffusion prior regularization、rendering loss 的整体流程 |
| Problem formulation | 定义要恢复的材质、光照和几何变量，说明 observation 是 RGB images |
| Ambiguity analysis | 解释为什么 rendering loss 无法唯一决定 albedo/specular/shading |
| Prior design | 说明 albedo prior 和 specular prior 分别建模什么，为什么和物理渲染方程对应 |
| Optimization / training | 解释 diffusion prior 如何参与优化，coarse-to-fine 如何提升多视角一致性 |

> [!TIP]
> Method 写得好的标志是：读者能回答“为什么这个模块非加不可”。如果一个模块只能被解释为“提升性能”，那它在论文叙事里还不够稳。

### 3.4 Experiments：用证据回答质疑

Experiments 的目标不是展示做了很多实验，而是回答 reviewer 最可能问的问题。每个实验都应该对应一个 claim：有效性、必要性、泛化性、鲁棒性、效率或边界。

#### 从 IntrinsicAnything 学到的正例

| Claim | 应有证据 | 这篇论文给我们的启发 |
|---|---|---|
| 方法能恢复更准确的材质 | real-world 和 synthetic datasets 上的 material recovery comparison | 主结果要覆盖不同数据来源，避免只在单一合成场景成立 |
| albedo prior 有必要 | 去掉 albedo prior 的 ablation | 消融要对应核心 claim，不能只消融无关超参数 |
| specular prior 有必要 | 去掉 specular prior 的 ablation | 如果方法声称 diffuse/specular 分解重要，就要分别验证 |
| guided / coarse-to-fine 策略有必要 | w/o guided 或相关训练策略的对比 | 训练策略不是附属细节，也需要证据支持 |
| 方法确实减少歧义 | 定性图展示 albedo、roughness、relighting 等结果 | 对 inverse rendering，视觉分解结果和 relighting 结果很重要，不能只看单一数值 |

#### 由正例反推的反例

| 不推荐实验 | 为什么不够 | 应该补什么 |
|---|---|---|
| 只给最终 material recovery 指标 | 无法证明 diffusion prior 是关键原因 | 加 w/o albedo prior、w/o specular prior、w/o guided strategy |
| 只在 synthetic dataset 上验证 | unknown illumination 和真实材质复杂性可能没有被验证 | 加 real-world 数据或真实采集结果 |
| 只展示好看的 relighting 图 | 容易被认为挑选样例 | 给失败样例、定量指标、与 baseline 的同场景对比 |
| ablation 名字只写 variant A/B/C | reviewer 不知道每个变体对应什么设计假设 | 变体命名应直接对应设计：w/o albedo prior、w/o specular prior、w/o guided sampling |

#### 表格后的解释示例

不推荐：

> Table 2 shows the ablation results. Our full model achieves the best performance.

推荐：

> Table 2 verifies the role of each prior in resolving material-lighting ambiguity. Removing the albedo prior causes the recovered base color to absorb illumination effects, while removing the specular prior weakens highlight and roughness estimation. The guided training variant further improves multi-view consistency, suggesting that the diffusion prior is most effective when it is constrained by image observations rather than used as an isolated generative model.

为什么更好：它不是复述表格，而是把每个实验变体和论文 claim 对齐。这样 reviewer 能看出 ablation 不是“凑实验”，而是在验证方法逻辑。

### 3.5 Related Work 和 Conclusion：定位贡献，收束边界

Related Work 的任务不是证明你读了很多论文，而是把你的工作放到正确坐标系里。Conclusion 的任务也不是重复摘要，而是收束贡献、承认边界、指出下一步。

#### 从 IntrinsicAnything 学到的正例

| 部分 | 正例思路 | 为什么好 |
|---|---|---|
| Related Work 组织 | 围绕 inverse rendering、material/lighting representation、diffusion priors for inverse problems 等路线组织 | 不是按年份堆论文，而是按“本文站在哪几条路线交叉处”组织 |
| 与已有工作区分 | 已有方法改进 geometry/material/light representation 或训练策略；本文强调 material prior regularization | 差异不是“我们效果更好”，而是“我们解决歧义的切入点不同” |
| Conclusion 收束 | 回到 unknown illumination 下的 material prior、albedo/specular diffusion models、coarse-to-fine training | 结论对应正文主线，没有散掉 |
| 局限表达 | 结果依赖已有几何重建质量，未来可学习 geometry prior | 局限具体且自然导向未来工作，不是空泛说 future work |

#### 由正例反推的反例

| 不推荐写法 | 问题 | 如何改 |
|---|---|---|
| “Many methods have studied inverse rendering. Some use neural rendering, some use diffusion models.” | 文献流水账，没有坐标系 | 按问题组织：capture constraints、differentiable inverse rendering、material priors、diffusion priors |
| “Our method is different from all previous methods.” | 过度割裂，容易显得不理解前人 | 说明本文继承 differentiable PBR 优化框架，但把贡献放在 material diffusion prior 上 |
| “Future work will improve the method.” | 没有边界信息 | 写清具体局限：几何误差会影响材质恢复，因此未来可以学习 geometry prior |

#### Conclusion 推荐写法

不推荐：

> In this paper, we propose a novel diffusion method for inverse rendering. Experiments show that our method is effective. In the future, we will improve the method.

推荐：

> This paper studies material recovery from posed images under unknown static illumination. To reduce the ambiguity between material, shading, and lighting, the method learns diffusion priors over albedo and specular components and uses them to regularize differentiable inverse rendering. Experiments and ablations should emphasize whether each prior resolves the corresponding ambiguity and whether the guided/coarse-to-fine strategy improves multi-view consistency. The conclusion should also state the boundary: if geometry is inaccurate, material recovery may still be affected, which naturally motivates future work on geometry priors.

为什么更好：它回到任务、方法、证据和边界。好的 conclusion 不会只说“有效”，而是说明“在哪个问题上有效、靠什么有效、还有什么没解决”。

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
- IntrinsicAnything / Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination：<https://arxiv.org/abs/2404.11593>
- Learning Diffusion Priors for Inverse Rendering Under Unknown Illumination, IEEE Transactions on Pattern Analysis and Machine Intelligence：<https://doi.org/10.1109/TPAMI.2026.3650770>
- Attention Is All You Need 论文页：<https://proceedings.neurips.cc/paper/7181-attention-is-all-you-need>
- NeRF 论文记录：<https://par.nsf.gov/biblio/10301170-nerf-representing-scenes-neural-radiance-fields-view-synthesis>
- AlphaFold 期刊论文：<https://www.nature.com/articles/s41586-021-03819-2>

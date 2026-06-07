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
> 本章例子集中在计算机视觉语境下，尤其是低层视觉、目标检测、语义分割、3D 视觉、新视角合成、多模态视觉等方向。正例和反例主要是为了解释写作观点而构造的教学样例，不对应评价某一篇具体论文。

### 3.1 Title 和 Abstract：最后写，但决定第一印象

Title 的任务是让读者一眼知道任务和贡献。Abstract 的任务不是“压缩全文”，而是让 reviewer 在 30 秒内知道：研究对象、现有问题、核心方法、主要证据和结论边界。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 标题是否说明任务 | 读者只看标题，是否知道是检测、分割、重建、增强、跟踪还是生成 |
| 标题是否说明贡献 | 标题里是否能看到方法机制、关键约束、目标性质或应用场景 |
| 摘要是否有证据 | 摘要里的精度、速度、鲁棒性、泛化 claim 是否能在实验中找到对应结果 |
| 摘要是否过度承诺 | 是否用了 universal、solves all、state-of-the-art on all settings 等过强表达 |

#### 视觉论文标题示例

| 类型 | 不推荐写法 | 推荐写法 | 为什么 |
|---|---|---|---|
| 低光增强 | `A Novel Network for Image Enhancement` | `Illumination-Aware Feature Fusion for Low-Light Image Enhancement` | 反例只说 novel network，任务和贡献都模糊；正例说明任务是 low-light enhancement，核心机制是 illumination-aware feature fusion |
| 语义分割 | `An Efficient Segmentation Method` | `Boundary-Guided Multi-Scale Features for Real-Time Semantic Segmentation` | 反例不知道分割什么、快在哪里；正例同时说明边界信息、多尺度特征和实时场景 |
| 3D 重建 | `A Better Reconstruction Framework` | `Geometry-Regularized Sparse-View 3D Reconstruction` | 反例像项目名；正例说明问题条件是 sparse-view，关键贡献是 geometry regularization |
| 新视角合成 | `Improving Neural Rendering` | `Occlusion-Aware Neural Rendering for Sparse-View Novel View Synthesis` | 正例把任务、难点和方法机制放进标题，读者能预判论文重点 |

#### 摘要示例

不推荐写法：

> Low-light image enhancement is important in computer vision. Existing methods still have many problems. In this paper, we propose a novel network. Experiments show that our method performs better than previous methods.

问题解释：这段摘要没有说明低光图像的具体困难是什么，也没有说明 novel network 到底 novel 在哪里；“performs better”没有指标、数据集或证据范围，reviewer 无法判断 claim 是否可信。

推荐写法：

> Low-light images often suffer from uneven illumination, amplified noise, and color distortion, which make restoration difficult in real-world scenes. Existing enhancement methods usually improve global brightness but fail to preserve local structure under spatially varying illumination. We propose an illumination-aware feature fusion framework that estimates coarse illumination maps and uses them to guide multi-scale restoration features. On paired and unpaired low-light benchmarks, the proposed method improves restoration quality while reducing over-exposure artifacts, and ablation studies show that illumination guidance contributes most to texture preservation.

为什么更好：它先定义视觉退化问题，再指出旧方法的具体失败点，然后给出方法机制，最后说明实验范围和主要证据。它没有空喊“novel”，而是把新意落在 illumination guidance 和 multi-scale restoration 上。

### 3.2 Introduction：把 reviewer 带到“这篇论文必须存在”的位置

Introduction 的核心不是“介绍背景”，而是“制造必要性”。读者读完 Introduction 后，应该自然接受三个判断：这个问题重要，旧方法确实不够，本文方法正好解决这个缺口。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 第一段是否定义了视觉任务 | 是否说清输入、输出、场景和评价目标 |
| 背景是否服务于 gap | 每一句背景是否都在把读者推向本文问题 |
| gap 是否具体 | 是否能指出旧方法在什么数据、假设、场景或限制下失败 |
| contribution 是否可验证 | 每条贡献是否能对应到方法设计或实验结果 |

#### 视觉论文 Introduction 反例模式

| 反例写法 | 问题 |
|---|---|
| “随着深度学习的发展，计算机视觉取得了巨大成功。” | 太泛，几乎任何视觉论文都能用，不能导向你的具体问题 |
| “现有方法仍然存在精度不高、鲁棒性差的问题。” | gap 太虚，没有说明在哪些条件下不高、不鲁棒 |
| “本文提出一种新网络，主要贡献如下。” | 方法突然出现，前文没有把读者推到“必须提出它”的位置 |

#### 视觉论文 Introduction 推荐写法

以“稀疏视角新视角合成”为例：

| 段落 | 推荐内容 | 写作目的 |
|---|---|---|
| 第 1 段 | 定义 sparse-view novel view synthesis：输入少量已知视角，输出未观测视角图像；说明它对移动端采集、机器人感知、虚拟内容生成的重要性 | 让读者知道任务是什么，为什么值得研究 |
| 第 2 段 | 概括已有路线：显式几何、多视图匹配、神经辐射场、泛化式渲染模型 | 证明你理解领域地图 |
| 第 3 段 | 指出具体 gap：视角很少时几何约束不足，网络容易把遮挡区域 hallucinate 成错误纹理 | 把问题从“大方向”收紧到本文要解决的失败条件 |
| 第 4 段 | 引出 insight：遮挡边界和跨视角一致性是稀疏视角下最容易崩的部分，因此需要显式建模不确定性 | 让方法设计变得自然 |
| 第 5 段 | 总结方法和贡献：遮挡感知特征聚合、一致性约束、稀疏视角 benchmark 上的对比和消融 | 把 contribution 和实验一一对齐 |

> [!WARNING]
> Introduction 最常见的问题不是英文差，而是 gap 太虚。`existing methods are limited` 不是 gap；`existing methods fail under sparse-view input because occlusion boundaries are not explicitly modeled` 才是 gap。

### 3.3 Method：不是代码说明书，而是设计论证

Method 的读者不是来复现每一行代码的，而是来判断你的设计是否合理、必要、可复现。写 Method 时不要按代码文件顺序写，而要按“设计问题”组织。

#### 写前反思

| 问题 | 自查方式 |
|---|---|
| 模块是否都有动机 | 每个模块前是否解释它解决什么问题 |
| 公式是否服务于理解 | 公式后是否解释变量、输入输出和直觉 |
| pipeline 是否闭环 | 读者是否能从输入一路跟到输出 |
| 实现细节是否分层 | 关键设计在正文；超参数、网络层数、训练细节可放 implementation details |

#### Method 反例模式

> Our framework consists of three modules: FeatureNet, FusionNet, and RefinementNet. FeatureNet extracts features. FusionNet fuses features. RefinementNet generates the final output.

问题解释：这段话像代码文件说明，三个模块都只是“做了什么”，没有解释“为什么需要”。读者不知道 FeatureNet 提取什么特征、FusionNet 为什么比简单 concat 更好、RefinementNet 解决什么失败情况。

#### Method 推荐写法

以“边界引导语义分割”为例：

| 模块 | 推荐写法 | 为什么 |
|---|---|---|
| Overview | “Given an input image, the model first extracts multi-scale semantic features, then predicts boundary-aware attention maps to refine object edges, and finally decodes dense segmentation masks.” | 先给完整闭环，读者能画出 pipeline |
| Boundary branch | “Small objects and thin structures are often lost after repeated downsampling. To preserve these regions, we introduce a boundary branch supervised by edge maps derived from segmentation labels.” | 先解释失败原因，再引出模块 |
| Feature fusion | “Instead of directly concatenating features, we use boundary attention to reweight high-resolution features before fusion.” | 说明为什么不是普通拼接 |
| Loss design | “The total loss combines segmentation loss and boundary loss, so the model is optimized for both region consistency and edge localization.” | 解释损失函数和 claim 的关系 |

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

#### 实验反例模式

| 反例写法 | 问题 |
|---|---|
| 只放一张主结果表，表后写 “our method achieves the best performance” | 没有解释提升来自哪里，也没有回答模块是否必要 |
| baseline 只选很旧的方法 | reviewer 会质疑比较不公平 |
| ablation 只去掉一个模块 | 无法证明每个设计选择都有贡献 |
| 只展示成功样例 | 看不出方法边界，容易被认为夸大 |

#### 视觉论文实验推荐布局

以“低光图像增强”为例：

| 小节 | 要回答的问题 | 推荐内容 |
|---|---|---|
| Experimental Setup | 比较是否公平 | 数据集、训练设置、评价指标、baseline、实现细节 |
| Main Results | 方法是否有效 | PSNR、SSIM、LPIPS、NIQE 等指标；同时给视觉对比图 |
| Ablation Study | 模块是否必要 | 去掉 illumination guidance、去掉 multi-scale fusion、替换 loss 的结果 |
| Robustness Analysis | 是否能泛化 | 不同噪声强度、不同相机、不同曝光程度下的表现 |
| Efficiency | 是否有实际代价 | 参数量、FLOPs、推理时间、显存占用 |
| Failure Cases | 不能解决什么 | 极端欠曝、运动模糊、强彩色光污染等失败样例 |

#### 表格后的解释示例

不推荐：

> Table 1 shows the quantitative results. Our method achieves the best results on most metrics.

推荐：

> Table 1 shows that the proposed illumination-aware fusion improves PSNR and SSIM on paired datasets, while reducing LPIPS on real low-light images. This suggests that the method improves both pixel-level fidelity and perceptual quality. The gain is larger on scenes with spatially uneven illumination, which supports our claim that explicit illumination guidance is most useful when global enhancement is insufficient.

为什么更好：它没有只重复表格，而是解释表格支持了哪个 claim，并指出在什么条件下提升更明显。

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

#### Related Work 反例模式

> Method A proposed a CNN model for segmentation. Method B proposed an attention model. Method C proposed a transformer model. Method D proposed a multi-scale model.

问题解释：这是文献流水账。它没有告诉读者这些方法属于什么路线、共同假设是什么、和本文的差异在哪里。

#### Related Work 推荐写法

以“实时语义分割”为例：

| 组织方式 | 推荐内容 |
|---|---|
| Efficient segmentation networks | 概括轻量化 backbone、双分支结构、特征压缩等路线，说明它们如何换取速度 |
| Boundary-aware segmentation | 概括边界监督、边缘分支、结构约束等路线，说明它们如何改善物体边界 |
| Multi-scale context modeling | 概括 pyramid pooling、dilated convolution、attention-based context 等路线，说明它们如何处理尺度变化 |
| 本文位置 | 说明本文不是单纯追求更轻量，而是把 boundary guidance 放进实时分割框架，在速度和边界质量之间取得平衡 |

#### Conclusion 推荐写法

不推荐：

> In this paper, we proposed a new method. Experiments show that our method is effective. In the future, we will improve our work.

推荐：

> This paper studied real-time semantic segmentation under the constraint of limited computation. We proposed a boundary-guided feature fusion framework that uses lightweight edge supervision to improve thin structures and object contours. Experiments on urban-scene benchmarks show that the proposed boundary branch improves boundary accuracy with limited inference overhead. The method still struggles with extremely small objects and severe motion blur, suggesting that future work should explore temporal cues and higher-resolution supervision.

为什么更好：它回到任务、方法和证据，同时承认边界。好的 conclusion 不会假装解决所有问题，而是告诉读者“本文证明了什么，还没有证明什么”。

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

<div align="center">

# 科研论文写作与参考文献规范

### 实验室新人科研写作训练手册

把科研经验从“口口相传”沉淀为可复用、可检查、可迭代的书面规范。

![Knowledge Base](https://img.shields.io/badge/Knowledge%20Base-Research%20Writing-2f4858)
![Reference Standard](https://img.shields.io/badge/Reference%20Style-Real%20Citations-5f7f71)
![For Lab Training](https://img.shields.io/badge/Audience-Lab%20Newcomers-8a6f4d)

</div>

---

## 目录

| 模块 | 你会得到什么 | 快速跳转 |
|---|---|---|
| 手册总览 | 明确科研写作训练的核心能力 | [进入章节](#1-手册总览科研写作到底在训练什么) |
| 项目到论文 | 从 story、实验到投稿的完整工作流 | [进入章节](#2-从项目到论文少走弯路的完整工作流) |
| 正文写作 | Title、Abstract、Introduction、Method、Experiments、Related Work、Conclusion 的统一写法 | [进入章节](#3-论文正文怎么写title-到-conclusion-的统一方法) |
| 参考文献 | 真实会议、期刊、文章编号、预印本、数据集、软件、网页等示例 | [进入章节](#4-参考文献规范字段格式实例与特殊情况) |
| 落地模板 | Notion / GitHub 知识库结构、数据库和检查清单 | [进入章节](#5-知识库落地方式数据库模板和检查清单) |

---

![科研论文写作飞轮](assets/paper_writing_flywheel.svg)

## 1. 手册总览：科研写作到底在训练什么

科研写作不是把实验结果翻译成英文，也不是把所有工作细节堆进 PDF。科研写作的本质是：让读者相信你发现了一个值得解决的问题，并且你提出的方案确实带来了可靠的新知识。

一篇论文至少要讲清四件事：

| 核心问题 | 新人常见误区 | 正确写法 |
|---|---|---|
| 研究什么 | 只说技术名，不说任务和场景 | 先定义任务，再说明应用价值 |
| 为什么重要 | 用大而空的背景铺垫 | 说明旧方法在具体场景下哪里失败 |
| 你做了什么 | 按代码顺序介绍模块 | 按“问题-动机-设计-优势”介绍方法 |
| 凭什么相信 | 只放一张主结果表 | 用 comparison、ablation、analysis、failure cases 支撑 claim |

写论文时要一直记住两个读者：

| 读者 | 他们关心什么 | 你要做什么 |
|---|---|---|
| 快速浏览的 reviewer | 这篇论文是不是高级、清楚、可信 | 标题、摘要、teaser、表格和 Introduction 要第一眼清楚 |
| 认真追问的 reviewer | claim 有没有证据，方法有没有必要，实验是否公平 | 每个 claim 都要能追到实验、引用、理论或分析 |

![Claim 与 Evidence 对齐图](assets/claim_evidence_alignment.svg)

### 最重要的写作原则

一段只讲一个 message。段落第一句要直接说出这个 message，后面的句子负责解释、支撑或过渡。不要让读者读完整段以后才猜出你想表达什么。

论文中所有强 claim 都要被支撑。尤其是 Abstract 和 Introduction 里的 claim，reviewer 会直接拿这些句子追问：你凭什么这么说？如果没有实验或引用支撑，就要补证据、降低语气，或者删除。

论文的美观是内容的一部分。好看的 teaser、清楚的 pipeline figure、整齐的表格和稳定的排版，会显著影响 reviewer 的第一印象。这里的“好看”不是装饰，而是降低理解成本。

---

## 2. 从项目到论文：少走弯路的完整工作流

### 2.1 先讲 story，再写句子

很多新人写论文会从 Method 开始，因为 Method 看起来最像“我实际做了什么”。但真正高效的写作顺序是：先把论文 story 梳理清楚，再写各部分。

一篇论文的 story 可以用下面的问题检查：

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

建议每个项目维护一个 `Story Outline` 页面。任何人第一次接手项目，都应该先读这个页面，而不是先翻代码。

### 2.2 推荐写作顺序

不要按论文最终目录顺序写。推荐顺序如下：

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

每次组会建议固定回答：

1. 本周想验证哪个 claim？
2. 哪个实验支撑了它？
3. 哪个实验不支持它？
4. 当前最大风险是什么？
5. 下周最重要的一个实验或写作修改是什么？

---

## 3. 论文正文怎么写：Title 到 Conclusion 的统一方法

这一章不拆成很多小章节，而是用统一逻辑讲每个部分：它的任务、写作方法、常见问题和检查标准。

### 3.1 Title 和 Abstract：最后写，但决定第一印象

Title 的任务是让读者一眼知道任务和贡献。标题不要只有模型名字，也不要为了高级感牺牲可理解性。

| 类型 | 模板 | 适合场景 |
|---|---|---|
| 方法型 | `[Method Name]: [Core Mechanism] for [Task]` | 方法命名清楚 |
| 任务型 | `[Task] via [Key Technique]` | 任务本身重要 |
| 挑战型 | `[Solving Challenge] for [Application]` | 挑战是主要卖点 |
| 性能型 | `[Efficient/Robust/Scalable] [Task] with [Method]` | 强调效率、鲁棒性或规模 |

Abstract 是整篇论文的压缩版。推荐结构是：

| 句子 | 内容 | 新人要避免 |
|---|---|---|
| 1 | 任务和应用价值 | 一上来写泛泛背景 |
| 2 | 现有方法的关键问题 | 笼统说 existing methods are limited |
| 3 | 我们的核心洞察 | 没有 insight，直接说 we propose |
| 4 | 方法概述 | 写成模块流水账 |
| 5 | 主要结果 | 没有数字或具体实验 |
| 6 | 贡献意义 | 夸大超出实验范围 |

Abstract 中最危险的是强 claim。例如 “significantly outperforms existing methods”“generalizes to complex scenes”“is robust to noise”。这些 claim 必须在实验部分找到对应证据，否则投稿前要改弱。

### 3.2 Introduction：把 reviewer 带到“这篇论文必须存在”的位置

Introduction 的核心任务不是介绍领域，而是建立必要性。一个清楚的 Introduction 通常包含六层：

| 层次 | 写什么 | 关键问题 |
|---|---|---|
| 任务 | 研究对象和输入输出 | 读者知道你在做什么吗 |
| 价值 | 科学价值或应用价值 | 为什么值得关心 |
| 旧方法 | 现有路线和代表方法 | 你是否理解领域 |
| 缺口 | 旧方法的具体失败点 | 问题是否真实且重要 |
| 洞察/方法 | 你的核心观察和解决思路 | 你的方案是否自然 |
| 贡献 | 明确列出贡献 | 是否能被实验支撑 |

写 Introduction 时建议倒着想、顺着写。先倒着问：我最后要让 reviewer 相信什么贡献？这个贡献由哪些实验支撑？为了让实验有意义，需要先说明什么挑战？为了说明挑战，需要介绍哪些旧方法？想清楚后，再按任务、价值、旧方法、缺口、方法、贡献的顺序写。

### 3.3 Method：不是代码说明书，而是设计论证

Method 的读者不是来复刻代码的第一读者，而是先判断方法是否合理。写 Method 前要回答：

| 问题 | 要写清楚的内容 |
|---|---|
| 方法由哪些模块组成 | pipeline、输入输出、模块关系 |
| 每个模块为什么需要 | 它解决了旧方法或前一模块的什么问题 |
| 每个模块怎么做 | 核心计算、公式、网络结构、训练目标 |
| 为什么这样做有效 | 直觉、理论、经验或实验动机 |
| 实现细节在哪里 | 正文讲主逻辑，细节放 Implementation Details 或附录 |

每个模块都可以按“三要素”写：

| 要素 | 解释 | 常用句式 |
|---|---|---|
| Module Design | 这个模块做什么 | We design ... to ... |
| Motivation | 为什么需要它 | Directly applying ... fails because ... |
| Technical Advantage | 为什么这个设计好 | This design enables ... while avoiding ... |

### 3.4 Experiments：用证据回答质疑

实验部分不是结果陈列，而是证据体系。它至少要回答三类问题：

| Reviewer 问题 | 对应实验 | 说明 |
|---|---|---|
| 方法真的有效吗 | comparison | 与强 baseline 在公平设置下比较 |
| 为什么有效 | ablation | 证明关键模块和设计选择有贡献 |
| 什么时候有效/无效 | analysis / robustness / failure cases | 说明边界，避免夸大 |

实验表格和图要有“结论导向”。caption 不应该只是 “Results on dataset X”，而要告诉读者应该看到什么，例如 “Our method improves reconstruction quality especially under sparse-view settings.”

### 3.5 Related Work 和 Conclusion：定位贡献，收束边界

Related Work 不是按年份堆论文，而是按问题组织已有路线，并说明本文位置。

| 段落 | 内容 | 目的 |
|---|---|---|
| 方向一 | 与任务直接相关的方法 | 说明领域主线 |
| 方向二 | 与技术路线相关的方法 | 说明技术基础 |
| 最相关工作 | 与本文最接近的方法 | 说明差异和推进 |

Conclusion 建议三句话结构：本文研究了什么问题并提出什么方法；实验证明了什么主要结论；当前方法有什么边界，未来可以怎么扩展。

---

## 4. 参考文献规范：字段、格式、实例与特殊情况

![一条完整参考文献的结构](assets/reference_anatomy.svg)

本章所有示例均使用真实存在的文献。除作者姓名按具体格式处理外，会议名称、期刊名称、出版社、论文集名称等信息尽量写全，不使用期刊或会议缩写。

### 4.1 完整参考文献应该包含什么

一条完整参考文献的目标是：让读者能准确找到同一份资料。不同类型文献格式不同，但核心字段相似。

| 字段 | 含义 | 是否通常必需 | 说明 |
|---|---|---|---|
| 作者 | 谁写的 | 必需 | 多作者按目标格式处理，如列全、使用 et al. 或中文“等” |
| 年份 | 何时发表 | 必需 | 在线优先和正式发表年份不同时，按目标期刊或会议格式处理 |
| 题名 | 文献标题 | 必需 | 论文题名、书名、数据集名、网页标题 |
| 来源 | 发表在哪里 | 必需 | 期刊名称、会议论文集名称、书名、网站、预印本平台 |
| 卷号 volume | 期刊卷 | 期刊常见 | 会议论文通常没有卷号 |
| 期号 issue 或 number | 期刊期 | 期刊常见 | 有些期刊没有期号，可省略 |
| 页码 pages | 起止页 | 有则写 | 电子期刊可能使用文章编号而非页码 |
| 文章编号 article number | 替代页码 | 部分期刊常见 | 例如 Science 的 `aac4716`，或期刊系统中的 Article 105432 |
| DOI | 持久标识符 | 强烈建议 | 有 DOI 时优先写 DOI |
| URL | 网页地址 | 网页、预印本、软件常见 | 无 DOI 时尤其重要 |
| 访问日期 | 何时访问网页 | 网页常见 | 稳定出版物通常不需要 |
| 版本号 | 软件、数据、预印本 | 视情况 | 数据集、软件、预印本版本可能需要 |

### 4.2 会议论文标准实例

#### 数字制示例

正文引用：

`Neural radiance fields can represent a scene as a continuous function for view synthesis [1].`

参考文献：

`[1] B. Mildenhall, P. P. Srinivasan, M. Tancik, J. T. Barron, R. Ramamoorthi, and R. Ng, "NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis," in Computer Vision – ECCV 2020: 16th European Conference, Glasgow, United Kingdom, August 23–28, 2020, Proceedings, Part I, Springer, 2020, pages 405–421, DOI: 10.1007/978-3-030-58452-8_24.`

字段解释：

| 部分 | 内容 | 解释 |
|---|---|---|
| 编号 | `[1]` | 按正文首次引用顺序编号 |
| 作者 | B. Mildenhall 等 | 作者姓名可按目标格式缩写；其他信息不缩写 |
| 题名 | NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis | 论文题名必须完整 |
| 来源 | Computer Vision – ECCV 2020: 16th European Conference ... Proceedings, Part I | 会议论文集名称和会议信息写全 |
| 出版社 | Springer | 会议论文集出版社 |
| 年份 | 2020 | 正式出版年份 |
| 页码 | pages 405–421 | 有页码必须写 |
| DOI | 10.1007/978-3-030-58452-8_24 | 有 DOI 必须优先保留 |

#### APA 7 示例

`Mildenhall, B., Srinivasan, P. P., Tancik, M., Barron, J. T., Ramamoorthi, R., & Ng, R. (2020). NeRF: Representing scenes as neural radiance fields for view synthesis. In A. Vedaldi, H. Bischof, T. Brox, & J.-M. Frahm (Eds.), Computer Vision – ECCV 2020: 16th European Conference, Glasgow, United Kingdom, August 23–28, 2020, Proceedings, Part I (pp. 405–421). Springer. https://doi.org/10.1007/978-3-030-58452-8_24`

### 4.3 期刊论文标准实例

#### 数字制示例

正文引用：

`AlphaFold demonstrates that deep learning can predict protein structures with high accuracy [2].`

参考文献：

`[2] J. Jumper, R. Evans, A. Pritzel, T. Green, M. Figurnov, O. Ronneberger, K. Tunyasuvunakool, R. Bates, A. Žídek, A. Potapenko, A. Bridgland, C. Meyer, S. A. A. Kohl, A. J. Ballard, A. Cowie, B. Romera-Paredes, S. Nikolov, R. Jain, J. Adler, T. Back, S. Petersen, D. Reiman, E. Clancy, M. Zielinski, M. Steinegger, M. Pacholska, T. Berghammer, S. Bodenstein, D. Silver, O. Vinyals, A. W. Senior, K. Kavukcuoglu, P. Kohli, and D. Hassabis, "Highly accurate protein structure prediction with AlphaFold," Nature, volume 596, number 7873, pages 583–589, 2021, DOI: 10.1038/s41586-021-03819-2.`

字段解释：

| 部分 | 内容 | 解释 |
|---|---|---|
| 期刊名称 | Nature | 期刊名称写全，不使用缩写 |
| 卷号 | volume 596 | 期刊卷号 |
| 期号 | number 7873 | 期刊期号；若期刊无期号则省略 |
| 页码 | pages 583–589 | 有页码必须写 |
| DOI | 10.1038/s41586-021-03819-2 | 真实 DOI，优先保留 |

#### APA 7 示例

`Jumper, J., Evans, R., Pritzel, A., Green, T., Figurnov, M., Ronneberger, O., Tunyasuvunakool, K., Bates, R., Žídek, A., Potapenko, A., Bridgland, A., Meyer, C., Kohl, S. A. A., Ballard, A. J., Cowie, A., Romera-Paredes, B., Nikolov, S., Jain, R., Adler, J., Back, T., Petersen, S., Reiman, D., Clancy, E., Zielinski, M., Steinegger, M., Pacholska, M., Berghammer, T., Bodenstein, S., Silver, D., Vinyals, O., Senior, A. W., Kavukcuoglu, K., Kohli, P., & Hassabis, D. (2021). Highly accurate protein structure prediction with AlphaFold. Nature, 596(7873), 583–589. https://doi.org/10.1038/s41586-021-03819-2`

### 4.4 中文 GB/T 7714 示例

顺序编码制常见写法：

`[序号] 作者. 题名[文献类型标识]. 来源, 年, 卷(期): 起止页码.`

真实期刊示例：

`[1] JUMPER J, EVANS R, PRITZEL A, 等. Highly accurate protein structure prediction with AlphaFold[J]. Nature, 2021, 596(7873): 583-589.`

真实会议示例：

`[2] MILDENHALL B, SRINIVASAN P P, TANCIK M, 等. NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis[C]//Computer Vision – ECCV 2020: 16th European Conference, Glasgow, United Kingdom, August 23–28, 2020, Proceedings, Part I. Cham: Springer, 2020: 405-421.`

说明：GB/T 7714 中 `[J]` 表示期刊文章，`[C]` 表示会议论文或会议录中的析出文献。中文论文如果引用英文文献，题名、会议名称、期刊名称仍应保持原文完整，不要随意翻译或缩写。

### 4.5 特殊情况怎么处理

| 情况 | 处理方式 | 真实示例 |
|---|---|---|
| 会议论文没有卷号 | 不写卷号；写完整会议论文集名称、年份、页码或论文编号 | NeRF 会议论文写会议论文集和 pages 405–421，不写 volume |
| 期刊有卷号和期号 | 写期刊名称、volume、number、pages、DOI | Jumper et al. 的 Nature 论文：volume 596, number 7873, pages 583–589 |
| 期刊有文章编号而非页码 | 用文章编号替代页码，不要伪造页码 | Open Science Collaboration, “Estimating the reproducibility of psychological science,” Science, volume 349, number 6251, article aac4716, 2015, DOI: 10.1126/science.aac4716 |
| 预印本 | 写预印本平台和编号；若已有正式发表版本，优先引用正式版 | Pumarola et al., “D-NeRF: Neural Radiance Fields for Dynamic Scenes,” arXiv preprint arXiv:2011.13961, 2020 |
| 数据集论文 | 按会议或期刊论文引用，不能只写数据集网址 | Lin et al., “Microsoft COCO: Common Objects in Context,” in Computer Vision – ECCV 2014, Springer, 2014, pages 740–755, DOI: 10.1007/978-3-319-10602-1_48 |
| 软件论文 | 如果软件有论文，优先引用论文；必要时同时给版本和网址 | Harris et al., “Array programming with NumPy,” Nature, volume 585, number 7825, pages 357–362, 2020, DOI: 10.1038/s41586-020-2649-2 |
| 网页 | 写机构或作者、网页标题、网站名、URL、访问日期 | American Psychological Association, “References,” APA Style, https://apastyle.apa.org/style-grammar-guidelines/references, accessed 2026-06-07 |
| 标准 | 写发布机构、标准号、标准名、年份 | National Information Standards Organization, ANSI/NISO Z39.29-2005, Bibliographic References, 2005 |
| 学位论文 | 写作者、题名、学位类型、学校、年份 | 按学校图书馆或目标格式要求补全 |
| 专利 | 写发明人或申请人、专利题名、国家或地区、专利号、日期 | 按专利数据库给出的正式信息记录 |

### 4.6 BibTeX 字段建议

会议论文真实示例：

```bibtex
@inproceedings{mildenhall2020nerf,
  author    = {Mildenhall, Ben and Srinivasan, Pratul P. and Tancik, Matthew and Barron, Jonathan T. and Ramamoorthi, Ravi and Ng, Ren},
  title     = {NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis},
  booktitle = {Computer Vision -- ECCV 2020: 16th European Conference, Glasgow, United Kingdom, August 23--28, 2020, Proceedings, Part I},
  publisher = {Springer},
  year      = {2020},
  pages     = {405--421},
  doi       = {10.1007/978-3-030-58452-8_24}
}
```

期刊论文真实示例：

```bibtex
@article{jumper2021highly,
  author  = {Jumper, John and Evans, Richard and Pritzel, Alexander and Green, Tim and Figurnov, Michael and Ronneberger, Olaf and Tunyasuvunakool, Kathryn and Bates, Russ and Zidek, Augustin and Potapenko, Anna and Bridgland, Alex and Meyer, Clemens and Kohl, Simon A. A. and Ballard, Andrew J. and Cowie, Andrew and Romera-Paredes, Bernardino and Nikolov, Stanislav and Jain, Rishub and Adler, Jonas and Back, Trevor and Petersen, Stig and Reiman, David and Clancy, Ellen and Zielinski, Michal and Steinegger, Martin and Pacholska, Michalina and Berghammer, Tamas and Bodenstein, Sebastian and Silver, David and Vinyals, Oriol and Senior, Andrew W. and Kavukcuoglu, Koray and Kohli, Pushmeet and Hassabis, Demis},
  title   = {Highly accurate protein structure prediction with AlphaFold},
  journal = {Nature},
  year    = {2021},
  volume  = {596},
  number  = {7873},
  pages   = {583--589},
  doi     = {10.1038/s41586-021-03819-2}
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

预印本真实示例：

```bibtex
@article{pumarola2020dnerf,
  author  = {Pumarola, Albert and Corona, Enric and Pons-Moll, Gerard and Moreno-Noguer, Francesc},
  title   = {D-NeRF: Neural Radiance Fields for Dynamic Scenes},
  journal = {arXiv preprint arXiv:2011.13961},
  year    = {2020}
}
```

数据集论文真实示例：

```bibtex
@inproceedings{lin2014microsoft,
  author    = {Lin, Tsung-Yi and Maire, Michael and Belongie, Serge and Hays, James and Perona, Pietro and Ramanan, Deva and Dollar, Piotr and Zitnick, C. Lawrence},
  title     = {Microsoft COCO: Common Objects in Context},
  booktitle = {Computer Vision -- ECCV 2014: 13th European Conference, Zurich, Switzerland, September 6--12, 2014, Proceedings, Part V},
  publisher = {Springer},
  year      = {2014},
  pages     = {740--755},
  doi       = {10.1007/978-3-319-10602-1_48}
}
```

软件论文真实示例：

```bibtex
@article{harris2020array,
  author  = {Harris, Charles R. and Millman, K. Jarrod and van der Walt, Stefan J. and Gommers, Ralf and Virtanen, Pauli and Cournapeau, David and Wieser, Eric and Taylor, Julian and Berg, Sebastian and Smith, Nathaniel J. and Kern, Robert and Picus, Matti and Hoyer, Stephan and van Kerkwijk, Marten H. and Brett, Matthew and Haldane, Allan and del Rio, Jaime Fernandez and Wiebe, Mark and Peterson, Pearu and Gerard-Marchant, Pierre and Sheppard, Kevin and Reddy, Tyler and Weckesser, Warren and Abbasi, Hameer and Gohlke, Christoph and Oliphant, Travis E.},
  title   = {Array programming with NumPy},
  journal = {Nature},
  year    = {2020},
  volume  = {585},
  number  = {7825},
  pages   = {357--362},
  doi     = {10.1038/s41586-020-2649-2}
}
```

网页真实示例：

```bibtex
@misc{apaStyleReferences,
  author       = {{American Psychological Association}},
  title        = {References},
  howpublished = {APA Style},
  url          = {https://apastyle.apa.org/style-grammar-guidelines/references},
  note         = {Accessed: 2026-06-07}
}
```

### 4.7 参考文献最终检查

投稿前逐项检查：

- 正文引用和参考文献列表是否一一对应。
- 是否引用了数据集、baseline、评价指标、工具库和理论来源。
- 是否优先引用正式发表版本，而不是只引用预印本。
- 作者名大小写是否正确，特别是 LaTeX 中的专有名词，如 `{NeRF}`、`{AlphaFold}`、`{NumPy}`。
- 会议名称、期刊名称、出版社是否写全。
- DOI 和 URL 是否有效。
- 页码、文章编号、卷期号是否放在正确字段。
- 同一作者同一年多篇文献是否按格式区分。
- 中文论文中英文参考文献大小写、标点、文献类型标识是否统一。

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

#### Paper Card

| 字段 | 内容 |
|---|---|
| 论文标题 |  |
| 研究问题 |  |
| 核心贡献 |  |
| 方法结构 |  |
| 主要实验 |  |
| 优点 |  |
| 局限 |  |
| 可借鉴写法 |  |
| 与当前项目关系 |  |

#### Story Outline

| 字段 | 内容 |
|---|---|
| Task |  |
| Application |  |
| Existing methods |  |
| Gap / Challenge |  |
| Key insight |  |
| Method |  |
| Contributions |  |
| Evidence |  |

#### Claim-Evidence Map

| Claim | 位置 | 证据 | 状态 | 处理 |
|---|---|---|---|---|
|  | Abstract / Introduction / Method | Table / Figure / Citation / Theory | supported / risky / missing | 保留 / 补实验 / 弱化 / 删除 |

#### Reviewer 自审清单

| 维度 | 问题 |
|---|---|
| Contribution | 贡献是否具体、可验证、和已有工作有清楚区别 |
| Writing | 每段是否只有一个 message，第一句是否说明段落作用 |
| Experiments | comparison、ablation、analysis 是否支撑所有核心 claim |
| Method | 每个模块是否有必要，是否解释为什么有效 |
| References | 是否引用关键工作、数据集、工具和理论来源 |
| Presentation | teaser、pipeline、表格、排版是否清楚美观 |

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
- NeRF 论文记录：<https://dblp.org/rec/conf/eccv/MildenhallSTBRN20.html>
- AlphaFold 期刊论文：<https://www.nature.com/articles/s41586-021-03819-2>

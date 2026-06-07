# 科研论文写作与参考文献规范：实验室新人手册

> 目标：把实验室科研经验从“口口相传”变成可复用、可检查、可迭代的书面规范。  
> 适用对象：实验室新人、第一次写论文的同学、正在整理项目投稿材料的同学。

![科研论文写作飞轮](assets/paper_writing_flywheel.svg)

## 目录

1. 手册总览：科研写作到底在训练什么
2. 从项目到论文：少走弯路的完整工作流
3. 论文正文怎么写：Title 到 Conclusion 的统一方法
4. 参考文献规范：字段、格式、实例与特殊情况
5. Notion 落地方式：数据库、模板和检查清单

---

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

建议每个项目在 Notion 里维护一个 `Story Outline` 页面。任何人第一次接手项目，都应该先读这个页面，而不是先翻代码。

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

常见标题结构：

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

常见问题：

| 问题 | 表现 | 修改方式 |
|---|---|---|
| 背景太大 | “近年来 AI 快速发展...” | 直接进入任务和应用 |
| challenge 不具体 | “existing methods are inaccurate” | 说明在哪个条件、哪个环节、为什么失败 |
| contribution 像功能列表 | “we design A, B, C” | 写清每个设计带来的科学或技术价值 |
| 和实验脱节 | Introduction 说鲁棒，实验没有鲁棒性 | 补实验或删除 claim |

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

Method 最常见的问题是“流水账”：先做 A，再做 B，再做 C，但没有解释为什么 A/B/C 必须存在。修改时要把每个模块改成“动机-设计-优势”的结构。

### 3.4 Experiments：用证据回答质疑

实验部分不是结果陈列，而是证据体系。它至少要回答三类问题：

| Reviewer 问题 | 对应实验 | 说明 |
|---|---|---|
| 方法真的有效吗 | comparison | 与强 baseline 在公平设置下比较 |
| 为什么有效 | ablation | 证明关键模块和设计选择有贡献 |
| 什么时候有效/无效 | analysis / robustness / failure cases | 说明边界，避免夸大 |

实验表格和图要有“结论导向”。caption 不应该只是 “Results on dataset X”，而要告诉读者应该看到什么，例如 “Our method improves reconstruction quality especially under sparse-view settings.”

实验部分的最低检查：

- baseline 是否足够强，是否包含最相关工作？
- 数据集和指标是否能支撑论文 claim？
- 每个关键模块是否都有消融？
- 是否解释了失败案例或局限？
- 表格是否标清 ↑/↓、最优、次优和实验设置？
- 定性图是否包含代表性样例，而不是只挑最好看的结果？

### 3.5 Related Work 和 Conclusion：定位贡献，收束边界

Related Work 不是按年份堆论文，而是按问题组织已有路线，并说明本文位置。

推荐写法：

| 段落 | 内容 | 目的 |
|---|---|---|
| 方向一 | 与任务直接相关的方法 | 说明领域主线 |
| 方向二 | 与技术路线相关的方法 | 说明技术基础 |
| 最相关工作 | 与本文最接近的方法 | 说明差异和推进 |

Related Work 要公平。不要把别人的方法写得很弱来衬托自己，这很容易被 reviewer 反感。正确做法是承认已有方法解决了什么，再准确指出它们没有覆盖的场景、假设或限制。

Conclusion 要短，但不能空。建议三句话结构：

1. 本文研究了什么问题，并提出了什么方法。
2. 实验证明了什么主要结论。
3. 当前方法有什么边界，未来可以怎么扩展。

---

## 4. 参考文献规范：字段、格式、实例与特殊情况

![一条完整参考文献的结构](assets/reference_anatomy.svg)

### 4.1 完整参考文献应该包含什么

一条完整参考文献的目标是：让读者能准确找到同一份资料。不同类型文献格式不同，但核心字段相似。

| 字段 | 含义 | 是否通常必需 | 说明 |
|---|---|---|---|
| 作者 | 谁写的 | 必需 | 多作者按目标格式处理，如 et al. 或列全 |
| 年份 | 何时发表 | 必需 | 在线优先和正式发表年份不同时，按目标格式 |
| 题名 | 文献标题 | 必需 | 论文题名、书名、数据集名、网页标题 |
| 来源 | 发表在哪里 | 必需 | 期刊名、会议名、书名、网站、arXiv |
| 卷号 volume | 期刊卷 | 期刊常见 | 会议论文通常没有卷号 |
| 期号 issue/number | 期刊期 | 期刊常见 | 有些期刊没有期号，可省略 |
| 页码 pages | 起止页 | 有则写 | 电子期刊可能是文章编号而非页码 |
| 文章编号 article number | 替代页码 | 部分期刊常见 | 如 e12345、012345、Article 105432 |
| DOI | 持久链接 | 强烈建议 | 有 DOI 优先写 DOI |
| URL | 网页地址 | 网页/预印本/软件常见 | 无 DOI 时尤其重要 |
| 访问日期 | 何时访问网页 | 网页常见 | 稳定出版物通常不需要 |
| 版本号 | 软件/数据/预印本 | 视情况 | 数据集、软件、arXiv 版本可能需要 |

### 4.2 会议论文标准实例

#### IEEE/ACM 数字制示例

正文引用：

`NeRF represents a scene as a continuous radiance field and renders novel views through volume rendering [1].`

参考文献：

`[1] B. Mildenhall, P. P. Srinivasan, M. Tancik, J. T. Barron, R. Ramamoorthi, and R. Ng, "NeRF: Representing scenes as neural radiance fields for view synthesis," in Proc. Eur. Conf. Comput. Vis. (ECCV), 2020, pp. 405-421.`

字段解释：

| 部分 | 内容 | 解释 |
|---|---|---|
| `[1]` | 编号 | 按正文首次引用顺序编号 |
| 作者 | B. Mildenhall 等 | IEEE 通常名缩写在前，姓在后 |
| 题名 | "NeRF: ..." | 文章标题用引号 |
| 来源 | Proc. ECCV | 会议论文集名称 |
| 年份 | 2020 | 发表年份 |
| 页码 | pp. 405-421 | 有页码就写 |

#### APA 7 示例

`Mildenhall, B., Srinivasan, P. P., Tancik, M., Barron, J. T., Ramamoorthi, R., & Ng, R. (2020). NeRF: Representing scenes as neural radiance fields for view synthesis. In A. Vedaldi, H. Bischof, T. Brox, & J.-M. Frahm (Eds.), Computer Vision - ECCV 2020 (pp. 405-421). Springer.`

APA 更重视作者、年份、题名、来源。会议论文如果出版在 Lecture Notes in Computer Science 这类书系里，通常会出现编辑、书名、页码和出版社。

### 4.3 期刊论文标准实例

#### IEEE 数字制示例

正文引用：

`Transformer architectures have become a foundation for sequence modeling [2].`

参考文献：

`[2] A. Vaswani et al., "Attention is all you need," IEEE Trans. Pattern Anal. Mach. Intell., vol. 45, no. 3, pp. 1234-1250, 2023, doi: 10.xxxx/tpami.2023.xxxxxx.`

字段解释：

| 部分 | 内容 | 解释 |
|---|---|---|
| 期刊名 | IEEE Trans. Pattern Anal. Mach. Intell. | 期刊名可按官方缩写 |
| vol. | 45 | 卷号 |
| no. | 3 | 期号 |
| pp. | 1234-1250 | 页码范围 |
| doi | 10.xxxx/... | DOI，有则强烈建议保留 |

#### APA 7 示例

`Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, L., & Polosukhin, I. (2023). Attention is all you need. IEEE Transactions on Pattern Analysis and Machine Intelligence, 45(3), 1234-1250. https://doi.org/10.xxxx/tpami.2023.xxxxxx`

APA 结构通常是：作者。年份。题名。期刊名，卷号(期号)，页码。DOI。

### 4.4 中文 GB/T 7714 示例

顺序编码制常见写法：

`[1] 作者. 题名[J]. 刊名, 年, 卷(期): 起止页码.`

期刊示例：

`[1] 张三, 李四. 面向动态场景的神经重建方法[J]. 计算机学报, 2025, 48(3): 501-516.`

会议示例：

`[2] 王五, 赵六. 稀疏视角三维重建方法[C]//中国计算机大会论文集. 北京: 电子工业出版社, 2025: 120-128.`

英文文献用于中文论文时，也可按 GB/T 7714 的英文条目格式处理：

`[3] MILDENHALL B, SRINIVASAN P P, TANCIK M, et al. NeRF: Representing scenes as neural radiance fields for view synthesis[C]//European Conference on Computer Vision. Cham: Springer, 2020: 405-421.`

### 4.5 特殊情况怎么处理

| 情况 | 怎么写 | 例子/说明 |
|---|---|---|
| 没有卷号 | 省略 volume | 会议论文通常没有卷号 |
| 有卷号没有期号 | 写卷号，省略期号 | `Journal Name, 12, 55-70` |
| 没有页码，有文章编号 | 用 Article/eLocator 替代页码 | `Article 105432` 或 `e105432` |
| 在线优先，没有卷期页 | 写 online first / advance online publication 和 DOI | 等正式信息出来后更新 |
| 会议论文没有页码 | 省略页码或写论文编号 | 按会议模板要求 |
| arXiv 预印本 | 写 arXiv ID 和年份 | `arXiv preprint arXiv:2401.12345` |
| 同一论文有 arXiv 和正式版 | 优先引用正式版 | 除非引用的是 arXiv 独有版本 |
| 数据集 | 作者/机构、数据集名、版本、年份、仓库/DOI | 数据集也要引用 |
| 软件/代码库 | 作者/组织、软件名、版本、年份、URL/DOI | 重要工具和库需引用 |
| 网页 | 作者/机构、标题、网站、日期、URL、访问日期 | 网页会变化，访问日期重要 |
| 标准/规范 | 机构、标准号、标准名、年份 | 如 ISO、GB/T、IEEE standards |
| 学位论文 | 作者、题名、学位类型、学校、年份 | 注意硕士/博士类型 |
| 专利 | 专利申请人、题名、国别、专利号、日期 | 工程领域可能使用 |

### 4.6 BibTeX 字段建议

会议论文：

```bibtex
@inproceedings{mildenhall2020nerf,
  author    = {Mildenhall, Ben and Srinivasan, Pratul P. and Tancik, Matthew and Barron, Jonathan T. and Ramamoorthi, Ravi and Ng, Ren},
  title     = {NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis},
  booktitle = {Proceedings of the European Conference on Computer Vision},
  year      = {2020},
  pages     = {405--421},
  doi       = {10.xxxx/example}
}
```

期刊论文：

```bibtex
@article{zhang2025dynamic,
  author  = {Zhang, Lei and Wang, Yue and Chen, Xin},
  title   = {Efficient Neural Reconstruction for Dynamic Scenes},
  journal = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year    = {2025},
  volume  = {47},
  number  = {2},
  pages   = {1001--1018},
  doi     = {10.xxxx/example}
}
```

文章编号而非页码：

```bibtex
@article{lee2025articleid,
  author        = {Lee, Min and Kumar, Arjun},
  title         = {Robust Visual Learning under Sparse Supervision},
  journal       = {Pattern Recognition},
  year          = {2025},
  volume        = {158},
  articlenumber = {111234},
  doi           = {10.xxxx/example}
}
```

arXiv：

```bibtex
@article{chen2026preprint,
  author  = {Chen, Hao and Liu, Mei},
  title   = {A Survey on Neural Rendering},
  journal = {arXiv preprint arXiv:2601.01234},
  year    = {2026}
}
```

网页：

```bibtex
@misc{notion2026docs,
  author       = {{Notion Labs}},
  title        = {Notion Help Center},
  year         = {2026},
  url          = {https://www.notion.com/help},
  note         = {Accessed: 2026-06-07}
}
```

### 4.7 参考文献最终检查

投稿前逐项检查：

- 正文引用和参考文献列表是否一一对应。
- 是否引用了数据集、baseline、评价指标、工具库和理论来源。
- 是否优先引用正式发表版本，而不是只引用 arXiv。
- 作者名大小写是否正确，特别是 LaTeX 中的专有名词，如 `{NeRF}`、`{iPhone}`。
- 会议名、期刊名是否符合模板缩写。
- DOI 和 URL 是否有效。
- 页码、文章编号、卷期号是否放在正确字段。
- 同一作者同一年多篇文献是否按格式区分。
- 中文论文中英文参考文献大小写、标点、文献类型标识是否统一。

---

## 5. Notion 落地方式：数据库、模板和检查清单

建议把这个手册放在实验室 Notion 的“科研训练”或“论文写作规范”栏目下。页面不要拆得太碎，采用一个主页面 + 几个数据库即可。

### 5.1 推荐页面结构

| 模块 | 内容 |
|---|---|
| 顶部说明 | 手册目的、适用对象、核心原则 |
| 目录 | 5 个大章节 |
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
- IEEE Author Center：<https://ieeeauthorcenter.ieee.org/>

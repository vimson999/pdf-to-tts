# 40-channel-ops

> 状态：频道实验期 / 暂未定名

这是一个独立新频道的**运营知识库与单集项目工作区**。

它不只是“选题文件夹”，而是用来长期沉淀：参考频道研究、选题方法、标题与封皮经验、视频结构、发布复盘，以及每一集从输入资料到最终数据的完整过程。

> 本工作区**不属于「兼听研报」**。兼听研报继续聚焦具体公司 / 具体标的；这里当前研究的是另一种内容形态。频道最终边界暂不预设，先通过真实 PDF 库、选题测试和发布数据逐步长出来。

## 1. 两层结构

本工作区分为两层：

```text
methods/    根方法：跨视频复用的当前最佳实践
episodes/   单集档案：每一期真实执行过程与结果
```

另外保留：

```text
batches/    上游输入批次：尚未归属具体单集的候选 PDF / JSON 清单
```

核心原则：

> **Methods 是“现在我们相信什么”；Episodes 是“我们为什么开始相信它”。**

## 2. 目录结构

```text
40-channel-ops/
├── README.md
├── methods/
│   ├── README.md
│   ├── 10-reference-channel-research.md
│   ├── 20-topic-selection.md
│   ├── 30-topic-scoring-model.md
│   ├── 40-report-format-strategy.md
│   ├── 50-title-playbook.md
│   ├── 60-thumbnail-playbook.md
│   ├── 70-video-structure.md
│   ├── 80-publishing-review.md
│   ├── 90-knowledge-promotion.md
│   └── 95-data-and-json-policy.md
├── batches/
│   └── README.md
└── episodes/
    ├── README.md
    └── _template/
        └── README.md
```

## 3. 工作方式

### 3.1 从资料开始，而不是先把频道定义死

当前阶段不急着给频道划死边界。

先做：

```text
PDF / JSON 库
    ↓
抽取候选命题
    ↓
评分 / 聚类 / 找冲突
    ↓
Top 选题
    ↓
制作并发布
    ↓
真实数据复盘
    ↓
反向修正 methods
```

让高分选题和真实数据逐步告诉我们频道最终应该是什么。

### 3.2 视频的基本单位不是 PDF，而是“问题 / 命题”

不要默认：

```text
1 PDF = 1 视频
```

可以是一份 PDF 深拆，也可以是多份 PDF 围绕同一个问题做补充、碰撞或观点演变。

### 3.3 单集经验不能直接冒充根方法

单集里发现的新经验，先留在该集 `episodes/...` 中。

只有经过重复验证后，才升级到 `methods/`。

建议状态：

```text
Observation  单集观察
Pattern      多集重复出现的模式
Rule         足够稳定，升级为根方法
```

## 4. 与 pdf-to-tts 其他能力的关系

这个工作区负责频道运营与单集项目管理；已有根目录 Prompt 仍负责具体生产能力：

```text
40-channel-ops
  ↓ 选题 / 单集决策
10-report-to-script.md
  ↓ 研究资料 -> 正文
TTS / 音频
  ↓
30-finance-audio-framing.md（按需）
  ↓
SRT / 视觉导演 / Thumbnail
  ↓
发布数据回流到 episode
  ↓
必要时升级 methods
```

## 5. 第一季测试

第一季先把它当实验系统使用：

- 不预设必须单篇或多篇；
- 不预设必须只做某几个宏观主题；
- 不为了填满栏目而做弱选题；
- 每一期保留完整决策链；
- 优先记录真实发布数据；
- 用第一季结果决定第二季是否需要收窄定位、调整题型和视觉包装。

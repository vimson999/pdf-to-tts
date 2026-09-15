# pdf-to-tts

财经研究内容到 TTS / 音频节目的 Prompt 与频道实验工作区。

## 文件命名规则

根目录单一能力采用：

```text
排序编号-能力名称.md
```

文件名描述“能力”，不描述版本。版本由文档内部和 Git 历史管理，避免 `final`、`new`、`v2-final` 等命名。

编号按 10 递增，方便未来插入：

```text
10-...
20-...
30-...
```

当某一主题已经不是单一 Prompt，而是会持续扩展出研究、规则、单集档案、样本与反馈数据时，使用**编号目录**管理。

## 当前 Prompt / 工作区

### `10-report-to-script.md`

**资料 / 研报 → 完整财经 TTS 文案**

用于一份或多份机构研报、行业报告、基金经理交流纪要等材料的分析、Debate Map 和最终节目文案生成。

### `20-xiaojunjun-honghao-editorial.md`

**洪灏原文 + 小君君主持人 → 双人音频节目**

用于保护作者原文，同时在关键节点加入主持人的解释、拆解与连接。

### `30-finance-audio-framing.md`

**已有财经音频 → 开场引导 + 播后分析总结**

用于已经存在音频、SRT 或逐字稿的场景。重点是找到最高信息张力，用开场制造认知缺口，并在原音频结束后完成事实、判断、条件、风险与验证变量的二次整理。

### `40-channel-ops/`

**独立新频道的运营知识库 + 单集项目工作区（频道暂未定名）**

这不是单纯的“选题目录”。它负责沉淀：

- 参考频道研究；
- 选题根方法；
- 单篇 / 多篇研报内容形态；
- 标题经验；
- Thumbnail / 封皮经验；
- 视频结构；
- 发布与数据复盘；
- 每一期完整项目档案；
- 从单集 Observation 到通用 Rule 的升级过程。

当前结构：

```text
40-channel-ops/
├── README.md
├── methods/      # 通用根方法
├── batches/      # 尚未归属具体单集的正式输入批次
└── episodes/     # 每一期完整项目档案
```

其中：

```text
methods = 现在我们相信什么
episodes = 我们为什么开始相信它
```

单集产生的新经验先留在 episode，经过重复验证后再升级到 methods。

> `40-channel-ops/` 不属于「兼听研报」。兼听研报继续聚焦具体公司 / 具体标的。这个新频道的最终边界暂不提前写死，先通过真实 PDF 库、第一季选题和发布数据逐步形成。

## 职责关系

```text
40-channel-ops：频道运营、选题、单集档案、复盘与方法沉淀
10-report-to-script：从研究资料生产节目正文
20-xiaojunjun-honghao-editorial：把作者原文编辑成双人节目
30-finance-audio-framing：给已有财经音频增加前后包装
```

第一季实验链路：

```text
PDF / JSON 库
  ↓
40-channel-ops/batches：正式输入批次
  ↓
选题 / 内容形态决策
  ↓
40-channel-ops/episodes/S01E..：创建单集
  ↓
10-report-to-script：正文
  ↓
TTS / 音频
  ↓
30-finance-audio-framing：按需增加开场与播后分析
  ↓
SRT / 视觉导演 / Thumbnail
  ↓
发布
  ↓
数据回流 episode
  ↓
必要时升级 methods
```

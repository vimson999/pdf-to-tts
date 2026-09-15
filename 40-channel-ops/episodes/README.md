# Episodes

这里存放每一集视频的完整项目档案。

目标不是只保存最终文案，而是保存：

> **这一集为什么做、怎么做、最后发生了什么。**

## 1. 命名

第一季建议：

```text
S01E01-<short-slug>/
S01E02-<short-slug>/
...
```

如果题目尚未最终确定，先使用稳定的短主题 slug，避免把营销标题直接当目录名。

## 2. 推荐单集结构

```text
episodes/S01E01-<slug>/
├── README.md
├── inputs/
│   └── source-manifest.json
├── 10-topic-decision.md
├── 20-research-notes.md
├── 30-claim-evidence-map.md
├── 40-script.md
├── 50-title-options.md
├── 60-thumbnail.md
├── 70-publish-metadata.md
└── 80-performance-review.md
```

不是每一期都必须机械生成全部文件；但只要某部分产生了有价值的信息，就应归到这一集，而不是散落在聊天记录里。

## 3. 各文件职责

### `README.md`

这一集的快速索引：状态、核心问题、最终标题、内容形态、主要来源、发布时间、结果摘要。

### `inputs/source-manifest.json`

只记录本集真正使用的资料及其角色，不复制整个 PDF 候选库。

### `10-topic-decision.md`

- 为什么选这个题；
- 淘汰过哪些角度；
- 评分；
- 为什么用一篇 / 多篇；
- 风险和关键限定条件。

### `20-research-notes.md`

对来源的研究笔记、机构观点、关键数据、分歧。

### `30-claim-evidence-map.md`

每个重要 Claim 对应到哪份报告、哪张图、哪段原文，以及事实 / 判断 / 推论的边界。

### `40-script.md`

最终或接近最终的口播文案。

### `50-title-options.md`

标题候选、最终选择及理由。

### `60-thumbnail.md`

封皮命题、版式、文字、原始研报画面使用方式、最终设计选择。

### `70-publish-metadata.md`

发布时间、平台、视频链接、时长、描述、tags 等。

### `80-performance-review.md`

CTR、观看量、留存、流量来源、评论反馈，以及这一集产生的 Observation。

## 4. 单集经验先留在单集

不要在制作过程中因为这一集“感觉不错”就立刻修改根方法。

流程：

```text
Episode Observation
    ↓
其他 Episode 继续验证
    ↓
Pattern
    ↓
Rule
    ↓
Methods
```

## 5. Episode 必须可独立回看

理想状态：几个月后打开一个 episode 文件夹，不需要重新找聊天记录，也能理解这期视频完整的决策过程。

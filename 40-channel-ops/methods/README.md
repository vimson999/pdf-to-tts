# Methods

这里存放频道的**根方法**：跨多集复用、经过验证后形成的当前最佳实践。

## 更新原则

根方法不是一次讨论后永久定型，而是持续演进：

```text
单集 Observation
    ↓
多集 Pattern
    ↓
稳定 Rule
    ↓
升级到 methods
```

反过来，如果真实数据连续否定某条 Rule，也应降级、修正或删除。

如果某条方法的形成经历了明显的失败、分歧、外部样本验证或多轮版本修正，应同时在 `../cases/` 保留一份决策案例。这样以后不仅知道“规则是什么”，也知道“为什么会有这条规则”。

## 当前模块

- `10-reference-channel-research.md`：参考频道历史样本与已提炼规律
- `15-reference-script-structure.md`：参考频道完整脚本的结构研究，重点研究“如何把研报讲细但不枯燥”
- `20-topic-selection.md`：选题基本单位、候选命题和筛选原则
- `30-topic-scoring-model.md`：候选命题评分模型
- `40-report-format-strategy.md`：单篇 / 多篇 / 观点演变的内容形态选择
- `50-title-playbook.md`：标题方法与测试记录
- `60-thumbnail-playbook.md`：封皮 / Thumbnail 方法与测试记录
- `70-video-structure.md`：视频叙事和证据结构
- `80-publishing-review.md`：发布数据与复盘框架
- `90-knowledge-promotion.md`：单集经验升级到根方法的规则
- `95-data-and-json-policy.md`：JSON、PDF 元数据与 Git 存储策略

## 使用要求

每次做新一集时：

1. 先读取相关 methods；
2. 如果某条方法旁边有重要 Case，按需读取 Case 理解其适用边界；
3. 将方法应用到具体 episode；
4. 不在执行过程中直接改根方法来迎合当期；
5. 单集结束后再判断是否有经验值得升级；
6. 只有重要的认知演进才建立 Case，不把 Cases 变成聊天流水账。

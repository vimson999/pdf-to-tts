# S01E01 — China Trade: Strong Surplus, Uneven Growth Support

```yaml
episode_id: S01E01
status: script-v6-review
working_topic: 中国出口这么强，为什么对就业和收入的拉动却没有同样强？
core_question: 中国出口与贸易顺差表现强劲，但为什么对实际产出、就业、收入和国内吸收的传导并不均衡？
format: single-report
primary_source: 摩根大通-中国贸易：顺差强劲，对增长的支撑却不均衡-260908.pdf
supporting_sources: []
final_title: 中国出口大涨25%，为什么普通人的体感没那么强？
thumbnail_text: 小摩：/ 中国出口大涨25% / 为什么普通人的体感没那么强？
publish_url:
```

## 当前判断

本集选题、标题、封皮方向已经基本锁定。参考频道“顺着研报讲”的核验带来新的方法修正，因此在 V5 之后增加一次 `Report-order audit`，并形成 **V6 原序深读版**。

当前不再把 V5 视为最终生产候选；先评审 V6，再进入 TTS。

主报告原始叙事链：

```text
贸易总量
  ↓
地区结构
  ↓
产品结构
  ↓
进口结构
  ↓
科技出口越来越具有价格 / 高价值产品驱动特征
  ↓
对实际产出、就业和收入的短期拉动弱于广泛出口量增长
  ↓
外部缓冲风险上升
  ↓
政策考验：把出口韧性转成更强的国内吸收
```

## 当前原则

- 先按 `single-report` 完整制作，不为了“多研报”强行加入其他报告；
- “普通人的体感”是传播层翻译，不是 J.P. Morgan 直接测量指标；正文必须落回实际产出、就业、收入与国内吸收；
- 采用“问题驱动的研报深读”，但不为了标题问题过度拆散报告本身已经成立的论证顺序；
- 区分 **机械逐句翻译** 与 **顺序深读**：高度跟随研报结构本身不是低价值；
- 关键图表应进入口播论证，而不是只留到 Storyboard 阶段当视觉素材；
- 通篇坚持自然优先、信息优先、技巧克制；
- 开头可以轻设计，结尾优先自然收住，不强求金句或价值升华；
- 封皮必须基于真实 PDF 首页做编辑设计，不重绘、不伪造。

## 脚本版本

```text
40-script.md        V3：研报深读版，主线与证据链基本成立
40-script-v4.md     V4：加强头尾设计；结尾后来被判断为设计过度
40-script-v5.md     V5：自然优先版；降低文案设计感，曾作为生产候选
40-script-v6.md     V6：当前评审候选；恢复原报告顺序，加强关键图表顺序深读
```

V5 → V6 的结构性原因记录在：

`47-report-order-audit.md`

核心变化：

```text
V5：总量 → 地区 → 产品 → 价格/数量 → 进口 → 政策 → 外部风险
V6：总量 → 地区 → 产品 → 进口 → 价格/数量与就业收入 → 外部风险 → 政策
```

V6 同时新增对原报告第 2–3 页关键图表的口播解释，包括：

- Exports volume vs. price；
- Export price breakdown；
- China export unit prices；
- China exports to US and RoW；
- China high-tech exports。

## 已锁定包装

标题：

> **中国出口大涨25%，为什么普通人的体感没那么强？**

封皮主文案：

```text
小摩：
中国出口大涨25%
为什么普通人的体感
没那么强？
```

封皮执行规范：

`61-thumbnail-spec-v1.md`

当前通过方向：真实 J.P. Morgan 第 1 页 + Editorial Split 版式 + 暖白底 + 墨黑文字 + 深酒红强调 `25%`。保留 `小摩：` 来源标签与轻量底部来源信息；当前左右视觉关系保持现状。

这套封皮结构目前仍属于 S01E01 Observation，等后续多集验证后再决定是否升级为频道 Rule。

## 本集文件

```text
README.md
10-topic-decision.md
20-research-notes.md
30-claim-evidence-map.md
35-video-plan.md
40-script.md
40-script-v4.md
40-script-v5.md
40-script-v6.md
45-script-review.md
46-reference-channel-comparison.md
47-report-order-audit.md
50-title-options.md
60-thumbnail.md
61-thumbnail-spec-v1.md
inputs/source-manifest.json
```

## 下一步

1. 先人工评审 `40-script-v6.md`：重点不是再找文案技巧，而是判断“像不像真的在带观众读这篇小摩报告”；
2. 如果方向通过，用 V6 生成第一版 TTS；
3. TTS 第一遍只听自然度：句子是否拗口、数字是否难听懂、图表解释是否过长、总时长是否合适；
4. 只做口语化微调，不轻易再次重构；
5. 音频锁定后生成 SRT；
6. 再进入视觉导演 / Storyboard，把 V6 已经点名的真实研报图表按时间戳匹配。

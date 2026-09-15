# S01E01 Thumbnail Directions

> 当前为设计方向，不直接生成成品图。

## 1. 总原则

沿用参考频道已经验证的“原始研报证据型封皮”，但不机械复制。

核心视觉：

```text
J.P. Morgan 报告首页
+ 关键原文 / 数字高亮
+ 一句中文矛盾
```

研报负责可信度，中文大字负责点击理由。

## 2. 最值得展示的原始信息

报告首页已经非常适合做 Thumbnail：

- `Exports rose 25.0%oya`
- `US$119.1bn surplus`
- `AI-related technology and EM Asia drove growth, with limited spillover`
- `weaker lift to real output, employment and income`

建议不要四句全塞，只选 1 个数字 + 1 个矛盾。

## 3. 中文大字候选

### 方向 A — 最直接

```text
出口+25%
就业收入呢？
```

优点：短、冲突明确。

### 方向 B — 更研究型

```text
出口很强
为何“不带人”？
```

说明：“不带人”是传播表达，正文必须马上解释为就业与收入外溢较弱，不能脱离原报告。

### 方向 C — 数字型

```text
1191亿顺差
谁真正受益？
```

优点：数字冲击强。
风险：报告没有直接回答“谁获得了全部收益”，正文需要避免把问题包装成已知答案。

### 方向 D — 最稳妥

```text
出口大涨
拉动却变弱？
```

优点：最贴近报告 `uneven growth support`。

## 4. 当前首选

建议第一版：

```text
背景：J.P. Morgan 第 1 页
左/中区域保留报告标题与机构标识
高亮：25.0% + weaker lift to ... employment and income
中文大字：出口+25%｜就业收入呢？
```

## 5. 不建议

- 不放集装箱、港口、工厂等 AI 大场景替代研报；
- 不把封皮写成完整摘要；
- 不同时堆高盛 / 小摩 / 花旗 Logo；
- 不写“出口越强，就业越差”这类报告没有支持的因果；
- 不写“普通人彻底没受益”这类绝对化结论。

## 6. 后续复盘字段

发布后记录：

```yaml
thumbnail_version:
thumbnail_text:
uses_report_screenshot: true
key_number: 25%
conflict_type: strong_export_vs_weaker_employment_income_lift
impressions:
ctr:
views_24h:
views_7d:
```

如果该结构表现好，先记为 Episode Observation；至少跨多期重复验证后，再升级到 `methods/60-thumbnail-playbook.md`。

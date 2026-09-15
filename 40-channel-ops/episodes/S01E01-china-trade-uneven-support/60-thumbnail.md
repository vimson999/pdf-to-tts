# S01E01 Thumbnail Directions

> 状态：V5 脚本后的第二轮设计方向。
> 原则：原始研报负责可信度，中文大字只负责把真实矛盾说清楚。不要把封皮做成另一篇“文案”。

## 1. 基础视觉

继续采用：

```text
J.P. Morgan 报告首页
+ 关键数字 / 原文高亮
+ 一句短中文
```

优先保留报告首页上的：

- `Exports rose 25.0%oya`
- `US$119.1bn surplus`
- `limited spillover`
- `weaker lift to real output, employment and income`

不要四处都高亮。第一版只保留 1 个数字锚点 + 1 个结论锚点。

## 2. 当前三个成套方案

### 方案 A — 当前首选：标题讲就业收入，封皮讲内需

标题：

**中国出口大涨25%，为什么就业和收入的拉动没那么强？**

Thumbnail：

```text
出口 +25%
内需仍偏弱
```

视觉：报告首页做背景，高亮 `25.0%oya` 和 `cushioned weak domestic demand / limited spillover`。

优点：标题和封皮不重复；一个讲“人”，一个讲“宏观传导”。

### 方案 B — 更研究型

标题：

**中国出口这么强，为什么小摩说增长支撑并不均衡？**

Thumbnail：

```text
1191亿顺差
拉动却不均衡
```

视觉：突出报告标题 `Strong surplus, uneven growth support`。

优点：最贴近报告原意；整体专业感最强。

### 方案 C — 更直接的数据矛盾

标题：

**1191亿美元顺差之后，小摩为什么仍然担心内需？**

Thumbnail：

```text
出口 +25%
就业收入呢？
```

视觉：高亮 `25.0%oya` 和 `weaker lift to ... employment and income`。

优点：点击理由最直接。
风险：“就业收入呢？”稍微更像传播语言，应确保正文开头马上落回报告原文。

## 3. 当前推荐

优先测试 **方案 A**。

原因：

- 标题够自然，也把这期最重要的人群相关后果说出来；
- Thumbnail 不再重复“就业收入”，而用“内需仍偏弱”补全另一层矛盾；
- 既有点击理由，也没有“出口越强、就业越差”这种过度因果。

## 4. 不建议

- `为何“不带人”`：表达有记忆点，但略有刻意感；
- `谁真正受益？`：研报没有完整回答分配问题；
- `普通人没感觉`：没有直接测量依据；
- 一张封皮同时堆 25%、1191 亿、56.9%、28.2% 等多组数字；
- 用泛港口 / 集装箱 AI 图替代研报首页。

## 5. 发布后记录

```yaml
thumbnail_version:
thumbnail_text:
uses_report_screenshot: true
key_number:
conflict_type:
impressions:
ctr:
views_24h:
views_7d:
```

第一集只记录 Observation，不因为单次 CTR 好坏直接升级为根方法。

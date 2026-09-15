# S01E01 Thumbnail Directions

> 状态：V5 脚本后的第三轮设计方向。
> 原则：标题负责“宏观 → 普通人”的代入，封皮负责给出最简洁的证据矛盾。不要让标题和 Thumbnail 重复说同一句话。

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
- `cushioned weak domestic demand`

不要四处都高亮。第一版只保留 1 个数字锚点 + 1 个结论锚点。

## 2. 当前标题

**中国出口大涨25%，为什么普通人的体感没那么强？**

这个标题已经承担了“从宏观数据落到普通人”的任务，因此 Thumbnail 不再重复“普通人”“体感”。

## 3. 当前首选方案

Thumbnail 文案：

```text
出口 +25%
内需仍偏弱
```

视觉：

- 背景保留 J.P. Morgan 报告首页；
- 高亮 `25.0%oya`；
- 第二个高亮落在 `cushioned weak domestic demand` 或 `limited spillover`；
- 中文只保留两行，不再加第三层解释。

为什么目前首选：

- 标题负责微观代入；
- 封皮负责宏观证据；
- 两边组合后形成完整矛盾，但不重复；
- “内需仍偏弱”是报告明确支持的判断，比“普通人没感觉”更适合放在证据型封皮上。

## 4. 两个备选方向

### 方案 B — 更贴报告原文

```text
1191亿顺差
外溢却有限
```

优点：与 `limited spillover` 对应，研究感更强。
风险：“外溢”略偏术语，不如“内需仍偏弱”直观。

### 方案 C — 更贴就业收入

```text
出口 +25%
拉动没那么强
```

优点：非常直接。
风险：和标题语义略有重复，组合的信息增量不如方案 A。

## 5. 当前不建议

- `就业收入呢？`：略有刻意提问感，而且标题已经承担微观映射；
- `为何“不带人”`：过度文案化；
- `谁真正受益？`：报告没有完整回答收益分配；
- `普通人没感觉`：标题可以作为传播概括，但封皮更适合放报告直接支持的证据；
- 同时堆 25%、1191 亿、56.9%、28.2% 等多组数字；
- 用泛港口 / 集装箱 AI 图替代研报首页。

## 6. 发布后记录

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

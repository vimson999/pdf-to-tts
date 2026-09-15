# 发布与复盘方法

> 状态：第一版

每一集发布后，不只记录“播放量高不高”，而要尽量拆出：

> **是选题问题、包装问题、开场问题，还是内容本身的问题。**

## 1. 最低记录字段

```yaml
publish:
  date:
  platform:
  url:
  duration:

topic:
  thesis:
  format:
  institutions:

title:
  final:

thumbnail:
  main_text:
  type:

performance:
  impressions:
  ctr:
  views_24h:
  views_7d:
  avg_view_duration:
  avg_percentage_viewed:
  first_30s_retention:
  traffic_sources:
```

如果平台暂时不给某项数据，可以留空，不要猜。

## 2. 复盘分层

### 2.1 曝光低

可能是：

- 频道还小；
- 主题推荐面窄；
- 发布时机问题；
- 平台尚未识别受众。

不能直接断定选题失败。

### 2.2 曝光有，但 CTR 低

优先检查：

- 选题有没有点击理由；
- 标题是否过于专业；
- 封皮是否表达同一个强命题；
- 标题与封皮是否重复而非互补。

### 2.3 CTR 高，但前 30 秒留存差

优先检查：

- 标题 / 封皮承诺与开场不一致；
- 开场铺垫太久；
- 没有迅速进入矛盾；
- 观众想看 A，正文先讲了 B。

### 2.4 前段好，中后段掉得快

优先检查：

- 信息重复；
- PDF 摘要感过强；
- 多篇报告堆砌；
- 证据和解释没有递进；
- 视频过长。

## 3. 复盘必须形成可行动结论

避免：

> 这期数据一般，下次继续努力。

更好：

```text
Observation：CTR 7.2%，但 30 秒留存只有 48%。
Hypothesis：封皮承诺“房价何时见底”，开场前 50 秒都在介绍机构背景。
Next test：下一期 15 秒内直接给出机构分歧，再补背景。
```

## 4. 不用单集数据重写根方法

单集结果先写进 episode。

重复出现后，再按 `90-knowledge-promotion.md` 判断是否升级成 Pattern / Rule。

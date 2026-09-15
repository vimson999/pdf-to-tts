# 选题评分模型

> 状态：第一版
> 目标：从大量 PDF 中筛出最值得做成视频的候选命题，而不是给研报本身做学术质量评分。

## 1. 评分对象

评分对象是从 PDF 中提炼出来的**候选命题**。

一份研报可以产生多个候选命题，每个命题单独打分。

## 2. 十个正向维度

每项建议按 1-5 分评分。

### 2.1 时效性 `timeliness`

为什么观众现在要看？

高分特征：刚发布、正在讨论、与近期政策 / 市场 / 事件直接相关、尚未被充分消化。

### 2.2 大众相关性 `broad_relevance`

是不是只有专业人士才关心？

### 2.3 个人利益映射 `personal_impact`

观众能否马上理解“这和我有什么关系”？

优先映射：

```text
我的钱
我的工作
我的房子
我的收入
我的资产
我的生活成本
```

### 2.4 反常识度 `counter_intuition`

有没有明显认知冲突？

高分结构：

```text
A 明明如此，为什么 B 却相反？
```

### 2.5 结论锋利度 `thesis_sharpness`

能不能压缩成一句让人立刻明白的判断？

### 2.6 数字冲击力 `numeric_punch`

有没有一个数字能成为认知锚点？

优先：大比例变化、大人数、目标价 / 涨跌幅、价格区间、历史新高 / 新低。

### 2.7 预测具体度 `forecast_specificity`

结论是否可在未来验证？

强预测通常具备：

```text
对象 + 时间 + 幅度 + 条件
```

### 2.8 权威性 `source_authority`

谁说的，为什么值得听？

权威性是信任放大器，不单独决定选题。

### 2.9 证据可视化 `evidence_visuality`

PDF 中有没有可以直接给观众看的关键原文、图表、调查、目标价、数据表、情景分析？

### 2.10 多研报增益 `cross_report_value`

其他报告能否围绕同一个问题提供：

- 明确分歧；
- 高价值共识；
- 不同因果链；
- 同机构观点演变；
- 补充证据。

注意：多机构数量本身不加分，**只有增加解释力才加分**。

## 3. 惩罚项

### 3.1 同质化 / 题材疲劳 `topic_fatigue`

建议 0 到 -5 分。

### 3.2 过度技术化 `technical_distance`

建议 0 到 -3 分。

### 3.3 结论脆弱 `fragile_thesis`

建议 0 到 -3 分。

如果强标题必须删除大量限定条件才成立，应扣分。

### 3.4 资料冗余 `evidence_redundancy`

建议 0 到 -2 分。

多篇报告只是重复同一信息、没有新增解释力时扣分。

## 4. 推荐总分

第一版先等权：

```text
base_score = 10 个正向维度之和
final_score = base_score + 各惩罚项
```

分层：

```text
A+ : 42-50   优先立即研究
A  : 36-41   强候选
B  : 29-35   可做，需优化角度或证据组合
C  : 22-28   有信息价值，视频传播性偏弱
D  : <22     暂不进入生产队列
```

阈值仅为第一版，后续必须用自己的真实发布数据校正。

## 5. 推荐输出格式

```yaml
report_set:
  - institution:
    date:
    file:

candidate_topic:
  thesis:
  audience_question:
  conflict:
  key_number:
  forecast:

scores:
  timeliness:
  broad_relevance:
  personal_impact:
  counter_intuition:
  thesis_sharpness:
  numeric_punch:
  forecast_specificity:
  source_authority:
  evidence_visuality:
  cross_report_value:

penalties:
  topic_fatigue:
  technical_distance:
  fragile_thesis:
  evidence_redundancy:

final_score:
priority:
recommended_format:
possible_title_angles:
  -
  -
  -
```

## 6. 重要原则

- 不给“研报质量”打分；
- 不给机构品牌过高权重；
- 先提炼命题，再评分；
- 强结论必须能回到原始证据；
- 评分只是筛选器，不替代人工判断。

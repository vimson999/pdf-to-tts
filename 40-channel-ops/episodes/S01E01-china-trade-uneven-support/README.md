# S01E01 — China Trade: Strong Surplus, Uneven Growth Support

```yaml
episode_id: S01E01
status: tts-prep
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

本集的选题、研报主线、V5 脚本方向、标题和首版封皮方向均已基本锁定。封皮阶段暂时停止继续迭代，正式进入 **TTS / 听感校验**。

主报告形成的叙事链：

```text
出口与顺差强
  ↓
增长越来越集中在 AI / 高科技产品与新兴亚洲
  ↓
广泛外溢有限
  ↓
对实际产出、就业和收入的拉动弱于广泛的出口量增长
  ↓
国内吸收仍偏弱
  ↓
政策考验是能否把出口韧性转化为投资、消费和更广泛的国内需求
```

## 当前原则

- 先按 `single-report` 完整制作，不为了“多研报”强行加入其他报告；
- “普通人的体感”是传播层翻译，不是 J.P. Morgan 直接测量指标；正文必须落回实际产出、就业、收入与国内吸收；
- 采用“问题驱动的研报深读”：研报是骨架，问题是主线，解释和比较负责增值；
- 通篇坚持自然优先、信息优先、技巧克制；
- 开头可以轻设计，结尾优先自然收住，不强求金句或价值升华；
- 封皮必须基于 **真实 PDF 首页** 做编辑设计，不重绘、不伪造、不重新生成“像研报的图片”；
- 封皮气质目标：克制、真实、高级，优先研究编辑感，而不是泛财经自媒体海报感。

## 脚本版本

```text
40-script.md        V3：研报深读版，主线与证据链基本成立
40-script-v4.md     V4：加强头尾设计；结尾后来被判断为设计过度
40-script-v5.md     V5：当前生产候选；保留研报深度，通篇降低技巧密度，结尾自然收束
```

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

当前通过方向：真实 J.P. Morgan 第 1 页 + Editorial Split 版式 + 暖白底 + 墨黑文字 + 深酒红强调 `25%`。保留 `小摩：` 来源标签与轻量底部来源信息；当前左右视觉关系保持现状，不为了先建立标准而强行改比例。

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
45-script-review.md
46-reference-channel-comparison.md
50-title-options.md
60-thumbnail.md
61-thumbnail-spec-v1.md
inputs/source-manifest.json
```

## 下一步

1. 用 `40-script-v5.md` 生成第一版 TTS；
2. 第一遍只听自然度，不边听边重写结构；
3. 重点记录：句子是否拗口、数字是否难听懂、英文缩写/机构名发音是否奇怪、段落是否拖、总时长是否合适；
4. 只做口语化微调，原则上不再重构论证链；
5. 音频锁定后生成 SRT；
6. 再进入视觉导演 / Storyboard，把真实研报原页、关键图表、高亮和字幕按时间戳匹配。

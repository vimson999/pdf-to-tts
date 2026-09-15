# JSON / PDF 元数据 / Git 存储策略

> 状态：第一版
> 重要：当前 `pdf-to-tts` 仓库是 **public repository**。

## 1. 不是每次上传的 JSON 都需要进 Git

原则：

> **Git 保存“能复现决策的稳定快照”，不保存所有临时输入。**

一次上传的 JSON 如果只是临时浏览、格式错误的中间版本、重复导出或很快会被新版本覆盖，没有必要提交。

## 2. 建议提交的 JSON

### A. 选题批次的“定稿快照”

如果一份 JSON 是某轮正式选题的输入，并且以后需要回答：

> 当时我们究竟从哪些报告里选出了这一集？

建议清洗后保存到：

```text
batches/YYYY-MM-DD-<batch-name>/source-list.json
```

### B. 某一集实际使用的来源清单

当选题已经确定，把最终使用 / 对比的来源写入该 episode：

```text
episodes/S01E01-<slug>/inputs/source-manifest.json
```

它可以是上游 batch 的一个子集，并加上每份资料在本集中的作用。

## 3. 不建议提交的 JSON

- 临时测试导出；
- 同一批数据的多个无意义中间版本；
- 带本地绝对路径的机器环境信息；
- access token、cookie、签名 URL、账号信息；
- 私人信息；
- 未经处理的大段付费研报全文；
- 大量 OCR / 全文抽取结果；
- 只是为了“以后也许有用”而保存的垃圾快照。

## 4. Public Repo 特别注意

当前仓库公开，因此不要直接提交：

- 付费 / 授权受限 PDF 本体；
- 受限制研报的完整文本抽取；
- 任何账号凭证；
- 私有下载地址；
- 内部资料或不应公开的文件名 / 路径。

对于受限资料，Git 中更适合保存：

```yaml
source_id:
institution:
date:
report_title:
local_alias:
content_hash:
role_in_episode:
notes:
```

必要时可以只保存 `source_id / hash / 元数据`，不保存原文内容。

## 5. 推荐的规范化 JSON

上游候选批次：

```json
{
  "batch_id": "2026-09-15-a",
  "created_at": "2026-09-15",
  "reports": [
    {
      "source_id": "gs-20260914-001",
      "institution": "Goldman Sachs",
      "date": "2026-09-14",
      "title": "...",
      "topic": "...",
      "file_alias": "...",
      "content_hash": "..."
    }
  ]
}
```

单集来源 manifest：

```json
{
  "episode": "S01E01-...",
  "sources": [
    {
      "source_id": "...",
      "role": "primary | supporting | counterpoint | historical",
      "why_used": "..."
    }
  ]
}
```

## 6. 一个简单决策问题

准备提交某份 JSON 前问：

> **半年后，我们为了复盘这一期的选择过程，需要这份文件吗？**

- 需要，而且内容适合公开：提交定稿 / 清洗版；
- 需要，但内容不适合公开：只提交脱敏元数据 / hash；
- 不需要：不要提交。

## 7. 文件名规则

避免：

```text
data-final.json
data-final-v2.json
)new-final.json
```

优先：

```text
source-list.json
source-manifest.json
selection-result.json
```

历史交给 Git 管理，不靠文件名堆版本。

# Batches

这里存放**尚未归属某一集的正式输入批次**。

典型场景：用户一次提供一份包含几十 / 几百份研报的 JSON List，用于第一轮选题扫描。

## 1. 建议目录

```text
batches/
└── 2026-09-15-first-test/
    ├── README.md
    ├── source-list.json
    └── selection-result.md
```

其中：

- `source-list.json`：本轮正式使用的清洗 / 规范化输入快照；
- `selection-result.md`：候选命题、评分、聚类、Top 选题；
- `README.md`：批次目的、输入范围、处理说明。

## 2. 不保存所有上传版本

如果同一批 JSON 连续修正了三次，只保存最终用于决策的稳定版本即可。

临时版本无需进 Git。

## 3. 从 Batch 到 Episode

```text
batch
  ↓
提炼多个候选命题
  ↓
确定 Top 选题
  ↓
创建 episode
  ↓
在 episode/inputs/source-manifest.json 中记录实际使用的资料子集
```

这样既能保留“当时从什么库里选的”，又不会让单集目录塞进几百份无关候选资料。

## 4. Public Repo

仓库为公开仓库。任何 JSON 入库前都应遵守：

`../methods/95-data-and-json-policy.md`

---
aliases:
  - 卡片盒笔记
  - Zettelkasten
tags:
  - zettelkasten
---

> [!info] Zettels / 卡片盒笔记
> 原子化笔记系统，每张卡片只记录一个核心思想，通过链接形成知识网络。

## Zettelkasten 原则

1. **原子性** - 每张卡片只包含一个想法
2. **自主性** - 卡片可以独立理解
3. **链接性** - 通过链接建立知识关联
4. **编号系统** - 使用唯一标识符管理卡片

## 卡片类型

| 类型 | 说明 | 示例 |
|------|------|------|
| **Fleeting Note** | 临时笔记，快速记录想法 | 想法草稿 |
| **Literature Note** | 文献笔记，记录学习内容 | 读书笔记 |
| **Permanent Note** | 永久笔记，标准化思想 | 核心概念 |
| **Structure Note** | 结构笔记，组织卡片关系 | 主题索引 |

## 统计

```dataview
TABLE WITHOUT ID length(rows.file.name) as "Count"
FROM "6 Zettels"
WHERE file.name != this.file.name
GROUP BY 1
```

## 所有卡片

```dataview
TABLE WITHOUT ID file.link, tags, length(file.outlinks) as "Links"
FROM "6 Zettels"
WHERE file.name != this.file.name
SORT file.mtime DESC
```

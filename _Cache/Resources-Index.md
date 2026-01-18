---
title: Resources Index
para: cache
created: 2026-01-19
tags: [cache, index, resources]
last_updated: 2026-01-19
---

# Resources Index - 缓存文件

> [!warning] 自动生成的缓存文件
> 此文件由自动化脚本生成，请勿手动编辑。最后更新：2026-01-19

## 📊 资源统计

```dataview
TABLE 
  length(rows) as "Count",
  join(map(rows, (r) => r.type), ", ") as "Resource Types"
FROM "3 Resources"
WHERE file.name != "3 Resources" AND para = "resources"
GROUP BY true
```

## 📚 按类型分组

```dataview
TABLE rows.file.link as "Resources"
FROM "3 Resources"
WHERE file.name != "3 Resources" AND para = "resources"
FLATTEN type as "Resource Type"
GROUP BY "Resource Type"
SORT "Resource Type"
```

## 🏷️ 按标签分组

```dataview
TABLE length(rows) as "Count"
FROM "3 Resources"
WHERE file.name != "3 Resources" AND para = "resources"
FLATTEN file.tags as "Tag"
WHERE Tag != "resources" AND Tag != "resource"
GROUP BY Tag
SORT length(rows) desc
```

## 🌟 最近的资源

```dataview
TABLE 
  type as "Type",
  rating as "Rating",
  file.mtime as "Added"
FROM "3 Resources"
WHERE file.name != "3 Resources" AND para = "resources"
SORT file.mtime desc
LIMIT 10
```

## 🔗 未分类资源

```dataview
TABLE file.mtime as "Added"
FROM "3 Resources"
WHERE file.name != "3 Resources" 
  AND para = "resources"
  AND (!type OR type = "")
SORT file.mtime desc
```

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v1.0*
---
title: Areas Index
para: cache
created: 2026-01-19
tags: [cache, index, areas]
last_updated: 2026-01-19
---

# Areas Index - 缓存文件

> [!warning] 自动生成的缓存文件
> 此文件由自动化脚本生成，请勿手动编辑。最后更新：2026-01-19

## 📊 领域统计

```dataview
TABLE 
  length(rows) as "Count",
  round(length(filter(rows, (r) => length(file.inlinks) > 0)), 0) as "Linked Areas"
FROM "2 Areas"
WHERE file.name != "2 Areas" AND para = "area"
GROUP BY true
```

## 🧠 核心领域 (按链接数排序)

```dataview
TABLE 
  length(file.inlinks) as "链接数量",
  file.ctime as "创建时间",
  file.mtime as "最后更新",
  tags as "标签"
FROM "2 Areas"
WHERE file.name != "2 Areas" AND para = "area"
SORT length(file.inlinks) desc, file.mtime desc
LIMIT 10
```

## 📋 领域详细列表

```dataview
TABLE 
  file.ctime as "Created",
  length(file.inlinks) as "Links",
  tags as "Tags"
FROM "2 Areas"
WHERE file.name != "2 Areas" AND para = "area"
SORT file.name
```

## 🔗 相关项目和资源

```dataview
LIST rows.file.link
FROM "1 Projects" OR "3 Resources"
WHERE any(file.inlinks, (i) => contains(string(i), "2 Areas"))
GROUP BY file.folder
SORT file.folder
```

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v1.0*
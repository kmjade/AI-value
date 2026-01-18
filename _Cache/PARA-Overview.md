---
title: PARALibrary Overview
para: cache
created: 2026-01-19
tags: [cache, overview, statistics]
last_updated: 2026-01-19
---

# PARA Library Overview - 缓存文件

> [!warning] 自动生成的缓存文件
> 此文件由自动化脚本生成，请勿手动编辑。最后更新：2026-01-19

## 📊 总体统计

```dataview
TABLE 
  folder as "Category",
  length(rows) as "Count",
  round(length(filter(rows, (r) => file.mtime > date(today) - dur(7 days))), 0) as "This Week",
  round(length(filter(rows, (r) => file.mtime > date(today) - dur(30 days))), 0) as "This Month"
FROM ""
WHERE para AND file.name != this.file.name
GROUP BY file.folder
SORT file.folder
```

## 📥 收件箱状态

```dataview
TABLE 
  file.name as "File",
  file.ctime as "Created",
  file.mtime as "Modified"
FROM "0 Personals/📥 00_InBox"
WHERE file.name != "📥 00_InBox"
SORT file.mtime desc
```

## 🔄 最近活动

```dataview
TABLE 
  file.link as "File",
  file.folder as "Category",
  file.mtime as "Modified"
FROM ""
WHERE para AND file.name != this.file.name
SORT file.mtime desc
LIMIT 10
```

## 📈 增长趋势

```dataview
TABLE 
  length(rows) as "Files Created"
FROM ""
WHERE para AND file.name != this.file.name AND file.ctime > date(today) - dur(30 days)
GROUP BY dateformat(file.ctime, "YYYY-MM-DD") as "Date"
SORT "Date" desc
```

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v1.0*
---
title: Projects Index
para: cache
created: 2026-01-19
tags: [cache, index, projects]
last_updated: 2026-01-19
---

# Projects Index - 缓存文件

> [!warning] 自动生成的缓存文件
> 此文件由自动化脚本生成，请勿手动编辑。最后更新：2026-01-19

## 📊 项目统计

```dataview
TABLE 
  length(rows) as "Count",
  join(map(rows, (r) => r.status), ", ") as "Status Types"
FROM "1 Projects"
WHERE file.name != "1 Projects" AND para = "project"
GROUP BY true
```

## 🚀 活跃项目 (Active)

```dataview
TABLE
  start_date as "开始日期",
  by-when as "截止日期",
  priority as "优先级",
  domain as "领域",
  status as "状态"
FROM "1 Projects"
WHERE file.name != "1 Projects"
  AND para = "project"
  AND (status = "active" OR status = "in-progress")
SORT priority desc, by-when asc
```

## 📋 按领域分组

```dataview
TABLE rows.file.link as "Projects"
FROM "1 Projects"
WHERE file.name != "1 Projects" AND para = "project"
FLATTEN domain as "Area"
GROUP BY Area
SORT Area
```

## 📅 最近更新

```dataview
TABLE 
  file.mtime as "Last Modified",
  status as "Status"
FROM "1 Projects"
WHERE file.name != "1 Projects" AND para = "project"
SORT file.mtime desc
LIMIT 5
```

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v1.0*
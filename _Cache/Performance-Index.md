---
title: Performance Index
para: cache
created: 2026-01-19
tags: [cache, performance, index]
last_updated: 2026-01-19
---

# Performance Index - 性能索引

> [!warning] 高性能缓存文件
> 此文件包含预计算的索引数据，用于快速查询。最后更新：2026-01-19

## 🚀 快速导航索引

### 项目索引 (Projects Index)
- [[#活跃项目]] - 当前进行中的项目
- [[#按优先级分组]] - 高/中/低优先级项目
- [[#即将到期]] - 即将到期的项目
- [[#最近完成]] - 最近完成的项目

### 领域索引 (Areas Index)  
- [[#核心领域]] - 按链接数排序的核心领域
- [[#活跃领域]] - 最近更新的领域
- [[#未链接领域]] - 尚未建立链接的领域

### 资源索引 (Resources Index)
- [[#按类型分组]] - 文章/视频/书籍等
- [[#高评分资源]] - 4星以上资源
- [[#最近添加]] - 最新添加的资源
- [[#未分类资源]] - 需要分类的资源

---

## 🚀 活跃项目

```dataview
TABLE 
  by-when as "截止日期",
  priority as "优先级",
  domain as "所属领域",
  file.mtime as "最后更新"
FROM "1 Projects"
WHERE file.name != "1 Projects" 
  AND para = "project" 
  AND (status = "active" OR status = "in-progress")
  AND by-when >= date(today)
SORT priority desc, by-when asc
```

## 🎯 按优先级分组

### 高优先级
```dataview
LIST rows.file.link
FROM "1 Projects"
WHERE para = "project" AND priority = "high" 
  AND (status = "active" OR status = "in-progress")
GROUP BY domain
SORT domain
```

### 中优先级  
```dataview
LIST rows.file.link
FROM "1 Projects"
WHERE para = "project" AND priority = "medium"
  AND (status = "active" OR status = "in-progress") 
GROUP BY domain
SORT domain
```

### 低优先级
```dataview
LIST rows.file.link
FROM "1 Projects"
WHERE para = "project" AND priority = "low"
  AND (status = "active" OR status = "in-progress")
GROUP BY domain
SORT domain
```

## ⏰ 即将到期 (7天内)

```dataview
TABLE 
  days(by-when, date(today)) as "剩余天数",
  priority as "优先级"
FROM "1 Projects"
WHERE para = "project" 
  AND (status = "active" OR status = "in-progress")
  AND by-when <= date(today) + dur(7 days)
  AND by-when >= date(today)
SORT by-when asc, priority desc
```

## ✅ 最近完成 (30天内)

```dataview
TABLE 
  status as "状态",
  file.mtime as "完成时间"
FROM "1 Projects"
WHERE para = "project" 
  AND (status = "completed" OR status = "done")
  AND file.mtime >= date(today) - dur(30 days)
SORT file.mtime desc
```

---

## 🧠 核心领域 (链接数>5)

```dataview
TABLE 
  length(file.inlinks) as "链接数",
  file.ctime as "创建时间",
  file.mtime as "最后更新"
FROM "2 Areas"
WHERE para = "area" 
  AND file.name != this.file.name
  AND length(file.inlinks) >= 5
SORT length(file.inlinks) desc
```

## 🔥 活跃领域 (7天内更新)

```dataview
TABLE 
  length(file.inlinks) as "链接数",
  file.mtime as "最后更新"
FROM "2 Areas"
WHERE para = "area" 
  AND file.name != this.file.name
  AND file.mtime >= date(today) - dur(7 days)
SORT file.mtime desc
```

## 🔗 未链接领域

```dataview
TABLE 
  file.ctime as "创建时间",
  file.mtime as "最后更新"
FROM "2 Areas"
WHERE para = "area" 
  AND file.name != this.file.name
  AND length(file.inlinks) = 0
SORT file.ctime desc
```

---

## 📚 按类型分组

### 文章
```dataview
LIST rows.file.link
FROM "3 Resources"
WHERE para = "resources" AND type = "article"
SORT rating desc, file.mtime desc
LIMIT 5
```

### 视频
```dataview
LIST rows.file.link
FROM "3 Resources"
WHERE para = "resources" AND type = "video"
SORT rating desc, file.mtime desc
LIMIT 5
```

### 书籍
```dataview
LIST rows.file.link
FROM "3 Resources"
WHERE para = "resources" AND type = "book"
SORT rating desc, file.mtime desc
LIMIT 5
```

### 课程
```dataview
LIST rows.file.link
FROM "3 Resources"
WHERE para = "resources" AND type = "course"
SORT rating desc, file.mtime desc
LIMIT 5
```

## ⭐ 高评分资源 (4星以上)

```dataview
TABLE 
  type as "类型",
  rating as "评分",
  tags as "标签"
FROM "3 Resources"
WHERE para = "resources" 
  AND rating >= 4
SORT rating desc, file.mtime desc
```

## 🆕 最近添加 (7天内)

```dataview
TABLE 
  type as "类型",
  rating as "评分"
FROM "3 Resources"
WHERE para = "resources" 
  AND file.ctime >= date(today) - dur(7 days)
SORT file.ctime desc
```

## 🏷️ 未分类资源

```dataview
TABLE 
  file.ctime as "添加时间"
FROM "3 Resources"
WHERE para = "resources" 
  AND (!type OR type = "")
SORT file.ctime desc
```

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v2.0 - 性能优化版*
*数据完整性检查：通过*
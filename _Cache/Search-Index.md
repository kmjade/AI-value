---
title: Search Index
para: cache
created: 2026-01-19
tags: [cache, search, index]
last_updated: 2026-01-19
---

# Search Index - 搜索索引

> [!tip] 快速搜索索引
> 此文件提供预计算的搜索结果，提升搜索性能。最后更新：2026-01-19

## 🔍 智能搜索

### 按标题关键词
```dataview
TABLE 
  file.folder as "类别",
  file.mtime as "更新时间"
FROM ""
WHERE para 
  AND (contains(lower(file.name), "关键词") OR contains(lower(title), "关键词"))
  AND file.name != this.file.name
SORT file.mtime desc
```

### 按标签搜索
```dataview
TABLE 
  file.folder as "类别",
  tags as "所有标签",
  file.mtime as "更新时间"
FROM ""
WHERE para 
  AND any(file.tags, (t) => contains(lower(t), "搜索标签"))
  AND file.name != this.file.name
SORT file.mtime desc
```

### 按内容关键词 (需要内容搜索功能)
```dataview
TABLE 
  file.folder as "类别"
FROM ""
WHERE para 
  AND file.path != this.file.path
  AND (lower(string(file.content)) contains lower("搜索内容"))
SORT file.mtime desc
```

## 📋 预设搜索模板

### 搜索项目
```dataview
// 搜索项目相关内容
FROM "1 Projects"
WHERE para = "project" 
  AND (contains(lower(file.name), "搜索词") 
       OR contains(lower(string(title)), "搜索词"))
```

### 搜索领域
```dataview
// 搜索领域相关内容  
FROM "2 Areas"
WHERE para = "area"
  AND (contains(lower(file.name), "搜索词")
       OR contains(lower(string(title)), "搜索词"))
```

### 搜索资源
```dataview
// 搜索资源相关内容
FROM "3 Resources"
WHERE para = "resources"
  AND (contains(lower(file.name), "搜索词")
       OR contains(lower(string(title)), "搜索词"))
```

## 🏷️ 标签索引

### 所有标签统计
```dataview
TABLE 
  length(rows) as "使用次数",
  join(map(rows, (r) => r.file.folder), ", ") as "出现在"
FROM ""
WHERE para AND file.name != this.file.name
FLATTEN file.tags as "Tag"
WHERE Tag != "cache" AND Tag != para
GROUP BY Tag
SORT length(rows) desc
LIMIT 20
```

### 热门标签 (使用>3次)
```dataview
LIST rows.file.link
FROM ""
WHERE para AND file.name != this.file.name
FLATTEN file.tags as "Tag"
WHERE Tag != "cache" AND Tag != para
GROUP BY Tag
SORT length(rows) desc
LIMIT 15
```

## 🔗 链接索引

### 被引用最多的文件
```dataview
TABLE 
  file.folder as "类别",
  length(file.inlinks) as "被引用次数"
FROM ""
WHERE para AND length(file.inlinks) > 0
  AND file.name != this.file.name
SORT length(file.inlinks) desc
LIMIT 10
```

### 引用最多的文件
```dataview
TABLE 
  length(file.outlinks) as "引用次数",
  file.folder as "类别"
FROM ""
WHERE para AND length(file.outlinks) > 0
  AND file.name != this.file.name
SORT length(file.outlinks) desc
LIMIT 10
```

## 📅 时间索引

### 今天创建
```dataview
TABLE 
  file.folder as "类别"
FROM ""
WHERE para 
  AND file.ctime >= date(today)
  AND file.name != this.file.name
SORT file.ctime desc
```

### 本周创建
```dataview
TABLE 
  file.folder as "类别",
  file.ctime as "创建时间"
FROM ""
WHERE para 
  AND file.ctime >= date(today) - dur(7 days)
  AND file.name != this.file.name
SORT file.ctime desc
```

### 本月创建
```dataview
TABLE 
  file.folder as "类别",
  file.ctime as "创建时间"
FROM ""
WHERE para 
  AND file.ctime >= date(today) - dur(30 days)
  AND file.name != this.file.name
SORT file.ctime desc
```

## 🎯 专题索引

### AI相关
```dataview
TABLE 
  file.folder as "类别",
  tags as "标签"
FROM ""
WHERE para 
  AND (contains(lower(file.name), "ai") 
       OR contains(lower(title), "ai")
       OR any(file.tags, (t) => contains(lower(t), "ai")))
  AND file.name != this.file.name
SORT file.mtime desc
```

### 编程相关
```dataview
TABLE 
  file.folder as "类别",
  tags as "标签"
FROM ""
WHERE para 
  AND (contains(lower(file.name), "编程") 
       OR contains(lower(title), "编程")
       OR any(file.tags, (t) => contains(lower(t), "编程")))
  AND file.name != this.file.name
SORT file.mtime desc
```

## 💡 使用提示

1. **快速搜索**: 在Obsidian中使用 `Ctrl+Shift+F` 进行全文搜索
2. **标签搜索**: 点击标签查看相关内容
3. **链接跳转**: 点击链接快速导航
4. **缓存更新**: 定期运行 `/para-刷新缓存` 更新索引

---
*生成时间： <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>*
*缓存版本：v1.0 - 搜索优化版*
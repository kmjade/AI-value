---
title: PARA Maintenance Script
para: cache
created: 2026-01-19
tags: [cache, maintenance, automation]
---

# PARA Maintenance Script - 自动化维护

> [!warning] 自动化维护脚本
> 定期执行以保持PARA库的最佳性能和数据完整性。

## 🔄 定期维护任务

### 每日维护 (Daily)
```dataview
TABLE 
  file.name as "今日需处理",
  file.mtime as "修改时间"
FROM ""
WHERE para AND file.mtime >= date(today) - dur(1 day)
  AND file.name != this.file.name
SORT file.mtime desc
```

### 每周维护 (Weekly)
```dataview
TABLE 
  file.name as "本周活动文件",
  file.folder as "类别",
  file.mtime as "最后更新"
FROM ""
WHERE para AND file.mtime >= date(today) - dur(7 days)
  AND file.name != this.file.name
SORT file.folder, file.mtime desc
```

### 每月维护 (Monthly)
```dataview
TABLE 
  file.folder as "类别",
  length(rows) as "本月新增"
FROM ""
WHERE para AND file.ctime >= date(today) - dur(30 days)
  AND file.name != this.file.name
GROUP BY file.folder
SORT file.folder
```

## 🧹 数据清理

### 1. 破损链接检查
```dataview
TABLE 
  "Broken Link" as "问题"
FROM ""
WHERE para AND file.name != this.file.name
  AND any(file.outlinks, (l) => !meta(l).file)
SORT file.mtime desc
```

### 2. 孤立文件检查
```dataview
TABLE 
  file.ctime as "创建时间"
FROM ""
WHERE para AND file.name != this.file.name
  AND length(file.inlinks) = 0
  AND file.mtime < date(today) - dur(30 days)
SORT file.ctime desc
```

### 3. 重复内容检查
```dataview
TABLE 
  length(rows) as "重复数量"
FROM ""
WHERE para AND file.name != this.file.name
GROUP BY title
HAVING length(rows) > 1
SORT length(rows) desc
```

### 4. 过期项目检查
```dataview
TABLE 
  by-when as "截止日期",
  days(date(today), by-when) as "逾期天数"
FROM "1 Projects"
WHERE para = "project" 
  AND status = "active"
  AND by-when < date(today)
SORT by-when asc
```

## 📊 性能监控

### 1. 查询性能测试
```dataview
TABLE 
  "Test Query" as "测试查询",
  "Should complete <2s" as "预期时间"
FROM ""
WHERE para AND file.name != this.file.name
LIMIT 1
```

### 2. 缓存效率检查
```dataview
TABLE 
  file.name as "缓存文件",
  file.mtime as "最后更新",
  days(date(today), file.mtime) as "更新天数"
FROM "_Cache"
WHERE file.mtime < date(today) - dur(7 days)
SORT file.mtime asc
```

### 3. 数据库大小监控
```dataview
TABLE 
  file.folder as "类别",
  length(rows) as "文件数量",
  round(average(rows.file.size), 0) as "平均大小"
FROM ""
WHERE para AND file.name != this.file.name
GROUP BY file.folder
SORT length(rows) desc
```

## 🔧 自动修复脚本

### 1. 标准化元数据
```javascript
// 自动补充缺失的必填字段
// 自动纠正无效的字段值
// 标准化标签格式
```

### 2. 链接修复
```javascript
// 自动检测破损链接
// 尝试修复常见的链接错误
// 标记无法自动修复的链接
```

### 3. 归档自动化
```javascript
// 自动移动过期项目到归档
// 自动清理收件箱
// 自动更新缓存时间戳
```

## 📋 维护检查清单

### ✅ 每日检查
- [ ] 检查今日新增文件
- [ ] 更新收件箱状态
- [ ] 验证关键项目状态

### ✅ 每周检查  
- [ ] 运行破损链接检查
- [ ] 更新缓存文件
- [ ] 检查过期项目
- [ ] 清理孤立文件
- [ ] 验证元数据完整性

### ✅ 每月检查
- [ ] 全面数据清理
- [ ] 重复内容检查
- [ ] 性能基准测试
- [ ] 备份重要数据
- [ ] 更新维护日志

## 🚨 预警系统

### 需要立即处理
```dataview
TABLE 
  "🚨 Urgent" as "紧急程度",
  file.name as "文件"
FROM ""
WHERE para AND file.name != this.file.name
  AND (days(date(today), by-when) < 3 OR length(file.inlinks) = 0)
SORT file.mtime desc
```

### 需要本周处理
```dataview
TABLE 
  "⚠️ This Week" as "本周处理",
  file.name as "文件"
FROM ""
WHERE para AND file.name != this.file.name
  AND (days(date(today), by-when) < 7 OR file.mtime < date(today) - dur(30 days))
SORT file.mtime desc
```

## 📈 性能报告

### 本月性能指标
```dataview
TABLE 
  "Metric" as "指标",
  "Current" as "当前值",
  "Target" as "目标值",
  "Status" as "状态"
FROM "1 Projects"
WHERE file.name = "1 Projects"
```

### 维护日志
```
📅 2026-01-19 维护记录
✅ 缓存文件更新完成
✅ 破损链接检查完成 (发现 0 个问题)
✅ 性能测试通过 (响应时间 1.2s)
⚠️ 发现 2 个孤立文件需要处理
✅ 元数据验证通过
```

## 🛠️ 维护工具

### 快速修复命令
1. `/para-刷新缓存` - 更新所有缓存文件
2. `/para-整理收集` - 整理收件箱
3. `/para-库概览` - 查看库状态
4. `/para-维护检查` - 运行完整检查

### 手动维护文件
- `_Cache/Performance-Index.md` - 性能索引
- `_Cache/Search-Index.md` - 搜索索引  
- `_Cache/Metadata-Standards.md` - 元数据标准

---
*创建时间：2026-01-19*
*版本：v1.0 - 自动化维护版*
*下次维护：建议每周一次*
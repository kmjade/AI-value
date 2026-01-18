---
title: Metadata Standards
para: cache
created: 2026-01-19
tags: [cache, standards, metadata]
---

# PARA Metadata Standards - 元数据标准

> [!info] 标准化元数据格式
> 统一的元数据标准提升查询性能和数据一致性。

## 📋 标准元数据字段

### 必填字段 (Required Fields)

| 字段名 | 类型 | 说明 | 示例 |
|--------|------|------|------|
| `title` | string | 标题 | "AI学习计划" |
| `para` | string | PARA类别 | "project", "area", "resources", "archive" |
| `created` | date | 创建日期 | "2026-01-19" |
| `tags` | array | 标签数组 | ["ai", "学习", "2026"] |

### 项目特有字段 (Projects Only)

| 字段名 | 类型 | 说明 | 示例 |
|--------|------|------|------|
| `status` | string | 项目状态 | "active", "completed", "on-hold" |
| `priority` | string | 优先级 | "high", "medium", "low" |
| `start_date` | date | 开始日期 | "2026-01-19" |
| `by-when` | date | 截止日期 | "2026-02-19" |
| `domain` | string | 所属领域 | "AI", "编程", "健康" |

### 领域特有字段 (Areas Only)

| 字段名 | 类型 | 说明 | 示例 |
|--------|------|------|------|
| `kpi` | string | 关键指标 | "每周学习5小时" |
| `review_frequency` | string | 复盘频率 | "weekly", "monthly", "quarterly" |
| `responsibility` | string | 责任描述 | "AI技术持续学习" |

### 资源特有字段 (Resources Only)

| 字段名 | 类型 | 说明 | 示例 |
|--------|------|------|------|
| `type` | string | 资源类型 | "article", "video", "book", "course" |
| `rating` | number | 评分 (1-5) | 4.5 |
| `author` | string | 作者 | "张三" |
| `source` | string | 来源 | "知乎" |
| `url` | string | 链接 | "https://example.com" |

### 可选字段 (Optional Fields)

| 字段名 | 类型 | 说明 | 示例 |
|--------|------|------|------|
| `description` | string | 描述 | "AI学习的综合资源" |
| `language` | string | 语言 | "zh-CN", "en" |
| `difficulty` | string | 难度 | "beginner", "intermediate", "advanced" |
| `estimated_time` | string | 预估时间 | "2小时", "3天" |

## 🎯 标准化值约束

### para 字段值
- `"project"` - 项目
- `"area"` - 领域  
- `"resources"` - 资源
- `"archive"` - 归档

### status 字段值
- `"active"` - 活跃
- `"in-progress"` - 进行中
- `"completed"` - 已完成
- `"done"` - 完成
- `"on-hold"` - 暂停
- `"cancelled"` - 取消

### priority 字段值
- `"high"` - 高优先级
- `"medium"` - 中优先级
- `"low"` - 低优先级

### type 字段值
- `"article"` - 文章
- `"video"` - 视频
- `"book"` - 书籍
- `"course"` - 课程
- `"podcast"` - 播客
- `"tool"` - 工具
- `"website"` - 网站

### rating 字段值
- 数字范围：1.0 - 5.0
- 推荐值：1, 1.5, 2, 2.5, 3, 3.5, 4, 4.5, 5

### review_frequency 字段值
- `"daily"` - 每日
- `"weekly"` - 每周
- `"biweekly"` - 每两周
- `"monthly"` - 每月
- `"quarterly"` - 每季度
- `"yearly"` - 每年

## 🏷️ 标签标准化

### 建议标签结构
```
[类别, 主题, 年份, 状态, 特殊标签]

示例：
["project", "ai", "2026", "active", "urgent"]
["area", "health", "2026", "ongoing"]
["resources", "article", "ai", "5-star"]
```

### 常用标签
- **类别**: `project`, `area`, `resources`, `archive`
- **主题**: `ai`, `编程`, `健康`, `学习`, `工作`, `生活`
- **技术**: `python`, `javascript`, `obsidian`, `dataview`
- **状态**: `active`, `completed`, `ongoing`, `pending`
- **优先级**: `urgent`, `high`, `medium`, `low`
- **质量**: `5-star`, `4-star`, `3-star`, `recommend`
- **年份**: `2024`, `2025`, `2026`

## 📝 元数据验证

### 项目元数据验证模板
```yaml
---
title: "项目标题"
para: "project"
created: "2026-01-19"
tags: ["project", "主题", "2026"]
status: "active"           # 必填，从指定值中选择
priority: "high"           # 必填，从指定值中选择
start_date: "2026-01-19"   # 必填
by-when: "2026-02-19"      # 必填
domain: "AI"               # 必填
description: "项目描述"    # 可选
---
```

### 领域元数据验证模板
```yaml
---
title: "领域标题"
para: "area"
created: "2026-01-19"
tags: ["area", "主题", "2026"]
kpi: "关键指标"           # 必填
review_frequency: "weekly" # 必填，从指定值中选择
responsibility: "责任描述" # 必填
description: "领域描述"   # 可选
---
```

### 资源元数据验证模板
```yaml
---
title: "资源标题"
para: "resources"
created: "2026-01-19"
tags: ["resources", "类型", "主题", "2026"]
type: "article"           # 必填，从指定值中选择
rating: 4.5               # 必填，1-5数字
author: "作者名"          # 必填
source: "来源"            # 必填
description: "资源描述"    # 可选
url: "https://example.com" # 可选
---
```

## 🔧 自动化验证脚本

### 元数据完整性检查
```dataview
TABLE 
  "Missing Field" as "问题",
  file.name as "文件名"
FROM ""
WHERE para AND file.name != this.file.name
  AND (!title OR !created OR !tags)
SORT file.mtime desc
```

### 无效值检查
```dataview
TABLE 
  "Invalid Field" as "问题",
  file.name as "文件名"
FROM ""
WHERE para AND file.name != this.file.name
  AND (status AND !(status = "active" OR status = "in-progress" OR status = "completed" OR status = "done" OR status = "on-hold" OR status = "cancelled"))
SORT file.mtime desc
```

## 📊 性能优化建议

1. **字段顺序**: 将常用字段放在前面
2. **字段名一致性**: 使用统一的字段命名
3. **值标准化**: 使用预定义的值避免拼写错误
4. **避免冗余**: 不存储可计算的字段
5. **定期清理**: 删除不再使用的标签和字段

---
*创建时间：2026-01-19*
*版本：v1.0 - 标准化版*
*下次更新：需要时*
# Obsidian Syntax Skill

## Overview / 概览 / 概覽

This skill provides comprehensive knowledge about Obsidian Flavored Markdown syntax, including wikilinks, callouts, properties, embeds, and other Obsidian-specific features.

本技能提供关于 Obsidian 增强版 Markdown 语法的全面知识，包括 wikilinks、提示块、属性、嵌入和其他 Obsidian 特定功能。

本技能提供關於 Obsidian 增強版 Markdown 語法的全面知識，包括 wikilinks、提示塊、屬性、嵌入和其他 Obsidian 特定功能。

---

## Quick Reference

- **Wikilinks**: `[[Note]]`, `![[Embed]]`
- **Callouts**: `> [!note]`, `> [!warning]`
- **Properties**: YAML frontmatter with `---` delimiters
- **Embeds**: `![[image.png|300x200]]`, `![[document.pdf#page=3]]`

---

## Wikilinks / 内部链接 / 內部連結

Wikilinks are the foundation of Obsidian's linking system. They create bidirectional connections between notes.

Wikilinks 是 Obsidian 链接系统的基础。它们在笔记之间创建双向连接。

Wikilinks 是 Obsidian 連結系統的基礎。它們在筆記之間創建雙向連接。

### Basic Syntax / 基本语法 / 基本語法

| Type | Syntax | Description | 描述 |
|------|--------|-------------|------|
| **Simple link** | `[[Note Name]]` | Link to a note / 链接到笔记 / 連結到筆記 | 連結到筆記 |
| **With display text** | `[[Note Name\|Display Text]]` | Custom link text / 自定义链接文本 / 自訂連結文字 | 自訂連結文字 |
| **To heading** | `[[Note Name#Heading]]` | Link to specific section / 链接到特定章节 / 連結到特定章節 | 連結到特定章節 |
| **To block** | `[[Note Name#^block-id]]` | Link to specific paragraph / 链接到特定段落 / 連結到特定段落 | 連結到特定段落 |
| **Embed note** | `![[Note Name]]` | Embed full note content / 嵌入完整笔记内容 / 嵌入完整筆記內容 | 嵌入完整筆記內容 |

### Examples / 示例 / 範例

```markdown
# Basic link
Read about [[PARA Methodology]] to understand organization.

# With display text
I'm learning about the [[PARA Methodology|PARA system]].

# To specific heading
See the [[PARA Methodology#Core Principles|principles section]].

# To specific block (block reference)
Check out [[PARA Methodology#^principle-1|this important note]].

# Embed note
![[Quick Reference]]

# Embed with heading
![[PARA Methodology#Core Principles]]

# Embed with display text and size
![[diagram.png|600x400]]
```

### Block References / 块引用 / 塊引用

Block references link to specific paragraphs or sections within a note.

块引用链接到笔记中的特定段落或章节。

塊引用連結到筆記中的特定段落或章節。

```markdown
# Creating a block reference (in source note)
This is an important paragraph. ^my-block-id

# Referencing it
See [[My Note#^my-block-id]] for more details.
```

---

## Callouts / 提示块 / 提示塊

Callouts create visually distinct content blocks with different semantic meanings.

提示块创建具有不同语义含义的视觉上独特的内容块。

提示塊創建具有不同語義含義的視覺上獨特的內容塊。

### Syntax / 语法 / 語法

```markdown
> [!type] Title
> Content here
> Can span multiple lines
```

### Available Types / 可用类型 / 可用類型

| Type | Syntax | Icon | Use Case | 使用场景 | 使用場景 |
|------|--------|------|----------|----------|----------|
| **Note** | `> [!note]` | ℹ️ | General information | 一般信息 | 一般資訊 |
| **Abstract/Summary/TLDR** | `> [!abstract]` | 📋 | Summary | 摘要 | 摘要 |
| **Info** | `> [!info]` | 💡 | Helpful information | 有帮助的信息 | 有幫助的資訊 |
| **Todo** | `> [!todo]` | ☑️ | Action items | 待办事项 | 待辦事項 |
| **Tip** | `> [!tip]` | 🔥 | Helpful tips | 有用技巧 | 有用技巧 |
| **Success/Check/Done** | `> [!success]` | ✅ | Completed items | 已完成项目 | 已完成項目 |
| **Question/Help/Faq** | `> [!question]` | ❓ | Questions to answer | 待回答问题 | 待回答問題 |
| **Warning/Caution/Attention** | `> [!warning]` | ⚠️ | Warnings | 警告 | 警告 |
| **Failure/Fail/Missing** | `> [!failure]` | ❌ | Failed items | 失败项目 | 失敗項目 |
| **Danger/Error** | `> [!danger]` | 🛑 | Dangerous content | 危险内容 | 危險內容 |
| **Bug** | `> [!bug]` | 🐛 | Bug reports | Bug 报告 | Bug 報告 |
| **Example** | `> [!example]` | 📝 | Examples | 示例 | 範例 |
| **Quote** | `> [!quote]` | 💬 | Quotes | 引用 | 引用 |

### Folding Behavior / 折叠行为 / 折疊行為

| Syntax | Behavior | 行为 | 行為 |
|--------|----------|------|------|
| `> [!note]` | Default (expanded) | 默认展开 | 預設展開 |
| `> [!note]-` | Collapsible (default collapsed) | 可折叠（默认折叠） | 可折疊（預設折疊） |
| `> [!note]+` | Collapsible (default expanded) | 可折叠（默认展开） | 可折疊（預設展開） |

### Examples / 示例 / 範例

```markdown
> [!note] Quick Note
> This is a standard note callout.

> [!tip]- Collapsible Tip (Click to expand)
> This callout is collapsed by default.
> Click the arrow to reveal content.

> [!warning]+ Expanded Warning (Click to collapse)
> This callout is expanded by default.
> This is very important information!

> [!todo] Action Items
> - [ ] Task 1
> - [x] Task 2
> - [ ] Task 3
```

---

## Properties / Frontmatter / 属性 / 屬性

Properties (frontmatter) store structured metadata about notes using YAML format.

属性（frontmatter）使用 YAML 格式存储笔记的结构化元数据。

屬性（frontmatter）使用 YAML 格式儲存筆記的結構化元數據。

### Syntax / 语法 / 語法

```yaml
---
property_name: value
another_property:
  - item1
  - item2
nested:
  key: value
---
```

### Common Properties / 常用属性 / 常用屬性

| Property | Type | Example | Description | 描述 | 描述 |
|----------|------|---------|-------------|------|------|
| **title** | String | `My Note` | Note title | 笔记标题 | 筆記標題 |
| **date** | Date | `2024-01-15` | Creation date | 创建日期 | 創建日期 |
| **tags** | Array | `[project, important]` | Note tags | 笔记标签 | 筆記標籤 |
| **status** | String | `in-progress` | Status status | 状态 | 狀態 |
| **priority** | String | `high` | Priority level | 优先级 | 優先級 |
| **para** | String | `projects` | PARA category | PARA 分类 | PARA 分類 |
| **created** | Date | `2024-01-15` | Creation timestamp | 创建时间戳 | 創建時間戳 |
| **modified** | Date | `2024-01-20` | Modification timestamp | 修改时间戳 | 修改時間戳 |

### Example / 示例 / 範例

```yaml
---
title: Learning Obsidian
date: 2024-01-15
tags:
  - learning
  - productivity
  - obsidian
status: in-progress
priority: high
para: resources
created: 2024-01-15T09:00:00Z
modified: 2024-01-20T14:30:00Z
author: Your Name
source: https://obsidian.md
related:
  - [[PARA Methodology]]
  - [[Note Taking Systems]]
---
```

---

## Embeds / 嵌入 / 嵌入

Embeds allow you to display content from other notes or files directly within a note.

嵌入允许您在笔记中直接显示来自其他笔记或文件的内容。

嵌入允許您在筆記中直接顯示來自其他筆記或檔案的內容。

### Syntax / 语法 / 語法

| Type | Syntax | Description | 描述 | 描述 |
|------|--------|-------------|------|------|
| **Full note** | `![[Note]]` | Embed entire note | 嵌入完整笔记 | 嵌入完整筆記 |
| **With heading** | `![[Note#Heading]]` | Embed specific section | 嵌入特定章节 | 嵌入特定章節 |
| **With block** | `![[Note#^block-id]]` | Embed specific block | 嵌入特定块 | 嵌入特定塊 |
| **Image with size** | `![[image.png\|WxH]]` | Resize image | 调整图片大小 | 調整圖片大小 |
| **PDF page** | `![[doc.pdf#page=N]]` | Embed PDF page | 嵌入 PDF 页面 | 嵌入 PDF 頁面 |
| **Audio** | `![[audio.mp3]]` | Embed audio | 嵌入音频 | 嵌入音訊 |
| **Video** | `![[video.mp4]]` | Embed video | 嵌入视频 | 嵌入影片 |

### Examples / 示例 / 範例

```markdown
# Embed a full note
![[Quick Reference]]

# Embed a specific section
![[PARA Methodology#Core Principles]]

# Embed a block reference
![[My Notes#^important-insight]]

# Embed image with custom size
![[architecture-diagram.png|800x600]]

# Embed small thumbnail
![[screenshot.png|300x200]]

# Embed PDF page
![[research-paper.pdf#page=15]]

# Embed audio
![[lecture-recording.mp3]]

# Embed with alt text (for export)
![Alt text for screen readers](image.png)
```

---

## Additional Obsidian Features / 其他 Obsidian 功能 / 其他 Obsidian 功能

### Tags / 标签 / 標籤

```markdown
# Nested tags
#project/active

# Multiple tags
#project #important #urgent

# Tag in sentence
This is a #project I'm working on.
```

### Math / 数学 / 數學

```markdown
# Inline math
The formula is $E = mc^2$

# Block math (LaTeX)
$$
\int_{0}^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$
```

### Code / 代码 / 程式碼

```markdown
# Inline code
Use `obsidian-markdown` skill for proper syntax.

# Code block with syntax highlighting
```python
def hello():
    print("Hello, Obsidian!")
```

# Code block with line numbers
```python {1,3-5}
def hello():
    print("Line 2")    # Not highlighted
    print("Line 3")    # Highlighted
    print("Line 4")    # Highlighted
    print("Line 5")    # Highlighted
```
```

### Tasks / 任务 / 任務

```markdown
- [ ] Unchecked task
- [x] Completed task
- [/] In-progress task
- [-] Cancelled task
- [ ] Task with date ⏫ 🔁 every day
- [ ] Sub-task 1
- [ ] Sub-task 2
```

### Tables / 表格 / 表格

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Row 1    | Data     | More     |
| Row 2    | Data     | More     |
```

---

## Best Practices / 最佳实践 / 最佳實踐

### 1. Descriptive Wikilinks / 描述性 Wikilinks / 描述性 Wikilinks

```markdown
# ✓ Good
[[PARA Methodology - Core Principles]]
[[2024-01-15 - Meeting Notes]]

# ✗ Avoid
[[Note 1]]
[[Untitled]]
```

### 2. Consistent Properties / 一致性属性 / 一致性屬性

```yaml
# ✓ Good - Always include these
---
title: Descriptive Title
date: 2024-01-15
tags: [relevant, tags]
status: in-progress
para: projects
---

# ✗ Avoid - Incomplete or missing
---
title: Quick note
---
```

### 3. Semantic Callouts / 语义化提示块 / 語義化提示塊

```markdown
# ✓ Good
> [!tip] Productivity Tip
> Use PARA to organize your notes.

> [!warning] Important Warning
> Don't mix Projects and Areas.

# ✗ Avoid - Using generic notes everywhere
> [!note] Tip
> Use PARA to organize your notes.
```

### 4. Proper Embed Sizing / 适当的嵌入大小 / 適當的嵌入大小

```markdown
# ✓ Good - Reasonable sizes
![[screenshot.png|600x400]]
![[diagram.png|800x600]]

# ✗ Avoid - Too large or too small
![[screenshot.png|1920x1080]]
![[diagram.png|100x50]]
```

---

## Common Patterns / 常见模式 / 常見模式

### Project Note Template / 项目笔记模板 / 專案筆記模板

```markdown
---
title: Project Name
date: 2024-01-15
tags: [project, active]
status: in-progress
priority: high
para: projects
---

# Project Overview

> [!info] Project Summary
> Brief description of what this project is about.

## Goals / 目标

- [ ] Goal 1
- [ ] Goal 2
- [ ] Goal 3

## Progress

![[Project Tasks]]

## Resources

![[Project Resources]]

## Notes

![[Project Journal]]
```

### Meeting Note Template / 会议笔记模板 / 會議筆記模板

```markdown
---
title: 2024-01-15 - Team Meeting
date: 2024-01-15
tags: [meeting, team]
status: done
para: archives
type: meeting
participants:
  - Alice
  - Bob
  - Charlie
---

# Team Meeting / 团队会议

**Date**: 2024-01-15
**Time**: 10:00 - 11:00
**Location**: Zoom

## Agenda / 议程

1. Review last week's progress
2. Discuss new features
3. Plan next sprint

## Notes / 笔记

> [!note] Key Decision
> We decided to launch the feature next Monday.

## Action Items / 行动项

- [ ] Alice: Write documentation
- [ ] Bob: Fix the bug
- [ ] Charlie: Prepare presentation

## Next Meeting

2024-01-22 - Team Meeting
```

---

## Related Skills / 相关技能 / 相關技能

- **para-methodology**: PARA structure and workflow / PARA 结构和工作流 / PARA 結構和工作流
- **markdown-standards**: File naming and conventions / 文件命名和规范 / 檔案命名和規範
- **obsidian-bases**: Database-like views and tables / 数据库类视图和表格 / 資料庫類視圖和表格

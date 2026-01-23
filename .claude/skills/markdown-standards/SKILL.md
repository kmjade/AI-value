# Markdown Standards Skill

## Overview / 概览 / 概覽

This skill provides standards and best practices for working with markdown files in the AI-value repository, including development notes, file naming conventions, and multilingual support.

本技能提供在 AI-value 仓库中处理 Markdown 文件的标准和最佳实践，包括开发说明、文件命名规范和多语言支持。

本技能提供在 AI-value 倉庫中處理 Markdown 檔案的標準和最佳實踐，包括開發說明、檔案命名規範和多語言支援。

---

## Quick Reference

- **File Format**: Markdown (`.md`) with YAML frontmatter
- **No Build System**: No npm, make, or build commands needed
- **Primary Tool**: Obsidian for markdown editing
- **Languages**: English, Simplified Chinese (简体中文), Traditional Chinese (繁體中文)

---

## Development Notes / 开发说明 / 開發說明

### Repository Nature / 仓库性质 / 倉庫性質

**This is a documentation/note repository, not a code project.**

**这是一个文档/笔记仓库，不是代码项目。**

**這是一個文件/筆記倉庫，不是程式碼專案。**

### Key Characteristics / 关键特性 / 關鍵特性

| Aspect | Description | 描述 | 描述 |
|--------|-------------|------|------|
| **Build System** | None / 无 / 無 | No npm, make, or build commands needed / 不需要 npm、make 或构建命令 |
| **Tests** | None / 无 / 無 | No automated testing framework / 无自动化测试框架 / 無自動化測試框架 |
| **Linting** | None / 无 / 無 | No code linting tools configured / 未配置代码检查工具 / 未配置程式碼檢查工具 |
| **File Format** | Markdown (`.md`) with YAML frontmatter | 基于 Markdown，带 YAML 前置数据 / 基於 Markdown，帶 YAML 前置數據 |
| **Primary Tool** | Obsidian | Use Obsidian for markdown editing with full syntax support / 使用 Obsidian 编辑，支持完整语法 / 使用 Obsidian 編輯，支援完整語法 |

### When Editing Markdown Files / 编辑 Markdown 文件时 / 編輯 Markdown 檔案時

Follow these guidelines:

遵循以下指南：

遵循以下指南：

1. **Use `obsidian-markdown` skill for proper syntax**
   - Ensure correct wikilink syntax: `[[Note]]` / 确保 wikilink 语法正确 / 確保 wikilink 語法正確
   - Use callouts for emphasis: `> [!note]` / 使用提示块强调 / 使用提示塊強調
   - Format code blocks with language tags / 使用语言标签格式化代码块 / 使用語言標籤格式化程式碼區塊

2. **Preserve YAML frontmatter for properties**
   - Keep existing metadata intact / 保持现有元数据完整 / 保持現有元數據完整
   - Add properties when creating new notes / 创建新笔记时添加属性 / 建立新筆記時添加屬性
   - Follow metadata standards / 遵循元数据标准 / 遵循元數據標準

3. **Use wikilinks `[[Note]]` for internal linking**
   - Never use absolute paths / 永远不要使用绝对路径 / 永遠不要使用絕對路徑
   - Use descriptive note names / 使用描述性笔记名称 / 使用描述性筆記名稱
   - Link to headings with `#`: `[[Note#Section]]` / 使用 `#` 链接到章节 / 使用 `#` 連結到章節

4. **Use callouts for emphasized content**
   - Choose appropriate callout types / 选择合适的提示块类型 / 選擇合適的提示塊類型
   - Use for warnings, tips, summaries / 用于警告、提示、摘要 / 用於警告、提示、摘要
   - Foldable sections with `-` or `+` / 使用 `-` 或 `+` 创建可折叠部分 / 使用 `-` 或 `+` 建立可折疊部分

5. **Respect PARA folder structure**
   - Place files in correct categories / 将文件放在正确的类别中 / 將檔案放在正確的類別中
   - Move completed items to Archives / 将已完成项目移至 Archives / 將已完成專案移至 Archives
   - Follow workflow: InBox → Projects → Archives / 遵循工作流：InBox → Projects → Archives

---

## Metadata Standards / 元数据标准 / 元數據標準

### PARA Category Values / PARA 类别值 / PARA 類別值

When working with PARA items, use these standard property values:

处理 PARA 项目时，使用这些标准属性值：

處理 PARA 專案時，使用這些標準屬性值：

| Category | para value | Example | 示例 | 範例 |
|----------|-----------|---------|--------|--------|
| **Projects** | `projects` | Active projects with deadlines / 有期限的活跃项目 / 有期限的活躍專案 | |
| **Areas** | `areas` | Ongoing responsibilities / 持续责任 / 持續責任 | |
| **Resources** | `resources` | Reference materials / 参考材料 / 參考材料 | |
| **Archives** | `archives` | Completed items / 已完成项目 / 已完成專案 | |

### Standard Properties / 标准属性 / 標準屬性

```yaml
---
# Core properties / 核心属性 / 核心屬性
title: Descriptive Note Title
date: 2024-01-15
created: 2024-01-15T09:00:00Z
modified: 2024-01-20T14:30:00Z

# Classification / 分类 / 分類
tags:
  - category
  - subcategory
para: projects  # or: areas, resources, archives

# Status tracking / 状态跟踪 / 狀態追蹤
status: in-progress  # Options: in-progress, done, on-hold, cancelled
priority: high        # Options: high, medium, low

# Optional metadata / 可选元数据 / 可選元數據
author: Your Name
source: https://example.com
related:
  - [[Related Note 1]]
  - [[Related Note 2]]
type: note  # e.g., meeting, project, resource, zettel
language: en  # en, zh-cn, zh-tw
---
```

### Required Properties for Different Note Types / 不同笔记类型的必需属性 / 不同筆記類型的必需屬性

#### Project Notes / 项目笔记 / 專案筆記

```yaml
---
title: Project Name
date: 2024-01-15
tags: [project, active]
status: in-progress
priority: high
para: projects
---
```

#### Area Notes / 领域笔记 / 領域筆記

```yaml
---
title: Area Name
date: 2024-01-15
tags: [area, ongoing]
status: ongoing
para: areas
---
```

#### Resource Notes / 资源笔记 / 資源筆記

```yaml
---
title: Resource Name
date: 2024-01-15
tags: [resource, reference]
status: active
para: resources
---
```

#### Zettel Notes / 原子笔记 / 原子筆記

```yaml
---
title: Zettel Title 💡
date: 2024-01-15
tags: [zettel, idea]
type: zettel
zettel-type: permanent  # fleeting, permanent, literature, structure
---
```

---

## Multilingual Support / 多语言支持 / 多語言支援

### Language Policy / 语言政策 / 語言政策

Documentation is maintained in **three languages**:

文档维护在 **三种语言** 中：

文件維護在 **三種語言** 中：

1. **English** (en)
2. **Simplified Chinese** (简体中文, zh-cn)
3. **Traditional Chinese** (繁體中文, zh-tw)

### Language in Content / 内容中的语言 / 內容中的語言

#### For Individual Notes / 对于单个笔记 / 對於單個筆記

**Option A: Single Language Notes / 单语言笔记 / 單語言筆記**

Create separate notes for each language:

为每种语言创建单独笔记：

為每種語言創建單獨筆記：

```
3 Resources/AI/
├── Obsidian Guide.md           # English
├── Obsidian 指南.md             # Simplified Chinese
└── Obsidian 指南.md             # Traditional Chinese
```

**Option B: Multilingual Notes / 多语言笔记 / 多語言筆記**

Include all three languages in one note:

在一个笔记中包含所有三种语言：

在一個筆記中包含所有三種語言：

```markdown
---
title: Obsidian Guide / Obsidian 指南 / Obsidian 指南
date: 2024-01-15
language: multilingual
---

# Obsidian Guide

## Quick Start / 快速开始 / 快速開始

This is a guide to using Obsidian. / 这是使用 Obsidian 的指南。 / 這是使用 Obsidian 的指南。

> [!tip] Tip / 提示 / 提示
> Use wikilinks to connect your notes. / 使用 wikilinks 连接笔记。 / 使用 wikilinks 連結筆記。
```

### Consistency Guidelines / 一致性指南 / 一致性指南

When creating new documentation, maintain consistency with existing multilingual patterns:

创建新文档时，保持与现有多语言模式的一致性：

建立新文件時，保持與現有多語言模式的一致性：

#### Structure / 结构 / 結構

```markdown
# English Title / 简体中文标题 / 繁體中文標題

## Section Header / 简体中文章节 / 繁體中文章節

English content. / 简体中文内容。 / 繁體中文內容。

### Subsection / 子章节 / 子章節

English sub-content. / 简体中文子内容。 / 繁體中文子內容。
```

#### Lists / 列表 / 列表

```markdown
- Item 1 / 项目 1 / 項目 1
- Item 2 / 项目 2 / 項目 2
  - Subitem 2.1 / 子项目 2.1 / 子項目 2.1
```

#### Tables / 表格 / 表格

```markdown
| English / 简体中文 / 繁體中文 | English 2 / 简体中文 2 / 繁體中文 2 |
|--------------------------------|------------------------------------|
| Data 1 / 数据 1 / 數據 1       | Data 2 / 数据 2 / 數據 2           |
```

#### Callouts / 提示块 / 提示塊

```markdown
> [!note] Note / 注意 / 注意
> English note content. / 简体中文注意内容。 / 繁體中文注意內容。

> [!warning] Warning / 警告 / 警告
> English warning. / 简体中文警告。 / 繁體中文警告。
```

### Language Property / 语言属性 / 語言屬性

Add language property to frontmatter:

在 frontmatter 中添加语言属性：

在 frontmatter 中添加語言屬性：

```yaml
---
language: en           # or: zh-cn, zh-tw, multilingual
---
```

---

## File Naming Conventions / 文件命名规范 / 檔案命名規範

### General Guidelines / 通用指南 / 通用指南

| Rule | Description | 描述 | 描述 | Examples |
|------|-------------|------|------|----------|
| **Descriptive names** | Use clear, meaningful names / 使用清晰、有意义的名称 / 使用清晰、有意義的名稱 | | | `PARA Methodology.md` ✅ <br> `Note.md` ❌ |
| **Avoid special characters** | No characters that break links / 避免破坏链接的特殊字符 / 避免破壞連結的特殊字符 | | | `My Note.md` ✅ <br> `My@Note.md` ❌ |
| **Use spaces** | Obsidian handles spaces well in wikilinks / Obsidian wikilinks 很好地处理空格 / Obsidian wikilinks 很好地處理空格 | | | `Learning Obsidian.md` ✅ <br> `LearningObsidian.md` ⚠️ |
| **Keep original language** | For multilingual content, keep original language names / 多语言内容保留原语言名称 / 多語言內容保留原語言名稱 | | | `Obsidian 指南.md` ✅ |
| **Template prefix** | Use `_template-` prefix for templates / 模板文件使用 `_template-` 前缀 / 模板檔案使用 `_template-` 前綴 | | | `_template-project.md` ✅ |
| **Zettel emoji prefix** | Use emoji prefixes for Zettels / Zettels 使用 emoji 前缀 / Zettels 使用 emoji 前綴 | | | `💡 Idea.md` ✅ |

### Special Characters to Avoid / 避免使用的特殊字符 / 避免使用的特殊字符

Avoid these characters in file names (they break links or cause issues):

文件名中避免使用这些字符（它们会破坏链接或导致问题）：

檔名中避免使用這些字符（它們會破壞連結或導致問題）：

| Character | Why to Avoid | Why / 为什么 / 為什麼 |
|-----------|--------------|----------------------|
| `:` | Reserved in some systems / 在某些系统中保留 / 在某些系統中保留 |
| `*` `?` | Wildcards in some systems / 某些系统中的通配符 / 某些系統中的通配符 |
| `"` | Can cause path issues / 可能导致路径问题 / 可能導致路徑問題 |
| `<` `>` `|` | Reserved characters / 保留字符 / 保留字符 |
| `\` `/` (in filenames) | Path separators / 路径分隔符 / 路徑分隔符 |

### Date-based Names / 基于日期的命名 / 基於日期的命名

For dated content (daily notes, meetings, etc.):

对于日期内容（每日笔记、会议等）：

對於日期內容（每日筆記、會議等）：

```markdown
# Daily notes / 每日笔记 / 每日筆記
2024-01-15.md
2024-01-16.md
2024-01-17.md

# Meeting notes / 会议笔记 / 會議筆記
2024-01-15 - Team Meeting.md
2024-01-20 - Project Review.md

# Journal entries / 日记条目 / 日記條目
2024-01-15 - Journal.md
```

### Naming by PARA Category / 按 PARA 类别命名 / 按 PARA 類別命名

#### Projects / 项目 / 專案

```
Project Name/
├── Main Note.md
├── Tasks.md
├── Progress.md
└── Resources.md

Or flat structure:
Project Name - Main.md
Project Name - Tasks.md
```

#### Areas / 领域 / 領域

```
Area Name/
├── Overview.md
├── Maintenance.md
└── Journal.md

Or flat structure:
Health - Overview.md
Health - Maintenance.md
```

#### Resources / 资源 / 資源

```
Resource Category/
├── Topic 1.md
├── Topic 2.md
└── Topic 3.md

Or flat structure:
AI - Machine Learning.md
AI - Deep Learning.md
```

#### Archives / 归档 / 歸檔

```
Archived Year/
├── Project Name (Completed).md
├── Old Resource.md
└── Historical Notes.md

Or:
[Completed] Project Name.md
[Archived] Resource.md
```

#### Zettels / 原子笔记 / 原子筆記

```
💡 Fleeting/
├── 💡 Quick idea.md
└── 💡 Random thought.md

📌 Permanent/
├── 📌 Key concept.md
└── 📌 Important principle.md

📚 Literature/
├── 📚 Paper summary.md
└── 📚 Book notes.md

📁 Structure/
├── 📁 Workflow.md
└── 📁 System overview.md
```

### Template Naming / 模板命名 / 模板命名

```markdown
_Template/
├── _template-project.md
├── _template-area.md
├── _template-resource.md
├── _template-zettel.md
├── _template-meeting.md
└── _template-daily-note.md
```

---

## Best Practices / 最佳实践 / 最佳實踐

### 1. Consistency / 一致性 / 一致性

- ✓ Use the same naming pattern throughout / 全程使用相同的命名模式 / 全程使用相同的命名模式
- ✗ Don't mix styles: `My Note.md`, `another-note.md`, `ThirdNote.md` / 不要混用风格 / 不要混用風格

### 2. Descriptiveness / 描述性 / 描述性

- ✓ Use descriptive names: `PARA Methodology - Core Principles.md` / 使用描述性名称 / 使用描述性名稱
- ✗ Avoid vague names: `Stuff.md`, `Things.md`, `Note.md` / 避免模糊名称 / 避免模糊名稱

### 3. Avoid Renaming / 避免重命名 / 避免重命名

- Renaming notes breaks all existing links to them / 重命名笔记会破坏所有指向它们的现有链接 / 重命名筆記會破壞所有指向它們的現有連結
- Plan names carefully before creating / 创建前仔细规划名称 / 建立前仔細規劃名稱
- Use alias if you need to change display text / 如需更改显示文本，使用别名 / 如需更改顯示文字，使用別名：`[[Old Name|New Display Name]]`

### 4. Length Considerations / 长度考虑 / 長度考慮

- ✓ Short enough to read: `Project Overview.md` / 足够短以便阅读 / 足夠短以便閱讀
- ✓ Long enough to be descriptive: `PARA Methodology - Core Principles.md` / 足够长以便描述 / 足夠長以便描述
- ✗ Too short: `P.md`, `N.md` / 太短 / 太短
- ✗ Too long: `This Is An Extremely Long And Unnecessarily Detailed File Name That Is Hard To Read.md` / 太长 / 太長

---

## Related Skills / 相关技能 / 相關技能

- **obsidian-syntax**: Obsidian-specific markdown syntax / Obsidian 特定 markdown 语法 / Obsidian 特定 markdown 語法
- **para-methodology**: PARA structure and organization / PARA 结构和组织 / PARA 結構和組織
- **repo-context**: Repository structure and paths / 仓库结构和路径 / 倉庫結構和路徑

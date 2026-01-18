This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## English / 简体中文 / 繁體中文

### Project Purpose / 项目目的 / 專案目的

**AI-value** is a personal knowledge management system using PARA methodology (Projects, Areas, Resources, Archives). It's a markdown-based knowledge base with Obsidian integration, designed to organize information systematically.

**AI-value** 是一个基于 PARA 方法论（项目、领域、资源、归档）的个人知识管理系统。这是一个基于 Markdown 的知识库，集成了 Obsidian，旨在系统地组织信息。

**AI-value** 是一個基於 PARA 方法論（Projects, Areas, Resources, Archives）的個人知識管理系統。這是一個基於 Markdown 的知識庫，整合了 Obsidian，旨在系統地組織資訊。

### Repository Information / 仓库信息 / 倉庫信息

- **License:** Apache 2.0
- **Remote:** https://github.com/kmjade/AI-value.git
- **Primary branch:** `main`
- **Working branch:** `main_para`

### Folder Structure / 文件夹结构 / 資料夾結構

```
AI-value/
├── 0 Personals/
│   └── 📥 00_InBox/    - 收件箱，临时收集内容
├── 1 Projects/            - Short-term efforts with deadlines
├── 2 Areas/               - Long-term responsibilities
├── 3 Resources/           - Topics of ongoing interest
├── 4 Archives/            - Completed/inactive items
├── 5 Zettels/            - 原子化笔记 (Zettelkasten)
├── _Template/             - PARA templates
├── _meta/                - System metadata and configuration
├── .claude/              - Claude Code configuration
├── .obsidian/            - Obsidian plugin settings
└── .idea/               - IntelliJ IDEA settings (gitignored)
```

**PARA Methodology:**
- **Projects** (`1 Projects/`): Active, short-term endeavors with deadlines
- **Areas** (`2 Areas/`): Ongoing responsibilities and areas of responsibility
- **Resources** (`3 Resources/`): Topics of interest and reference material
- **Archives** (`4 Archives/`): Completed projects and inactive items

**Extended Structure:**
- **InBox** (`0 Personals/📥 00_InBox/`): Temporary collection for quick capture
- **Zettels** (`6 Zettels/`): Atomic notes system for knowledge networking

### Claude Code Commands / Claude Code 指令

Commands are located in `.claude/commands/` and invoked with `/command-name`.

#### PARA Management Commands

| Command | File | Purpose |
|---------|------|---------|
| `/para-库概览` | `para-库概览.md` | Display PARA library overview and statistics |
| `/para-整理收集` | `para-整理收集.md` | Organize InBox contents by PARA principles |

**Usage Examples:**

```
/para-库概览
# Output:
# 📊 PARA 库概览
#
# | 文件夹 | 文件数 | 状态 |
# |--------|--------|------|
# | 0 Personals/📥 00_InBox | X | ⚠️ 需要整理 / ✅ 已清空 |
# | 1 Projects | X | |
# | 2 Areas | X | |
# | 3 Resources | X | |
# | 4 Archives | X | |
# | 5 Zettels | X | |
#
# 📁 进行中的项目 (1 Projects)：
# - 公众号
# - AI日报
```

```
/para-整理收集
# Output:
# 📥 整理收件箱
#
# 发现 X 个待处理笔记：
# 1. "学习笔记.md"
#    - 建议: 🗂️ Resource → [[AI]]
#    - 动作: [归档] [跳过] [编辑]
```

#### Helper Commands

| Command | File | Purpose |
|---------|------|---------|
| `/创建指令` | `创建指令.md` | Create new Claude Code commands |
| `/创建技能` | `创建技能.md` | Create new Claude Code skills (calls skill-creator) |
| `/claudian` | `claudian.md` | Claude-specific PARA management commands |
| `/obsidian` | `obsidian.md` | Auto-select appropriate Obsidian skill |

### Claude Code Skills / Claude Code 技能

Skills are located in `.claude/skills/` and are automatically triggered or manually invoked based on context.

#### Available Skills

| Skill | Description | Use When |
|-------|-------------|----------|
| **obsidian-markdown** | Create/edit Obsidian Flavored Markdown with wikilinks, embeds, callouts, properties | Working with `.md` files, wikilinks `[[Note]]`, frontmatter, callouts, tags |
| **obsidian-bases** | Create/edit Obsidian Bases (.base) with views, filters, formulas | Creating database views, tables, cards, formulas |
| **json-canvas** | Create/edit JSON Canvas files (.canvas) with nodes, edges | Creating mind maps, flowcharts, visual canvases |

**Automatic Skill Selection:**

The `/obsidian` command automatically selects the appropriate skill:
- `.md` files → `obsidian-markdown`
- `.base` files → `obsidian-bases`
- `.canvas` files → `json-canvas`

### Obsidian-Specific Syntax

#### Wikilinks / internal links

```markdown
[[Note Name]]
[[Note Name|Display Text]]
[[Note Name#Heading]]
[[Note Name#^block-id]]
![[Embedded Note]]
```

#### Callouts / 提示块

```markdown
> [!note] Note
> [!info] Info
> [!tip] Tip
> [!warning] Warning
> [!faq]- Collapsible
> [!todo]-+ Expanded by default
```

#### Properties / Frontmatter / 属性

```yaml
---
title: My Note
date: 2024-01-15
tags:
  - project
  - important
status: in-progress
priority: high
---
```

#### Embeds / 嵌入

```markdown
![[Note Name#Heading]]
![[image.png|640x480]]
![[document.pdf#page=3]]
```

### Development Notes / 开发说明 / 開發說明

This is a documentation/note repository, not a code project. Key considerations:

- **No build system**: No npm, make, or other build commands needed
- **No tests**: No automated testing framework
- **No linting**: No code linting tools configured
- **File format**: Markdown (`.md`) with YAML frontmatter
- **Primary tool**: Use Obsidian for markdown editing with full syntax support

**When editing markdown files:**
- Use `obsidian-markdown` skill for proper syntax
- Preserve YAML frontmatter for properties
- Use wikilinks `[[Note]]` for internal linking
- Use callouts for emphasized content
- Respect PARA folder structure

**Metadata Standards:**
| Category | para value |
|----------|-----------|
| Projects | `projects` |
| Areas | `areas` |
| Resources | `resources` |
| Archives | `archives` |

**Multilingual Support:**
Documentation is maintained in three languages:
- English
- Simplified Chinese (简体中文)
- Traditional Chinese (繁體中文)

When creating new documentation, maintain consistency with existing multilingual patterns.

### PARA Workflow

1. **Capture**: Add new information to `0 Personals/📥 00_InBox/`
2. **Organize**: Use `/para-整理收集` to organize InBox contents
3. **Review**: Use `/para-库概览` to review library status
4. **Archive**: Move completed items to `4 Archives/`

**Zettelkasten Workflow:**
1. Create atomic notes in `5 Zettels/`
2. Link related concepts using wikilinks
3. Use unique IDs for reference
4. Connect to PARA categories as needed

### File Naming Conventions

- Use descriptive names
- Avoid special characters that break links
- Use spaces (Obsidian handles them well in wikilinks)
- For multilingual content, keep original language names
- Template files use `_template-` prefix

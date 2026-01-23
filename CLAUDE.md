# AI-value Knowledge Management System / AI-value 知识管理系统 / AI-value 知識管理系統

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

本文件为 Claude Code (claude.ai/code) 在此仓库中工作时提供指导。

本文件為 Claude Code (claude.ai/code) 在此倉庫中工作時提供指導。

---

## Quick Reference / 快速参考 / 快速參考

| Category | Value / 值 / 值 |
|----------|-----------------|
| **PARA Structure** | `0 Personals` → `1 Projects` → `2 Areas` → `3 Resources` → `4 Archives` → `5 Zettels` |
| **Key Commands** | `/para-库概览`, `/para-整理收集`, `/para-刷新缓存`, `/search`, `/obsidian` |
| **File Format** | Markdown (`.md`) with YAML frontmatter and Obsidian syntax |
| **Primary Tool** | Obsidian for markdown editing / Obsidian markdown 编辑器 / Obsidian markdown 編輯器 |
| **License** | Apache 2.0 |
| **Working Branch** | `main_para` |

---

## Core Principles / 核心原则 / 核心原則

### 1. PARA Methodology / PARA 方法论 / PARA 方法論

Organize information by **actionability** and **time horizon**:

根据 **可执行性** 和 **时间跨度** 组织信息：

根據 **可執行性** 和 **時間跨度** 組織資訊：

| Category | Description / 描述 | 描述 |
|----------|-------------------|------|
| **Projects** (`1 Projects/`) | Active, short-term endeavors with deadlines / 有期限的活跃短期项目 / 有期限的活躍短期專案 |
| **Areas** (`2 Areas/`) | Long-term responsibilities / 长期责任 / 長期責任 |
| **Resources** (`3 Resources/`) | Topics of ongoing interest / 持续感兴趣的主题 / 持續感興趣的主題 |
| **Archives** (`4 Archives/`) | Completed or inactive items / 已完成或非活跃项目 / 已完成或非活躍專案 |

**Extended Structure / 扩展结构 / 擴展結構:**
- **InBox** (`0 Personals/📥 00_InBox/`): Temporary collection for quick capture / 临时收集区 / 臨時收集區
- **Zettels** (`5 Zettels/`): Atomic notes for knowledge networking / 原子化笔记系统 / 原子化筆記系統
  - `💡 fleeting/` - Quick thoughts / 闪念笔记 / 閃念筆記
  - `📌 permanent/` - Knowledge atoms / 永久笔记 / 永久筆記
  - `📚 literature/` - Research notes / 文献笔记 / 文獻筆記
  - `📁 structure/` - System notes / 结构笔记 / 結構筆記

### 2. Workflow / 工作流 / 工作流

```
Daily: Capture → Organize → Review
Weekly: Process InBox, Refresh cache
Monthly: Deep clean Archives
```

**PARA Workflow / PARA 工作流 / PARA 工作流:**
1. **Capture / 收集**: Add to `0 Personals/📥 00_InBox/`
2. **Organize / 整理**: Use `/para-整理收集` to process by PARA
3. **Review / 复盘**: Use `/para-库概览` to check status
4. **Archive / 归档**: Move completed items to `4 Archives/`

**Zettelkasten Workflow / 卡片盒工作流 / 卡片盒工作流:**
1. Create atomic notes in `5 Zettels/` / 创建原子笔记 / 建立原子筆記
2. Link using wikilinks `[[Note]]` / 使用 wikilinks 链接 / 使用 wikilinks 連結
3. Use unique IDs (`YYYYMMDD-XXXX`) / 使用唯一 ID / 使用唯一 ID
4. Connect to PARA categories as needed / 按需连接到 PARA / 按需連結到 PARA

### 3. File Standards / 文件标准 / 檔案標準

| Aspect / 方面 / 方面 | Standard / 标准 / 標準 |
|----------------------|-----------------------|
| **Naming** | Descriptive, use spaces / 描述性，使用空格 / 描述性，使用空格 |
| **Format** | Markdown (`.md`) + YAML frontmatter |
| **Links** | Relative wikilinks only: `[[Note]]` / 仅使用相对 wikilinks / 僅使用相對 wikilinks |
| **Paths** | From vault root: `1 Projects/note.md` / 从 vault root 开始 / 從 vault root 開始 |
| **Templates** | Use `_template-` prefix / 使用 `_template-` 前缀 / 使用 `_template-` 前綴 |
| **Zettels** | Use emoji prefixes: `💡`, `📌`, `📚`, `📁` |

### 4. Metadata Standards / 元数据标准 / 元數據標準

```yaml
---
title: Note Title / 笔记标题 / 筆記標題
date: 2024-01-15
tags: [category, topic]
para: projects  # or: areas, resources, archives
status: in-progress
language: en  # or: zh-cn, zh-tw
---
```

---

## Skills Index / Skills 索引 / Skills 索引

Comprehensive knowledge modules are available in `.claude/skills/`:

`.claude/skills/` 中提供全面的知识模块：

`.claude/skills/` 中提供全面的知識模組：

| Skill | Directory | Description / 描述 | 描述 | Use When / 何时使用 / 何時使用 |
|-------|-----------|-------------------|------|------------------------------|
| **para-methodology** | `.claude/skills/para-methodology/` | PARA structure, workflow, metadata / PARA 结构、工作流、元数据 / PARA 結構、工作流、元數據 | Working with PARA organization / 处理 PARA 组织 / 處理 PARA 組織 |
| **obsidian-syntax** | `.claude/skills/obsidian-syntax/` | Wikilinks, callouts, properties, embeds / Wikilinks、提示块、属性、嵌入 / Wikilinks、提示塊、屬性、嵌入 | Editing markdown files / 编辑 markdown 文件 / 編輯 markdown 檔案 |
| **repo-context** | `.claude/skills/repo-context/` | Repository structure, paths, Git info / 仓库结构、路径、Git 信息 / 倉庫結構、路徑、Git 資訊 | Understanding the repository / 理解仓库 / 理解倉庫 |
| **markdown-standards** | `.claude/skills/markdown-standards/` | File naming, multilingual support, conventions / 文件命名、多语言支持、规范 / 檔案命名、多語言支援、規範 | Creating or organizing files / 创建或组织文件 / 建立或組織檔案 |
| **claude-commands** | `.claude/skills/claude-commands/` | Command usage and workflows / 指令使用和工作流 / 指令使用和工作流 | Using Claude Code commands / 使用 Claude Code 指令 / 使用 Claude Code 指令 |
| **zettelkasten-workflow** | `.claude/skills/zettelkasten-workflow/` | Atomic notes, linking, unique IDs / 原子笔记、链接、唯一 ID / 原子筆記、連結、唯一 ID | Working with Zettelkasten system / 使用 Zettelkasten 系统 / 使用 Zettelkasten 系統 |

### Built-in Obsidian Skills / 内置 Obsidian 技能 / 內建 Obsidian 技能

| Skill | File Types / 文件类型 / 檔案類型 | Description / 描述 | 描述 |
|-------|-------------------------------|-------------------|------|
| **obsidian-markdown** | `.md` | Obsidian Flavored Markdown with wikilinks, callouts, properties / 带 wikilinks、提示块、属性的 Obsidian 增强版 Markdown / 帶 wikilinks、提示塊、屬性的 Obsidian 增強版 Markdown |
| **obsidian-bases** | `.base` | Database views, tables, cards, formulas / 数据库视图、表格、卡片、公式 / 資料庫視圖、表格、卡片、公式 |
| **json-canvas** | `.canvas` | Mind maps, flowcharts, visual canvases / 思维导图、流程图、可视化画布 / 思維導圖、流程圖、視覺化畫布 |

> [!tip] Tip / 提示 / 提示
> Use `/obsidian` to automatically select the appropriate skill based on file type.
> 使用 `/obsidian` 根据文件类型自动选择合适的技能。
> 使用 `/obsidian` 根據檔案類型自動選擇合適的技能。

---

## Quick Reference Links / 快速参考链接 / 快速參考連結

### Commands / 指令 / 指令

| Command | Purpose / 用途 | 用途 | Skill / 技能 / 技能 |
|---------|---------------|------|-------------------|
| `/para-库概览` | Display PARA library overview / 显示 PARA 库概览 / 顯示 PARA 庫概覽 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/para-整理收集` | Organize InBox by PARA / 按 PARA 整理收件箱 / 按 PARA 整理收件箱 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/para-刷新缓存` | Update cache files / 更新缓存文件 / 更新快取檔案 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/search` | Search content / 搜索内容 / 搜尋內容 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/obsidian` | Auto-select Obsidian skill / 自动选择 Obsidian 技能 / 自動選擇 Obsidian 技能 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/claudian` | PARA assistant menu / PARA 助手菜单 / PARA 助手選單 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/创建指令` | Create new command / 创建新指令 / 創建新指令 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| `/创建技能` | Create new skill / 创建新技能 / 創建新技能 | [claude-commands](.claude/skills/claude-commands/SKILL.md) |

### Syntax Reference / 语法参考 / 語法參考

| Feature / 功能 / 功能 | Example / 示例 / 範例 | Skill / 技能 / 技能 |
|--------------------|-------------------|-------------------|
| **Wikilink** | `[[Note]]` / `[[Note\|Display]]` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |
| **Embed** | `![[Note]]` / `![[image.png\|300x200]]` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |
| **Callout** | `> [!note] Title` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |
| **Properties** | YAML frontmatter with `---` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |
| **Block Reference** | `[[Note#^block-id]]` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |

### Common Tasks / 常见任务 / 常見任務

| Task / 任务 / 任務 | Action / 行动 / 行動 | Reference / 参考 / 參考 |
|------------------|-------------------|-------------------|
| **Create new note** | Use templates from `_Template/` | [markdown-standards](.claude/skills/markdown-standards/SKILL.md) |
| **Organize InBox** | Use `/para-整理收集` | [para-methodology](.claude/skills/para-methodology/SKILL.md) |
| **Check library status** | Use `/para-库概览` | [para-methodology](.claude/skills/para-methodology/SKILL.md) |
| **Create Zettel** | Use unique ID `YYYYMMDD-XXXX` | [zettelkasten-workflow](.claude/skills/zettelkasten-workflow/SKILL.md) |
| **Link notes** | Use wikilinks `[[Note]]` | [obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md) |
| **Find content** | Use `/search` | [claude-commands](.claude/skills/claude-commands/SKILL.md) |
| **Improve performance** | Use `/para-刷新缓存` | [claude-commands](.claude/skills/claude-commands/SKILL.md) |

---

## Repository Context / 仓库上下文 / 倉庫上下文

### Key Information / 关键信息 / 關鍵資訊

| Item / 项目 / 項目 | Value / 值 / 值 |
|-------------------|-----------------|
| **Repository** | AI-value Personal Knowledge Management System |
| **Remote URL** | https://github.com/kmjade/AI-value.git |
| **Primary branch** | `main` |
| **Working branch** | `main_para` |
| **License** | Apache 2.0 |
| **Vault Path** | `D:\Knowledge\AI-value` |
| **Languages** | English, Simplified Chinese (简体中文), Traditional Chinese (繁體中文) |

### Path Rules / 路径规则 / 路徑規則

| Context / 上下文 / 上下文 | Rule / 规则 / 規則 | Example / 示例 / 範例 |
|--------------------------|------------------|-------------------|
| **Vault files** | Use relative paths from vault root / 使用从 vault root 开始的相对路径 / 使用從 vault root 開始的相對路徑 | `1 Projects/note.md` ✅ <br> `/1 Projects/note.md` ❌ |
| **Export paths** | Write-only: `~/Desktop`, `~/Downloads` | `pandoc ./note.md -o ~/Desktop/output.docx` |
| **External contexts** | Full read/write access (when enabled) | `/absolute/path/to/context` |

---

## Getting Started / 快速开始 / 快速開始

### New to AI-value? / AI-value 新手？ / AI-value 新手？

1. **Read the PARA methodology** / 阅读 PARA 方法论 / 閱讀 PARA 方法論: [[.claude/skills/para-methodology/SKILL.md]]
2. **Learn Obsidian syntax** / 学习 Obsidian 语法 / 學習 Obsidian 語法: [[.claude/skills/obsidian-syntax/SKILL.md]]
3. **Start capturing** / 开始捕获 / 開始捕獲: Add notes to `0 Personals/📥 00_InBox/`
4. **Organize regularly** / 定期整理 / 定期整理: Use `/para-整理收集` daily
5. **Review progress** / 审查进度 / 審查進度: Use `/para-库概览` weekly

### Daily Workflow / 每日工作流 / 每日工作流

```bash
# Morning routine / 早晨例程 / 早晨例程
/para-库概览          # Check status / 检查状态 / 檢查狀態
/obsidian             # Load appropriate skill / 加载合适的技能 / 加載合適的技能

# Work / 工作 / 工作
/capture ideas → InBox # Capture to InBox / 捕获到 InBox / 捕獲到 InBox

# Evening / 晚上 / 晚上
/para-整理收集         # Process InBox / 处理收件箱 / 處理收件箱
```

---

## Need Help? / 需要帮助？/ 需要幫助？

| Question / 问题 / 問題 | Reference / 参考 / 參考 |
|----------------------|-------------------|
| How to organize notes? | [[.claude/skills/para-methodology/SKILL.md\|PARA Methodology]] |
| How to format markdown? | [[.claude/skills/obsidian-syntax/SKILL.md\|Obsidian Syntax]] |
| How to name files? | [[.claude/skills/markdown-standards/SKILL.md\|Markdown Standards]] |
| What commands are available? | [[.claude/skills/claude-commands/SKILL.md\|Claude Commands]] |
| How to use Zettelkasten? | [[.claude/skills/zettelkasten-workflow/SKILL.md\|Zettelkasten Workflow]] |

> [!info] Note / 注意 / 注意
> All skills are located in `.claude/skills/` and contain detailed documentation in three languages.
> 所有技能都位于 `.claude/skills/` 中，包含三种语言的详细文档。
> 所有技能都位於 `.claude/skills/` 中，包含三種語言的詳細文件。

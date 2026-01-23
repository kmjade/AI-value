# Claude Commands Skill

## Overview / 概览 / 概覽

This skill provides comprehensive documentation about Claude Code commands in the AI-value repository, including PARA management commands and helper commands.

本技能提供关于 AI-value 仓库中 Claude Code 指令的全面文档，包括 PARA 管理指令和辅助指令。

本技能提供關於 AI-value 倉庫中 Claude Code 指令的全面文件，包括 PARA 管理指令和輔助指令。

---

## Quick Reference

- **Command Location**: `.claude/commands/`
- **Invocation**: Use `/command-name` to invoke commands
- **Key PARA Commands**: `/para-库概览`, `/para-整理收集`, `/para-刷新缓存`
- **Helper Commands**: `/创建指令`, `/创建技能`, `/claudian`, `/obsidian`, `/search`

---

## Command Structure / 指令结构 / 指令結構

### Location / 位置 / 位置

All commands are located in the `.claude/commands/` directory:

所有指令位于 `.claude/commands/` 目录中：

所有指令位於 `.claude/commands/` 目錄中：

```
.claude/
└── commands/
    ├── para-库概览.md
    ├── para-整理收集.md
    ├── para-刷新缓存.md
    ├── 创建指令.md
    ├── 创建技能.md
    ├── claudian.md
    ├── obsidian.md
    └── search.md
```

### Invocation / 调用 / 調用

Commands are invoked using the `/` prefix followed by the command name:

指令使用 `/` 前缀后跟指令名称调用：

指令使用 `/` 前綴後跟指令名稱調用：

```bash
/para-库概览
/para-整理收集
/obsidian
/search
```

---

## PARA Management Commands / PARA 管理指令 / PARA 管理指令

These commands are specifically designed for managing the PARA knowledge system:

这些指令专门用于管理 PARA 知识系统：

這些指令專門用於管理 PARA 知識系統：

| Command | File | Purpose / 用途 | 用途 |
|---------|------|---------------|------|
| `/para-库概览` | `para-库概览.md` | Display PARA library overview and statistics / 显示 PARA 库概览和统计 | 顯示 PARA 庫概覽和統計 |
| `/para-整理收集` | `para-整理收集.md` | Organize InBox contents by PARA principles / 按 PARA 原则整理收件箱 | 按 PARA 原則整理收件箱 |
| `/para-刷新缓存` | `para-刷新缓存.md` | Update PARA cache files for performance / 更新 PARA 缓存以提升性能 | 更新 PARA 快取以提升效能 |

### `/para-库概览` / `/para-库概览` / `/para-庫概覽`

**Purpose**: Display PARA library overview and statistics / 显示 PARA 库概览和统计 / 顯示 PARA 庫概覽和統計

**File**: `.claude/commands/para-库概览.md`

#### Usage / 使用 / 使用

```bash
/para-库概览
```

#### Example Output / 示例输出 / 範例輸出

```
📊 PARA 库概览

| 文件夹 | 文件数 | 状态 |
|--------|--------|------|
| 0 Personals/📥 00_InBox | 15 | ⚠️ 需要整理 |
| 1 Projects | 8 | ✅ 活跃 |
| 2 Areas | 12 | ✅ 维护中 |
| 3 Resources | 45 | ✅ 活跃 |
| 4 Archives | 120 | ✅ 已归档 |
| 5 Zettels | 200+ | ✅ 活跃 |

📁 进行中的项目 (1 Projects):
- 公众号 (status: in-progress)
- AI日报 (status: in-progress)
- 读书笔记 (status: on-hold)

📊 统计信息:
- 总文件数: 400+
- 待整理收件箱: 15
- 活跃项目: 2

⚡ 缓存状态:
- 最后更新: 2024-01-20 14:30:00
- 状态: ✅ 已同步
```

#### When to Use / 何时使用 / 何時使用

- **Daily check**: Review InBox status / 每日检查：审查收件箱状态 / 每日檢查：審查收件箱狀態
- **Weekly review**: Assess overall library health / 每周审查：评估整体库健康度 / 每週審查：評估整體庫健康度
- **Before organizing**: Check what needs attention / 整理前：检查需要注意的内容 / 整理前：檢查需要注意的內容
- **After organizing**: Verify changes / 整理后：验证更改 / 整理後：驗證更改

---

### `/para-整理收集` / `/para-整理收集` / `/para-整理收集`

**Purpose**: Organize InBox contents by PARA principles / 按 PARA 原则整理收件箱 / 按 PARA 原則整理收件箱

**File**: `.claude/commands/para-整理收集.md`

#### Usage / 使用 / 使用

```bash
/para-整理收集
```

#### Example Output / 示例输出 / 範例輸出

```
📥 整理收件箱

发现 15 个待处理笔记:

1. "学习 Obsidian 笔记.md"
   - 分析: Contains learning materials / 包含学习材料 / 包含學習材料
   - 建议: 🗂️ Resource → [[3 Resources/Obsidian/Obsidian 指南.md]]
   - 动作: [归档] [跳过] [编辑]

2. "待办任务清单.md"
   - 分析: Contains actionable tasks / 包含可执行任务 / 包含可執行任務
   - 建议: 📋 Project → [[1 Projects/本月任务/任务清单.md]]
   - 动作: [归档] [跳过] [编辑]

3. "健康检查记录.md"
   - 分析: Ongoing health monitoring / 持续健康监控 / 持續健康監控
   - 建议: 🔄 Area → [[2 Areas/Health/健康检查.md]]
   - 动作: [归档] [跳过] [编辑]

4. "旧会议笔记.md"
   - 分析: Historical meeting notes from 2023 / 2023年的历史会议笔记 / 2023年的歷史會議筆記
   - 建议: 📦 Archive → [[4 Archives/2023/Old meeting notes.md]]
   - 动作: [归档] [跳过] [编辑]

---

🔄 处理选项:
- 输入数字选择要整理的笔记
- 输入 'all' 整理所有建议项目
- 输入 'quit' 退出
```

#### When to Use / 何时使用 / 何時使用

- **Daily capture**: After adding new items to InBox / 每日收集：向 InBox 添加新项目后 / 每日收集：向 InBox 添加新項目後
- **Weekly cleanup**: When InBox gets too large / 每周清理：当 InBox 变得太大时 / 每週清理：當 InBox 變得太大時
- **Before starting work**: Clear mental clutter / 开始工作前：清理心理杂乱 / 開始工作前：清理心理雜亂
- **After brainstorming**: Organize captured ideas / 头脑风暴后：组织捕获的想法 / 頭腦風暴後：組織捕獲的想法

---

### `/para-刷新缓存` / `/para-刷新缓存` / `/para-刷新快取`

**Purpose**: Update PARA cache files for performance / 更新 PARA 缓存以提升性能 / 更新 PARA 快取以提升效能

**File**: `.claude/commands/para-刷新缓存.md`

#### Usage / 使用 / 使用

```bash
/para-刷新缓存
```

#### Example Output / 示例输出 / 範例輸出

```
🔄 刷新 PARA 缓存

正在扫描 PARA 文件夹...
✓ 扫描 0 Personals/📥 00_InBox/ (15 files)
✓ 扫描 1 Projects/ (8 files)
✓ 扫描 2 Areas/ (12 files)
✓ 扫描 3 Resources/ (45 files)
✓ 扫描 4 Archives/ (120 files)
✓ 扫描 5 Zettels/ (200+ files)

正在更新缓存文件...
✓ 更新 _Cache/para-cache.json
✓ 更新 _Cache/search-index.json
✓ 更新 _Cache/metadata-cache.json

✅ 缓存刷新完成！

📊 缓存统计:
- 总文件数: 400+
- PARA 项目: 200
- Zettels: 200+
- 更新时间: 2024-01-20 14:30:00

💡 提示: 缓存已更新，查询性能将显著提升
```

#### When to Use / 何时使用 / 何時使用

- **After adding many files**: Large bulk operations / 添加大量文件后：大量批量操作 / 添加大量檔案後：大量批次操作
- **Search is slow**: Performance degradation / 搜索变慢：性能下降 / 搜尋變慢：效能下降
- **Weekly maintenance**: Regular cache refresh / 每周维护：定期缓存刷新 / 每週維護：定期快取刷新
- **After manual edits**: Direct file changes / 手动编辑后：直接文件更改 / 手動編輯後：直接檔案更改

---

## Helper Commands / 辅助指令 / 輔助指令

These commands provide helper utilities for managing Claude Code configuration and skills:

这些指令提供用于管理 Claude Code 配置和技能的辅助工具：

這些指令提供用於管理 Claude Code 配置和技能的輔助工具：

| Command | File | Purpose / 用途 | 用途 |
|---------|------|---------------|------|
| `/创建指令` | `创建指令.md` | Create new Claude Code commands / 创建新的 Claude Code 指令 | 創建新的 Claude Code 指令 |
| `/创建技能` | `创建技能.md` | Create new Claude Code skills / 创建新的 Claude Code 技能 | 創建新的 Claude Code 技能 |
| `/claudian` | `claudian.md` | Claude-specific PARA management commands / Claude 专用的 PARA 管理指令 | Claude 專用的 PARA 管理指令 |
| `/obsidian` | `obsidian.md` | Auto-select appropriate Obsidian skill / 自动选择合适的 Obsidian 技能 | 自動選擇合適的 Obsidian 技能 |
| `/search` | `search.md` | Search InBox and PARA contents / 搜索 InBox 和 PARA 内容 | 搜尋 InBox 和 PARA 內容 |

### `/创建指令` / `/创建指令` / `/創建指令`

**Purpose**: Create new Claude Code commands / 创建新的 Claude Code 指令 / 創建新的 Claude Code 指令

**File**: `.claude/commands/创建指令.md`

#### Usage / 使用 / 使用

```bash
/创建指令
```

#### Interactive Workflow / 交互式工作流 / 互動式工作流

```
📝 创建新指令

请输入指令名称: my-command
请输入指令描述: My custom command description
请输入指令分类: [para] [helper] [custom] (默认: custom)
```

**Result**: Creates `.claude/commands/my-command.md` with template structure / 结果：创建 `.claude/commands/my-command.md`，包含模板结构 / 結果：建立 `.claude/commands/my-command.md`，包含模板結構

#### When to Use / 何时使用 / 何時使用

- **New workflow**: When you need a repeatable command pattern / 新工作流：需要可重复的指令模式時 / 新工作流：需要可重複的指令模式時
- **Automation**: Automate common tasks / 自动化：自动化常见任务 / 自動化：自動化常見任務
- **Custom utilities**: Add specialized helper commands / 自定义工具：添加专用辅助指令 / 自訂工具：新增專用輔助指令

---

### `/创建技能` / `/创建技能` / `/創建技能`

**Purpose**: Create new Claude Code skills (calls skill-creator) / 创建新的 Claude Code 技能（调用 skill-creator）/ 創建新的 Claude Code 技能（調用 skill-creator）

**File**: `.claude/commands/创建技能.md`

#### Usage / 使用 / 使用

```bash
/创建技能
```

#### Interactive Workflow / 交互式工作流 / 互動式工作流

```
🛠️ 创建新技能

请输入技能名称: my-custom-skill
请输入技能描述: Description of what this skill does
请输入技能触发条件: [automatic] [manual] (默认: manual)
```

**Result**: Creates `.claude/skills/my-custom-skill/SKILL.md` with template / 结果：创建 `.claude/skills/my-custom-skill/SKILL.md`，包含模板 / 結果：建立 `.claude/skills/my-custom-skill/SKILL.md`，包含模板

#### When to Use / 何时使用 / 何時使用

- **Domain expertise**: Specialized knowledge areas / 领域专业知识：专业知识领域 / 領域專業知識：專業知識領域
- **Complex workflows**: Multi-step procedures / 复杂工作流：多步骤程序 / 複雜工作流：多步驟程序
- **Reusable patterns**: Common operations / 可重用模式：常见操作 / 可重用模式：常見操作

---

### `/claudian` / `/claudian` / `/claudian`

**Purpose**: Claude-specific PARA management commands / Claude 专用的 PARA 管理指令 / Claude 專用的 PARA 管理指令

**File**: `.claude/commands/claudian.md`

#### Usage / 使用 / 使用

```bash
/claudian
```

#### Interactive Menu / 交互式菜单 / 互動式選單

```
🤖 Claudian - PARA Assistant

选择操作:
[1] 查看库概览
[2] 整理收件箱
[3] 刷新缓存
[4] 搜索内容
[5] 批量操作
[6] 设置
[0] 退出

请选择 (1-6):
```

#### Sub-commands / 子指令 / 子指令

| Sub-command | Action / 动作 | 動作 |
|-------------|---------------|------|
| `1` | View library overview / 查看库概览 / 查看庫概覽 |
| `2` | Organize InBox / 整理收件箱 / 整理收件箱 |
| `3` | Refresh cache / 刷新缓存 / 重新整理快取 |
| `4` | Search content / 搜索内容 / 搜尋內容 |
| `5` | Batch operations / 批量操作 / 批次操作 |
| `6` | Settings / 设置 / 設定 |

#### When to Use / 何时使用 / 何時使用

- **General PARA management**: Day-to-day PARA operations / 通用 PARA 管理：日常 PARA 操作 / 通用 PARA 管理：日常 PARA 操作
- **Quick access**: Menu-driven PARA tasks / 快速访问：菜单驱动的 PARA 任务 / 快速存取：選單驅動的 PARA 任務
- **Beginner-friendly**: Guided PARA workflows / 初学者友好：引导式 PARA 工作流 / 初學者友善：引導式 PARA 工作流

---

### `/obsidian` / `/obsidian` / `/obsidian`

**Purpose**: Auto-select appropriate Obsidian skill / 自动选择合适的 Obsidian 技能 / 自動選擇合適的 Obsidian 技能

**File**: `.claude/commands/obsidian.md`

#### Usage / 使用 / 使用

```bash
/obsidian
```

#### Automatic Skill Selection / 自动技能选择 / 自動技能選擇

This command automatically selects the appropriate skill based on file type:

此指令根据文件类型自动选择合适的技能：

此指令根據檔案類型自動選擇合適的技能：

| File Type | Skill Selected / 选择的技能 / 選擇的技能 |
|-----------|-------------------------------------------|
| `.md` files | `obsidian-markdown` / Obsidian Markdown / Obsidian Markdown |
| `.base` files | `obsidian-bases` / Obsidian Bases / Obsidian Bases |
| `.canvas` files | `json-canvas` / JSON Canvas / JSON Canvas |

#### Example Usage / 示例使用 / 範例使用

```bash
# Working with markdown file
/obsidian
# → Loads obsidian-markdown skill

# Working with database file
/obsidian
# → Loads obsidian-bases skill

# Working with canvas file
/obsidian
# → Loads json-canvas skill
```

#### When to Use / 何时使用 / 何時使用

- **Working with Obsidian files**: Any Obsidian-specific content / 处理 Obsidian 文件：任何 Obsidian 特定内容 / 處理 Obsidian 檔案：任何 Obsidian 特定內容
- **Need proper syntax**: Ensure correct formatting / 需要正确语法：确保正确格式 / 需要正確語法：確保正確格式
- **Switching file types**: Changing between .md, .base, .canvas / 切换文件类型：在 .md、.base、.canvas 之间切换 / 切換檔案類型：在 .md、.base、.canvas 之間切換

---

### `/search` / `/search` / `/search`

**Purpose**: Search InBox and PARA contents / 搜索 InBox 和 PARA 内容 / 搜尋 InBox 和 PARA 內容

**File**: `.claude/commands/search.md`

#### Usage / 使用 / 使用

```bash
/search [query]
```

#### Examples / 示例 / 範例

```bash
# Basic search
/search para

# Search with quotes for exact match
/search "PARA methodology"

# Search in specific folder
/search PARA methodology --folder="1 Projects"

# Search by tags
/search #project #active

# Search with filters
/search obsidian --filter=tags:learning,filter=status:in-progress
```

#### Example Output / 示例输出 / 範例輸出

```
🔍 搜索结果: "PARA methodology"

找到 12 个匹配结果:

InBox (2):
- [1] "学习 PARA 笔记.md" - 匹配度: 高
- [2] "PARA 方法论总结.md" - 匹配度: 中

Projects (3):
- [3] [[1 Projects/知识整理/Implementing PARA.md]] - 匹配度: 高
- [4] [[1 Projects/Obsidian/Obsidian Setup.md]] - 匹配度: 中
- [5] [[1 Projects/写作/PARA Writing Guide.md]] - 匹配度: 低

Resources (5):
- [6] [[3 Resources/Productivity/PARA Methodology.md]] - 匹配度: 高
- [7] [[3 Resources/Productivity/Organization Systems.md]] - 匹配度: 中
...

💡 提示: 输入数字打开文件，输入 'q' 退出
```

#### When to Use / 何时使用 / 何時使用

- **Finding specific content**: When you know what you're looking for / 查找特定内容：当你知道要找什么时 / 查找特定內容：當你知道要找什麼時
- **Exploring topics**: Discover related notes / 探索主题：发现相关笔记 / 探索主題：發現相關筆記
- **Cross-referencing**: Connect scattered ideas / 交叉引用：连接分散的想法 / 交叉引用：連結分散的想法
- **Auditing library**: Review content by keyword / 审计库：按关键词审查内容 / 審計庫：按關鍵詞審查內容

---

## Command Best Practices / 指令最佳实践 / 指令最佳實踐

### 1. Regular Usage / 定期使用 / 定期使用

| Frequency | Command | Purpose / 目的 | 目的 |
|-----------|---------|---------------|------|
| **Daily** | `/para-库概览` | Check InBox status / 检查收件箱状态 / 檢查收件箱狀態 |
| **Daily** | `/search` | Find current information / 查找当前信息 / 查找當前資訊 |
| **Weekly** | `/para-整理收集` | Process InBox / 处理收件箱 / 處理收件箱 |
| **Weekly** | `/para-刷新缓存` | Update cache / 更新缓存 / 更新快取 |
| **As needed** | `/obsidian` | Work with Obsidian files / 处理 Obsidian 文件 / 處理 Obsidian 檔案 |
| **As needed** | `/创建指令` | Create new commands / 创建新指令 / 創建新指令 |

### 2. Workflow Integration / 工作流集成 / 工作流整合

```
早晨例行程序 / Morning Routine / 晨間例行程序:
1. /para-库概览 (检查收件箱)
2. /search [today's topic] (查找今日主题)
3. /obsidian (开始工作)

工作流程 / Work Workflow / 工作流程:
1. 捕获笔记到 InBox
2. /para-整理收集 (定期整理)
3. /search [相关主题] (连接想法)

每周审查 / Weekly Review / 每週審查:
1. /para-库概览 (整体健康度)
2. /para-整理收集 (清空收件箱)
3. /para-刷新缓存 (更新性能)
```

### 3. Command Aliases / 指令别名 / 指令別名

You can create shorter aliases by creating command files that call other commands:

可以通过创建调用其他指令的指令文件来创建更短的别名：

可以透過建立呼叫其他指令的指令檔案來建立更短的別名：

```markdown
---
title: Quick Overview
---

/para-库概览
```

Save as `.claude/commands/qo.md`, then invoke with `/qo`

保存为 `.claude/commands/qo.md`，然后用 `/qo` 调用

儲存為 `.claude/commands/qo.md`，然後用 `/qo` 調用

---

## Related Skills / 相关技能 / 相關技能

- **para-methodology**: PARA structure and workflow / PARA 结构和工作流 / PARA 結構和工作流
- **obsidian-syntax**: Obsidian-specific syntax / Obsidian 特定语法 / Obsidian 特定語法
- **repo-context**: Repository structure and configuration / 仓库结构和配置 / 倉庫結構和配置

# Repository Context Skill

## Overview / 概览 / 概覽

This skill provides comprehensive context about the AI-value repository structure, purpose, and configuration.

本技能提供关于 AI-value 仓库结构、目的和配置的全面上下文信息。

本技能提供關於 AI-value 倉庫結構、目的和配置的全面上下文資訊。

---

## Quick Reference

- **Repository**: AI-value Personal Knowledge Management System
- **License**: Apache 2.0
- **Primary branch**: `main`
- **Working branch**: `main_para`
- **Language**: Multilingual (English, 简体中文, 繁體中文)

---

## Project Purpose / 项目目的 / 專案目的

### English

**AI-value** is a personal knowledge management system using PARA methodology (Projects, Areas, Resources, Archives). It's a markdown-based knowledge base with Obsidian integration, designed to organize information systematically.

### 简体中文

**AI-value** 是一个基于 PARA 方法论（项目、领域、资源、归档）的个人知识管理系统。这是一个基于 Markdown 的知识库，集成了 Obsidian，旨在系统地组织信息。

### 繁體中文

**AI-value** 是一個基於 PARA 方法論（Projects, Areas, Resources, Archives）的個人知識管理系統。這是一個基於 Markdown 的知識庫，整合了 Obsidian，旨在系統地組織資訊。

### Key Features / 核心功能 / 核心功能

- ✅ **PARA Methodology**: Systematic organization by actionability and time horizon / 系统组织：按可执行性和时间跨度 / 系統組織：按可執行性和時間跨度
- ✅ **Markdown-based**: Plain text, version control friendly / 基于 Markdown：纯文本，版本控制友好 / 基於 Markdown：純文字，版本控制友好
- ✅ **Obsidian Integration**: Native support for wikilinks, properties, plugins / Obsidian 集成：原生支持 wikilinks、属性、插件 / Obsidian 整合：原生支援 wikilinks、屬性、外掛
- ✅ **Zettelkasten**: Atomic notes for knowledge networking / 卡片盒笔记：知识网络化 / 卡片盒筆記：知識網絡化
- ✅ **Multilingual**: Documentation in English, Simplified Chinese, Traditional Chinese / 多语言：英、简、繁文档 / 多語言：英、簡、繁文件
- ✅ **Cache System**: Performance optimization for large vaults / 缓存系统：大型 vault 性能优化 / 快取系統：大型 vault 效能優化

---

## Repository Information / 仓库信息 / 倉庫信息

### Basic Info / 基本信息 / 基本資訊

| Property | Value | 值 | 值 |
|----------|-------|-----|-----|
| **Name** | AI-value | AI-value | AI-value |
| **Description** | Personal Knowledge Management System / 个人知识管理系统 / 個人知識管理系統 | | |
| **License** | Apache 2.0 | Apache 2.0 | Apache 2.0 |
| **Type** | Documentation / Knowledge Base / 文档 / 知识库 / 文件 / 知識庫 | | |
| **Language** | Python (for tooling), Markdown (for content) / Python（工具），Markdown（内容） / Python（工具），Markdown（內容） | | |

### Git Information / Git 信息 / Git 資訊

| Property | Value | 值 | 值 |
|----------|-------|-----|-----|
| **Remote URL** | `https://github.com/kmjade/AI-value.git` | | |
| **Primary branch** | `main` | | |
| **Working branch** | `main_para` | | |
| **Default branch** | `main` | | |

### Branch Strategy / 分支策略 / 分支策略

- **`main`**: Stable releases / 稳定发布 / 穩定發布
- **`main_para`**: Active development branch for PARA implementation / PARA 实施的活跃开发分支 / PARA 實施的活躍開發分支
- **Feature branches**: For specific features or experiments / 特定功能或实验 / 特定功能或實驗

---

## Folder Structure / 文件夹结构 / 資料夾結構

### Root Level Structure / 根级结构 / 根級結構

```
AI-value/
├── 0 Personals/               # Personal items / 个人项目 / 個人專案
│   └── 📥 00_InBox/          # 收件箱 / Inbox for quick capture
├── 1 Projects/               # Projects / 项目 / 專案
├── 2 Areas/                  # Areas / 领域 / 領域
├── 3 Resources/              # Resources / 资源 / 資源
├── 4 Archives/               # Archives / 归档 / 歸檔
├── 5 Zettels/               # Atomic notes / 原子化笔记 / 原子化筆記
│   ├── 💡 fleeting/         # Fleeting notes / 闪念笔记 / 閃念筆記
│   ├── 📌 permanent/        # Permanent notes / 永久笔记 / 永久筆記
│   ├── 📚 literature/       # Literature notes / 文献笔记 / 文獻筆記
│   └── 📁 structure/        # Structure notes / 结构笔记 / 結構筆記
├── _Template/               # Templates / 模板 / 模板
├── _meta/                   # Metadata and config / 元数据和配置 / 元數據和配置
├── _Cache/                  # Performance cache / 性能缓存 / 效能快取
├── .claude/                 # Claude Code configuration / Claude Code 配置 / Claude Code 配置
├── .obsidian/               # Obsidian settings / Obsidian 设置 / Obsidian 設定
└── .idea/                   # IntelliJ IDEA settings (gitignored)
```

### Detailed Breakdown / 详细分解 / 詳細分解

#### 0 Personals / 个人 / 個人

```
0 Personals/
└── 📥 00_InBox/
    ├── Quick notes/
    └── To organize/
```

- **Purpose**: Temporary collection for personal items / 个人项目的临时收集 / 個人專案的臨時收集
- **Content**: Quick captures, drafts, unorganized notes / 快速捕获、草稿、未整理笔记 / 快速捕獲、草稿、未整理筆記
- **Action**: Process regularly with `/para-整理收集` / 定期使用 `/para-整理收集` 处理 / 定期使用 `/para-整理收集` 處理

#### 1 Projects / 项目 / 專案

```
1 Projects/
├── Project A/
│   ├── Main Note.md
│   └── Tasks.md
└── Project B/
    └── Main Note.md
```

- **Purpose**: Active, short-term endeavors with deadlines / 有期限的活跃短期项目 / 有期限的活躍短期專案
- **Characteristics**: Time-bound, actionable, outcome-oriented / 有时限、可执行、结果导向 / 有時限、可執行、結果導向
- **Lifecycle**: Active → Completed → Archived / 活跃 → 已完成 → 已归档 / 活躍 → 已完成 → 已歸檔

#### 2 Areas / 领域 / 領域

```
2 Areas/
├── Health/
├── Finance/
├── Career/
└── Relationships/
```

- **Purpose**: Long-term responsibilities / 长期责任 / 長期責任
- **Characteristics**: Ongoing, maintenance-oriented, indefinite / 持续进行、维护导向、无期限 / 持續進行、維護導向、無期限
- **Examples**: Health monitoring, Financial planning, Professional development / 健康监测、财务规划、职业发展 / 健康監測、財務規劃、職業發展

#### 3 Resources / 资源 / 資源

```
3 Resources/
├── AI/
├── Programming/
├── Cooking/
└── Languages/
```

- **Purpose**: Topics of ongoing interest / 持续感兴趣的主题 / 持續感興趣的主題
- **Characteristics**: Reference material, educational, inspirational / 参考材料、教育性、启发性 / 參考材料、教育性、啟發性
- **Usage**: Look up information, learn new topics, find inspiration / 查找信息、学习新主题、寻找灵感 / 查找資訊、學習新主題、尋找靈感

#### 4 Archives / 归档 / 歸檔

```
4 Archives/
├── Completed Projects/
├── Old Resources/
└── Historical Notes/
```

- **Purpose**: Completed or inactive items / 已完成或非活跃项目 / 已完成或非活躍專案
- **Characteristics**: Done, on hold, no longer active / 已完成、暂停、不再活跃 / 已完成、暫停、不再活躍
- **Action**: Keep accessible but out of the way / 保持可访问但不碍事 / 保持可訪問但不礙事

#### 5 Zettels / 原子化笔记 / 原子化筆記

```
5 Zettels/
├── 💡 fleeting/
│   └── Quick thoughts and ideas/
├── 📌 permanent/
│   └── Knowledge atoms/
├── 📚 literature/
│   └── Research notes/
└── 📁 structure/
    └── System notes/
```

- **Purpose**: Atomic notes for knowledge networking / 知识网络的原子化笔记 / 知識網絡的原子化筆記
- **Flow**: fleeting → permanent → literature / 闪念 → 永久 → 文献 / 閃念 → 永久 → 文獻
- **Characteristics**: Atomic, interconnected, unique IDs / 原子化、互联、唯一 ID / 原子化、互聯、唯一 ID

#### _Template / 模板 / 模板

```
_Template/
├── Project Template.md
├── Area Template.md
├── Resource Template.md
└── Zettel Template.md
```

- **Purpose**: Standardized note templates / 标准化笔记模板 / 標準化筆記模板
- **Usage**: Speed up note creation, ensure consistency / 加速笔记创建、确保一致性 / 加速筆記創建、確保一致性

#### _meta / 元数据 / 元數據

```
_meta/
├── system-config.md
└── documentation/
```

- **Purpose**: System metadata and configuration / 系统元数据和配置 / 系統元數據和配置
- **Content**: Configuration files, system documentation / 配置文件、系统文档 / 配置文件、系統文件

#### _Cache / 缓存 / 快取

```
_Cache/
├── para-cache.json
└── search-index.json
```

- **Purpose**: Performance optimization cache files / 性能优化缓存文件 / 效能優化快取檔案
- **Management**: Update with `/para-刷新缓存` / 使用 `/para-刷新缓存` 更新 / 使用 `/para-刷新快取` 更新

#### .claude / Claude Code Configuration

```
.claude/
├── commands/
│   ├── para-库概览.md
│   ├── para-整理收集.md
│   └── para-刷新缓存.md
├── skills/
│   ├── obsidian-markdown/
│   ├── obsidian-bases/
│   ├── json-canvas/
│   └── [more skills]
└── CLAUDE.md
```

- **Purpose**: Claude Code configuration and skills / Claude Code 配置和技能 / Claude Code 配置和技能
- **Commands**: Reusable command patterns / 可重用的命令模式 / 可重用的命令模式
- **Skills**: Specialized capabilities / 专业能力 / 專業能力

#### .obsidian / Obsidian Settings

```
.obsidian/
├── plugins/
├── themes/
├── workspaces.json
└── config.json
```

- **Purpose**: Obsidian plugin settings and configuration / Obsidian 插件设置和配置 / Obsidian 外掛設定和配置
- **Note**: Version controlled (unless sensitive) / 版本控制（除非敏感） / 版本控制（除非敏感）

---

## Vault Absolute Path / Vault 绝对路径 / Vault 絕對路徑

```
D:\Knowledge\AI-value
```

This is the root directory from which all relative paths are calculated.

这是计算所有相对路径的根目录。

這是計算所有相對路徑的根目錄。

---

## Path Rules / 路径规则 / 路徑規則

### Vault Files / Vault 文件 / Vault 檔案

When working with vault files, **always use relative paths** from the vault root:

处理 vault 文件时，**始终使用**从 vault root 开始的 **相对路径**：

處理 vault 檔案時，**始終使用**從 vault root 開始的 **相對路徑**：

| Format | Correct / 正确 | Wrong / 错误 |
|--------|---------------|--------------|
| **Note** | `notes/my-note.md` ✅ | `/notes/my-note.md` ❌ |
| **Note** | `my-note.md` ✅ | `D:\Knowledge\AI-value\my-note.md` ❌ |
| **Note** | `folder/subfolder/file.md` ✅ | `C:/Users/me/Documents/file.md` ❌ |
| **Root** | `.` ✅ | `/` ❌ |

### Export Paths / 导出路径 / 匯出路徑

Write-only destinations outside the vault:

vault 外部的只写目标：

vault 外部的只寫目標：

- `~/Desktop`
- `~/Downloads`

```bash
# Direct export / 直接导出 / 直接匯出
pandoc ./note.md -o ~/Desktop/note.docx

# Pipe to stdout (no temp file) / 管道到标准输出（无临时文件） / 管道到標準輸出（無臨時檔案）
pandoc ./note.md | head -100

# Copy to export location / 复制到导出位置 / 複製到匯出位置
cp ./note.md ~/Desktop/note.md
```

### External Contexts / 外部上下文 / 外部上下文

When external contexts are enabled, they have **full read/write access**:

启用外部上下文时，它们具有 **完全读写权限**：

啟用外部上下文時，它們具有 **完全讀寫權限**：

```xml
<external_contexts>
/absolute/path/one
/absolute/path/two
</external_contexts>
```

These paths are treated as additional roots with full access.

这些路径被视为具有完全访问权限的附加根目录。

這些路徑被視為具有完全訪問權限的附加根目錄。

### Path Specificity / 路径特异性 / 路徑特異性

When paths overlap, the **more specific path wins**:

当路径重叠时，**更具体的路径获胜**：

當路徑重疊時，**更具體的路徑獲勝**：

Example / 示例 / 範例:

- `~/Desktop` → Export (write-only)
- `~/Desktop/Workspace` → External context (full access)

→ Files in `~/Desktop/Workspace` have **full read/write access**
→ Files directly in `~/Desktop` remain **write-only**

→ `~/Desktop/Workspace` 中的文件具有 **完全读写权限**
→ 直接在 `~/Desktop` 中的文件保持 **只写权限**

→ `~/Desktop/Workspace` 中的檔案具有 **完全讀寫權限**
→ 直接在 `~/Desktop` 中的檔案保持 **只寫權限**

---

## Git Strategy / Git 策略 / Git 策略

### Commit Conventions / 提交约定 / 提交約定

Follow conventional commits:

遵循传统提交格式：

遵循傳統提交格式：

```bash
# Format / 格式
<type>(<scope>): <subject>

# Types / 类型
- feat: New feature / 新功能
- fix: Bug fix / 修复 Bug / 修復 Bug
- docs: Documentation changes / 文档变更 / 文件變更
- refactor: Code refactoring / 代码重构 / 程式碼重構
- chore: Maintenance tasks / 维护任务 / 維護任務
- para: PARA-related changes / PARA 相关变更 / PARA 相關變更

# Examples / 示例
feat(commands): add new PARA overview command
fix(notes): correct broken wikilinks
docs(readme): update installation instructions
para(projects): reorganize project structure
```

### Branch Naming / 分支命名 / 分支命名

```bash
# Feature branches / 功能分支
feature/new-command
feature/improve-cache

# Bugfix branches / 修复分支
fix/broken-link
fix/cache-update

# Experiment branches / 实验分支
exp/zettelkasten-improvement
exp/new-template
```

### What to Commit / 提交什么 / 提交什麼

**Do commit / 应该提交 / 應該提交:**
- ✅ Markdown files and content / Markdown 文件和内容 / Markdown 檔案和內容
- ✅ `.claude/` configuration / `.claude/` 配置 / `.claude/` 配置
- ✅ `.obsidian/` settings (non-sensitive) / `.obsidian/` 设置（非敏感） / `.obsidian/` 設定（非敏感）
- ✅ Template files / 模板文件 / 模板檔案
- ✅ Documentation / 文档 / 文件

**Do NOT commit / 不应提交 / 不應提交:**
- ❌ Personal API keys / 个人 API 密钥 / 個人 API 金鑰
- ❌ `.idea/` (already gitignored)
- ❌ Sensitive configuration / 敏感配置 / 敏感配置
- ❌ Cache files (consider adding to .gitignore) / 缓存文件（考虑添加到 .gitignore） / 快取檔案（考慮添加到 .gitignore）

---

## Related Skills / 相关技能 / 相關技能

- **para-methodology**: PARA structure and workflow / PARA 结构和工作流 / PARA 結構和工作流
- **obsidian-syntax**: Obsidian-specific syntax / Obsidian 特定语法 / Obsidian 特定語法
- **markdown-standards**: File naming and conventions / 文件命名和规范 / 檔案命名和規範
- **zettelkasten-workflow**: Atomic notes system / 原子化笔记系统 / 原子化筆記系統

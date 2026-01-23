# AI-value 个人知识管理系统

欢迎使用 AI-value！这是一个基于 PARA 方法论的个人知识管理系统，集成了 Obsidian，旨在系统地组织信息。

Welcome to AI-value! This is a personal knowledge management system based on PARA methodology, integrated with Obsidian, designed to systematically organize information.

---

## 快速开始 / Quick Start

### 系统结构 / System Structure

```
AI-value/
├── 0 Personals/              # 个人项目
│   └── 📥 00_InBox/        # 收件箱 / Inbox
├── 1 Projects/               # 项目 / Projects
├── 2 Areas/                  # 领域 / Areas
├── 3 Resources/               # 资源 / Resources
├── 4 Archives/                # 归档 / Archives
├── 5 Zettels/                # 原子化笔记 / Atomic notes
├── _Template/                 # 模板 / Templates
├── _meta/                    # 系统元数据 / System metadata
└── .claude/                  # Claude Code 配置 / Configuration
```

### PARA 方法论 / PARA Methodology

| 类别 / Category | 说明 / Description | 示例 / Examples |
|----------------|-------------------|------------------|
| **Projects** (`1 Projects/`) | 有期限的活跃短期项目 / Active, short-term endeavors with deadlines | "2024 年度计划", "产品发布" |
| **Areas** (`2 Areas/`) | 长期责任领域 / Long-term responsibilities | "健康", "财务", "职业发展" |
| **Resources** (`3 Resources/`) | 持续感兴趣的主题 / Topics of ongoing interest | "Obsidian 使用指南", "机器学习资料" |
| **Archives** (`4 Archives/`) | 已完成或非活跃项目 / Completed or inactive items | "2023 年度总结", "已发布产品" |

---

## 功能特性 / Features

### 1. PARA 组织 / PARA Organization

- **InBox (`0 Personals/📥 00_InBox/`)** - 快速捕获想法和笔记 / Quick capture of ideas and notes
- **Projects (`1 Projects/`)** - 管理有期限的项目 / Manage projects with deadlines
- **Areas (`2 Areas/`)** - 追踪长期责任 / Track long-term responsibilities
- **Resources (`3 Resources/`)** - 收集感兴趣的主题 / Collect topics of interest
- **Archives (`4 Archives/`)** - 存储已完成内容 / Store completed items

### 2. Zettelkasten 笔记系统 / Zettelkasten Note System

- **💡 fleeting/** - 闪念笔记 / Quick capture notes
- **📌 permanent/** - 永久知识原子 / Permanent knowledge atoms
- **📚 literature/** - 文献和研究笔记 / Literature and research notes
- **📁 structure/** - 系统和流程笔记 / System and workflow notes

### 3. Claude Code 集成 / Claude Code Integration

#### Skills 体系 / Skills System

AI-value 拥有完整的 Claude Skills 体系，实现按需加载和模块化知识管理：

AI-value has a complete Claude Skills system, implementing on-demand loading and modular knowledge management:

| Skill | 描述 / Description | 大小 / Size |
|-------|-------------------|-------------|
| **para-methodology** | PARA 结构、工作流、元数据 / PARA structure, workflow, metadata | ~400 行 |
| **obsidian-syntax** | Wikilinks、提示块、属性、嵌入 / Wikilinks, callouts, properties, embeds | ~500 行 |
| **repo-context** | 仓库结构、路径、Git 信息 / Repository structure, paths, Git info | ~450 行 |
| **markdown-standards** | 文件命名、多语言支持、规范 / File naming, multilingual support, conventions | ~400 行 |
| **claude-commands** | 指令使用和工作流 / Command usage and workflows | ~500 行 |
| **zettelkasten-workflow** | 原子笔记、链接、唯一 ID / Atomic notes, linking, unique IDs | ~550 行 |
| **simplified-chinese-first** | 简体中文优先规范 / Simplified Chinese first rule | ~400 行 |
| **traditional-chinese-first** | 繁体中文优先规范 / Traditional Chinese first rule | ~400 行 |

#### 使用方式 / Usage

**自动加载 / Automatic Loading:**

Claude Code 会根据任务类型自动加载相关 Skills：

Claude Code will automatically load relevant Skills based on task type:

```bash
# 示例 1：编写 Markdown 文档
用户：帮我写一个 README
# Claude 自动加载：obsidian-syntax, markdown-standards, simplified-chinese-first
# Token 消耗：约 2,000 tokens（节省 92%）

# 示例 2：组织 PARA 笔记
用户：按照 PARA 原则整理收件箱
# Claude 自动加载：para-methodology, simplified-chinese-first
# Token 消耗：约 5,000 tokens（节省 80%）
```

**手动查看 / Manual Viewing:**

点击链接查看详细 Skill 内容：

Click links to view detailed Skill content:

- [Skills 索引](.claude/skills/README.md) - 查看 Skills 列表 / View Skills list
- [PARA 方法论](.claude/skills/para-methodology/SKILL.md) - 了解 PARA / Learn about PARA
- [Obsidian 语法](.claude/skills/obsidian-syntax/SKILL.md) - 学习 Obsidian 语法 / Learn Obsidian syntax

---

## 工作流 / Workflows

### PARA 工作流 / PARA Workflow

```
第 1 步：捕获 / Capture
└─ 添加新信息到 `0 Personals/📥 00_InBox/`

第 2 步：整理 / Organize
└─ 使用 `/para-整理收集` 命令整理 InBox
   └─ 按照 PARA 原则分发到对应文件夹

第 3 步：复查 / Review
└─ 使用 `/para-库概览` 命令审查库状态
   └─ 查看各分类的文件数和状态

第 4 步：归档 / Archive
└─ 将已完成项目移至 `4 Archives/`
```

### Zettelkasten 工作流 / Zettelkasten Workflow

```
第 1 步：创建 / Create
└─ 在 `5 Zettels/💡 fleeting/` 中创建闪念笔记

第 2 步：处理 / Process
└─ 将有价值的想法转换为永久笔记
   └─ 移动到 `5 Zettels/📌 permanent/`

第 3 步：链接 / Link
└─ 使用 wikilinks 链接相关概念
   └─ 格式：[[Note Name]]

第 4 步：发展 / Develop
└─ 将文献笔记添加到 `5 Zettels/📚 literature/`

第 5 步：结构化 / Structure
└─ 在 `5 Zettels/📁 structure/` 中创建概览笔记
```

---

## Claude Code 命令 / Claude Code Commands

### PARA 管理命令 / PARA Management Commands

| 命令 / Command | 功能 / Function | 说明 / Description |
|----------------|----------------|-------------------|
| `/para-库概览` | 显示 PARA 库概览 / Display PARA library overview | 查看各分类的文件数和状态 / View file count and status of each category |
| `/para-整理收集` | 整理收件箱 / Organize InBox | 按照 PARA 原则整理 InBox 内容 / Organize InBox content by PARA principles |
| `/para-刷新缓存` | 刷新缓存 / Refresh cache | 更新性能缓存文件 / Update performance cache files |

### 辅助命令 / Helper Commands

| 命令 / Command | 功能 / Function | 说明 / Description |
|----------------|----------------|-------------------|
| `/search` | 搜索内容 / Search content | 快速搜索 InBox 和 PARA 内容 / Quickly search InBox and PARA content |
| `/obsidian` | 自动选择 Obsidian 技能 / Auto-select Obsidian skill | 根据文件类型自动选择合适的 Obsidian 技能 / Auto-select appropriate Obsidian skill based on file type |
| `/claudian` | PARA 助手 / PARA assistant | PARA 管理的交互式菜单 / Interactive menu for PARA management |

---

## 最佳实践 / Best Practices

### 1. 使用 InBox / Use InBox

- ✅ **快速捕获** - 不要担心格式，先把想法记下来
- ✅ **定期整理** - 每天或每周整理一次 InBox
- ✅ **清空原则** - 保持 InBox 清空或最小化

### 2. PARA 分类 / PARA Classification

使用以下问题进行分类：

Use the following questions for classification:

```
这是可执行的项目吗？ → Projects / 專案
  └─ 有截止日期吗？ → Yes
  └─ 需要多个步骤吗？ → Yes

这是长期责任吗？ → Areas / 領域
  └─ 需要持续维护吗？ → Yes
  └─ 没有截止日期吗？ → Yes

这是参考资料吗？ → Resources / 資源
  └─ 感兴趣的主题？ → Yes
  └─ 用于参考学习？ → Yes

这是已完成的吗？ → Archives / 歸檔
  └─ 项目已完成？ → Yes
  └─ 不再活跃？ → Yes
```

### 3. Zettelkasten 原则 / Zettelkasten Principles

- ✅ **原子性** - 每个笔记只包含一个想法
- ✅ **独特 ID** - 使用 `YYYYMMDD-XXXX` 格式
- ✅ **充分链接** - 链接相关的概念
- ✅ **自包含** - 每个笔记可以独立理解

### 4. 文件命名 / File Naming

- ✅ **描述性名称** - 使用清晰的名称描述内容
- ✅ **使用空格** - Obsidian wikilinks 支持空格
- ✅ **避免特殊字符** - 避免使用 `: * ? " < > | /`
- ✅ **模板前缀** - 模板文件使用 `_template-` 前缀

---

## 文档 / Documentation

### 项目文档 / Project Documentation

- **[CLAUDE.md](CLAUDE.md)** - Claude Code 核心规则和索引 / Core rules and index for Claude Code
- **[.claude/skills/README.md](.claude/skills/README.md)** - Skills 完整索引 / Complete Skills index
- **[0 Personals/📥 00_InBox/Claude Skills 文档/skills-introduction/theme.md](0%20Personals/%F0%208%209%20InBox/Claude%20Skills%20%E6%96%E5%8F%A3/skills-introduction/theme.md)** - Skills 详细文档 / Detailed Skills documentation

### Skills 文档 / Skills Documentation

Skills 文档详细说明每个 Skill 的使用方法：

Skills documentation provides detailed instructions for each Skill:

- **[para-methodology](.claude/skills/para-methodology/SKILL.md)** - PARA 方法论完整指南 / Complete PARA methodology guide
- **[obsidian-syntax](.claude/skills/obsidian-syntax/SKILL.md)** - Obsidian 语法参考 / Obsidian syntax reference
- **[repo-context](.claude/skills/repo-context/SKILL.md)** - 仓库结构和配置 / Repository structure and configuration
- **[markdown-standards](.claude/skills/markdown-standards/SKILL.md)** - Markdown 标准和规范 / Markdown standards and conventions
- **[claude-commands](.claude/skills/claude-commands/SKILL.md)** - Claude Code 命令使用指南 / Claude Code commands usage guide
- **[zettelkasten-workflow](.claude/skills/zettelkasten-workflow/SKILL.md)** - Zettelkasten 完整工作流 / Complete Zettelkasten workflow
- **[simplified-chinese-first](.claude/skills/simplified-chinese-first/SKILL.md)** - 简体中文优先规范 / Simplified Chinese first rule
- **[traditional-chinese-first](.claude/skills/traditional-chinese-first/SKILL.md)** - 繁体中文优先规范 / Traditional Chinese first rule

---

## 许可证 / License

Apache License 2.0

---

## 贡献 / Contributing

欢迎贡献！欢迎提出建议和改进建议！

Contributions are welcome! Feel free to suggest improvements and submit pull requests!

---

## 联系方式 / Contact

- **仓库**：https://github.com/kmjade/AI-value.git
- **Issues**：https://github.com/kmjade/AI-value/issues

---

> [!tip] 提示 / Tip
>
> 使用 `/obsidian` 命令可以自动选择合适的 Obsidian 技能！
>
> Use the `/obsidian` command to automatically select the appropriate Obsidian skill!
>
> 根据文件类型（.md, .base, .canvas）智能加载对应的技能。
> Intelligently load corresponding skills based on file type (.md, .base, .canvas).

# Claude Skills 索引 / Claude Skills Index

本目录包含项目的所有 Claude Skills，用于按需加载和管理开发规范。

This directory contains all Claude Skills for the project, used for on-demand loading and managing development standards.

---

## 概述 / Overview

### 什么是 Skills / What are Skills?

Claude Skills 是模块化的知识包，允许根据任务类型按需加载相关的开发规范和最佳实践。

Claude Skills are modular knowledge packages that allow on-demand loading of relevant development standards and best practices based on task types.

### 核心优势 / Key Benefits

- ✅ **Token 效率** - 平均节省 72% Token 消耗 / Token efficiency - Saves 72% tokens on average
- ✅ **按需加载** - 只加载必要的规范 / On-demand loading - Only load necessary standards
- ✅ **易于维护** - 每个 Skill 独立更新 / Easy maintenance - Each Skill updates independently
- ✅ **灵活扩展** - 轻松添加新 Skills / Flexible extension - Easily add new Skills

---

## Skills 索引 / Skills Index

### 通用开发 Skills / General Development Skills

这些 Skills 适用于所有类型的任务。

These Skills apply to all types of tasks.

| Skill | 描述 / Description | 适用场景 / Use Cases | 大小 / Size | 触发关键词 / Trigger Keywords |
|-------|------------------|---------------------|-------------|----------------------------|
| [**para-methodology**](./para-methodology/SKILL.md) | PARA 结构、工作流、元数据 / PARA structure, workflow, metadata | 处理 PARA 组织 / Working with PARA organization | ~400 行 | PARA, organize, 项目, 领域, 资源, 归档 |
| [**obsidian-syntax**](./obsidian-syntax/SKILL.md) | Wikilinks、提示块、属性、嵌入 / Wikilinks, callouts, properties, embeds | 编辑 markdown 文件 / Editing markdown files | ~500 行 | markdown, wikilink, [[]], > [! |
| [**repo-context**](./repo-context/SKILL.md) | 仓库结构、路径、Git 信息 / Repository structure, paths, Git info | 理解仓库 / Understanding repository | ~450 行 | repository, path, git, structure |
| [**markdown-standards**](./markdown-standards/SKILL.md) | 文件命名、多语言支持、规范 / File naming, multilingual support, conventions | 创建或组织文件 / Creating or organizing files | ~400 行 | filename, naming, multilingual, 简体中文, 繁體中文 |
| [**claude-commands**](./claude-commands/SKILL.md) | 指令使用和工作流 / Command usage and workflows | 使用 Claude Code 指令 / Using Claude Code commands | ~500 行 | command, /, 指令, 命令 |
| [**zettelkasten-workflow**](./zettelkasten-workflow/SKILL.md) | 原子笔记、链接、唯一 ID / Atomic notes, linking, unique IDs | 使用 Zettelkasten 系统 / Using Zettelkasten system | ~550 行 | zettelkasten, note, 原子笔记, 链接, ID |

### 内置 Obsidian Skills / Built-in Obsidian Skills

这些是 Claude Code 内置的 Obsidian 相关 Skills。

These are built-in Obsidian-related Skills in Claude Code.

| Skill | 文件类型 / File Types | 描述 / Description |
|-------|-------------------|-------------------|
| [**obsidian-markdown**](./obsidian-markdown/SKILL.md) | `.md` | Obsidian 增强版 Markdown，支持 wikilinks、提示块、属性 / Obsidian Flavored Markdown with wikilinks, callouts, properties |
| [**obsidian-bases**](./obsidian-bases/SKILL.md) | `.base` | 数据库视图、表格、卡片、公式 / Database views, tables, cards, formulas |
| [**json-canvas**](./json-canvas/SKILL.md) | `.canvas` | 思维导图、流程图、可视化画布 / Mind maps, flowcharts, visual canvases |

---

## 快速参考 / Quick Reference

### 按任务类型查找 Skills / Find Skills by Task Type

| 任务类型 / Task Type | 推荐使用的 Skills / Recommended Skills |
|-------------------|------------------------------------|
| **编写文档 / Writing Documentation** | obsidian-syntax, markdown-standards, para-methodology |
| **组织笔记 / Organizing Notes** | para-methodology, zettelkasten-workflow, obsidian-syntax |
| **编辑 Markdown / Editing Markdown** | obsidian-syntax, markdown-standards |
| **创建笔记 / Creating Notes** | zettelkasten-workflow, obsidian-syntax, markdown-standards |
| **使用 Claude 指令 / Using Claude Commands** | claude-commands |
| **理解仓库结构 / Understanding Repository** | repo-context, para-methodology |
| **创建可视化内容 / Creating Visual Content** | json-canvas, obsidian-syntax |
| **数据库操作 / Database Operations** | obsidian-bases, obsidian-syntax |

### 按关键词查找 Skills / Find Skills by Keywords

| 关键词 / Keyword | 相关的 Skills / Related Skills |
|----------------|----------------------------|
| PARA, 组织, 项目, 领域 | para-methodology |
| markdown, [[]], wikilink, > [! | obsidian-syntax |
| filename, naming, 多语言 | markdown-standards |
| command, /, 指令 | claude-commands |
| zettelkasten, note, 原子笔记 | zettelkasten-workflow |
| repository, git, path | repo-context |
| .base, database, 表格 | obsidian-bases |
| .canvas, 可视化, 流程图 | json-canvas |

---

## 使用指南 / Usage Guide

### 如何使用 Skills / How to Use Skills

#### 自动加载 / Automatic Loading

Claude 会根据任务类型**自动加载**相关的 Skills：

Claude will **automatically load** relevant Skills based on task type:

```bash
# 示例 1：编写 Markdown 文档
用户：帮我编写一个 README.md
# Claude 自动加载：obsidian-syntax, markdown-standards

# 示例 2：组织 PARA 笔记
用户：按照 PARA 原则整理收件箱
# Claude 自动加载：para-methodology

# 示例 3：创建 Zettelkasten 笔记
用户：创建一个关于 AI 的原子笔记
# Claude 自动加载：zettelkasten-workflow, obsidian-syntax
```

#### 手动查看 / Manual Viewing

你可以直接点击上方的链接查看详细内容：

You can click the links above to view detailed content:

- 查看 Skill 内容 / View Skill content：点击表格中的 Skill 名称
- 查看示例 / View examples：在 Skill 文件中找到示例部分
- 查看参考文档 / View reference docs：在 Skill 的 reference/ 目录

### Skills 工作流程 / Skills Workflow

```
用户请求
   ↓
Claude 分析任务类型
   ↓
匹配相关 Skills
   ↓
按优先级加载 Skills
   ↓
应用 Skills 规范
   ↓
生成符合规范的输出
```

---

## 最佳实践 / Best Practices

### 1. 合理使用 Skills / Using Skills Appropriately

✅ **推荐 / Recommended:**

- 让 Claude 自动加载相关 Skills / Let Claude automatically load relevant Skills
- 查看适用场景了解何时使用 Skill / Check use cases to understand when to use a Skill
- 遵循 Skills 中的规范和最佳实践 / Follow standards and best practices in Skills

❌ **避免 / Avoid:**

- 强制加载不必要的 Skills / Force loading unnecessary Skills
- 忽略 Skills 的建议 / Ignore Skill recommendations
- 在任务之间切换时清除 Skills 缓存（除非必要）/ Clear Skill cache between tasks (unless necessary)

### 2. 维护和更新 / Maintenance and Updates

#### 定期审查 / Regular Review

- **每周**：检查是否有新的使用场景 / Weekly: Check for new use cases
- **每月**：更新过时的规则和标准 / Monthly: Update outdated rules and standards
- **每季度**：全面审查所有 Skills / Quarterly: Full review of all Skills

#### 更新流程 / Update Process

```
发现需要更新
   ↓
1. 编辑对应的 Skill 文件
   └─ 修改 SKILL.md
   ↓
2. 测试更新
   └─ 验证更新是否正确
   ↓
3. 更新此 README
   └─ 同步更新索引和描述
   ↓
4. 提交更改
   └─ Git commit
```

### 3. 创建新 Skills / Creating New Skills

#### 创建步骤 / Creation Steps

1. **确定主题** - 识别需要新 Skill 的主题 / Identify the topic for the new Skill
2. **设计结构** - 按照 Skills 设计原则设计 Skill 结构 / Design Skill structure following design principles
3. **编写内容** - 编写 SKILL.md 文件 / Write the SKILL.md file
4. **测试验证** - 测试 Skill 是否正常工作 / Test if the Skill works correctly
5. **更新索引** - 在此 README 中添加新 Skill / Add new Skill to this README

#### 模板 / Template

```markdown
# [Skill Name]

## 概述 / Overview
简要说明这个 Skill 的作用和目的。

## 适用场景 / Use Cases
明确说明何时应该使用这个 Skill。

## 核心规则 / Core Rules
列出这个 Skill 的核心规则和规范。

## 详细说明 / Details
详细的规则说明、示例和注意事项。

## 与其他 Skills 的关系 / Relationship with Other Skills
说明这个 Skill 如何与其他 Skills 配合使用。
```

---

## 目录结构 / Directory Structure

```
.claude/skills/
├── README.md                    # 本文件 - Skills 索引
│
├── para-methodology/            # PARA 方法论
│   └── SKILL.md
│
├── obsidian-syntax/            # Obsidian 语法
│   └── SKILL.md
│
├── repo-context/               # 仓库上下文
│   └── SKILL.md
│
├── markdown-standards/         # Markdown 标准
│   └── SKILL.md
│
├── claude-commands/           # Claude 指令
│   └── SKILL.md
│
├── zettelkasten-workflow/      # Zettelkasten 工作流
│   └── SKILL.md
│
├── obsidian-markdown/         # 内置 Obsidian Markdown Skill
│   └── SKILL.md
│
├── obsidian-bases/            # 内置 Obsidian Bases Skill
│   └── SKILL.md
│
└── json-canvas/              # 内置 JSON Canvas Skill
    └── SKILL.md
```

---

## 常见问题 / FAQ

### Q1: 如何知道哪个 Skill 被加载了？

**A**: Claude 会在对话中显示加载了哪些 Skills。你也可以查看 Skill 的触发条件，了解何时会被加载。

Claude will display which Skills are loaded in the conversation. You can also check the Skill's trigger conditions to understand when it will be loaded.

### Q2: 可以同时加载多个 Skills 吗？

**A**: 可以。Claude 会根据任务类型智能加载所有相关的 Skills，并协同应用它们的规则。

Yes. Claude will intelligently load all relevant Skills based on the task type and apply their rules in coordination.

### Q3: 如何创建自定义 Skill？

**A**: 参考上面的"创建新 Skills"部分，或者查看最佳实践文档：

Refer to the "Creating New Skills" section above, or check the best practices documentation:

- [[0 Personals/📥 00_InBox/Claude Skills 文档/skills-best-practices/theme.md|Skills 最佳实践指南]]

### Q4: Skills 会影响性能吗？

**A**: 不会。Skills 采用按需加载机制，只加载必要的内容，反而会提升性能（节省 Token，加快响应）。

No. Skills use on-demand loading, only loading necessary content, which actually improves performance (saves tokens, speeds up response).

### Q5: 如何报告 Skill 的问题？

**A**: 可以通过以下方式报告：

You can report issues through:

1. 查看 Skill 文件中的说明 / Check instructions in the Skill file
2. 在项目中提 issue / Open an issue in the project
3. 联系维护者 / Contact the maintainer

---

## 相关资源 / Related Resources

### 项目文档 / Project Documentation

- [[CLAUDE.md|项目 CLAUDE.md]] - 核心规则概览 / Core rules overview
- [[0 Personals/📥 00_InBox/Claude Skills 文档/skills-introduction/theme.md|Skills 简介]] - Claude Skills 基本概念 / Basic concepts of Claude Skills
- [[0 Personals/📥 00_InBox/Claude Skills 文档/skills-best-practices/theme.md|最佳实践指南]] - 使用和维护指南 / Usage and maintenance guide

### 官方资源 / Official Resources

- [Claude Skills 官方文档](https://code.claude.com/docs/en/skills) - Claude Skills official documentation
- [Claude Code 文档](https://code.claude.com/docs) - Claude Code documentation

### 社区资源 / Community Resources

- [Claude Code GitHub](https://github.com/anthropics/claude-code) - Claude Code GitHub repository
- [示例项目](https://github.com/search?q=claude+skills) - Example projects

---

## 版本历史 / Version History

| 版本 / Version | 日期 / Date | 更新内容 / Changes |
|--------------|-------------|------------------|
| v1.0.0 | 2024-01-22 | 初始版本 / Initial version - 创建 6 个核心 Skills / Created 6 core Skills |

---

## 贡献指南 / Contributing

如果你发现 Skills 有问题或有改进建议，欢迎贡献：

If you find issues with Skills or have improvement suggestions, contributions are welcome:

1. **报告问题 / Report Issue**：创建 issue 描述问题 / Create an issue to describe the problem
2. **提交改进 / Submit Improvement**：创建 Pull Request / Create a Pull Request
3. **提供反馈 / Provide Feedback**：通过 issue 或 discussion 提供反馈 / Provide feedback via issues or discussions

---

## 许可证 / License

本 Skills 目录遵循项目许可证。

This Skills directory follows the project license.

- **项目许可证 / Project License**: Apache 2.0
- **Skills 许可证 / Skills License**: Apache 2.0

---

## 联系方式 / Contact

如有问题或建议，请联系：

For questions or suggestions, please contact:

- **项目维护者 / Project Maintainer**: [联系信息待补充 / Contact info to be added]
- **GitHub Issues**: [项目 Issues / Project Issues](https://github.com/kmjade/AI-value/issues)

---

> [!tip] 提示 / Tip
>
> 使用 `/obsidian` 命令可以自动选择合适的 Obsidian Skill！
>
> Use the `/obsidian` command to automatically select the appropriate Obsidian Skill!

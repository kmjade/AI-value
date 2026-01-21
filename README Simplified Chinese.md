# AI-value
---
# PARA 方法论  
---

## 简体中文

### 概述

PARA 是由 [Tiago Forte](https://fortelabs.co/) 提出的生产力方法论，用于组织个人知识和任务。

### 四个分类

| 分类 | 描述 | 示例 |
|------|------|------|
| **Projects（项目）** | 有明确目标和截止日期的短期努力 | "发布新网站"、"完成报税" |
| **Areas（领域）** | 没有截止日期的长期责任 | "健康"、"财务"、"职业发展" |
| **Resources（资源）** | 持续感兴趣的话题 | "生产力技巧"、"烹饪食谱"、"市场调研" |
| **Archives（归档）** | 已完成或不再活跃的项目 | 旧项目、过时的资源 |

### 使用方法

1. **Projects**：为每个项目创建新的 markdown 文件，使用 `_template.md` 作为模板
2. **Areas**：添加需要持续维护的责任领域
3. **Resources**：存储你感兴趣或正在研究的话题信息
4. **Archives**：完成后将项目或不活跃的项目移至此处

### 建议

- 每周回顾 Projects
- 每月回顾 Areas
- 定期归档以保持系统整洁
- 保持文件名描述清晰且简洁

---

## 文件夹结构

```
AI-value/
├── 0 Personals/
│   └── 📥 00_InBox/    - 收件箱，用于快速捕捉想法
├── 1 Projects/         - 有截止日期的活跃项目
├── 2 Areas/            - 持续的职责领域
├── 3 Resources/        - 感兴趣的话题和参考资料
├── 4 Archives/         - 已完成/不活跃的项目
├── 5 Zettels/         - 原子笔记（Zettelkasten 系统）
├── _Template/          - 新笔记的模板
├── _meta/             - 系统元数据和配置
├── _Cache/            - PARA 库缓存
└── .obsidian/         - Obsidian 插件设置
```

### 扩展结构

- **InBox** (`0 Personals/📥 00_InBox/`)：临时收集区，用于在组织到 PARA 类别之前快速捕捉想法、笔记和参考资料
- **Zettels** (`5 Zettels/`)：原子笔记系统，使用 Zettelkasten 方法论创建知识网络

---

## 工作流程

### 1. 捕捉
- 将新信息添加到 `0 Personals/📥 00_InBox/` 进行快速捕捉
- 在捕捉阶段不必担心组织结构

### 2. 处理
- 定期回顾 InBox 项目
- 将每个项目归类到 PARA 四个类别之一：
  - 是**项目**吗？ → `1 Projects/`
  - 是**领域**责任吗？ → `2 Areas/`
  - 是**资源**或参考资料吗？ → `3 Resources/`
  - 已完成或不活跃吗？ → `4 Archives/`

### 3. 组织
- 创建描述性的文件名
- 使用正确的文件夹结构
- 添加相关的标签和元数据

### 4. 连接
- 使用 wikilinks `[[笔记名称]]` 连接相关笔记
- 在 `5 Zettels/` 中创建原子笔记以构建知识网络
- 根据需要将 Zettels 链接到 PARA 类别

### 5. 回顾
- **每周**：回顾活跃的 Projects
- **每月**：回顾 Areas
- **每季度**：清理和归档

---

## Obsidian 集成

此知识库针对 Obsidian 进行了优化，具有以下功能：

### Frontmatter 属性

为您的笔记添加元数据：

```yaml
---
title: 我的笔记
date: 2024-01-15
tags:
  - project
  - important
status: in-progress
priority: high
---
```

### Wikilinks

- `[[笔记名称]]` - 链接到另一个笔记
- `[[笔记名称|显示文本]]` - 使用自定义显示文本的链接
- `[[笔记名称#标题]]` - 链接到特定标题
- `![[嵌入笔记]]` - 嵌入笔记内容

### Callouts

使用 callouts 强调内容：

```markdown
> [!note] 笔记
> 重要信息

> [!tip] 提示
> 有用的建议

> [!warning] 警告
> 需要谨慎
```

### 标签

使用标签进行分类：
- `#project` - 项目相关笔记
- `#area` - 领域相关笔记
- `#resource` - 资源相关笔记
- `#archive` - 归档项目

---

## Zettelkasten 系统

### 什么是 Zettelkasten？

Zettelkasten（德语意为"卡片盒"）是一种笔记和个人知识管理方法。它强调创建原子、自包含且高度互连的笔记。

### 创建原子笔记

1. 保持笔记专注于单一想法
2. 使笔记自包含（不假设上下文）
3. 使用唯一 ID 进行引用
4. 使用 wikilinks 链接相关概念

### 示例

```markdown
# 2024-01-15 - 原子笔记

Zettelkasten 方法强调创建专注于单一想法的原子笔记。

相关：
- [[2024-01-16 - 链接笔记]]
- [[3 Resources/Productivity]]
```

---

## PARA 指令

使用 Claude Code 指令管理您的 PARA 库：

| 指令 | 用途 |
|------|------|
| `/para-库概览` | 显示 PARA 库概览和统计信息 |
| `/para-整理收集` | 根据 PARA 原则整理 InBox 内容 |

---

## 最佳实践

1. **从简单开始**：不要过度复杂化。从基本的捕捉和组织开始。
2. **一致的命名**：使用描述性、一致的文件名。
3. **定期回顾**：安排定期回顾 PARA 系统。
4. **链接一切**：使用 wikilinks 在笔记之间创建连接。
5. **保持活跃**：仅在真正不活跃时才将项目移至 Archives。
6. **使用模板**：从 `_template.md` 开始以保持一致的格式。
7. **明智标记**：明智地使用标签以便于检索。

---

## 许可证

本项目采用 Apache 2.0 许可证。

---

## 致谢

- [PARA 方法](https://fortelabs.co/) 由 Tiago Forte 创建
- [Obsidian](https://obsidian.md/) - 知识库应用程序
- [Zettelkasten](https://zettelkasten.de/) - 笔记方法论



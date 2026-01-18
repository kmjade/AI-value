---
aliases:
  - 模板
  - Templates
tags:
  - template
---

> [!info] AI-value 模板文件夹
> 这里存放各种笔记模板，用于快速创建结构化的笔记。

## 模板分类

### PARA 模板 (`para/`)

| 文件 | 说明 |
|------|------|
| `_template-project.md` | 项目笔记模板 |
| `_template-areas.md` | 领域笔记模板 |
| `_template-resource.md` | 资源笔记模板 |
| `_template-archive.md` | 归档笔记模板 |

### 如何使用模板

1. **使用 Templater 插件**（推荐）
   - 按 `Ctrl/Cmd + P` 打开命令面板
   - 搜索 "Templater: Insert Template"
   - 选择模板文件

2. **手动复制**
   - 打开对应的模板文件
   - 复制内容到新笔记
   - 修改元数据字段

## 模板设计原则

- **一致性** - 所有模板使用统一的元数据结构
- **灵活性** - 预留扩展字段以适应不同需求
- **可读性** - 清晰的标题层级和分隔
- **可维护性** - 简单的结构便于更新

## 自定义模板

如需添加自定义模板：
1. 在对应文件夹创建新模板文件
2. 使用 `_template-` 前缀标识
3. 在此文件中添加说明

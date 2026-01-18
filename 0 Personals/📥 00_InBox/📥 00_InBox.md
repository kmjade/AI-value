---
aliases:
  - 收件箱
  - Inbox
tags:
  - inbox
---

> [!note] InBox / 收件箱
> 临时收集的想法、笔记、资源等，待整理后归入 PARA 分类。

## 快速操作 / Quick Actions

### 增强功能

```dataview
TABLE WITHOUT ID
  file.link as "功能",
  description as "说明",
  file_path as "文件"
FROM ""
WHERE contains(tags, "quick-action")
SORT file.mtime DESC
```

| 功能 | 文件 | 说明 |
|------|------|---------|
| 工作流管理 | `1-工作流.md` | PARA 自动化工作流 |
| 搜索功能 | `1-搜索功能.md` | 全局搜索和筛选 |

## 整理流程

| 子文件夹 | 说明 |
|----------|------|
| 0-待办/ | 待办事项，短期任务 |
| 1-链接/ | 保存的链接，待后续处理 |
| 2-素材/ | 图片、视频、音频等素材 |
| 根文件夹 | InBox 根内容，建议移动到对应 PARA 文件夹 |

### 整理步骤

1. 定期检查 InBox 内容
2. 根据内容性质移动到对应 PARA 分类：
   - 有明确目标和截止日期 → `1 Projects/`
   - 长期责任领域 → `2 Areas/`
   - 持续感兴趣的话题 → `3 Resources/`
   - 完成或不再活跃 → `4 Archives/`
3. 列出整理建议清单，等待用户确认
4. 用户确认后执行移动

## 当前待处理

```dataview
TABLE WITHOUT ID file.link, file.mtime as "Modified"
FROM "0 Personals/📥 00_InBox"
WHERE file.name != this.file.name
SORT file.mtime DESC
```

> [!info] 使用 `/para-整理收集` 命令
> 此命令会自动分析 InBox 内容并建议 PARA 分类，快速完成整理工作。

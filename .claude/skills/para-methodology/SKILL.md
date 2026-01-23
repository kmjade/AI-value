# PARA Methodology Skill

## Overview / 概览 / 概覽

This skill provides comprehensive knowledge about the PARA (Projects, Areas, Resources, Archives) methodology implemented in the AI-value knowledge management system.

本技能提供关于在 AI-value 知识管理系统中实施的 PARA（项目、领域、资源、归档）方法论的全面知识。

本技能提供關於在 AI-value 知識管理系統中實施的 PARA（Projects, Areas, Resources, Archives）方法論的全面知識。

## Quick Reference

- **PARA Structure**: `0 Personals` → `1 Projects` → `2 Areas` → `3 Resources` → `4 Archives` → `5 Zettels`
- **Key Commands**: `/para-库概览`, `/para-整理收集`, `/para-刷新缓存`

---

## PARA Methodology / PARA 方法论 / PARA 方法論

### Core Principles

The PARA methodology organizes information by **actionability** and **time horizon**:

PARA 方法论根据 **可执行性** 和 **时间跨度** 组织信息：

PARA 方法論根據 **可執行性** 和 **時間跨度** 組織資訊：

#### Projects (`1 Projects/`) / 项目 / 專案
- **Definition**: Short-term endeavors with deadlines / 有明确期限的短期努力 / 有明確期限的短期努力
- **Characteristics**: Active, actionable, time-bound / 活跃、可执行、有时间限制 / 活躍、可執行、有時間限制
- **Examples**: Writing a book, Launching a product, Organizing an event / 撰写书籍、发布产品、组织活动 / 撰寫書籍、發布產品、組織活動

#### Areas (`2 Areas/`) / 领域 / 領域
- **Definition**: Long-term responsibilities without deadlines / 没有期限的长期责任 / 沒有期限的長期責任
- **Characteristics**: Ongoing, requires maintenance, indefinite / 持续进行、需要维护、无期限 / 持續進行、需要維護、無期限
- **Examples**: Health, Finance, Relationships, Professional development / 健康、财务、人际关系、职业发展 / 健康、財務、人際關係、職業發展

#### Resources (`3 Resources/`) / 资源 / 資源
- **Definition**: Topics of ongoing interest / 持续感兴趣的主题 / 持續感興趣的主題
- **Characteristics**: Reference material, inspirational, educational / 参考材料、启发性、教育性 / 參考材料、啟發性、教育性
- **Examples**: Recipes, Language learning, Research articles / 食谱、语言学习、研究文章 / 食譜、語言學習、研究文章

#### Archives (`4 Archives/`) / 归档 / 歸檔
- **Definition**: Completed or inactive items / 已完成或非活跃的项目 / 已完成或非活躍的項目
- **Characteristics**: Done, on hold, no longer needed / 已完成、暂停、不再需要 / 已完成、暫停、不再需要
- **Purpose**: Keep completed work accessible but out of the way / 保持已完成工作可访问但不碍事 / 保持已完成工作可訪問但不礙事

### Extended Structure

#### InBox (`0 Personals/📥 00_InBox/`) / 收件箱 / 收件箱
- **Purpose**: Temporary collection for quick capture / 临时收集，快速捕获 / 臨時收集，快速捕獲
- **Usage**: Capture first, organize later / 先收集，后整理 / 先收集，後整理
- **Workflow**: Capture → Process → Organize / 收集 → 处理 → 整理 / 收集 → 處理 → 整理

#### Zettels (`5 Zettels/`) / 原子化笔记 / 原子化筆記
- **Purpose**: Atomic notes system for knowledge networking / 知识网络的原子化笔记系统 / 知識網絡的原子化筆記系統
- **Subcategories**:
  - `💡 fleeting/` - Quick capture thoughts and ideas / 闪念笔记，快速捕获 / 閃念筆記，快速捕獲
  - `📌 permanent/` - Permanent knowledge atoms / 永久知识原子 / 永久知識原子
  - `📚 literature/` - Literature and research notes / 文献和研究笔记 / 文獻和研究筆記
  - `📁 structure/` - System and workflow notes / 系统和流程笔记 / 系統和流程筆記

---

## PARA Workflow / PARA 工作流 / PARA 工作流

### Standard Workflow / 标准工作流 / 標準工作流

1. **Capture / 收集 / 收集**:
   - Add new information to `0 Personals/📥 00_InBox/`
   - Don't organize yet, just capture / 暂时不整理，只收集 / 暫時不整理，只收集
   - Use quick capture whenever inspiration strikes / 灵感来袭时快速捕获 / 靈感來襲時快速捕獲

2. **Organize / 整理 / 整理**:
   - Use `/para-整理收集` to process InBox contents / 使用 `/para-整理收集` 处理收件箱内容 / 使用 `/para-整理收集` 處理收件箱內容
   - Decide: Action (Project) → Maintain (Area) → Reference (Resource) → Archive / 决定：行动（项目）→ 维护（领域）→ 参考（资源）→ 归档 / 決定：行動（專案）→ 維護（領域）→ 參考（資源）→ 歸檔

3. **Review / 复盘 / 復盤**:
   - Use `/para-库概览` to review library status and statistics / 使用 `/para-库概览` 审查库状态和统计 / 使用 `/para-庫概覽` 審查庫狀態和統計
   - Check: What's active? What's stalled? What's complete? / 检查：什么在活跃？什么停滞？什么完成？/ 檢查：什麼在活躍？什麼停滯？什麼完成？

4. **Archive / 归档 / 歸檔**:
   - Move completed items to `4 Archives/` / 将已完成项目移至 `4 Archives/` / 將已完成專案移至 `4 Archives/`
   - Keep active workspace clean and focused / 保持活跃工作区整洁专注 / 保持活躍工作區整潔專注

### Metadata Standards / 元数据标准 / 元數據標準

When working with PARA items, use these metadata properties:

处理 PARA 项目时，使用以下元数据属性：

處理 PARA 專案時，使用以下元數據屬性：

| Category | para value | Use Case / 使用场景 / 使用場景 |
|----------|-----------|--------------------------------|
| Projects | `projects` | Active projects with deadlines / 有期限的活跃项目 / 有期限的活躍專案 |
| Areas | `areas` | Ongoing responsibilities / 持续责任 / 持續責任 |
| Resources | `resources` | Reference materials / 参考材料 / 參考材料 |
| Archives | `archives` | Completed items / 已完成项目 / 已完成專案 |

Example frontmatter:
```yaml
---
title: My Note
date: 2024-01-15
tags:
  - project
  - important
status: in-progress
priority: high
para: projects
---
```

---

## PARA Management Commands / PARA 管理指令 / PARA 管理指令

Commands are located in `.claude/commands/` and invoked with `/command-name`.

指令位于 `.claude/commands/` 中，使用 `/command-name` 调用。

指令位於 `.claude/commands/` 中，使用 `/command-name` 調用。

| Command | File | Purpose | 用途 |
|---------|------|---------|------|
| `/para-库概览` | `para-库概览.md` | Display PARA library overview and statistics / 显示库概览和统计 | 顯示庫概覽和統計 |
| `/para-整理收集` | `para-整理收集.md` | Organize InBox contents by PARA principles / 按 PARA 原则整理收件箱 | 按 PARA 原則整理收件箱 |
| `/para-刷新缓存` | `para-刷新缓存.md` | Update PARA cache files for performance / 更新缓存以提升性能 | 更新緩存以提升性能 |
| `/search` | `search.md` | Search InBox and PARA contents / 搜索 InBox 和 PARA 内容 | 搜索 InBox 和 PARA 內容 |

### Usage Examples / 使用示例 / 使用範例

#### Overview Command / 概览命令 / 概覽命令

```bash
/para-库概览
```

Output:
```
📊 PARA 库概览

| 文件夹 | 文件数 | 状态 |
|--------|--------|------|
| 0 Personals/📥 00_InBox | 15 | ⚠️ 需要整理 |
| 1 Projects | 8 | |
| 2 Areas | 12 | |
| 3 Resources | 45 | |
| 4 Archives | 120 | |
| 5 Zettels | 200+ | |

📁 进行中的项目 (1 Projects)：
- 公众号
- AI日报
- 读书笔记
```

#### Organize Command / 整理命令 / 整理命令

```bash
/para-整理收集
```

Output:
```
📥 整理收件箱

发现 15 个待处理笔记：

1. "学习笔记.md"
   - 建议: 🗂️ Resource → [[AI/机器学习]]
   - 动作: [归档] [跳过] [编辑]

2. "待办清单.md"
   - 建议: 📋 Project → [[本月任务]]
   - 动作: [归档] [跳过] [编辑]

3. "健康检查记录.md"
   - 建议: 🔄 Area → [[健康]]
   - 动作: [归档] [跳过] [编辑]
```

---

## Best Practices / 最佳实践 / 最佳實踐

### 1. Actionability Test / 可执行性测试 / 可執行性測試

When organizing InBox, ask: **Is there a next action?**

整理收件箱时，问：**有下一步行动吗？**

整理收件箱時，問：**有下一步行動嗎？**

- **Yes** → It's a **Project** / 是 → **项目** / 是 → **專案**
- **No, but I need to maintain it** → It's an **Area** / 不，但需要维护 → **领域** / 不，但需要維護 → **領域**
- **No, it's just for reference** → It's a **Resource** / 不，只是参考 → **资源** / 不，只是參考 → **資源**
- **No, it's done** → It goes to **Archives** / 不，已完成 → **归档** / 不，已完成 → **歸檔**

### 2. Regular Review Cycles / 定期审查周期 / 定期審查週期

- **Daily**: Check InBox (`/para-库概览`) / 每日：检查收件箱 / 每日：檢查收件箱
- **Weekly**: Review Projects status / 每周：审查项目状态 / 每週：審查專案狀態
- **Monthly**: Deep clean Archives / 每月：深度清理归档 / 每月：深度清理歸檔
- **Quarterly**: Reassess Areas / 每季度：重新评估领域 / 每季：重新評估領域

### 3. Maintain Flow / 保持流动性 / 保持流動性

- Don't let Projects pile up in Archives / 不要让项目堆积在归档中 / 不要讓專案堆積在歸檔中
- Keep InBox empty or small / 保持收件箱清空或小巧 / 保持收件箱清空或小巧
- Archive Projects only when truly complete / 只在真正完成时归档项目 / 只在真正完成時歸檔專案
- Reactivate Archives when relevant / 在相关时重新激活归档 / 在相關時重新啟動歸檔

---

## File Path Rules / 文件路径规则 / 文件路徑規則

When working with PARA folders, always use **relative paths** from the vault root:

使用 PARA 文件夹时，始终使用从 vault root 开始的 **相对路径**：

使用 PARA 資料夾時，始終使用從 vault root 開始的 **相對路徑**：

- ✓ Correct: `1 Projects/my-project.md` / 正确 / 正確
- ✓ Correct: `2 Areas/health/diet.md` / 正确 / 正確
- ✗ WRONG: `/1 Projects/my-project.md` / 错误 / 錯誤
- ✗ WRONG: `D:\Knowledge\AI-value\1 Projects/my-project.md` / 错误 / 錯誤

---

## Common Patterns / 常见模式 / 常見模式

### Project Structure / 项目结构 / 專案結構

```
1 Projects/Project Name/
├── 📋 Main Note.md          # Project overview
├── 📝 Tasks.md              # Actionable items
├── 📊 Progress.md           # Status tracking
└── 🔗 Resources.md          # Links to relevant resources
```

### Area Maintenance / 领域维护 / 領域維護

```
2 Areas/Health/
├── 🏃 Fitness.md
├── 🥗 Nutrition.md
├── 😴 Sleep.md
└── 📊 Health Metrics.md
```

### Resource Collection / 资源收集 / 資源收集

```
3 Resources/AI/
├── 📚 Tutorials/
├── 🔬 Research Papers/
├── 🛠️ Tools/
└── 📖 Documentation/
```

---

## Related Skills / 相关技能 / 相關技能

- **zettelkasten-workflow**: For atomic notes and knowledge networking / 原子化笔记和知识网络 / 原子化筆記和知識網絡
- **markdown-standards**: For file naming and multilingual support / 文件命名和多语言支持 / 文件命名和多語言支持
- **obsidian-syntax**: For proper Obsidian markdown formatting / 正确的 Obsidian markdown 格式 / 正確的 Obsidian markdown 格式

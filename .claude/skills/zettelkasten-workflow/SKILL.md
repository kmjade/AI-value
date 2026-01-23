# Zettelkasten Workflow Skill

## Overview / 概览 / 概覽

This skill provides comprehensive guidance on implementing the Zettelkasten (card box) note-taking system within the AI-value knowledge management repository.

本技能提供关于在 AI-value 知识管理仓库中实施 Zettelkasten（卡片盒）笔记系统的全面指导。

本技能提供關於在 AI-value 知識管理倉庫中實施 Zettelkasten（卡片盒）筆記系統的全面指導。

---

## Quick Reference

- **Location**: `5 Zettels/`
- **Core Principle**: Atomic, interconnected notes with unique IDs / 原子化、互联的笔记，带唯一 ID / 原子化、互聯的筆記，帶唯一 ID
- **Flow**: fleeting → permanent → literature / 闪念 → 永久 → 文献 / 閃念 → 永久 → 文獻
- **Key Features**: Atomic notes, unique IDs, bidirectional linking / 原子化笔记、唯一 ID、双向链接 / 原子化筆記、唯一 ID、雙向連結

---

## What is Zettelkasten? / 什么是 Zettelkasten？/ 什麼是 Zettelkasten？

### English

**Zettelkasten** (German for "slip box") is a method of note-taking and personal knowledge management that emphasizes atomic, interconnected notes with unique identifiers. Developed by sociologist Niklas Luhmann, it creates a network of ideas rather than a hierarchical structure.

### 简体中文

**Zettelkasten**（德语"卡片盒"）是一种笔记和个人知识管理方法，强调原子化、互联的笔记和唯一标识符。由社会学家 Niklas Luhmann 开发，它创建的是思想网络而不是层次结构。

### 繁體中文

**Zettelkasten**（德語"卡片盒"）是一種筆記和個人知識管理方法，強調原子化、互聯的筆記和唯一標識符。由社會學家 Niklas Luhmann 開發，它創建的是思想網絡而不是層次結構。

### Key Principles / 核心原则 / 核心原則

| Principle | Description | 描述 | 描述 |
|-----------|-------------|------|------|
| **Atomicity** | One idea per note / 每个笔记一个想法 / 每個筆記一個想法 | |
| **Connectivity** | Link related notes / 链接相关笔记 / 連結相關筆記 | |
| **Unique IDs** | Each note has a unique identifier / 每个笔记都有唯一标识符 / 每個筆記都有唯一標識符 | |
| **Self-contained** | Each note can stand alone / 每个笔记都可以独立存在 / 每個筆記都可以獨立存在 | |
| **Evolutionary** | Ideas grow and develop over time / 思想随时间发展和演变 / 思想隨時間發展和演變 | |

---

## Zettelkasten Structure / Zettelkasten 结构 / Zettelkasten 結構

### Folder Organization / 文件夹组织 / 資料夾組織

```
5 Zettels/
├── 💡 fleeting/              # Fleeting notes / 闪念笔记 / 閃念筆記
│   ├── Quick thoughts.md
│   └── Random ideas.md
├── 📌 permanent/             # Permanent notes / 永久笔记 / 永久筆記
│   ├── 202401150001 - Core concept.md
│   └── 202401150002 - Important principle.md
├── 📚 literature/            # Literature notes / 文献笔记 / 文獻筆記
│   └── 202401150003 - Paper summary.md
└── 📁 structure/             # Structure notes / 结构笔记 / 結構筆記
    └── 202401150004 - Workflow overview.md
```

### Subcategories Explained / 子类别说明 / 子類別說明

#### 💡 Fleeting Notes / 闪念笔记 / 閃念筆記

**Purpose**: Capture quick thoughts and ideas without worrying about structure / 捕获快速想法和灵感，无需担心结构 / 捕獲快速想法和靈感，無需擔心結構

**Characteristics / 特点 / 特點:**
- Quick and informal / 快速和非正式 / 快速和非正式
- Temporary / 临时 / 臨時
- No strict format / 无严格格式 / 無嚴格格式
- Designed to be processed / 旨在被处理 / 旨在被處理

**When to use / 何时使用 / 何時使用:**
- Random thoughts / 随机想法 / 隨機想法
- Quick ideas / 快速想法 / 快速想法
- Meeting notes to process / 待处理的会议笔记 / 待處理的會議筆記
- Inspirations / 灵感 / 靈感

**Example / 示例 / 範例:**

```markdown
---
title: Fleeting Idea
date: 2024-01-15
type: fleeting
---

💡 Quick thought: Maybe use AI to help organize my Zettelkasten notes automatically?
```

---

#### 📌 Permanent Notes / 永久笔记 / 永久筆記

**Purpose**: Atomic, self-contained knowledge atoms / 原子化、自包含的知识原子 / 原子化、自包含的知識原子

**Characteristics / 特点 / 特點:**
- One idea per note / 每个笔记一个想法 / 每個筆記一個想法
- Self-contained / 自包含 / 自包含
- Unique ID format: `YYYYMMDD-XXXX` / 唯一 ID 格式：`YYYYMMDD-XXXX` / 唯一 ID 格式：`YYYYMMDD-XXXX`
- Richly linked to other notes / 与其他笔记丰富链接 / 與其他筆記豐富連結

**When to use / 何时使用 / 何時使用:**
- Core concepts / 核心概念 / 核心概念
- Important principles / 重要原则 / 重要原則
- Key insights / 关键洞察 / 關鍵洞察
- Synthesized knowledge / 综合知识 / 綜合知識

**Example / 示例 / 範例:**

```markdown
---
title: 202401150001 - Atomic Note Principle
id: 202401150001
date: 2024-01-15
tags: [zettelkasten, note-taking, atomicity]
type: permanent
---

# Atomic Note Principle

Each note in a Zettelkasten should contain only one idea, making it easy to reference and connect.

> [!info] Definition
> An atomic note is a self-contained unit that expresses a single concept or idea.

## Key Points / 关键点 / 關鍵點

- One idea per note / 每个笔记一个想法 / 每個筆記一個想法
- Self-contained / 自包含 / 自包含
- Can be understood independently / 可以独立理解 / 可以獨立理解
- Easy to link / 易于链接 / 易於連結

## Related Notes / 相关笔记 / 相關筆記

- [[202401150002 - Note Connectivity]]
- [[202401150003 - Unique Identifiers]]
```

---

#### 📚 Literature Notes / 文献笔记 / 文獻筆記

**Purpose**: Summaries and insights from external sources / 外部资源的摘要和洞察 / 外部資源的摘要和洞察

**Characteristics / 特点 / 特點:**
- Source attribution / 来源归因 / 來源歸因
- Key insights only / 仅关键洞察 / 僅關鍵洞察
- Personal interpretation / 个人解读 / 個人解讀
- Linked to permanent notes / 链接到永久笔记 / 連結到永久筆記

**When to use / 何时使用 / 何時使用:**
- Book summaries / 书籍摘要 / 書籍摘要
- Research paper notes / 研究论文笔记 / 研究論文筆記
- Article highlights / 文章亮点 / 文章亮點
- Video notes / 视频笔记 / 影片筆記

**Example / 示例 / 範例:**

```markdown
---
title: 202401150003 - How to Take Smart Notes Summary
id: 202401150003
date: 2024-01-15
tags: [zettelkasten, book-summary, sonke-ahrens]
type: literature
source:
  title: How to Take Smart Notes
  author: Sönke Ahrens
  year: 2017
  url: https://example.com
---

# Book Summary: How to Take Smart Notes / 书籍摘要 / 書籍摘要

**Author**: Sönke Ahrens
**Year**: 2017

## Key Insights / 关键洞察 / 關鍵洞察

### 1. The Zettelkasten Method / Zettelkasten 方法 / Zettelkasten 方法
> [!quote] From the book
> "The slip-box is the shipping container of the academic world."

### 2. Externalize Thinking / 外化思维 / 外化思維
Writing is not just for communicating; it's for thinking.

> [!tip] Key concept / 关键概念 / 關鍵概念
> Externalizing thoughts by writing them down makes thinking easier.

## Personal Takeaways / 个人收获 / 個人收穫

- [[202401150001 - Atomic Note Principle]]
- [[202401150004 - Workflow Overview]]

## Next Steps / 下一步 / 下一步

- Implement permanent notes structure / 实施永久笔记结构 / 實施永久筆記結構
- Set up daily Zettelkasten routine / 建立日常 Zettelkasten 例程 / 建立日常 Zettelkasten 例程
```

---

#### 📁 Structure Notes / 结构笔记 / 結構筆記

**Purpose**: Overview notes that connect clusters of ideas / 连接想法集群的概览笔记 / 連結想法集群的概覽筆記

**Characteristics / 特点 / 特點:**
- Hub notes / 中心笔记 / 中心筆記
- Index or MOC (Map of Content) / 索引或目录 / 索引或目錄
- Entry points to topics / 主题入口点 / 主題入口點
- Evolving over time / 随时间演变 / 隨時間演變

**When to use / 何时使用 / 何時使用:**
- Topic overviews / 主题概览 / 主題概覽
- Workflow documentation / 工作流文档 / 工作流文件
- Project summaries / 项目摘要 / 專案摘要
- Concept clusters / 概念集群 / 概念集群

**Example / 示例 / 範例:**

```markdown
---
title: 202401150004 - Zettelkasten Workflow Overview
id: 202401150004
date: 2024-01-15
tags: [zettelkasten, workflow, overview]
type: structure
---

# Zettelkasten Workflow Overview / Zettelkasten 工作流概览 / Zettelkasten 工作流概覽

## Core Principles / 核心原则 / 核心原則

> [!info] Workflow Summary
> Capture fleeting notes → Process into permanent notes → Connect and develop

## Key Concepts / 关键概念 / 關鍵概念

### Note Types / 笔记类型 / 筆記類型
- [[202401150001 - Atomic Note Principle]]
- [[202401150002 - Note Connectivity]]

### Tools & Methods / 工具和方法 / 工具和方法
- [[Unique Identifiers]]
- [[Bidirectional Linking]]

## Related Topics / 相关主题 / 相關主題

- **Capture Process**: [[Note Taking Workflow]]
- **Organization**: [[Tag System]]
- **Review**: [[Daily Review Routine]]

## Resources / 资源 / 資源
- [[How to Take Smart Notes Summary]] (literature note)
```

---

## Zettelkasten Workflow / Zettelkasten 工作流 / Zettelkasten 工作流

### Standard Workflow / 标准工作流 / 標準工作流

```
💡 Capture          📌 Process            🔗 Connect        🔄 Review
  ↓                    ↓                    ↓                 ↓
Fleeting Notes  →  Permanent Notes  →  Link Related  →  Regular Review
   (Quick)              (Atomic)            (Network)         (Maintain)
```

#### Step 1: Capture / 捕获 / 捕獲

Capture ideas quickly in fleeting notes:

快速捕获想法到闪念笔记：

快速捕獲想法到閃念筆記：

```markdown
💡 Random thought: Use tags for better organization
```

**Best Practices / 最佳实践 / 最佳實踐:**
- Don't worry about structure / 不要担心结构 / 不要擔心結構
- Capture immediately / 立即捕获 / 立即捕獲
- Use simple format / 使用简单格式 / 使用簡單格式
- Don't edit yet / 暂不编辑 / 暫不編輯

---

#### Step 2: Process / 处理 / 處理

Convert fleeting notes to permanent notes:

将闪念笔记转换为永久笔记：

將閃念筆記轉換為永久筆記：

```markdown
---
title: 202401150005 - Tag-Based Organization
id: 202401150005
date: 2024-01-15
tags: [zettelkasten, organization, tagging]
type: permanent
---

# Tag-Based Organization

Tags provide a flexible way to categorize and discover notes in a Zettelkasten.

## Key Points / 关键点 / 關鍵點
- Tags are flexible / 标签是灵活的 / 標籤是靈活的
- Tags enable discovery / 标签支持发现 / 標籤支援發現
- Tags can be hierarchical / 标签可以是分层的 / 標籤可以是分層的
```

**Best Practices / 最佳实践 / 最佳實踐:**
- Extract core idea / 提取核心想法 / 提取核心想法
- Make it atomic / 使其原子化 / 使其原子化
- Add unique ID / 添加唯一 ID / 添加唯一 ID
- Write clearly / 清晰书写 / 清晰書寫

---

#### Step 3: Connect / 连接 / 連結

Link related notes:

链接相关笔记：

連結相關筆記：

```markdown
## Related Notes / 相关笔记 / 相關筆記

- [[202401150001 - Atomic Note Principle]] (context)
- [[202401150006 - Discovery Methods]] (elaboration)
- [[202401150007 - Tagging Best Practices]] (example)
```

**Best Practices / 最佳实践 / 最佳實踐:**
- Link to context / 链接到上下文 / 連結到上下文
- Link to elaborations / 链接到阐述 / 連結到闡述
- Link to examples / 链接到示例 / 連結到範例
- Link to counter-arguments / 链接到反驳论点 / 連結到反駁論點

---

#### Step 4: Review / 复查 / 復查

Regularly review and improve notes:

定期复查和改进笔记：

定期復查和改進筆記：

**Daily Review / 每日复查 / 每日復查:**
- Process fleeting notes / 处理闪念笔记 / 處理閃念筆記
- Create 1-2 permanent notes / 创建 1-2 个永久笔记 / 建立 1-2 個永久筆記

**Weekly Review / 每周复查 / 每周復查:**
- Review connection density / 审查连接密度 / 審查連結密度
- Update structure notes / 更新结构笔记 / 更新結構筆記
- Identify knowledge gaps / 识别知识缺口 / 識別知識缺口

**Monthly Review / 每月复查 / 每月復查:**
- Deep dive into a topic / 深入探讨一个主题 / 深入探討一個主題
- Create cluster notes / 创建集群笔记 / 建立集群筆記
- Archive outdated notes / 归档过时笔记 / 歸檔過時筆記

---

## Unique ID System / 唯一 ID 系统 / 唯一 ID 系統

### Format / 格式 / 格式

```
YYYYMMDD-XXXX
```

Where: / 其中 / 其中：
- `YYYY`: Year / 年 / 年
- `MM`: Month / 月 / 月
- `DD`: Day / 日 / 日
- `XXXX`: Sequential number (0001-9999) / 序号 / 序號

### Examples / 示例 / 範例

```
202401150001  # First note on January 15, 2024
202401150002  # Second note on January 15, 2024
202401160001  # First note on January 16, 2024
```

### Why Unique IDs? / 为什么需要唯一 ID？/ 為什麼需要唯一 ID？

| Benefit / 益处 / 益處 | Description / 描述 | 描述 |
|----------------------|-------------------|------|
| **Stable links** / 稳定链接 / 穩定連結 | Links never break even if titles change / 即使标题改变，链接也不会断 / 即使標題改變，連結也不會斷 |
| **Chronological** / 按时间顺序 / 按時間順序 | Easy to see development over time / 易于观察随时间的发展 / 易於觀察隨時間的發展 |
| **Referenceable** / 可引用 / 可引用 | Easy to cite specific notes / 易于引用特定笔记 / 易於引用特定筆記 |
| **Sortable** / 可排序 / 可排序 | Notes can be sorted by ID / 笔记可以按 ID 排序 / 筆記可以按 ID 排序 |

---

## Linking Strategies / 链接策略 / 連結策略

### Types of Links / 链接类型 / 連結類型

| Type / 类型 / 類型 | Syntax / 语法 / 語法 | Purpose / 用途 | 用途 |
|-------------------|-------------------|-----------------|------|
| **Wikilink** | `[[202401150001]]` | Link to note / 链接到笔记 / 連結到筆記 |
| **With display text** | `[[202401150001\|The Concept]]` | Custom link text / 自定义链接文本 / 自訂連結文字 |
| **Block reference** | `[[202401150001#^block-id]]` | Link to specific paragraph / 链接到特定段落 / 連結到特定段落 |
| **Embed** | `![[202401150001]]` | Embed full note / 嵌入完整笔记 / 嵌入完整筆記 |

### Link Categories / 链接分类 / 連結分類

#### Context Links / 上下文链接 / 上下文連結
Provide background or foundation information / 提供背景或基础信息 / 提供背景或基礎資訊

```markdown
Based on [[202401150001 - Atomic Note Principle]]
```

#### Elaboration Links / 阐述链接 / 闡述連結
Expand or elaborate on the idea / 扩展或阐述想法 / 擴展或闡述想法

```markdown
See [[202401150006 - Advanced Techniques]] for more details
```

#### Example Links / 示例链接 / 範例連結
Provide practical examples / 提供实际示例 / 提供實際範例

```markdown
Example: [[202401150007 - Tagging Example]]
```

#### Counter-argument Links / 反驳论点链接 / 反駁論點連結
Present alternative viewpoints / 呈现替代观点 / 呈現替代觀點

```markdown
Contrast with [[202401150008 - Alternative Approach]]
```

#### Similar/Related Links / 相似/相关链接 / 相似/相關連結
Connect similar concepts / 连接相似概念 / 連結相似概念

```markdown
Also see [[202401150009 - Similar Concept]]
```

---

## Best Practices / 最佳实践 / 最佳實踐

### 1. Atomicity / 原子化 / 原子化

**Do / 应该 / 應該:**
```markdown
# Good - One idea per note / 好的 - 每个笔记一个想法 / 好的 - 每個筆記一個想法
---
title: 202401150001 - Atomic Note Principle
---
Each note contains one idea.
```

**Don't / 不应该 / 不應該:**
```markdown
# Bad - Multiple ideas in one note / 坏的 - 一个笔记多个想法 / 壞的 - 一個筆記多個想法
---
title: Notes about Note Taking
---
1. Atomicity is important
2. Unique IDs help
3. Linking is crucial
4. Tags are useful
```

---

### 2. Self-contained / 自包含 / 自包含

**Do / 应该 / 應該:**
```markdown
# Good - Can be understood alone / 好的 - 可以独立理解 / 好的 - 可以獨立理解
---
title: 202401150010 - Bidirectional Linking
---

Bidirectional linking creates a two-way connection between notes.

## Key Points / 关键点 / 關鍵點
- Works in both directions / 双向工作 / 雙向工作
- Creates a network / 创建网络 / 創建網絡
- No single source of truth / 没有单一真实来源 / 沒有單一真實來源
```

**Don't / 不应该 / 不應該:**
```markdown
# Bad - Requires reading other notes / 坏的 - 需要阅读其他笔记 / 壞的 - 需要閱讀其他筆記
---
title: Linking (continued)
---

As mentioned in the previous note...
(Requires reading the previous note to understand)
```

---

### 3. Consistent Format / 一致格式 / 一致格式

```yaml
---
title: 202401150015 - Title
id: 202401150015
date: 2024-01-15
tags: [zettelkasten, category, topic]
type: permanent
---
```

---

### 4. Regular Processing / 定期处理 / 定期處理

- ✓ Process fleeting notes daily / 每日处理闪念笔记 / 每日處理閃念筆記
- ✓ Create 1-2 permanent notes daily / 每日创建 1-2 个永久笔记 / 每日建立 1-2 個永久筆記
- ✓ Link new notes to existing ones / 将新笔记链接到现有笔记 / 將新筆記連結到現有筆記
- ✗ Don't let fleeting notes pile up / 不要让闪念笔记堆积 / 不要讓閃念筆記堆積

---

## Common Patterns / 常见模式 / 常見模式

### Concept Development Note / 概念开发笔记 / 概念開發筆記

```markdown
---
title: 202401150020 - [Concept Name]
id: 202401150020
date: 2024-01-15
tags: [zettelkasten, [category]]
type: permanent
---

# [Concept Name]

Brief definition of the concept.

## Core Idea / 核心思想 / 核心思想
[Main idea in 1-2 sentences]

## Key Insights / 关键洞察 / 關鍵洞察
- [Insight 1]
- [Insight 2]
- [Insight 3]

## Examples / 示例 / 範例
- [Practical example]

## Related Notes / 相关笔记 / 相關筆記
- [[Context note]]
- [[Elaboration note]]
- [[Example note]]
```

### Question-Based Note / 基于问题的笔记 / 基於問題的筆記

```markdown
---
title: 202401150025 - Question: [Topic]?
id: 202401150025
date: 2024-01-15
tags: [zettelkasten, question, [topic]]
type: permanent
---

# Question: [Topic]?

## Question / 问题 / 問題
[Clear question about the topic]

## Initial Thoughts / 初步想法 / 初步想法
[Your current understanding]

## Research Needed / 需要的研究 / 需要的研究
- [ ] [Research point 1]
- [ ] [Research point 2]

## Related Questions / 相关问题 / 相關問題
- [[Related question note]]
```

### Argument Note / 论证笔记 / 論證筆記

```markdown
---
title: 202401150030 - Argument: [Claim]
id: 202401150030
date: 2024-01-15
tags: [zettelkasten, argument, [topic]]
type: permanent
---

# Argument: [Claim]

## Claim / 论点 / 論點
[Clear statement of the argument]

## Supporting Evidence / 支持证据 / 支持證據
- [Evidence 1]
- [Evidence 2]

## Counter-arguments / 反驳论点 / 反駁論點
- [[Counter-argument note]]

## Conclusion / 结论 / 結論
[Summary of the argument]

## Related Notes / 相关笔记 / 相關筆記
- [[Supporting note]]
- [[Contrasting note]]
```

---

## Integration with PARA / 与 PARA 集成 / 與 PARA 集成

### Relationship / 关系 / 關係

```
PARA (Organization)          Zettelkasten (Knowledge Network)
     ↓                                ↓
 Projects, Areas, Resources  ←→  Permanent Notes, Literature Notes
     ↓                                ↓
   Container                     Content network
```

### Workflow Integration / 工作流集成 / 工作流整合

```
1. Capture in InBox (PARA)
   ↓
2. Process to Project/Area/Resource (PARA)
   ↓
3. Extract atomic ideas → Create Zettels (Zettelkasten)
   ↓
4. Link Zettels back to PARA notes
   ↓
5. Use structure notes to organize Zettelkasten clusters
```

### When to Use Each / 何时使用哪个 / 何時使用哪個

| Use Case / 使用场景 / 使用場景 | Use PARA / 使用 PARA | Use Zettelkasten / 使用 Zettelkasten |
|-------------------------|-------------------|-------------------------------|
| Project tasks / 项目任务 / 專案任務 | ✓ Projects | ✗ |
| Long-term maintenance / 长期维护 / 長期維護 | ✓ Areas | ✗ |
| Reference materials / 参考材料 / 參考材料 | ✓ Resources | ✗ |
| Core ideas / 核心想法 / 核心想法 | ✗ | ✓ Permanent notes |
| Book summaries / 书籍摘要 / 書籍摘要 | Resources (link) | ✓ Literature notes |
| Concept connections / 概念连接 / 概念連結 | ✗ | ✓ Permanent notes + links |

---

## Related Skills / 相关技能 / 相關技能

- **para-methodology**: PARA structure and workflow / PARA 结构和工作流 / PARA 結構和工作流
- **obsidian-syntax**: Obsidian-specific syntax for linking / Obsidian 特定的链接语法 / Obsidian 特定的連結語法
- **markdown-standards**: File naming and conventions / 文件命名和规范 / 檔案命名和規範

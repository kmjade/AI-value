# AI-value

# PARA 方法论  

### 概述

PARA 是由 [Tiago Forte](https://fortelabs.co/) 提出的生產力方法論，用於組織個人知識和任務。

### 四個分類

| 分類                | 描述              | 示例                    |
| ----------------- | --------------- | --------------------- |
| **Projects（專案）**  | 有明確目標和截止日期的短期努力 | "發布新網站"、"完成報稅"        |
| **Areas（領域）**     | 沒有截止日期的長期責任     | "健康"、"財務"、"職業發展"      |
| **Resources（資源）** | 持續感興趣的話題        | "生產力技巧"、"烹飪食譜"、"市場調研" |
| **Archives（歸檔）**  | 已完成或不再活躍的專案     | 舊專案、過時的資源             |

### 使用方法

1. **Projects**：為每個專案創建新的 markdown 文件，使用 `_template.md` 作為模板
2. **Areas**：添加需要持續維護的責任領域
3. **Resources**：存儲你感興趣或正在研究的話題信息
4. **Archives**：完成後將專案或不活躍的專案移至此處

### 建議

- 每週回顧 Projects
- 每月回顧 Areas
- 定期歸檔以保持系統整潔
- 保持文件名描述清晰且簡潔

---

## 文件夾結構

```
AI-value/
├── 0 Personals/
│   └── 📥 00_InBox/    - 收件箱，用於快速捕捉想法
├── 1 Projects/         - 有截止日期的活躍專案
├── 2 Areas/            - 持續的職責領域
├── 3 Resources/        - 感興趣的話題和參考資料
├── 4 Archives/         - 已完成/不活躍的專案
├── 5 Zettels/         - 原子筆記（Zettelkasten 系統）
├── _Template/          - 新筆記的模板
├── _meta/             - 系統元數據和配置
├── _Cache/            - PARA 庫緩存
└── .obsidian/         - Obsidian 插件設置
```

### 擴展結構

- **InBox** (`0 Personals/📥 00_InBox/`)：臨時收集區，用於在組織到 PARA 類別之前快速捕捉想法、筆記和參考資料
- **Zettels** (`5 Zettels/`)：原子筆記系統，使用 Zettelkasten 方法論創建知識網絡

---

## 工作流程

### 1. 捕捉
- 將新信息添加到 `0 Personals/📥 00_InBox/` 進行快速捕捉
- 在捕捉階段不必擔心組織結構

### 2. 處理
- 定期回顧 InBox 項目
- 將每個項目歸類到 PARA 四個類別之一：
  - 是**專案**嗎？ → `1 Projects/`
  - 是**領域**責任嗎？ → `2 Areas/`
  - 是**資源**或參考資料嗎？ → `3 Resources/`
  - 已完成或不活躍嗎？ → `4 Archives/`

### 3. 組織
- 創建描述性的文件名
- 使用正確的文件夾結構
- 添加相關的標籤和元數據

### 4. 連接
- 使用 wikilinks `[[筆記名稱]]` 連接相關筆記
- 在 `5 Zettels/` 中創建原子筆記以構建知識網絡
- 根據需要將 Zettels 鏈接到 PARA 類別

### 5. 回顧
- **每週**：回顧活躍的 Projects
- **每月**：回顧 Areas
- **每季度**：清理和歸檔

---

## Obsidian 集成

此知識庫針對 Obsidian 進行了優化，具有以下功能：

### Frontmatter 屬性

為您的筆記添加元數據：

```yaml
---
title: 我的筆記
date: 2024-01-15
tags:
  - project
  - important
status: in-progress
priority: high
---
```

### Wikilinks

- `[[筆記名稱]]` - 鏈接到另一個筆記
- `[[筆記名稱|顯示文本]]` - 使用自定義顯示文本的鏈接
- `[[筆記名稱#標題]]` - 鏈接到特定標題
- `![[嵌入筆記]]` - 嵌入筆記內容

### Callouts

使用 callouts 強調內容：

```markdown
> [!note] 筆記
> 重要信息

> [!tip] 提示
> 有用的建議

> [!warning] 警告
> 需要謹慎
```

### 標籤

使用標籤進行分類：
- `#project` - 專案相關筆記
- `#area` - 領域相關筆記
- `#resource` - 資源相關筆記
- `#archive` - 歸檔項目

---

## Zettelkasten 系統

### 什麼是 Zettelkasten？

Zettelkasten（德語意為"卡片盒"）是一種筆記和個人知識管理方法。它強調創建原子、自包含且高度互連的筆記。

### 創建原子筆記

1. 保持筆記專注於單一想法
2. 使筆記自包含（不假設上下文）
3. 使用唯一 ID 進行引用
4. 使用 wikilinks 鏈接相關概念

### 示例

```markdown
# 2024-01-15 - 原子筆記

Zettelkasten 方法強調創建專注於單一想法的原子筆記。

相關：
- [[2024-01-16 - 鏈接筆記]]
- [[3 Resources/Productivity]]
```

---

## PARA 指令

使用 Claude Code 指令管理您的 PARA 庫：

| 指令 | 用途 |
|------|------|
| `/para-庫概覽` | 顯示 PARA 庫概覽和統計信息 |
| `/para-整理收集` | 根據 PARA 原則整理 InBox 內容 |

---

## 最佳實踐

1. **從簡單開始**：不要過度複雜化。從基本的捕捉和組織開始。
2. **一致的命名**：使用描述性、一致的文件名。
3. **定期回顧**：安排定期回顧 PARA 系統。
4. **鏈接一切**：使用 wikilinks 在筆記之間創建連接。
5. **保持活躍**：僅在真正不活躍時才將專案移至 Archives。
6. **使用模板**：從 `_template.md` 開始以保持一致的格式。
7. **明智標記**：明智地使用標籤以便於檢索。

---

## 許可證

本項目採用 Apache 2.0 許可證。

---

## 致謝

- [PARA 方法](https://fortelabs.co/) 由 Tiago Forte 創建
- [Obsidian](https://obsidian.md/) - 知識庫應用程序
- [Zettelkasten](https://zettelkasten.de/) - 筆記方法論



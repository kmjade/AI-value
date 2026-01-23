---
aliases:
  - 數字組織
  - 数据组织
status: active
tags:
  - area
  - productivity
  - knowledge-management
---

# Digital Organization / 數字組織

> [!info] 區域概覽
> 數字組織包含有效管理數字資訊的系統與實踐。此領域包括檔案管理、筆記系統、數字整理、工作流自動化與知識組織方法論。

---

## 📖 领域說明 / Area Description

> **數字組織** 是一項持續性責任，專注於在所有平台與設備上維護高效、可持續的數字資訊管理系統。

### 為何此區域重要
- 📚 **知識保留**：防止寶貴資訊在數字雜亂中遺失
- ⚡ **生產力**：減少搜尋檔案與資訊的時間
- 🔄 **一致性**：在工作與個人生活中維護一致的組織系統
- 🧠 **心智清晰**：透過可靠的外部系統降低認知負擔

### 核心原則
1. **可靠擷取** (Capture reliably) - 永不遺失好點子
2. **邏輯組織** (Organize logically) - 讓檢索直觀
3. **定期維護** (Maintain regularly) - 保持系統更新與整潔
4. **持續迭代** (Iterate continuously) - 根據使用情況改進系統

---

## 🎯 目標 / Goals

- [ ] 建立完整的 PARA 檔案組織系統
- [ ] 實現「收件箱清空」的日常習慣
- [ ] 每月進行一次數字整理與歸檔
- [ ] 建立跨設備的同步與備份機制
- [ ] 掌握 3 種以上的數字工具工作流
- [ ] 每季度優化一次組織系統

---

## ✅ 近期任務 / Recent Tasks

- [ ] 整理 `0 Personals/📥 00_InBox` 資料夾
- [ ] 建立檔案命名規範並應用
- [ ] 設置自動化備份流程
- [ ] 清理桌面和下載資料夾
- [ ] 審查並整理瀏覽器書籤
- [ ] 建立數位收件箱統一入口

---

## 📂 子主題 / Subtopics
---

> [!tip] QuickAdd 整合
> 使用 **QuickAdd** → `Add Subtopic` 可快速在此區域下建立新子主題筆記。

```dataview
Table without id (subtopic + " (" + length(rows.file.link) + ")") as "子主題", sort(rows.file.link) as 檔案, max(rows.file.mtime) AS "最近更新"
WHERE contains(file.path, this.file.folder) AND file.name != this.file.name
FLATTEN subtopic
GROUP BY subtopic
SORT subtopic
```

## 关联项目 / Related Projects
---
```dataview
TABLE WITHOUT id
  file.link as "项目",
  status as "状态",
  due as "截止日期"
FROM [[Digital Organization]]
WHERE para = "projects"
SORT due ASC
```

- [[1 Projects/测试项目]]

---

## 🔗 連結筆記 / Linked Notes

```dataview
Table sort(rows.file.link) as 檔案
FROM [[]]
WHERE !contains(file.folder, this.file.name)
GROUP BY file.folder as 資料夾
```

---

## 🗂️ 相關資源 / Related Resources

### 樣板 / Templates
- [[Resource Template]] - 資源筆記樣板
- [[Project Template]] - 專案筆記樣板

### 核心系統
- [[PARA Methodology]] - 主要組織架構
- [[Zettelkasten]] - 原子筆記系統
- [[Obsidian Workflows]] - 個人知識管理

---

## 📌 備註 / Notes

> [!note] Dataview 說明
> - **子主題**：子主題名稱，括號內為該子主題下筆記的數量
> - **最近更新**：子主題中最近一次被編輯的時間，方便快速檢視活躍度
> - 每週檢視子主題的筆記累積情況，確保重要領域持續產出

### 建議子主題 / Suggested Subtopics
可考慮為這些面向建立筆記：
- [[Note-Taking Workflows]] - 擷取、處理、組織、回顧的四階段工作流
- [[PARA Methodology]] - 完整的 PARA 方法論指南
- [[Zettelkasten]] - 卡片盒筆記法完整指南
- [[Obsidian Workflows]] - Obsidian 工作流完整指南
- [[File Management Systems]] - 檔案管理系統完整指南
- 數字整理 (Digital Decluttering)
- 自動化與工作流 (Automation & Workflows)
- 備份與同步策略 (Backup & Sync Strategies)
- 郵件管理 (Email Management)
- 瀏覽器與書籤組織 (Browser & Bookmark Organization)
- 任務管理整合 (Task Management Integration)

---

## 📅 週期回顧 / Periodic Review

> 在您的每日/每週筆記中使用此區段追蹤進度

```dataview
TABLE subtopic AS "子主題", length(rows.file.link) AS "筆記數"
FROM ""
WHERE contains(file.path, this.file.folder)
GROUP BY subtopic
SORT length(rows.file.link) DESC
```

### 回顧問題 / Review Questions
- 我是否已正確擷取新資訊？
- 收件箱是否已清空？
- 系統是否運作順暢？
- 本月需要優化什麼？
- 我是否遵循命名規範？

---

**最後更新**：`{{date:YYYY-MM-DD}}`
**下次回顧**：`{{date+1M:YYYY-MM-DD}}`

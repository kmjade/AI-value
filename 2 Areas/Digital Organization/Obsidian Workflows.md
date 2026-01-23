---
aliases:
  - Obsidian 工作流
  - Obsidian 使用指南
tags:
  - subtopic
  - productivity
  - obsidian
  - tools
  - workflows
status: active
created: 2026-01-19
---

# Obsidian Workflows / Obsidian 工作流

> [!info] 工作流概覽
> Obsidian 是一款強大的個人知識管理工具，本指南涵蓋從基礎設置到高級工作流的完整使用方法，幫助您建立高效的知識管理系統。

---

## 📖 Obsidian 簡介 / Introduction

### 什麼是 Obsidian？

Obsidian 是一款基於本地文件的知識管理工具，具有以下核心特性：

- 📁 **本地存儲**：所有數據存儲在本地，完全掌控
- 🔗 **雙向鏈接**：使用 `[[wikilinks]]` 建立知識連接
- 🧩 **插件生態**：豐富的社區插件擴展功能
- 🎨 **高度客製化**：外觀和功能都可以個性化
- 💻 **跨平台**：支持桌面、移動端、瀏覽器
- 🆓 **開源免費**：核心功能完全免費

### 為何選擇 Obsidian？

| 特性 | 優勢 |
|------|------|
| **本地優先** | 數據完全掌控，離線可用 |
| **Markdown 原生** | 純文本格式，跨工具相容 |
| **雙向鏈接** | 建立知識網絡，促進創造性思維 |
| **插件生態** | 功能無限擴展 |
| **快速響應** | 本地運行，無延遲 |
| **免費開源** | 無訂閱費，持續更新 |

---

## 🚀 快速開始 / Quick Start

### 1. 安裝與設置

#### 下載與安裝
- **桌面版**：[obsidian.md](https://obsidian.md/download)
- **移動版**：App Store / Google Play
- **Linux**：Snap / Flatpak

#### 基礎設置

**1. 創建保管庫（Vault）**
```
文件 → 打開文件夾作為保管庫 → 選擇您的資料夾
```

**2. 設置編輯器**
```
設置 → 編輯器
- 啟用：嚴格分行、拼写檢查、建議鏈接
- 顯示：行號、標尺、摺疊
```

**3. 設置外觀**
```
設置 → 外觀
- 主題：預設、Minimal、AnuPpuccin
- 基礎字體：支援中文的字體（如微軟正黑體）
```

**4. 設置文件與鏈接**
```
設置 → 文件與鏈接
- 默認位置：當前文件所在的文件夾
- 新建筆記的存放位置：在文件夾 root
- Wiki 鏈接：使用 [[Wikilinks]]
```

### 2. 核心功能介紹

#### Markdown 語法基礎

```markdown
# 一級標題
## 二級標題
### 三級標題

**粗體**
*斜體*
==高亮==
~~刪除線~~

- 無序列表
1. 有序列表

> 引用

`行內代碼`

```
代碼塊
```

[連結文字](https://example.com)
![[嵌入圖片]]
```

#### 雙向鏈接（Wikilinks）

```markdown
# 基本鏈接
[[Note Name]]

# 顯示文字
[[Note Name|顯示的文字]]

# 鏈接到標題
[[Note Name#Heading]]

# 鏈接到區塊
[[Note Name#^block-id]]

# 嵌入內容
![[Note Name]]
![[Note Name#Heading]]
![[image.png|400x300]]
```

#### 嵌入與引用

```markdown
# 嵌入整個筆記
![[Digital Organization]]

# 嵌入標題
![[Note-Taking Workflows#核心原則]]

# 嵌入圖片（調整大小）
![[image.png|600x400]]

# 嵌入 PDF 頁面
![[document.pdf#page=5]]

# 嵌入區塊（使用 ^block-id）
![[Note Name#^block-id]]
```

#### Callouts（提示塊）

```markdown
> [!info] 信息
> 這是一個信息提示塊

> [!note] 筆記
> 這是一個筆記提示塊

> [!tip] 提示
> 這是一個提示塊

> [!warning] 警告
> 這是一個警告塊

> [!faq]- 折疊
> 這是可折疊的內容

> [!todo]++ 展開
> 這是默認展開的內容
```

可用類型：`info`, `note`, `tip`, `success`, `question`, `warning`, `failure`, `danger`, `bug`, `example`, `quote`, `hint`, `caution`, `error`, `attention`, `abstract`, `summary`, `tldr`, `todo`, `check`, `done`, `help`, `faq`, `idea`, `important`, `best-practice`

#### Frontmatter（元數據）

```yaml
---
title: 筆記標題
aliases:
  - 別名1
  - 別名2
tags:
  - tag1
  - tag2
status: in-progress
created: 2026-01-19
modified: 2026-01-19
---

# 筆記內容
```

---

## 🧩 核心插件推薦 / Core Plugins

### 內置核心插件

| 插件 | 功能 | 必要性 | 設置建議 |
|------|------|--------|----------|
| **Daily Notes** | 每日筆記 | ⭐⭐⭐⭐⭐ | 設置模板和默認文件夾 |
| **Backlinks** | 反向鏈接面板 | ⭐⭐⭐⭐⭐ | 啟用顯示 |
| **Outgoing Links** | 外部鏈接面板 | ⭐⭐⭐⭐ | 啟用顯示 |
| **Tags** | 標籤面板 | ⭐⭐⭐⭐ | 啟用顯示 |
| **Graph View** | 知識圖譜 | ⭐⭐⭐⭐ | 設置分組和過濾 |
| **Canvas** | 畫布視圖 | ⭐⭐⭐⭐⭐ | 用於思維導圖 |
| **Bookmarks** | 書籤管理 | ⭐⭐⭐ | 快速訪問常用筆記 |
| **Templates** | 模板系統 | ⭐⭐⭐⭐⭐ | 設置模板文件夾 |

### Daily Notes 設置

```yaml
# 設置路徑：設置 → 每日筆記

新建筆記存放位置：0 Personals/Daily Notes/
日期格式：YYYY-MM-DD
模板文件位置：_Template/daily-note.md

# 模板內容
---
date: {{date}}
tags:
  - daily-note
---

# {{date:YYYY年MM月DD日 星期}}

## 📋 今日計劃
-

## 💡 想法與閃念
-

## 📝 今日筆記
-

## 🔗 今日關聯
-
```

---

## 🎛️ 社區插件推薦 / Community Plugins

### 必裝插件（Top 5）

#### 1. Dataview ⭐⭐⭐⭐⭐

**功能**：強大的數據查詢和展示插件

**用途**：
- 查詢筆記、任務、屬性
- 創建動態表格和列表
- 自動化內容聚合

**基礎查詢範例**：

```dataview
TABLE
  file.link AS 筆記,
  tags AS 標籤,
  status AS 狀態
FROM ""
WHERE contains(tags, "project")
SORT file.mtime DESC
```

```dataview
LIST
FROM "5 Zettels"
WHERE type = "permanent"
SORT file.ctime DESC
LIMIT 10
```

**任務查詢**：

```dataview
TASK
WHERE !completed
WHERE contains(path, this.file.folder)
GROUP BY file.link
```

**安裝設置**：
```
設置 → 社區插件 → 瀏覽 → 搜索 Dataview → 安裝
設置 → Dataview → 啟用 JavaScript 查詢（可選）
```

#### 2. Tasks ⭐⭐⭐⭐⭐

**功能**：增強任務管理和查詢

**用途**：
- 優先任務管理
- 任務查詢和過濾
- 設置截止日期和提醒

**任務語法**：

```markdown
- [ ] 基本任務
- [x] 已完成任務
- [ ] 重要任務 #high
- [ ] 中等優先級 #medium
- [ ] 低優先級 #low
- [ ] 有截止日期 📅 2026-01-20
- [ ] 重複任務 🔁 every day
- [ ] 開始日期 ⏳ 2026-01-20
```

**任務查詢**：

```tasks
not done
path includes Digital Organization
sort by due
sort by priority
```

```tasks
done after 2026-01-01
group by function task.file.folder
```

#### 3. Templater ⭐⭐⭐⭐⭐

**功能**：強大的模板系統，支持 JavaScript

**用途**：
- 動態模板（日期、時間、選擇器）
- 模板命令和腳本
- 自動化工作流

**模板範例**：

```yaml
---
<%*
  let title = await tp.system.prompt("輸入標題");
  let type = await tp.system.suggester(["專案", "領域", "資源"], ["project", "area", "resource"]);
  tR += `
title: ${title}
type: ${type}
created: ${tp.date.now("YYYY-MM-DD HH:mm:ss")}
`;
-%>
---

# ${title}

> [!info] 創建時間：${tp.date.now()}
> 類型：${type}

## 說明

-

## 目標

-

## 關連筆記

- [[]]
```

**常用命令**：

```javascript
// 日期和時間
<% tp.date.now() %>
<% tp.date.now("YYYY-MM-DD") %>
<% tp.date.now("YYYY年MM月DD日") %>

// 用戶輸入
<% await tp.system.prompt("問題") %>

// 選擇器
<% await tp.system.suggester(["選項1", "選項2"], ["value1", "value2"]) %>

// 文件信息
<% tp.file.title %>
<% tp.file.path %>
<% tp.file.folder %>

// 創建新筆記
<% await tp.file.create_new("新筆記內容") %>
```

#### 4. QuickAdd ⭐⭐⭐⭐

**功能**：快速創建內容和執行腳本

**用途**：
- 一鍵創建特定類型的筆記
- 腳本執行和自動化
- 動態菜單選項

**設置範例**：

```yaml
# 選項：創建 Zettelkasten 永久筆記
格式：
---
id: {{DATE:YYYYMMDDHHmmss}}
type: permanent
tags: []
created: {{DATE}}
---

# {{VALUE:title}}

## 核心思想

-

## 說明

-

## 參見

- [[]]
```

#### 5. Calendar ⭐⭐⭐⭐

**功能**：日曆視圖，管理每日筆記

**用途**：
- 可視化查看每日筆記
- 快速導航到特定日期
- 追蹤筆記創建頻率

---

### 實用插件（推薦）

#### 6. Excalidraw ⭐⭐⭐⭐

**功能**：繪圖和手寫筆記

**用途**：
- 思維導圖
- 流程圖
- 手寫筆記

#### 7. Advanced Tables ⭐⭐⭐⭐

**功能**：增強表格編輯

**用途**：
- 快速格式化表格
- 對齊和調整列寬
- Excel 風格編輯

#### 8. Obsidian Git ⭐⭐⭐

**功能**：Git 版本控制集成

**用途**：
- 自動提交和推送
- 版本歷史管理
- 跨設備同步

#### 9. Hotkeys for Templates ⭐⭐⭐

**功能**：模板快捷鍵

**用途**：
- 快速插入模板
- 減少點擊操作

#### 10. Tag Wrangler ⭐⭐⭐

**功能**：標籤管理

**用途**：
- 批量重命名標籤
- 查找未使用標籤
- 標籤搜索和過濾

---

## 🔄 日常工作流 / Daily Workflows

### 每日工作流（30 分鐘）

#### 1. 早晨啟動（5 分鐘）

```
1. 打開 Daily Notes（Ctrl/Cmd + D）
2. 複製昨日未完成任務
3. 設定今日 3 個優先任務
4. 快速瀏覽 Graph View 發現連結
```

**模板**：

```markdown
## 🌅 晨間計劃

### 優先任務（Top 3）
1. [ ]
2. [ ]
3. [ ]

### 昨日未完成
- [ ]

### 今日安排
- 📅 上午：
- 📅 下午：
- 📅 晚上：
```

#### 2. 工作中隨時（全天）

```
1. 快速記錄想法到 Daily Notes 或閃念筆記
2. 創建和編輯專案筆記
3. 使用 Backlinks 面板查看相關筆記
4. 適時創建 Zettelkasten 卡片
```

**快捷操作**：
- `Ctrl/Cmd + N`：新建筆記
- `Ctrl/Cmd + O`：快速打開
- `Ctrl/Cmd + E`：切換預覽/編輯模式
- `Ctrl/Cmd + K`：插入 Wikilink

#### 3. 晚間回顧（20 分鐘）

```
1. 檢視今日完成的任務
2. 整理閃念筆記（轉換為永久筆記）
3. 建立新筆記的鏈接
4. 更新專案進度
5. 記錄今日學習和心得
```

**模板**：

```markdown
## 🌙 晚間回顧

### 今日完成
- [x]
- [x]
- [x]

### 今日學習
-

### 今日心得
-

### 明日計劃
- [ ]

### 待處理筆記
- [ ] 整理閃念筆記
- [ ] 建立新鏈接
```

### 週工作流（1 小時）

#### 週日回顧

```markdown
# 週回顧 - 週次 XX

## 📊 本週統計

- 新增筆記：X 筆
- 完成任務：X 個
- 創建鏈接：X 個

## 🎯 專案進度

### 進行中
- [[專案1]] - 狀態
- [[專案2]] - 狀態

### 已完成
- [[專案3]] - 完成日期

## 📚 知識管理

### Zettelkasten
- 新增永久筆記：X 筆
- 建立新鏈接：X 個

### 閃念筆記處理
- 已處理：X 筆
- 待處理：X 筆

## 🧠 洞察與想法
-

## 📋 下週計劃
-

## 🔧 系統優化
-
```

---

## 🗂️ 文件組織策略 / File Organization

### PARA 結構在 Obsidian 中

```
📁 AI-value/
├── 📁 0 Personals/
│   └── 📁 Daily Notes/          # 每日筆記
│   └── 📁 📥 00_InBox/         # 收件箱
├── 📁 1 Projects/              # 專案
├── 📁 2 Areas/                 # 領域
│   └── 📁 Digital Organization/
│       ├── Digital Organization.md
│       ├── Note-Taking Workflows.md
│       ├── PARA Methodology.md
│       └── Zettelkasten.md
├── 📁 3 Resources/             # 資源
├── 📁 4 Archives/              # 歸檔
├── 📁 5 Zettels/              # Zettelkasten
├── 📁 _Template/              # 模板
└── 📁 Attachments/            # 附件
```

### 文件命名規範

```markdown
# 專案
2026-01-19 推出新網站.md
2026-Q1 學習 Python.md

# 領域
Digital Organization.md
Health & Fitness.md

# 資源
AI Tools & Applications.md
Productivity Tips.md

# Zettels
健康-WHO定義.md
深度工作-定義.md

# 每日筆記
2026-01-19.md
```

---

## 🎨 主題與外觀 / Themes & Appearance

### 推薦主題

#### 1. Minimal ⭐⭐⭐⭐⭐

**特點**：極簡設計，專注於內容

**設置**：
```
設置 → 外觀 → 主題 → 瀏覽 → Minimal → 使用
設置 → 外觀 → Minimal Theme Settings → 啟用 Flow Style
```

#### 2. AnuPpuccin ⭐⭐⭐⭐⭐

**特點**：現代感強，多配色方案

**設置**：
```
設置 → 外觀 → 主題 → 瀏覽 → AnuPpuccin → 使用
設置 → 外觀 → AnuPpuccin Theme Settings → 選擇配色
```

#### 3. Things Theme ⭐⭐⭐⭐

**特點**：類似 macOS 應用的美觀設計

### 字體設置

**中文推薦字體**：
- 微軟正黑體（Microsoft JhengHei）
- 思源黑體（Noto Sans CJK）
- 蘋方（PingFang SC - macOS）

**設置**：
```
設置 → 外觀 → 字體
- 界面字體：選擇中文字體
- 文本字體：選擇中文字體
- 等寬字體：JetBrains Mono, Fira Code
```

---

## 🔗 同步與備份 / Sync & Backup

### 同步方案

#### 方案 1：Obsidian Sync（付費）

**優點**：
- 官方支持，穩定可靠
- 自動同步，無需配置
- 支持歷史版本

**設置**：
```
設置 → 同步 → 開啟同步 → 登錄賬號 → 選擇要同步的文件夾
```

#### 方案 2：Git + GitHub（免費）

**優點**：
- 完全免費
- 版本控制
- 跨平台支持

**設置**：
1. 安裝 Git
2. 創建 GitHub 倉庫
3. 安裝 Obsidian Git 插件
4. 配置自動提交和推送

**配置**：

```yaml
# 設置 → Obsidian Git
自動備份間隔：15 分鐘
提交時自動推送：啟用
提交前先拉取：啟用
```

#### 方案 3：雲端同步（免費）

**工具**：
- iCloud（macOS/iOS）
- OneDrive
- Google Drive
- Dropbox

**注意**：
- 避免同時在多個設備編輯
- 定期檢查衝突文件

### 備份策略

```markdown
# 本地備份
- 定期複製保管庫到外部硬碟
- 使用壓縮軟件歸檔舊版本

# 雲端備份
- 使用雲端同步自動備份
- 定期導出 Markdown 到其他位置

# 版本備份
- Git 版本控制
- Obsidian Sync 歷史版本
```

---

## 📊 效能優化 / Performance Optimization

### 提升效能

1. **限制 Graph View 顯示**
   ```
   設置 → 圖譜視圖 → 顯示節點數量：50-100
   ```

2. **禁用不必要的插件**
   - 定期審查已安裝插件
   - 禁用不常用的插件

3. **優化圖片**
   - 壓縮大圖片
   - 使用外部鏈接而非嵌入

4. **清理未使用附件**
   - 定期檢查 Attachments 文件夾
   - 刪除未引用的圖片和文件

### Dataview 優化

```dataview
# 限制查詢範圍
FROM "2 Areas"  # 而非 FROM ""
LIMIT 100       # 限制結果數量
```

---

## 🎯 進階技巧 / Advanced Tips

### 1. 使用 Canvas 進行視覺化思考

**用途**：
- 思維導圖
- 項目規劃
- 概念映射

**操作**：
```
Ctrl/Cmd + N → Canvas
拖動筆記到畫布
連接卡片（Shift + 點擊並拖動）
```

### 2. 使用標籤系統

**標籤層級**：
```markdown
# 一級標籤
#productivity

# 二級標籤
#productivity/deep-work

# 三級標籤
#productivity/deep-work/strategies
```

**標籤查詢**：
```dataview
FROM #productivity
```

### 3. 使用屬性（Properties）

```yaml
---
title: 筆記標題
type: permanent
status: in-progress
priority: high
created: 2026-01-19
modified: 2026-01-19
due: 2026-01-20
tags: [productivity, workflow]
---
```

**查詢**：
```dataview
TABLE file.link, status, priority
FROM ""
WHERE type = "permanent" AND status = "in-progress"
```

### 4. 使用腳本自動化

**Templater 腳本範例**：

```javascript
<%*
  // 自動創建每日筆記並關聯
  let today = tp.date.now("YYYY-MM-DD");
  let yesterday = tp.date.now("YYYY-MM-DD", -1);

  tR += `
## 昨日連結
[[${yesterday}]]
`;
%>
```

---

## 📚 學習資源 / Learning Resources

### 官方文檔
- [Obsidian 官方文檔](https://help.obsidian.md/)
- [Obsidian 发布公告](https://forum.obsidian.md/)

### 社群資源
- [Obsidian 官方論壇](https://forum.obsidian.md/)
- [Obsidian 官方 Discord](https://discord.gg/ve6W84cD4A)
- [Reddit r/ObsidianMD](https://www.reddit.com/r/ObsidianMD/)
- [YouTube Obsidian 頻道](https://www.youtube.com/@obsidianmd)

### 推薦教程
- [Obsidian 101 系列教程](https://www.youtube.com/playlist?list=PL3C8Cn8v7cKvQx9M2XQ9K3K3J3J3J3J3J)
- [Obsidian 中文社區](https://obsidian-chinese.github.io/)
- [Obsidian 插件庫](https://github.com/obsidianmd/obsidian-releases)

### 書籍
- [[Building a Second Brain]] - Tiago Forte
- [[How to Take Smart Notes]] - Sönke Ahrens

---

## 📌 常見問題 / FAQ

### Q1: Obsidian 是免費的嗎？

**A**: 核心功能完全免費。付費服務包括：
- Obsidian Sync（同步服務）
- Obsidian Publish（發布服務）

### Q2: 如何同步到多個設備？

**A**: 有三種方案：
1. **Obsidian Sync**（付費）- 最簡單
2. **Git**（免費）- 需要技術配置
3. **雲端同步**（免費）- 注意衝突

### Q3: Dataview 和 Tasks 有什麼區別？

**A**:
- **Dataview**: 查詢和展示數據，更靈活
- **Tasks**: 專門管理任務，更易用

建議：兩個都安裝，根據需求選擇使用。

### Q4: 如何導出筆記？

**A**:
- **PDF 導出**：打印為 PDF
- **Markdown 導出**：使用 Pandoc
- **HTML 導出**：使用 Obsidian Publish
- **批量導出**：使用插件

### Q5: 如何保護數據安全？

**A**:
- 定期備份到多個位置
- 使用 Git 版本控制
- 不要刪除衝突文件前查看內容
- 使用密碼管理器存儲敏感信息

---

## 🎯 下一步行動 / Next Steps

### 立即行動
- [ ] 安裝推薦的核心插件
- [ ] 設置 Daily Notes 模板
- [ ] 創建第一個 Zettelkasten 卡片
- [ ] 配置同步和備份方案

### 本週目標
- [ ] 建立每日工作流習慣
- [ ] 創建至少 10 張筆記
- [ ] 設置和使用 Dataview 查詢
- [ ] 創建個人化的模板庫

### 本月目標
- [ ] 完成專案：`[[obsidian知识库]]`
- [ ] 積累至少 50 張永久筆記
- [ ] 建立穩定的知識管理工作流
- [ ] 優化系統效能和外觀

---

## 🔗 關連筆記 / Related Notes

- [[Digital Organization]]
- [[Note-Taking Workflows]]
- [[PARA Methodology]]
- [[Zettelkasten]]
- [[How to Take Smart Notes]] - How to Take Smart Notes 書籍學習筆記
- [[obsidian知识库]]
- [[File Management Systems]]

---

**建立日期**：2026-01-19
**最後更新**：`{{date:YYYY-MM-DD}}`
**下次回顧**：`{{date+3M:YYYY-MM-DD}}`

---
aliases:
  - 檔案管理系統
  - 文件管理系统
  - 文件组织
tags:
  - subtopic
  - productivity
  - file-management
  - organization
status: active
created: 2026-01-20
---

# File Management Systems / 檔案管理系統

> [!info] 系統概覽
> 檔案管理系統是數字組織的基礎，涵蓋文件夾結構、命名規範、歸檔策略和跨設備同步，幫助建立高效、可維護的數字環境。

---

## 📖 系統簡介 / Introduction

### 什麼是檔案管理系統？

檔案管理系統是一套系統化的方法，用於組織、命名、存儲和檢索數字文件。它確保您能夠快速找到需要的文件，避免數字雜亂，並維持長期的組織效率。

### 為何需要檔案管理系統？

| 問題 | 影響 | 解決方案 |
|------|------|---------|
| ❌ 找不到文件 | 浪費時間搜尋 | 統一的命名和分類 |
| ❌ 檔案重複 | 佔用空間、混淆 | 單一來源原則 |
| ❌ 版本混亂 | 使用錯誤版本 | 版本控制策略 |
| ❌ 備份缺失 | 數據丟失風險 | 自動備份系統 |
| ❌ 跨設備不同步 | 無法隨時訪問 | 雲端同步方案 |

### 檔案管理的核心原則

1. **統一性**（Consistency）- 使用一致的命名和結構
2. **層次性**（Hierarchy）- 清晰的文件夾層級
3. **可預測性**（Predictability）- 知道文件在哪裡
4. **可擴展性**（Scalability）- 系統隨時間成長
5. **可維護性**（Maintainability）- 易於清理和更新

---

## 🗂️ 核心系統架構 / Core Architecture

### PARA 檔案結構

```
📁 AI-value/
│
├── 📁 0 Personals/                 # 個人內容
│   ├── 📁 📥 00_InBox/          # 收件箱
│   │   ├── 📄 00_InBox.md
│   │   ├── 📁 0-待辦/
│   │   ├── 📁 1-鏈接/
│   │   └── 📁 2-素材/
│   └── 📁 Daily Notes/            # 每日筆記
│
├── 📁 1 Projects/                  # 專案
│   ├── 📁 2026-Q1/               # 按季度組織
│   │   ├── 📄 2026-01-19 推出新網站.md
│   │   └── 📄 2026-Q1 學習 Python.md
│   ├── 📁 2026-Q2/
│   └── 📄 Active Projects.md
│
├── 📁 2 Areas/                     # 領域
│   ├── 📁 Digital Organization/
│   │   ├── 📄 Digital Organization.md
│   │   ├── 📄 Note-Taking Workflows.md
│   │   ├── 📄 PARA Methodology.md
│   │   ├── 📄 Zettelkasten.md
│   │   └── 📄 Obsidian Workflows.md
│   ├── 📁 Health & Fitness/
│   └── 📁 Personal Finance/
│
├── 📁 3 Resources/                 # 資源
│   ├── 📁 AI/
│   │   └── 📄 AI Tools & Applications.md
│   ├── 📁 Productivity/
│   └── 📁 Investment/
│
├── 📁 4 Archives/                  # 歸檔
│   ├── 📁 2025/
│   │   ├── 📁 Projects/
│   │   ├── 📁 Areas/
│   │   └── 📁 Resources/
│   └── 📁 2024/
│
├── 📁 5 Zettels/                  # Zettelkasten
│   ├── 📄 5 Zettels.md
│   ├── 📁 fleeting/
│   ├── 📁 literature/
│   ├── 📁 permanent/
│   └── 📁 structure/
│
├── 📁 _Template/                  # 模板
│   ├── 📄 daily-note.md
│   ├── 📄 project.md
│   └── 📁 para/
│
├── 📁 _meta/                     # 系統元數據
│   └── 📄 _meta.md
│
├── 📁 Attachments/                # 附件
├── 📁 .obsidian/                 # Obsidian 配置
└── 📁 .claude/                  # Claude Code 配置
```

### 結構設計原則

#### 1. 數字前綴排序

```
0 Personals/    # 00 - 個人相關（最高優先級）
1 Projects/     # 01 - 專案（短期行動）
2 Areas/        # 02 - 領域（長期責任）
3 Resources/    # 03 - 資源（知識庫）
4 Archives/     # 04 - 歸檔（不活躍）
5 Zettels/     # 05 - Zettelkasten（知識網絡）
_Template/     # 系統文件夾
_meta/         # 系統元數據
```

**優勢**：
- 文件夾按優先級自動排序
- 清楚區分活躍和不活躍內容
- 符合 PARA 方法的分類邏輯

#### 2. 時間基礎歸檔

```
4 Archives/
├── 📁 2026/          # 當年
├── 📁 2025/          # 去年
├── 📁 2024/          # 2024 年
└── 📁 2023/          # 2023 年
```

**優勢**：
- 按年份輕鬆瀏覽
- 便於按時間段備份
- 清晰的歷史記錄

#### 3. 功能性文件夾前綴

```
📁 0-待辦/          # 0 - 待辦事項
📁 1-鏈接/          # 1 - 保存的鏈接
📁 2-素材/          # 2 - 圖片、文件等素材
```

**優勢**：
- 功能分類清晰
- 自動排序
- 快速識別內容類型

---

## 📝 命名規範 / Naming Conventions

### 通用命名原則

> [!warning] 命名規範原則
> 一致性 > 個性化。保持統一的命名規範比創意命名更重要。

#### 1. 文件夾命名

```
✅ 好的命名：
- Digital Organization/
- Health & Fitness/
- AI Tools & Applications/

❌ 壞的命名：
- Digital Org/
- health/
- AI Stuff/
```

**規範**：
- ✅ 使用英文或繁體中文（統一）
- ✅ 使用標題格式（首字母大寫）
- ✅ 使用空格分隔單詞（Obsidian 支持良好）
- ✅ 使用清晰描述性名稱
- ❌ 避免特殊字符（如 `/`, `\`, `:`, `*`, `?`, `"`, `<`, `>`, `|`）
- ❌ 避免過度縮寫

#### 2. 檔案命名

**專案檔案**：

```markdown
格式：YYYY-MM-DD 專案名稱.md
範例：
✅ 2026-01-19 推出新網站.md
✅ 2026-Q1 學習 Python.md
✅ 2026-03 完成年度報告.md

❌ 新網站.md
❌ Python 學習.md
❌ 年度報告 2026.md
```

**優勢**：
- 按日期自動排序
- 清楚顯示專案時間
- 便於批量處理

**筆記檔案**：

```markdown
格式：主題-具體概念.md
範例：
✅ 健康-WHO定義.md
✅ 深度工作-定義.md
✅ PARA-方法論.md

❌ WHO定義.md
❌ 定義-深度工作.md
❌ PARA.md
```

**Zettels 檔案**：

```markdown
格式：主題-具體概念.md
範例：
✅ 健康-WHO定義.md
✅ 營養-基礎代謝率.md
✅ 運動-運動強度.md

閃念筆記：
✅ 閃念-深度工作.md
✅ 閃念-時間管理.md
```

**文獻筆記**：

```markdown
格式：書名-作者-章節.md
範例：
✅ 深度工作-Cal Newport-第3章.md
✅ How to Take Smart Notes-Sönke Ahrens-第1章.md
```

**結構筆記**：

```markdown
格式：主題-結構.md
範例：
✅ 健康管理-結構.md
✅ PARA-結構.md
```

#### 3. 附件命名

```
格式：YYYY-MM-DD-描述.擴展名
範例：
✅ 2026-01-19-會議記錄.png
✅ 2026-01-20-報告草稿.pdf
✅ 2026-01-20-流程圖.png

❌ 截圖1.png
❌ 最終版本.pdf
❌ 圖片.png
```

**優勢**：
- 按時間排序
- 清楚描述內容
- 避免版本混淆

#### 4. 特殊字符處理

| 字符 | 是否允許 | 建議替代 |
|------|---------|---------|
| `A-Z`, `a-z`, `0-9` | ✅ 允許 | - |
| 空格 | ✅ 允許 | - |
| `_` 下劃線 | ✅ 允許 | - |
| `-` 連字符 | ✅ 允許 | - |
| `()` 括號 | ⚠️ 謹慎使用 | 用於補充信息 |
| `[]` 方括號 | ❌ 避免 | 某些系統不支持 |
| `{}` 花括號 | ❌ 避免 | 某些系統不支持 |
| `#` 井號 | ❌ 避免 | 用於標籤而非文件名 |
| `@` 艾特符號 | ❌ 避免 | 用於標籤而非文件名 |
| `:` 冒號 | ❌ 避免 | 用於時間而非文件名 |
| `*` 星號 | ❌ 避免 | 萬用字符 |
| `?` 問號 | ❌ 避免 | 萬用字符 |
| `" "` 雙引號 | ❌ 避免 | 命令行問題 |
| `<` `>` 小於/大於 | ❌ 避免 | 重定向符號 |
| `|` 管道符號 | ❌ 避免 | 命令行問題 |
| `\` `/` 路徑符號 | ❌ 避免 | 路徑分隔符 |

---

## 🔄 版本控制策略 / Version Control

### 1. 手動版本控制

#### 版本命名規範

```
格式：文件名-v1.0.擴展名
範例：
✅ 項目報告-v1.0.docx
✅ 項目報告-v1.1.docx
✅ 項目報告-v2.0.docx

❌ 項目報告.docx
❌ 項目報告-最終.docx
❌ 項目報告-最終最終.docx
```

#### 版本號規則

```
v1.0 - 初始版本
v1.1 - 小修訂（bug 修復、小改進）
v2.0 - 大版本（重大變更、新增功能）
```

### 2. 自動版本控制

#### 使用 Git

**優勢**：
- 自動追蹤所有更改
- 可以回滾到任何版本
- 支持分支和合併
- 適合編程和文檔項目

**設置**：

```bash
# 初始化 Git 倉庫
cd /path/to/AI-value
git init

# 添加 .gitignore
cat > .gitignore << EOF
.obsidian/
.claude/
.DS_Store
Thumbs.db
*.log
node_modules/
EOF

# 初次提交
git add .
git commit -m "Initial commit"

# 推送到 GitHub
git remote add origin https://github.com/username/AI-value.git
git branch -M main
git push -u origin main
```

**日常使用**：

```bash
# 提交更改
git add .
git commit -m "Update: 添加 Obsidian Workflows 筆記"

# 推送到遠端
git push

# 拉取最新更改
git pull

# 查看歷史
git log --oneline

# 回滾到特定版本
git checkout <commit-hash>
```

#### 使用 Obsidian Git 插件

**配置**：

```yaml
# 設置 → Obsidian Git
自動備份間隔：15 分鐘
提交時自動推送：啟用
提交前先拉取：啟用
備份路徑：.git
```

### 3. 雲端版本控制

#### OneDrive 版本歷史

```
設置：
1. 右鍵文件 → 版本歷史
2. 查看和恢復舊版本

優勢：
- 自動版本歷史
- 無需額外設置
- 雲端同步
```

#### Google Drive 版本歷史

```
設置：
1. 右鍵文件 → 管理版本
2. 查看和恢復舊版本

優勢：
- 自動版本歷史
- 多設備同步
- 協作功能
```

---

## 📦 歸檔策略 / Archiving Strategies

### 歸檔時機

#### 專案歸檔

```markdown
歸檔條件：
✅ 專案完成
✅ 專案取消
✅ 專案暫停超過 6 個月

歸檔步驟：
1. 將專案移動到 "4 Archives/年份/Projects/"
2. 更新專案狀態為 "archived"
3. 從 Active Projects.md 中移除
4. 備份重要資源到 Resources
```

#### 資源歸檔

```markdown
歸檔條件：
✅ 資源不再感興趣
✅ 資源過時
✅ 資源已完全掌握

歸檔步驟：
1. 將資源移動到 "4 Archives/年份/Resources/"
2. 檢查並更新相關的 Zettelkasten 卡片
3. 考慮是否需要保留或刪除
```

#### 定期歸檔計畫

```markdown
每週：
- [ ] 檢查是否有完成的專案需要歸檔

每月：
- [ ] 檢查資源是否需要歸檔
- [ ] 清理 InBox 中的舊內容

每季：
- [ ] 大規模歸檔清理
- [ ] 檢查並壓縮舊歸檔

每年：
- [ ] 歸檔去年的內容
- [ ] 考慮刪除超過 2 年的歸檔
```

### 歸檔維護

#### 歸檔清理

```
1. 每年檢視歸檔內容
2. 識別無價值的歸檔
3. 壓縮或刪除
4. 備份重要內容到外部存儲
```

#### 歸檔檢查清單

- [ ] 所有專案是否正確歸檔？
- [ ] 歸檔的文件是否命名一致？
- [ ] 是否有重複的歸檔？
- [ ] 歸檔的年份是否正確？
- [ ] 需要保留的內容是否已備份？

---

## 🔄 同步策略 / Sync Strategies

### 同步方案對比

| 方案 | 優勢 | 劣勢 | 成本 | 推薦度 |
|------|------|------|------|--------|
| **Obsidian Sync** | 官方支持、穩定可靠 | 付費服務 | $10/月 | ⭐⭐⭐⭐⭐ |
| **Git + GitHub** | 免費、版本控制 | 需要技術配置 | 免費 | ⭐⭐⭐⭐ |
| **iCloud** | 原生支持（Apple 設備） | 限制 5GB、Android 不支持 | 免費（5GB） | ⭐⭐⭐⭐ |
| **OneDrive** | Windows 原生支持、大空間 | 同步延遲、衝突處理 | 免費（5GB） | ⭐⭐⭐ |
| **Google Drive** | 大空間、協作支持 | 同步延遲、桌面客戶端一般 | 免費（15GB） | ⭐⭐⭐ |

### 推薦同步方案

#### 方案 1：Obsidian Sync（最簡單）

**適合**：希望無需配置的用戶

**設置**：

```
1. 註冊 Obsidian Sync 賬戶
2. 在 Obsidian 中登錄
3. 設置 → 同步 → 開啟同步
4. 選擇要同步的文件夾
5. 在其他設備上登錄
```

**價格**：
- 個人：$10/月
- 團隊：$50/月（5 用戶）

**優勢**：
- 官方支持，穩定可靠
- 自動同步，無需配置
- 支持歷史版本（30 天）
- 加密傳輸
- 支持移動端

#### 方案 2：Git + GitHub（免費推薦）

**適合**：技術用戶、需要版本控制

**設置**：

```bash
# 1. 安裝 Git
# macOS: brew install git
# Windows: https://git-scm.com/download/win
# Linux: sudo apt install git

# 2. 創建 GitHub 倉庫
# 訪問 https://github.com/new
# 倉庫名：AI-value
# 設為私有倉庫

# 3. 初始化本地 Git
cd /path/to/AI-value
git init

# 4. 添加 .gitignore
cat > .gitignore << 'EOF'
.obsidian/
.claude/
.DS_Store
Thumbs.db
*.log
node_modules/
.vscode/
.idea/
EOF

# 5. 初次提交
git add .
git commit -m "Initial commit"

# 6. 連接遠端
git remote add origin https://github.com/username/AI-value.git
git branch -M main
git push -u origin main
```

**自動化提交**：

使用 **Obsidian Git** 插件：

```yaml
設置 → Obsidian Git

自動備份間隔：15 分鐘
提交時自動推送：啟用
提交前先拉取：啟用
提交訊息模板：Update: {{date:YYYY-MM-DD}}
```

**優勢**：
- 完全免費
- 版本控制
- 跨平台支持
- 開源生態
- 可以回滾到任何版本

#### 方案 3：iCloud（Apple 設備）

**適合**：全 Apple 設備用戶

**設置**：

```
1. 在 Finder 中打開 iCloud Drive
2. 將 AI-value 文件夾移動到 iCloud Drive
3. 在其他 Apple 設備上安裝 Obsidian
4. 選擇 iCloud Drive 中的 AI-value 文件夾
```

**優勢**：
- 原生支持，無需第三方
- 自動同步
- 無需額外配置

**限制**：
- 僅限 Apple 設備
- 免費空間 5GB
- Android 設備不支持

#### 方案 4：OneDrive（Windows 用戶）

**適合**：Windows 用戶

**設置**：

```
1. 打開 OneDrive 文件夾
2. 將 AI-value 文件夾移動到 OneDrive
3. 在其他設備上安裝 Obsidian
4. 選擇 OneDrive 中的 AI-value 文件夾
```

**優勢**：
- Windows 原生支持
- 大空間（免費 5GB，$1.99/月 100GB）
- 版本歷史

**限制**：
- 同步延遲
- 衝突處理不夠智能

---

## 💾 備份策略 / Backup Strategies

### 3-2-1 備份原則

```
3 - 保存至少 3 份副本
2 - 備份存儲在至少 2 種類型的存儲設備上
1 - 至少 1 份備份在異地
```

### 推薦備份方案

#### 方案 1：本地 + 雲端 + 異地

```
1. 本地備份：
   - 定期複製到外部硬碟
   - 使用 Time Machine（macOS）
   - 使用 File History（Windows）

2. 雲端備份：
   - 使用同步服務（iCloud、OneDrive、GitHub）
   - 自動同步所有更改

3. 異地備份：
   - 保存重要內容到另一個地點
   - 使用另一個雲端服務
```

#### 方案 2：自動化備份

**macOS Time Machine**：

```
設置：
1. 連接外部硬碟
2. 系統偏好設置 → Time Machine
3. 選擇備份磁碟
4. 開啟自動備份

優勢：
- 完全系統備份
- 自動增量備份
- 可以恢復到任何時間點
```

**Windows File History**：

```
設置：
1. 連接外部硬碟
2. 設置 → 更新和安全 → 備份
3. 添加驅動器
4. 開啟自動備份

優勢：
- 文件版本歷史
- 自動備份
- 選擇性備份
```

#### 方案 3：腳本備份

**Linux/macOS 備份腳本**：

```bash
#!/bin/bash
# backup.sh - 備份腳本

SOURCE="/path/to/AI-value"
BACKUP="/path/to/backup"
DATE=$(date +%Y%m%d_%H%M%S)

# 創建備份目錄
mkdir -p "$BACKUP/$DATE"

# 複製文件
rsync -av --progress "$SOURCE/" "$BACKUP/$DATE/"

# 壓縮
cd "$BACKUP"
tar -czf "AI-value_$DATE.tar.gz" "$DATE"

# 刪除 7 天前的備份
find "$BACKUP" -type d -mtime +7 -exec rm -rf {} \;

echo "備份完成：$DATE"
```

**設置定時任務**：

```bash
# 添加到 crontab（每天凌晨 2 點執行）
crontab -e
0 2 * * * /path/to/backup.sh
```

### 備份驗證

```markdown
備份驗證清單：
- [ ] 備份成功創建？
- [ ] 備份文件大小合理？
- [ ] 可以從備份恢復文件？
- [ ] 備份包含所有重要內容？
- [ ] 異地備份可訪問？

定期測試：
- 每月嘗試恢復一個文件
- 每季驗證完整備份
- 每年測試災難恢復
```

---

## 🧹 檔案清理 / File Cleanup

### 定期清理計畫

#### 每日清理（5 分鐘）

```markdown
- [ ] 清空 InBox
- [ ] 刪除重複文件
- [ ] 整理下載資料夾
- [ ] 清空剪貼簿
```

#### 每週清理（30 分鐘）

```markdown
- [ ] 清理桌面文件
- [ ] 刪除未使用的附件
- [ ] 檢查並整理瀏覽器下載
- [ ] 清理臨時文件
- [ ] 檢查並歸檔完成的專案
```

#### 每月清理（1 小時）

```markdown
- [ ] 大規模檔案審查
- [ ] 刪除過時的資源
- [ ] 壓縮大型文件
- [ ] 清理雲端存儲
- [ ] 檢查並更新文件名稱
```

#### 每年清理（2-3 小時）

```markdown
- [ ] 全面檔案審查
- [ ] 刪除超過 2 年的歸檔
- [ ] 重新評估文件組織結構
- [ ] 更新備份策略
- [ ] 記錄並改進系統
```

### 清理工具

#### 手動清理

```
1. 使用文件搜索（Command/Ctrl + P）查找重複
2. 按大小排序，識別大文件
3. 按修改日期排序，找出舊文件
4. 使用文件預覽，決定保留或刪除
```

#### 自動化清理工具

**macOS**：
- **DaisyDisk** - 可視化磁碟空間
- **CleanMyMac X** - 清理系統文件
- **Disk Inventory X** - 免費磁碟分析

**Windows**：
- **WinDirStat** - 可視化磁碟空間
- **CCleaner** - 清理系統文件
- **WizTree** - 快速磁碟分析

**Linux**：
- **ncdu** - 命令行磁碟分析
- **BleachBit** - 清理系統文件
- **du** - 內置磁碟使用分析

---

## 📊 系統監控 / System Monitoring

### 檔案系統統計

#### Dataview 查詢

```dataview
TABLE
  file.folder AS 資料夾,
  length(rows) AS 檔案數,
  sum(rows.file.size, 0) / 1024 / 1024 AS "大小 (MB)"
FROM ""
WHERE file.name != this.file.name
GROUP BY file.folder
SORT sum(rows.file.size) DESC
```

#### 存儲空間監控

```markdown
每月檢查：
- [ ] 總存儲空間使用
- [ ] 各類別空間使用
- [ ] 大文件（> 100MB）
- [ ] 重複文件數量
- [ ] 未使用附件數量
```

### 系統健康檢查

#### 每月健康檢查清單

```markdown
文件組織：
- [ ] 文件夾結構清晰？
- [ ] 命名規範一致？
- [ ] 歸檔及時完成？

系統效能：
- [ ] 備份正常運行？
- [ ] 同步無衝突？
- [ ] 檔案搜索快速？

數據完整性：
- [ ] 無重複文件？
- [ ] 無損壞文件？
- [ ] 連結全部有效？

改進機會：
- [ ] 有哪些檔案混亂？
- [ ] 有哪些重複勞動？
- [ ] 有哪些可以自動化？
```

---

## 🎯 最佳實踐 / Best Practices

### ✅ 應該做的事

1. **從收件箱開始**
   - 所有新內容進入 InBox
   - 定期處理 InBox
   - 清空收件箱

2. **統一命名規範**
   - 制定並遵循命名規範
   - 避免特殊字符
   - 使用日期前綴

3. **定期歸檔**
   - 專案完成立即歸檔
   - 資源不再使用歸檔
   - 定期清理舊歸檔

4. **自動化備份**
   - 設置自動備份
   - 遵循 3-2-1 原則
   - 定期驗證備份

5. **限制文件夾深度**
   - 避免過深的文件夾層級
   - 保持 3-4 層以內
   - 扁平化結構更易導航

### ❌ 不應該做的事

1. **避免過度分類**
   - 不要創建太多細分類別
   - 保持簡單的 PARA 結構
   - 使用標籤而非文件夾細分類

2. **不要忽視歸檔**
   - 完成的專案立即歸檔
   - 不要讓活躍區域混亂
   - 定期清理不活躍內容

3. **不要忽視備份**
   - 不要依賴單一備份
   - 定期驗證備份
   - 使用多種備份方式

4. **不要同時編輯**
   - 避免在多個設備同時編輯
   - 等待同步完成
   - 處理衝突文件

---

## 📌 常見問題 / FAQ

### Q1: 如何處理同時編輯的衝突？

**A**:
1. 等待同步完成
2. 檢查衝突文件（通常以 `conflict` 結尾）
3. 比較並合併更改
4. 保留正確版本
5. 刪除衝突文件

### Q2: 應該使用多少層文件夾？

**A**: 建議 3-4 層以內。

```
✅ 好的結構：
AI-value/
└── 2 Areas/
    └── Digital Organization/
        └── Note-Taking Workflows.md

❌ 太深的結構：
AI-value/
└── 2 Areas/
    └── Digital Organization/
        └── Workflows/
            └── Note-Taking/
                └── Daily/
                    └── Morning/
                        └── Workflow.md
```

### Q3: 如何遷移現有文件到新系統？

**A**:
1. 備份現有系統
2. 創建新的 PARA 結構
3. 批量處理文件：
   - 移動到對應的 PARA 類別
   - 重命名以符合規範
   - 建立連結
4. 定期清理舊結構
5. 驗證所有文件已遷移

### Q4: 如何處理大型附件？

**A**:
1. 評估附件的必要性
2. 壓縮大型圖片
3. 考慮外部存儲（如 Cloudinary、Imgur）
4. 使用鏈接而非嵌入
5. 定期清理未使用的附件

### Q5: 如何維護跨平台的一致性？

**A**:
1. 使用相對路徑而非絕對路徑
2. 避免平台特定的應用
3. 使用雲端同步服務
4. 定期檢查各平台的文件一致性
5. 使用跨平台工具（如 Obsidian）

---

## 🎯 下一步行動 / Next Steps

### 立即行動
- [ ] 建立或更新文件夾結構
- [ ] 制定並遵循命名規範
- [ ] 設置自動備份系統
- [ ] 配置文件同步方案

### 本週目標
- [ ] 完成所有現有文件的重新命名
- [ ] 處理並清空 InBox
- [ ] 歸檔所有完成的專案
- [ ] 測試備份和恢復

### 本月目標
- [ ] 建立穩定的文件組織系統
- [ ] 遷移所有舊文件到新系統
- [ ] 優化備份和同步策略
- [ ] 建立定期清理習慣

---

## 🔗 關連筆記 / Related Notes

- [[Digital Organization]]
- [[Note-Taking Workflows]]
- [[PARA Methodology]]
- [[Zettelkasten]]
- [[Obsidian Workflows]]
- [[Backup & Sync Strategies]]

---

**建立日期**：2026-01-20
**最後更新**：`{{date:YYYY-MM-DD}}`
**下次回顧**：`{{date+3M:YYYY-MM-DD}}`

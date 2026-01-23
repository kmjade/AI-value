# 繁體中文優先規範 / Traditional Chinese First Rule

## 概述

強制所有交流、文件、註解使用繁體中文。

Enforce that all communication, documentation, and comments use Traditional Chinese.

---

## 適用場景 / Use Cases

適用於所有任務 / Applies to all tasks:

- 用戶交流 / User communication
- 文件編寫 / Documentation writing
- 程式碼註解 / Code comments
- 變數命名說明 / Variable naming descriptions
- 日誌輸出 / Log output
- API 回應訊息 / API response messages
- 錯誤訊息 / Error messages
- UI 文字 / UI text

---

## 核心規則 / Core Rules

### 1. 絕對強制 / Absolutely Mandatory

**所有內容必須使用繁體中文**

All content must use Traditional Chinese.

✅ **正確 / Correct:**
```markdown
# 商品評論系統

本系統允許用戶對購買的商品進行評價和反饋。
```

❌ **錯誤 / Wrong:**
```markdown
# Product Comment System

This system allows users to review and provide feedback on purchased products.
```

### 2. 無例外 / No Exceptions

不允許使用英文（除非是技術術語 / Do not use English unless technical terms）

✅ **允許 / Allowed:**
- 技術術語：API, RESTful, SQL, JSON, HTTP
- 程式語言關鍵字：public, private, class, return
- 框架/庫名稱：Spring, Vue.js, React

❌ **不允許 / Not Allowed:**
- 一般描述文字 / General descriptive text
- 錯誤訊息 / Error messages
- UI 顯示文字 / UI display text
- 日誌輸出 / Log output
- 程式註解 / Code comments

### 3. 嚴格檢查 / Strict Checking

輸出前必須驗證語言 / Must verify language before outputing

```
輸出前檢查清單 / Pre-output checklist:
□ 所有用戶交流使用繁體中文？
□ 所有文件編寫使用繁體中文？
□ 所有程式註解使用繁體中文？
□ 所有錯誤訊息使用繁體中文？
□ 所有 UI 文字使用繁體中文？
```

---

## 詳細說明 / Details

### 1. 用戶交流 / User Communication

#### 規則 / Rule

所有與用戶的交流必須使用繁體中文。

All communication with users must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```
我理解您的需求，現在開始分析程式碼...
```

❌ **錯誤 / Wrong:**
```
I understand your requirements. Now I'll analyze the code...
```

✅ **正確 / Correct:**
```
請問您需要哪種類型的協助？
```

❌ **錯誤 / Wrong:**
```
What type of assistance do you need?
```

### 2. 程式註解 / Code Comments

#### 規則 / Rule

所有程式註解必須使用繁體中文。

All code comments must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```java
/**
 * 建立訂單服務
 * @param orderDTO 訂單資料傳輸物件
 * @return 建立的訂單 ID
 */
public Long createOrder(OrderDTO orderDTO) {
    // 驗證訂單資料
    if (orderDTO == null) {
        throw new IllegalArgumentException("訂單資料不能為空");
    }

    // 儲存訂單
    Order order = convertToOrder(orderDTO);
    orderMapper.insert(order);

    return order.getId();
}
```

❌ **錯誤 / Wrong:**
```java
/**
 * Create order service
 * @param orderDTO Order data transfer object
 * @return Created order ID
 */
public Long createOrder(OrderDTO orderDTO) {
    // Validate order data
    if (orderDTO == null) {
        throw new IllegalArgumentException("Order data cannot be null");
    }

    // Save order
    Order order = convertToOrder(orderDTO);
    orderMapper.insert(order);

    return order.getId();
}
```

### 3. 文件編寫 / Documentation Writing

#### 規則 / Rule

所有文件（README, API 文件, 設計文件等）必須使用繁體中文。

All documentation (README, API docs, design docs, etc.) must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```markdown
# 商品評論 API

## 介面說明

建立商品評論介面，允許用戶對購買的商品進行評價。

## 請求參數

| 參數名 | 類型 | 必填 | 說明 |
|--------|------|------|------|
| productId | Long | 是 | 商品 ID |
| content | String | 是 | 評論內容 |
```

❌ **錯誤 / Wrong:**
```markdown
# Product Comment API

## Interface Description

Create product comment interface, allowing users to review purchased products.

## Request Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| productId | Long | Yes | Product ID |
| content | String | Yes | Comment content |
```

### 4. API 回應 / API Responses

#### 規則 / Rule

所有 API 回應訊息必須使用繁體中文。

All API response messages must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```json
{
  "code": 200,
  "message": "操作成功",
  "data": {
    "id": 12345
  }
}
```

```json
{
  "code": 400,
  "message": "參數錯誤：商品 ID 不能為空"
}
```

❌ **錯誤 / Wrong:**
```json
{
  "code": 200,
  "message": "Success",
  "data": {
    "id": 12345
  }
}
```

```json
{
  "code": 400,
  "message": "Parameter error: Product ID cannot be empty"
}
```

### 5. 錯誤訊息 / Error Messages

#### 規則 / Rule

所有錯誤訊息必須使用繁體中文。

All error messages must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```java
throw new BusinessException("商品不存在");
throw new BusinessException("用戶沒有權限");
throw new BusinessException("系統忙碌，請稍後再試");
```

❌ **錯誤 / Wrong:**
```java
throw new BusinessException("Product not found");
throw new BusinessException("User has no permission");
throw new BusinessException("System busy, please try again later");
```

### 6. 日誌輸出 / Log Output

#### 規則 / Rule

所有日誌輸出必須使用繁體中文（除非是技術日誌）。

All log output must use Traditional Chinese (unless technical logs).

#### 示例 / Examples

✅ **正確 / Correct:**
```java
logger.info("開始處理訂單: {}", orderId);
logger.warn("商品庫存不足: {}", productId);
logger.error("訂單建立失敗: {}", orderDTO);
```

❌ **錯誤 / Wrong:**
```java
logger.info("Start processing order: {}", orderId);
logger.warn("Product stock insufficient: {}", productId);
logger.error("Order creation failed: {}", orderDTO);
```

**例外 / Exception:**

技術日誌可以使用英文 / Technical logs can use English:

```java
logger.debug("SQL execution time: {}ms", executionTime);
logger.trace("API request: {}", request);
```

### 7. UI 文字 / UI Text

#### 規則 / Rule

所有 UI 顯示文字必須使用繁體中文。

All UI display text must use Traditional Chinese.

#### 示例 / Examples

✅ **正確 / Correct:**
```javascript
// 按鈕
const submitButton = {
  text: "提交",
  onClick: handleSubmit
};

// 表單標籤
const formLabels = {
  username: "用戶名",
  password: "密碼",
  email: "電子郵件"
};

// 錯誤提示
const errorMessages = {
  required: "此欄位為必填",
  invalid: "格式不正確"
};
```

❌ **錯誤 / Wrong:**
```javascript
// 按鈕
const submitButton = {
  text: "Submit",
  onClick: handleSubmit
};

// 表單標籤
const formLabels = {
  username: "Username",
  password: "Password",
  email: "Email"
};

// 錯誤提示
const errorMessages = {
  required: "This field is required",
  invalid: "Invalid format"
};
```

---

## 常見錯誤 / Common Mistakes

### ❌ 錯誤 1：混合語言 / Mistake 1: Mixed Languages

```
❌ 錯誤 / Wrong:
```java
/**
 * 建立訂單 service
 * Create order service
 */
public void createOrder() {
    // ...
}
```

✅ 正確 / Correct:
```java
/**
 * 建立訂單服務
 */
public void createOrder() {
    // ...
}
```

### ❌ 錯誤 2：使用簡體字 / Mistake 2: Using Simplified Chinese

```
❌ 錯誤 / Wrong:
```markdown
# 商品评论系统
```

✅ 正確 / Correct:
```markdown
# 商品評論系統
```

### ❌ 錯誤 3：技術術語也翻譯 / Mistake 3: Translating Technical Terms

```
❌ 錯誤 / Wrong:
```java
// 發送超文字傳輸協定請求
sendHttpRequest();
```

✅ 正確 / Correct:
```java
// 發送 HTTP 請求
sendHttpRequest();
```

### ❌ 錯誤 4：註解不完整 / Mistake 4: Incomplete Comments

```
❌ 錯誤 / Wrong:
```java
// 查詢
List<Product> list = productMapper.selectAll();
```

✅ 正確 / Correct:
```java
// 查詢所有商品資訊
List<Product> list = productMapper.selectAll();
```

---

## 技術術語指南 / Technical Term Guidelines

### 允許的英文術語 / Allowed English Terms

以下技術術語可以使用英文 / The following technical terms can use English:

| 分類 / Category | 術語 / Terms | 示例 / Examples |
|--------------|----------------|-----------------|
| **程式語言關鍵字** / Programming Keywords | public, private, class, interface, return, void | `public class User {}` |
| **API 相關** / API Related | API, RESTful, JSON, XML, HTTP, GET, POST | `@GetMapping` |
| **資料庫相關** / Database Related | SQL, Table, Index, Primary Key | `CREATE TABLE` |
| **框架相關** / Framework Related | Spring, Vue, React, Express | `@Service` |
| **協議相關** / Protocol Related | HTTP, HTTPS, TCP, UDP | `https://` |
| **資料格式** / Data Format | JSON, XML, YAML, CSV | `application/json` |
| **工具相關** / Tool Related | Git, Maven, NPM, Docker | `git commit` |

### 需要翻譯的術語 / Terms to Translate

以下術語必須翻譯為繁體中文 / The following terms must be translated to Traditional Chinese:

| 英文 / English | 繁體中文 / Traditional Chinese |
|--------------|---------------------------|
| **user** | 用戶 |
| **customer** | 客戶 |
| **product** | 商品 |
| **order** | 訂單 |
| **comment** | 評論 |
| **review** | 審查 |
| **submit** | 提交 |
| **cancel** | 取消 |
| **save** | 儲存 |
| **delete** | 刪除 |
| **edit** | 編輯 |
| **update** | 更新 |
| **create** | 建立 |
| **search** | 搜尋 |
| **filter** | 篩選 |

---

## 與其他 Skills 的關係 / Relationship with Other Skills

這個 Skill 是所有任務的基礎，應該始終加載 / This Skill is the foundation for all tasks, should always be loaded:

- 所有任務都需要遵循此 Skill / All tasks need to follow this Skill
- 與其他 Skills 配合使用時，優先級最高 / When used with other Skills, this has the highest priority
- 其他 Skills 產生的輸出也必須遵循此規範 / Output from other Skills must also follow this rule

**配合使用 / Used with:**

- [[obsidian-syntax/SKILL.md|Obsidian 語法]] - 編寫 Obsidian 文件時
- [[markdown-standards/SKILL.md|Markdown 標準]] - 編寫 Markdown 文件時
- [[claude-commands/SKILL.md|Claude 指令]] - 使用 Claude 指令時

---

## 輸出驗證清單 / Output Verification Checklist

在產生任何輸出前，必須檢查以下項目 / Before generating any output, must check the following items:

```
□ 用戶交流使用繁體中文？
   └─ 所有對話文字都是繁體中文

□ 文件內容使用繁體中文？
   └─ 所有文件、註解、說明都是繁體中文

□ 程式註解使用繁體中文？
   └─ 所有程式註解都是繁體中文

□ 錯誤訊息使用繁體中文？
   └─ 所有錯誤提示都是繁體中文

□ UI 文字使用繁體中文？
   └─ 所有介面顯示文字都是繁體中文

□ API 回應訊息使用繁體中文？
   └─ 所有 API 回應都是繁體中文

□ 日誌輸出使用繁體中文？
   └─ 所有日誌訊息都是繁體中文（技術日誌除外）

□ 沒有簡體中文字元？
   └─ 檢查並轉換為繁體中文
```

---

## 繁簡轉換工具 / Traditional-Simplified Conversion Tools

如果在簡體中文和繁體中文之間轉換時，請使用可靠的工具 / When converting between Simplified and Traditional Chinese, please use reliable tools:

### 推薦工具 / Recommended Tools

1. **OpenCC**
   - 網址：https://github.com/BYVoid/OpenCC
   - 支援：簡繁轉換
   - 準確度：高

2. **zhconv**
   - Python 庫：https://github.com/skywind3000/ZhConv
   - 支援：簡繁轉換
   - 準確度：高

3. **線上工具**
   - https://www.zhconvert.com/
   - https://www.aivtp.com/convert

### 注意事項 / Notes

- ⚠️ 工具可能不完美，需要人工檢查 / Tools may not be perfect, need manual check
- ⚠️ 特定詞彙需要調整 / Specific terms may need adjustment
- ⚠️ 技術術語保持英文 / Keep technical terms in English

---

## 參考資源 / Reference Resources

### 相關 Skills / Related Skills

- [[chinese-first-rule/SKILL.md|簡體中文優先規範]] - 簡體中文版本
- [[obsidian-syntax/SKILL.md|Obsidian 語法]] - 編寫 Obsidian 文件
- [[markdown-standards/SKILL.md|Markdown 標準]] - 文件命名和規範

### 繁體中文資源 / Traditional Chinese Resources

- [繁體中文轉換工具](https://www.zhconvert.com/)
- [繁體中文資料庫](https://github.com/BYVoid/OpenCC)
- [繁體中文檢查工具](https://github.com/skywind3000/ZhConv)

---

## 快速測試 / Quick Test

### 測試 1：基本輸出 / Test 1: Basic Output

**指令 / Prompt:**
```
用繁體中文寫一個簡單的問候語。
```

**預期輸出 / Expected Output:**
```
您好！歡迎使用本系統。
```

### 測試 2：程式註解 / Test 2: Code Comments

**指令 / Prompt:**
```
用繁體中文為以下程式碼添加註解：

public class User {
    private String name;
    private String email;
}
```

**預期輸出 / Expected Output:**
```java
/**
 * 用戶類別
 */
public class User {
    /**
     * 用戶名稱
     */
    private String name;

    /**
     * 電子郵件
     */
    private String email;
}
```

### 測試 3：API 文件 / Test 3: API Documentation

**指令 / Prompt:**
```
用繁體中文編寫一個用戶登入 API 的文件。
```

**預期輸出 / Expected Output:**
```markdown
# 用戶登入 API

## 介面說明

用戶透過使用者名稱和密碼登入系統。

## 請求參數

| 參數名 | 類型 | 必填 | 說明 |
|--------|------|------|------|
| username | String | 是 | 用戶名稱 |
| password | String | 是 | 密碼 |

## 回應範例

```json
{
  "code": 200,
  "message": "登入成功",
  "data": {
    "token": "xxx"
  }
}
```
```

---

> [!info] 注意 / Note
>
> 這個 Skill 適用於需要強制使用繁體中文的專案。
> This Skill is suitable for projects that require mandatory use of Traditional Chinese.
>
> 如果需要使用簡體中文，請使用 [[chinese-first-rule/SKILL.md|簡體中文優先規範]]。
> If you need to use Simplified Chinese, please use [[chinese-first-rule/SKILL.md]].

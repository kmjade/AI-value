# English First Rule

## Overview

Enforce that all communication, documentation, and comments use English.

强制所有交流、文档、注释使用英文。

---

## Use Cases / 适用场景

Applies to all tasks / 适用于所有任务:

- User communication / 用户交流
- Documentation writing / 文档编写
- Code comments / 代码注释
- Variable naming descriptions / 变量命名说明
- Log output / 日志输出
- API response messages / API 响应消息
- UI text / UI 文字
- Error messages / 错误消息

---

## Core Rules / 核心规则

### 1. Absolutely Mandatory / 绝对强制

**All content must use English**

所有内容必须使用英文。

✅ **Correct / 正确:**
```markdown
# Product Comment System

This system allows users to review and provide feedback on purchased products.
```

❌ **Wrong / 错误:**
```markdown
# 商品评论系统

本系统允许用户对购买的商品进行评价和反馈。
```

### 2. No Exceptions / 无例外

English should be used for all content (except technical terms in other languages)

不允許使用其他语言（除非是其他語言的技術術語）

✅ **Allowed / 允許:**
- Technical terms in other languages: API, RESTful, SQL, JSON
- Programming language keywords: public, private, class, return
- Framework/library names: Spring, Vue.js, React

❌ **Not Allowed / 不允許:**
- General descriptive text in other languages: 一般描述文字
- Error messages in other languages: 錯誤訊息
- UI display text in other languages: UI 顯示文字
- Log output in other languages: 日誌輸出
- Code comments in other languages: 程式註解

### 3. Strict Checking / 严格检查

Verify language before outputing / 输出前必须验证语言

```
Output verification checklist / 输出前检查清单:
□ Is all user communication in English? / 所有用户交流使用英文？
□ Is all documentation writing in English? / 所有文档编写使用英文？
□ Is all code comments in English? / 所有代码注释使用英文？
□ Is all error messages in English? / 所有错误消息使用英文？
□ Is all UI text in English? / 所有 UI 文字使用英文？
□ Is all API response messages in English? / 所有 API 响应使用英文？
□ Is all log output in English? / 所有日志输出使用英文？
```

---

## Details / 详细说明

### 1. User Communication / 用户交流

#### Rule / 规则

All communication with users must be in English.

所有与用户的交流必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
```
I understand your requirements. Now I'll analyze the code...
```

❌ **Wrong / 错误:**
```
我理解您的需求，现在开始分析代码...
```

✅ **Correct / 正确:**
```
What type of assistance do you need?
```

❌ **Wrong / 错误:**
```
请问您需要哪种类型的帮助？
```

### 2. Code Comments / 代码注释

#### Rule / 规则

All code comments must be in English.

所有代码注释必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
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

❌ **Wrong / 错误:**
```java
/**
 * 建立订单服务
 * @param orderDTO 订单数据传输对象
 * @return 建立的订单 ID
 */
public Long createOrder(OrderDTO orderDTO) {
    // 验证订单数据
    if (orderDTO == null) {
        throw new IllegalArgumentException("订单数据不能为空");
    }

    // 保存订单
    Order order = convertToOrder(orderDTO);
    orderMapper.insert(order);

    return order.getId();
}
```

### 3. Documentation Writing / 文档编写

#### Rule / 规则

All documentation (README, API docs, design docs, etc.) must be in English.

所有文档（README, API 文档, 设计文档等）必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
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

❌ **Wrong / 错误:**
```markdown
# 商品评论 API

## 接口说明

创建商品评论接口，允许用户对购买的商品进行评价。

## 请求参数

| 参数名 | 类型 | 必填 | 说明 |
|--------|------|------|------|
| productId | Long | 是 | 商品 ID |
| content | String | 是 | 评论内容 |
```

### 4. API Responses / API 响应

#### Rule / 规则

All API response messages must be in English.

所有 API 响应消息必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
```json
{
  "code": 200,
  "message": "Operation successful",
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

❌ **Wrong / 错误:**
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
  "message": "参数错误：商品 ID 不能为空"
}
```

### 5. Error Messages / 错误消息

#### Rule / 规则

All error messages must be in English.

所有错误消息必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
```java
throw new BusinessException("Product not found");
throw new BusinessException("User has no permission");
throw new BusinessException("System busy, please try again later");
```

❌ **Wrong / 错误:**
```java
throw new BusinessException("商品不存在");
throw new BusinessException("用户没有权限");
throw new BusinessException("系统繁忙，请稍后再试");
```

### 6. Log Output / 日志输出

#### Rule / 规则

All log output must be in English (unless technical logs).

所有日志输出必须使用英文（除非是技术日志）。

#### Examples / 示例

✅ **Correct / 正确:**
```java
logger.info("Start processing order: {}", orderId);
logger.warn("Product stock insufficient: {}", productId);
logger.error("Order creation failed: {}", orderDTO);
```

❌ **Wrong / 错误:**
```java
logger.info("开始处理订单: {}", orderId);
logger.warn("商品库存不足: {}", productId);
logger.error("订单创建失败: {}", orderDTO);
```

**Exception / 例外:**

Technical logs can use other languages as needed / 技术日志可以根据需要使用其他语言:

```java
logger.debug("SQL execution time: {}ms", executionTime);
logger.trace("API request: {}", request);
```

### 7. UI Text / UI 文字

#### Rule / 规则

All UI display text must be in English.

所有 UI 显示文字必须使用英文。

#### Examples / 示例

✅ **Correct / 正确:**
```javascript
// Button
const submitButton = {
  text: "Submit",
  onClick: handleSubmit
};

// Form labels
const formLabels = {
  username: "Username",
  password: "Password",
  email: "Email"
};

// Error messages
const errorMessages = {
  required: "This field is required",
  invalid: "Invalid format"
};
```

❌ **Wrong / 错误:**
```javascript
// Button
const submitButton = {
  text: "提交",
  onClick: handleSubmit
};

// Form labels
const formLabels = {
  username: "用户名",
  password: "密码",
  email: "电子邮箱"
};

// Error messages
const errorMessages = {
  required: "此字段为必填",
  invalid: "格式不正确"
};
```

---

## Common Mistakes / 常见错误

### ❌ Mistake 1: Mixed Languages / 错误 1：混合语言

```
❌ Wrong / 错误:
```java
/**
 * Create order service
 * 创建订单服务
 */
public void createOrder() {
    // ...
}
```

✅ Correct / 正确:
```java
/**
 * Create order service
 */
public void createOrder() {
    // ...
}
```

### ❌ Mistake 2: Using Other Languages / 错误 2：使用其他语言

```
❌ Wrong / 错误:
```markdown
# 商品评论系统
```

✅ Correct / 正确:
```markdown
# Product Comment System
```

### ❌ Mistake 3: Translating Technical Terms / 错误 3：翻译技术术语

```
❌ Wrong / 错误:
```java
// 发送超文本传输协议请求
sendHttpRequest();
```

✅ Correct / 正确:
```java
// Send HTTP request
sendHttpRequest();
```

### ❌ Mistake 4: Incomplete Comments / 错误 4：注释不完整

```
❌ Wrong / 错误:
```java
// Query
List<Product> list = productMapper.selectAll();
```

✅ Correct / 正确:
```java
// Query all product information
List<Product> list = productMapper.selectAll();
```

---

## Technical Term Guidelines / 技术术语指南

### Allowed English Terms / 允许的英文术语

The following technical terms can use English / 以下技术术语可以使用英文:

| Category / 分类 | Terms / 术语 | Examples / 示例 |
|--------------|----------------|-----------------|
| **Programming Keywords** / 编程语言关键字 | public, private, class, interface, return, void | `public class User {}` |
| **API Related** / API 相关 | API, RESTful, JSON, XML, HTTP, GET, POST | `@GetMapping` |
| **Database Related** / 数据库相关 | SQL, Table, Index, Primary Key | `CREATE TABLE` |
| **Framework Related** / 框架相关 | Spring, Vue, React, Express | `@Service` |
| **Protocol Related** / 协议相关 | HTTP, HTTPS, TCP, UDP | `https://` |
| **Data Format** / 数据格式 | JSON, XML, YAML, CSV | `application/json` |
| **Tool Related** / 工具相关 | Git, Maven, NPM, Docker | `git commit` |

### Terms in Other Languages / 其他语言的术语

The following terms in other languages must be translated to English / 以下其他语言的术语必须翻译为英文:

| Chinese / 中文 | English / 英文 |
|--------------|------------------|
| **用户** | User |
| **客户** | Customer |
| **商品** | Product |
| **订单** | Order |
| **评论** | Comment |
| **审查** | Review |
| **提交** | Submit |
| **取消** | Cancel |
| **保存** | Save |
| **删除** | Delete |
| **编辑** | Edit |
| **更新** | Update |
| **创建** | Create |
| **搜索** | Search |
| **筛选** | Filter |

---

## Relationship with Other Skills / 与其他 Skills 的关系

This Skill is the foundation for all tasks, should always be loaded / 这个 Skill 是所有任务的基础，应该始终加载:

- All tasks need to follow this Skill / 所有任务都需要遵循此 Skill
- When used with other Skills, this has the highest priority / 与其他 Skills 配合使用时，优先级最高
- Output from other Skills must also follow this rule / 其他 Skills 产生的输出也必须遵循此规则

**Used with / 配合使用:**

- [[obsidian-syntax/SKILL.md|Obsidian Syntax]] - When editing Obsidian files / 编写 Obsidian 文件时
- [[markdown-standards/SKILL.md|Markdown Standards]] - When writing Markdown files / 编写 Markdown 文件时
- [[claude-commands/SKILL.md|Claude Commands]] - When using Claude Code commands / 使用 Claude Code 指令时

---

## Output Verification Checklist / 输出验证清单

Before generating any output, must check the following items / 在产生任何输出前，必须检查以下项目:

```
□ Is all user communication in English? / 所有用户交流使用英文？
   └─ All conversation text is English / 所有对话文字都是英文

□ Is all documentation content in English? / 所有文档内容使用英文？
   └─ All documentation, comments, descriptions are English / 所有文档、注释、说明都是英文

□ Is all code comments in English? / 所有代码注释使用英文？
   └─ All code comments are English / 所有代码注释都是英文

□ Is all error messages in English? / 所有错误消息使用英文？
   └─ All error prompts are English / 所有错误提示都是英文

□ Is all UI text in English? / 所有 UI 文字使用英文？
   └─ All interface display text is English / 所有界面显示文字都是英文

□ Is all API response messages in English? / 所有 API 响应消息使用英文？
   └─ All API responses are English / 所有 API 响应都是英文

□ Is all log output in English? / 所有日志输出使用英文？
   └─ All log messages are English (except technical logs) / 所有日志消息都是英文（技术日志除外）

□ No characters from other languages? / 没有其他语言的字符？
   └─ Check and convert non-English characters to English / 检查并转换非英文字符为英文
```

---

## Translation Tools / 翻译工具

When translating between English and other languages, please use reliable tools / 在英文和其他语言之间转换时，请使用可靠的工具:

### Recommended Tools / 推荐工具

1. **Google Translate**
   - URL: https://translate.google.com/
   - Supports: Multi-language translation
   - Accuracy: High / 准确度：高

2. **DeepL**
   - URL: https://www.deepl.com/translator
   - Supports: Multi-language translation
   - Accuracy: High / 准确度：高

3. **Online Tools**
   - https://www.onlinetranslation.com/
   - https://www.systran.net/

### Notes / 注意事项

- ⚠️ Tools may not be perfect, need manual check / 工具可能不完美，需要人工检查
- ⚠️ Specific terms may need adjustment / 特定词汇可能需要调整
- ⚠️ Keep technical terms in their original language / 保持技术术语使用原始语言

---

## Reference Resources / 参考资源

### Related Skills / 相关 Skills

- [[simplified-chinese-first/SKILL.md|Simplified Chinese First Rule]] - 简体中文版本 / Simplified Chinese version
- [[traditional-chinese-first/SKILL.md|Traditional Chinese First Rule]] - 繁体中文版本 / Traditional Chinese version
- [[obsidian-syntax/SKILL.md|Obsidian Syntax]] - 编辑 Obsidian 文件 / Editing Obsidian files
- [[markdown-standards/SKILL.md|Markdown Standards]] - 文件命名和规范 / File naming and standards

### English Resources / 英文资源

- [Translation Tools](https://www.onlinetranslation.com/)
- [English Grammar Check](https://www.grammarly.com/)
- [English Dictionary](https://www.merriam-webster.com/)

---

## Quick Test / 快速测试

### Test 1: Basic Output / 测试 1：基本输出

**Prompt / 指令:**
```
Write a simple greeting in English.
```

**Expected Output / 预期输出:**
```
Hello! Welcome to our system.
```

### Test 2: Code Comments / 测试 2：代码注释

**Prompt / 指令:**
```
Add English comments to the following code:

public class User {
    private String name;
    private String email;
}
```

**Expected Output / 预期输出:**
```java
/**
 * User class
 */
public class User {
    /**
     * User name
     */
    private String name;

    /**
     * Email address
     */
    private String email;
}
```

### Test 3: API Documentation / 测试 3：API 文档

**Prompt / 指令:**
```
Write API documentation in English for a user login API.
```

**Expected Output / 预期输出:**
```markdown
# User Login API

## Interface Description

User logs into the system using username and password.

## Request Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| username | String | Yes | User name |
| password | String | Yes | Password |

## Response Example

```json
{
  "code": 200,
  "message": "Login successful",
  "data": {
    "token": "xxx"
  }
}
```
```

---

> [!info] Note / 注意 / Note
>
> This Skill applies to projects that require mandatory use of English.
> 这个 Skill 适用于需要强制使用英文的项目。
>
> If you need to use Simplified Chinese, please use [[simplified-chinese-first/SKILL.md|Simplified Chinese First Rule]].
> 如果需要使用简体中文，请使用简体中文优先规范。
>
> If you need to use Traditional Chinese, please use [[traditional-chinese-first/SKILL.md|Traditional Chinese First Rule]].
> 如果需要使用繁体中文，请使用繁体中文优先规范。

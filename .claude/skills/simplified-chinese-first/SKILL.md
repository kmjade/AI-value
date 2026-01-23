# 简体中文优先规范 / Simplified Chinese First Rule

## 概述

强制所有交流、文档、注释使用简体中文。

Enforce that all communication, documentation, and comments use Simplified Chinese.

---

## 适用场景 / Use Cases

适用于所有任务 / Applies to all tasks:

- 用户交流 / User communication
- 文档编写 / Documentation writing
- 代码注释 / Code comments
- 变量命名说明 / Variable naming descriptions
- 日志输出 / Log output
- API 响应消息 / API response messages
- UI 文字 / UI text
- 错误消息 / Error messages

---

## 核心规则 / Core Rules

### 1. 绝对强制 / Absolutely Mandatory

**所有内容必须使用简体中文**

All content must use Simplified Chinese.

✅ **正确 / Correct:**
```markdown
# 商品评论系统

本系统允许用户对购买的商品进行评价和反馈。
```

❌ **错误 / Wrong:**
```markdown
# Product Comment System

This system allows users to review and provide feedback on purchased products.
```

### 2. 无例外 / No Exceptions

不允许使用英文（除非是技术术语） / Do not use English unless technical terms

✅ **允许 / Allowed:**
- 技术术语：API, RESTful, SQL, JSON, HTTP
- 编程语言关键字：public, private, class, return
- 框架/库名称：Spring, Vue.js, React

❌ **不允许 / Not Allowed:**
- 一般描述文字 / General descriptive text
- 错误消息 / Error messages
- UI 显示文字 / UI display text
- 日志输出 / Log output
- 代码注释 / Code comments

### 3. 严格检查 / Strict Checking

输出前必须验证语言 / Must verify language before outputing

```
输出前检查清单 / Pre-output checklist:
□ 所有用户交流使用简体中文？
□ 所有文档编写使用简体中文？
□ 所有代码注释使用简体中文？
□ 所有错误消息使用简体中文？
□ 所有 UI 文字使用简体中文？
□ 所有 API 响应使用简体中文？
□ 所有日志输出使用简体中文？
□ 没有繁体中文字符？
```

---

## 详细说明 / Details

### 1. 用户交流 / User Communication

#### 规则 / Rule

所有与用户的交流必须使用简体中文。

All communication with users must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
```
我理解您的需求，现在开始分析代码...
```

❌ **错误 / Wrong:**
```
I understand your requirements. Now I'll analyze the code...
```

✅ **正确 / Correct:**
```
请问您需要哪种类型的帮助？
```

❌ **错误 / Wrong:**
```
What type of assistance do you need?
```

### 2. 代码注释 / Code Comments

#### 规则 / Rule

所有代码注释必须使用简体中文。

All code comments must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
```java
/**
 * 创建订单服务
 * @param orderDTO 订单数据传输对象
 * @return 创建的订单ID
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

❌ **错误 / Wrong:**
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

### 3. 文档编写 / Documentation Writing

#### 规则 / Rule

所有文档（README, API 文档, 设计文档等）必须使用简体中文。

All documentation (README, API docs, design docs, etc.) must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
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

❌ **错误 / Wrong:**
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

### 4. API 响应 / API Responses

#### 规则 / Rule

所有 API 响应消息必须使用简体中文。

All API response messages must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
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

❌ **错误 / Wrong:**
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

### 5. 错误消息 / Error Messages

#### 规则 / Rule

所有错误消息必须使用简体中文。

All error messages must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
```java
throw new BusinessException("商品不存在");
throw new BusinessException("用户没有权限");
throw new BusinessException("系统繁忙，请稍后再试");
```

❌ **错误 / Wrong:**
```java
throw new BusinessException("Product not found");
throw new BusinessException("User has no permission");
throw new BusinessException("System busy, please try again later");
```

### 6. 日志输出 / Log Output

#### 规则 / Rule

所有日志输出必须使用简体中文（除非是技术日志）。

All log output must use Simplified Chinese (unless technical logs).

#### 示例 / Examples

✅ **正确 / Correct:**
```java
logger.info("开始处理订单: {}", orderId);
logger.warn("商品库存不足: {}", productId);
logger.error("订单创建失败: {}", orderDTO);
```

❌ **错误 / Wrong:**
```java
logger.info("Start processing order: {}", orderId);
logger.warn("Product stock insufficient: {}", productId);
logger.error("Order creation failed: {}", orderDTO);
```

**例外 / Exception:**

技术日志可以使用英文 / Technical logs can use English:

```java
logger.debug("SQL execution time: {}ms", executionTime);
logger.trace("API request: {}", request);
```

### 7. UI 文字 / UI Text

#### 规则 / Rule

所有 UI 显示文字必须使用简体中文。

All UI display text must use Simplified Chinese.

#### 示例 / Examples

✅ **正确 / Correct:**
```javascript
// 按钮
const submitButton = {
  text: "提交",
  onClick: handleSubmit
};

// 表单标签
const formLabels = {
  username: "用户名",
  password: "密码",
  email: "电子邮箱"
};

// 错误提示
const errorMessages = {
  required: "此字段为必填",
  invalid: "格式不正确"
};
```

❌ **错误 / Wrong:**
```javascript
// 按钮
const submitButton = {
  text: "Submit",
  onClick: handleSubmit
};

// 表单标签
const formLabels = {
  username: "Username",
  password: "Password",
  email: "Email"
};

// 错误提示
const errorMessages = {
  required: "This field is required",
  invalid: "Invalid format"
};
```

---

## 常见错误 / Common Mistakes

### ❌ 错误 1：混合语言 / Mistake 1: Mixed Languages

```
❌ 错误 / Wrong:
```java
/**
 * 创建订单 service
 * Create order service
 */
public void createOrder() {
    // ...
}
```

✅ 正确 / Correct:
```java
/**
 * 创建订单服务
 */
public void createOrder() {
    // ...
}
```

### ❌ 错误 2：使用繁体字 / Mistake 2: Using Traditional Chinese

```
❌ 错误 / Wrong:
```markdown
# 商品評論系統
```

✅ 正确 / Correct:
```markdown
# 商品评论系统
```

### ❌ 错误 3：技术术语也翻译 / Mistake 3: Translating Technical Terms

```
❌ 错误 / Wrong:
```java
// 发送超文本传输协议请求
sendHttpRequest();
```

✅ 正确 / Correct:
```java
// 发送 HTTP 请求
sendHttpRequest();
```

### ❌ 错误 4：注释不完整 / Mistake 4: Incomplete Comments

```
❌ 错误 / Wrong:
```java
// 查询
List<Product> list = productMapper.selectAll();
```

✅ 正确 / Correct:
```java
// 查询所有商品信息
List<Product> list = productMapper.selectAll();
```

---

## 技术术语指南 / Technical Term Guidelines

### 允许的英文术语 / Allowed English Terms

以下技术术语可以使用英文 / The following technical terms can use English:

| 分类 / Category | 术语 / Terms | 示例 / Examples |
|--------------|---------------|------------------|
| **编程语言关键字** / Programming Keywords | public, private, class, interface, return, void | `public class User {}` |
| **API 相关** / API Related | API, RESTful, JSON, XML, HTTP, GET, POST | `@GetMapping` |
| **数据库相关** / Database Related | SQL, Table, Index, Primary Key | `CREATE TABLE` |
| **框架相关** / Framework Related | Spring, Vue, React, Express | `@Service` |
| **协议相关** / Protocol Related | HTTP, HTTPS, TCP, UDP | `https://` |
| **数据格式** / Data Format | JSON, XML, YAML, CSV | `application/json` |
| **工具相关** / Tool Related | Git, Maven, NPM, Docker | `git commit` |

### 需要翻译的术语 / Terms to Translate

以下术语必须翻译为简体中文 / The following terms must be translated to Simplified Chinese:

| 英文 / English | 简体中文 / Simplified Chinese |
|--------------|---------------------------------|
| **user** | 用户 |
| **customer** | 客户 |
| **product** | 商品 |
| **order** | 订单 |
| **comment** | 评论 |
| **review** | 评论 |
| **submit** | 提交 |
| **cancel** | 取消 |
| **save** | 保存 |
| **delete** | 删除 |
| **edit** | 编辑 |
| **update** | 更新 |
| **create** | 创建 |
| **search** | 搜索 |
| **filter** | 筛选 |

---

## 与其他 Skills 的关系 / Relationship with Other Skills

这个 Skill 是所有任务的基础，应该始终加载 / This Skill is the foundation for all tasks, should always be loaded:

- 所有任务都需要遵循此 Skill / All tasks need to follow this Skill
- 与其他 Skills 配合使用时，优先级最高 / When used with other Skills, this has the highest priority
- 其他 Skills 产生的输出也必须遵循此规则 / Output from other Skills must also follow this rule

**配合使用 / Used with:**

- [[obsidian-syntax/SKILL.md|Obsidian 语法]] - 编写 Obsidian 文件时
- [[markdown-standards/SKILL.md|Markdown 标准]] - 编写 Markdown 文件时
- [[claude-commands/SKILL.md|Claude 命令]] - 使用 Claude 命令时

---

## 输出验证清单 / Output Verification Checklist

在产生任何输出前，必须检查以下项目 / Before generating any output, must check the following items:

```
□ 用户交流使用简体中文？
   └─ 所有对话文字都是简体中文

□ 文档内容使用简体中文？
   └─ 所有文档、注释、说明都是简体中文

□ 代码注释使用简体中文？
   └─ 所有代码注释都是简体中文

□ 错误消息使用简体中文？
   └─ 所有错误提示都是简体中文

□ UI 文字使用简体中文？
   └─ 所有界面显示文字都是简体中文

□ API 响应消息使用简体中文？
   └─ 所有 API 响应都是简体中文

□ 日志输出使用简体中文？
   └─ 所有日志消息都是简体中文（技术日志除外）

□ 没有繁体中文字符？
   └─ 检查并转换为简体中文
```

---

## 繁简转换工具 / Simplified-Traditional Conversion Tools

如果在简体中文和繁体中文之间转换时，请使用可靠的工具 / When converting between Simplified and Traditional Chinese, please use reliable tools:

### 推荐工具 / Recommended Tools

1. **OpenCC**
   - 网址：https://github.com/BYVoid/OpenCC
   - 支持：简繁转换
   - 准确度：高

2. **zhconv**
   - Python 库：https://github.com/skywind3000/zhConv
   - 支持：简繁转换
   - 准确度：高

3. **在线工具**
   - https://www.zhconvert.com/
   - https://www.aivtp.com/convert

### 注意事项 / Notes

- ⚠️ 工具可能不完美，需要人工检查 / Tools may not be perfect, need manual check
- ⚠️ 特定词汇需要调整 / Specific words may need adjustment
- ⚠️ 技术术语保持英文 / Keep technical terms in English

---

## 参考资源 / Reference Resources

### 相关 Skills / Related Skills

- [[traditional-chinese-first/SKILL.md|繁体中文优先规范]] - 繁体中文版本 / Traditional Chinese version
- [[obsidian-syntax/SKILL.md|Obsidian 语法]] - 编写 Obsidian 文件 / Writing Obsidian files
- [[markdown-standards/SKILL.md|Markdown 标准]] - 文件命名和规范 / File naming and standards

### 简体中文资源 / Simplified Chinese Resources

- [简体中文转换工具](https://www.zhconvert.com/)
- [简体中文数据库](https://github.com/BYVoid/OpenCC)
- [简体中文检查工具](https://github.com/skywind3000/zhConv)

---

## 快速测试 / Quick Test

### 测试 1：基本输出 / Test 1: Basic Output

**指令 / Prompt:**
```
用简体中文写一个简单的问候语。
```

**预期输出 / Expected Output:**
```
您好！欢迎使用本系统。
```

### 测试 2：代码注释 / Test 2: Code Comments

**指令 / Prompt:**
```
用简体中文为以下代码添加注释：

public class User {
    private String name;
    private String email;
}
```

**预期输出 / Expected Output:**
```java
/**
 * 用户类别
 */
public class User {
    /**
     * 用户名称
     */
    private String name;

    /**
     * 电子邮箱
     */
    private String email;
}
```

### 测试 3：API 文档 / Test 3: API Documentation

**指令 / Prompt:**
```
用简体中文编写一个用户登录 API 的文档。
```

**预期输出 / Expected Output:**
```markdown
# 用户登录 API

## 接口说明

用户通过用户名和密码登录系统。

## 请求参数

| 参数名 | 类型 | 必填 | 说明 |
|--------|------|------|------|
| username | String | 是 | 用户名 |
| password | String | 是 | 密码 |

## 响应示例

```json
{
  "code": 200,
  "message": "登录成功",
  "data": {
    "token": "xxx"
  }
}
```
```

---

> [!info] 注意 / Note
>
> 这个 Skill 适用于需要强制使用简体中文的项目。
> This Skill is suitable for projects that require mandatory use of Simplified Chinese.
>
> 如果需要使用繁体中文，请使用 [[traditional-chinese-first/SKILL.md|繁体中文优先规范]]。
> If you need to use Traditional Chinese, please use [[traditional-chinese-first/SKILL.md]].

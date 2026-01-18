# AGENTS.md

This file provides guidance for agentic coding agents working in the AI-value repository.

## Project Status

**AI-value** is in early planning phase. Technology stack not yet determined. Currently configured as Java module in IntelliJ IDEA, but this may change.

---

## ENGLISH SECTION

### Build/Lint/Test Commands

**Note:** Commands are placeholders. Update when technology stack is finalized.

```bash
# Build commands (examples for different stacks)
# npm run build          # Node.js/JavaScript
# mvn compile            # Java/Maven
# cargo build            # Rust
# python -m build        # Python

# Lint commands
# npm run lint           # JavaScript/TypeScript
# mvn checkstyle:check   # Java
# cargo clippy           # Rust
# ruff check .           # Python

# Test commands
# npm test               # JavaScript
# mvn test               # Java
# cargo test             # Rust
# pytest -v             # Python

# Single test commands
# npm test -- --testNamePattern="specific_test"
# mvn test -Dtest=SpecificTest
# cargo test specific_test
# pytest tests/test_specific.py -v
```

### Code Style Guidelines

#### General Principles
- Write clean, readable, maintainable code
- Follow language-specific conventions
- Use meaningful variable and function names
- Keep functions small and focused
- Add comments for complex logic

#### Import Organization
- Group imports: standard library → third-party → local
- Remove unused imports
- Use explicit imports over wildcard imports
- Sort imports alphabetically within groups

#### Formatting
- Use consistent indentation (2 spaces for JS/TS, 4 for Python, tabs for Java)
- Add trailing commas in multi-line structures
- Use semicolons where required by language
- Keep lines under 100 characters

#### Type Safety
- Use strong typing when available
- Add type annotations for clarity
- Avoid `any`/`Object` types when possible
- Use interfaces for complex object shapes

#### Naming Conventions
- **Variables:** camelCase (JS/TS), snake_case (Python), camelCase (Java)
- **Functions:** camelCase (JS/TS), snake_case (Python), camelCase (Java)
- **Classes:** PascalCase (JS/TS/Java), PascalCase (Python)
- **Constants:** UPPER_SNAKE_CASE (all languages)
- **Files:** kebab-case (JS/TS), snake_case (Python), PascalCase (Java)

#### Error Handling
- Use try-catch blocks appropriately
- Provide meaningful error messages
- Log errors with context
- Fail fast and explicitly
- Use language-specific error types

#### Testing
- Write unit tests for core functionality
- Use descriptive test names
- Follow AAA pattern (Arrange, Act, Assert)
- Mock external dependencies
- Test both success and failure cases

---

## 简体中文部分 (Simplified Chinese)

### 构建/检查/测试命令

**注意:** 以下命令为占位符。技术栈确定后请更新。

```bash
# 构建命令 (不同技术栈示例)
# npm run build          # Node.js/JavaScript
# mvn compile            # Java/Maven
# cargo build            # Rust
# python -m build        # Python

# 代码检查命令
# npm run lint           # JavaScript/TypeScript
# mvn checkstyle:check   # Java
# cargo clippy           # Rust
# ruff check .           # Python

# 测试命令
# npm test               # JavaScript
# mvn test               # Java
# cargo test             # Rust
# pytest -v             # Python

# 单个测试命令
# npm test -- --testNamePattern="specific_test"
# mvn test -Dtest=SpecificTest
# cargo test specific_test
# pytest tests/test_specific.py -v
```

### 代码风格指南

#### 通用原则
- 编写干净、可读、可维护的代码
- 遵循语言特定约定
- 使用有意义的变量和函数名
- 保持函数小而专注
- 为复杂逻辑添加注释

#### 导入组织
- 分组导入：标准库 → 第三方 → 本地
- 移除未使用的导入
- 使用显式导入而非通配符导入
- 组内按字母顺序排序

#### 格式化
- 使用一致的缩进（JS/TS 2个空格，Python 4个空格，Java制表符）
- 在多行结构中添加尾随逗号
- 在语言要求时使用分号
- 保持行长度在100字符以内

#### 类型安全
- 在可用时使用强类型
- 为清晰性添加类型注解
- 尽可能避免 `any`/`Object` 类型
- 对复杂对象形状使用接口

---

## 繁體中文部分 (Traditional Chinese)

### 建置/檢查/測試指令

**注意:** 以下指令為佔位符。技術堆疊確定後請更新。

```bash
# 建置指令 (不同技術堆疊範例)
# npm run build          # Node.js/JavaScript
# mvn compile            # Java/Maven
# cargo build            # Rust
# python -m build        # Python

# 程式碼檢查指令
# npm run lint           # JavaScript/TypeScript
# mvn checkstyle:check   # Java
# cargo clippy           # Rust
# ruff check .           # Python

# 測試指令
# npm test               # JavaScript
# mvn test               # Java
# cargo test             # Rust
# pytest -v             # Python

# 單一測試指令
# npm test -- --testNamePattern="specific_test"
# mvn test -Dtest=SpecificTest
# cargo test specific_test
# pytest tests/test_specific.py -v
```

### 程式碼風格指南

#### 通用原則
- 編寫乾淨、可讀、可維護的程式碼
- 遵循語言特定約定
- 使用有意義的變數和函數名稱
- 保持函數小而專注
- 為複雜邏輯新增註解

#### 導入組織
- 分組導入：標準函式庫 → 第三方 → 本地
- 移除未使用的導入
- 使用顯式導入而非萬用字元導入
- 組內按字母順序排序

#### 格式化
- 使用一致的縮排（JS/TS 2個空格，Python 4個空格，Java製表符）
- 在多行結構中新增尾隨逗號
- 在語言要求時使用分號
- 保持行長度在100字元以內

---

## Multilingual Development Standards

### Code Comments
- Use English for code comments in shared libraries
- Use language-specific comments for business logic
- Include multilingual examples in documentation

### Documentation
- README files should include all three languages
- API documentation: English primary, with translations
- Code examples: Provide multilingual versions when helpful

### Error Messages
- User-facing errors: Support multiple languages
- Developer errors: English preferred
- Log messages: English with context in local language if needed

### File Naming
- Use English for technical files (config, scripts)
- Use appropriate language for content files
- Be consistent across the project

---

## Development Workflow

1. **Before Coding:**
   - Check existing code patterns
   - Understand the technology stack
   - Review this AGENTS.md file

2. **During Coding:**
   - Follow the style guidelines above
   - Write tests as you code
   - Add meaningful comments

3. **After Coding:**
   - Run linting and formatting tools
   - Execute tests (including single test)
   - Update documentation if needed

4. **Before Commit:**
   - Ensure all tests pass
   - Check code quality
   - Write clear commit messages

---

## Technology Stack Decision Guidelines

When choosing the technology stack:

1. **Consider project requirements**
2. **Evaluate team expertise**
3. **Check existing integrations**
4. **Update this AGENTS.md file with specific commands**

Current indicators:
- IntelliJ IDEA configuration suggests Java
- Original .gitignore mentioned LangChain/LangGraph
- No source files present yet
- Decision pending - keep guidelines flexible
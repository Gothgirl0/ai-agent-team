# 贡献指南

感谢你考虑为 AI Agent Team SKILL 做出贡献！我们欢迎各种形式的贡献。

## 📋 目录

- [行为准则](#行为准则)
- [如何贡献](#如何贡献)
- [开发流程](#开发流程)
- [代码规范](#代码规范)
- [提交规范](#提交规范)
- [问题反馈](#问题反馈)

---

## 行为准则

### 我们的承诺

为了营造开放和友好的环境，我们承诺让每个人都能参与项目，无论经验水平、性别、性别认同和表达、性取向、残疾、个人外貌、体型、种族、民族、年龄、宗教或国籍如何。

### 我们的标准

积极行为包括：
- ✅ 使用友好和包容的语言
- ✅ 尊重不同的观点和经验
- ✅ 优雅地接受建设性批评
- ✅ 关注对社区最有利的事情
- ✅ 对其他社区成员表示同理心

不可接受的行为包括：
- ❌ 使用性别化语言或图像，以及不受欢迎的性关注或调情
- ❌ 恶搞、侮辱/贬损的评论，以及个人或政治攻击
- ❌ 公开或私下骚扰
- ❌ 未经明确许可发布他人的私人信息
- ❌ 其他在专业场合可能被合理认为不适当的行为

---

## 如何贡献

### 报告 Bug

1. 检查 [Issues](https://github.com/Sunnyeung369/ai-agent-team/issues) 确保问题未被报告
2. 如果没有，创建新的 Issue
3. 使用 Bug Report 模板填写信息
4. 提供清晰的标题和详细描述
5. 包含复现步骤和预期行为

### 提出新功能

1. 先在 [Discussions](https://github.com/Sunnyeung369/ai-agent-team/discussions) 讨论
2. 说明功能的使用场景和价值
3. 考虑是否适合本项目
4. 创建 Feature Request Issue

### 提交代码

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 进行更改并测试
4. 提交更改（遵循[提交规范](#提交规范)）
5. 推送到分支 (`git push origin feature/AmazingFeature`)
6. 创建 Pull Request

### 改进文档

- 修正错别字和语法错误
- 改进示例和说明
- 添加新的使用场景
- 翻译文档

---

## 开发流程

### 环境设置

```bash
# 1. Fork 并克隆仓库
git clone https://github.com/YOUR_USERNAME/ai-agent-team.git
cd ai-agent-team

# 2. 添加上游远程仓库
git remote add upstream https://github.com/Sunnyeung369/ai-agent-team.git

# 3. 创建特性分支
git checkout -b feature/your-feature-name
```

### 分支命名规范

- `feature/` - 新功能
  - `feature/add-new-agent`
  - `feature/improve-workflow`
- `fix/` - Bug 修复
  - `fix/typo-in-readme`
  - `fix/agent-coordination-issue`
- `docs/` - 文档更新
  - `docs/update-installation-guide`
  - `docs/add-examples`
- `refactor/` - 代码重构
  - `refactor/optimize-agent-logic`
- `test/` - 测试相关
  - `test/add-ci-checks`

### 开发流程

1. **创建分支**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **进行更改**
   - 编辑文件
   - 添加测试（如果适用）
   - 更新文档

3. **本地测试**
   ```bash
   # 验证 SKILL.md 语法
   # 检查文档格式
   # 测试功能
   ```

4. **提交更改**
   ```bash
   git add .
   git commit -m "feat: add new feature"
   ```

5. **同步上游**
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

6. **推送分支**
   ```bash
   git push origin feature/your-feature-name
   ```

7. **创建 Pull Request**
   - 在 GitHub 上创建 PR
   - 填写 PR 模板
   - 等待审查

---

## 代码规范

### SKILL.md 规范

```yaml
---
name: skill-name
version: "1.0.0"
description: "清晰简洁的描述"
user-invocable: true
---
```

**必需字段**：
- `name`: SKILL 名称（小写，连字符分隔）
- `version`: 语义化版本号
- `description`: 功能描述（1-2 句话）
- `user-invocable`: 是否用户可调用

### Markdown 规范

- 使用 UTF-8 编码
- 行尾使用 LF（不是 CRLF）
- 标题使用 ATX 风格（`# H1`, `## H2`）
- 代码块指定语言
- 列表使用 `-` 而非 `*`
- 链接使用参考式或内联式

### 文档规范

**README.md**：
- 清晰的项目介绍
- 安装说明
- 使用示例
- 贡献指南链接

**CHANGELOG.md**：
- 遵循 [Keep a Changelog](https://keepachangelog.com/)
- 版本号使用语义化版本

---

## 提交规范

我们使用 [Conventional Commits](https://www.conventionalcommits.org/) 规范。

### 提交格式

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Type 类型

- `feat`: 新功能
- `fix`: Bug 修复
- `docs`: 文档更新
- `style`: 代码格式（不影响功能）
- `refactor`: 重构
- `perf`: 性能优化
- `test`: 测试相关
- `chore`: 构建/工具相关
- `ci`: CI 配置

### 示例

```bash
# 新功能
git commit -m "feat(writer): add word count limit"

# Bug 修复
git commit -m "fix(chief): correct agent coordination logic"

# 文档更新
git commit -m "docs: update installation guide"

# 重构
git commit -m "refactor(agents): optimize agent task distribution"
```

### 详细提交

```bash
git commit -m "feat: add new agent type

Add support for custom agent types with user-defined
roles and capabilities.

- Add agent type configuration
- Update documentation
- Add examples

Closes #123"
```

---

## Pull Request 规范

### PR 标题

使用与提交信息相同的格式：

```
feat: add new feature
fix: resolve agent coordination issue
docs: update README
```

### PR 描述

使用 PR 模板，包含：

- **更改类型**: feat / fix / docs / refactor
- **更改说明**: 清晰描述更改内容
- **动机**: 为什么做这些更改
- **测试**: 如何测试这些更改
- **相关 Issue**: 关联的 Issue 编号

### PR 审查

- 确保所有 CI 检查通过
- 响应审查评论
- 进行必要的更改
- 保持 PR 专注和简洁

---

## 问题反馈

### Bug Report

创建 Issue 时提供：

1. **清晰标题**
   - ✅ "Chief Agent fails to coordinate Researcher and Writer"
   - ❌ "Not working"

2. **环境信息**
   - OS: Windows / macOS / Linux
   - Claude Code 版本
   - ai-agent-team 版本

3. **复现步骤**
   ```
   1. Run '[Chief] write an article'
   2. Wait for Researcher to complete
   3. Error occurs
   ```

4. **预期行为**
   - 应该发生什么

5. **实际行为**
   - 实际发生了什么

6. **日志/截图**
   - 错误信息
   - 相关截图

### Feature Request

1. **功能描述**
   - 清晰描述想要的功能

2. **使用场景**
   - 在什么情况下会用到
   - 解决什么问题

3. **替代方案**
   - 考虑过其他方案吗

4. **优先级**
   - 高 / 中 / 低

---

## 测试指南

### 手动测试

```bash
# 1. 安装 SKILL
cd ~/.claude/skills
git clone https://github.com/YOUR_USERNAME/ai-agent-team.git

# 2. 测试基本功能
claude
> [Chief] 测试基本功能

# 3. 测试各个 Agent
> [@researcher] 研究测试
> [@writer] 写作测试
> [@editor] 编辑测试

# 4. 测试工作流程
> [task:research] 任务分类测试
```

### 自动化测试

CI 会自动运行：
- SKILL.md 语法检查
- 必需文件检查
- Markdown 格式检查
- YAML frontmatter 验证

---

## 发布流程

### 版本号

遵循语义化版本 (Semantic Versioning)：

```
MAJOR.MINOR.PATCH

1.0.0  -> Major version (不兼容的 API 更改)
1.1.0  -> Minor version (向后兼容的功能新增)
1.1.1  -> Patch version (向后兼容的问题修复)
```

### 发布步骤

1. **更新版本号**
   - 在 SKILL.md 中更新版本
   - 在 CHANGELOG.md 中添加变更

2. **创建 Release**
   ```bash
   git tag -a v1.0.0 -m "Release v1.0.0"
   git push origin v1.0.0
   ```

3. **GitHub Release**
   - 在 GitHub 创建 Release
   - 添加 Release Notes
   - 上传附件（如果有）

---

## 获得帮助

- 💬 **Discussions**: [GitHub Discussions](https://github.com/Sunnyeung369/ai-agent-team/discussions)
- 🐛 **Bug 报告**: [Issues](https://github.com/Sunnyeung369/ai-agent-team/issues)
- 💡 **功能建议**: [Feature Requests](https://github.com/Sunnyeung369/ai-agent-team/issues)
- 📧 **邮件**: Sunnyeung369@users.noreply.github.com

---

## 许可证

贡献的代码将基于 [MIT License](LICENSE) 发布。

---

## 致谢

感谢所有贡献者！

<a href="https://github.com/Sunnyeung369/ai-agent-team/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Sunnyeung369/ai-agent-team" />
</a>

---

**再次感谢你的贡献！** 🎉

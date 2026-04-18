# 第 1 部分：环境准备与上下文工程

[🎮 在线演示](../docs/) • [📚 实验指南](../docs/step.html) • [← 总览](00-overview.md)

---

> ⏱️ **时长：** 约 15 分钟

本部分将完成开发环境初始化，并让 GitHub Copilot 理解你的代码库上下文。

---

## 🔧 初始配置

### 步骤 1：创建你的仓库

1. 打开本仓库并点击 **Use this template** → **Create a new repository**
2. 创建你的仓库（例如 `my-soc-ops-csharp`）
   - Name: `my-soc-ops-csharp`
   - Visibility: **Public**
3. ✅ 你的 Soc Ops 仓库创建完成

### 步骤 2：启用 GitHub Pages

1. 打开仓库 **Settings** → **Pages**
2. 在 “Build and deployment” 中选择 **GitHub Actions**
3. ✅ 每次提交都会发布到：`https://{username}.github.io/{repo-name}`

### 步骤 3：克隆并在 VS Code 打开

1. 打开 VS Code
2. 运行命令：`Git: Clone` → `Clone from GitHub`
3. 选择你新建的仓库
4. 提示时安装 **recommended extensions**

### 步骤 4：运行 Setup 智能体

在 Chat 面板输入：

```
/setup
```

智能体会：
- 识别当前环境
- 安装缺失依赖
- 启动开发服务器

✅ **成功标志：** 应用已在浏览器中运行

---

## 📚 认识上下文工程

上下文工程就是让 AI 理解你项目细节的过程，这会让 Copilot 的建议更准确、更相关。

### 任务 1：生成工作区指令

指令文件会影响所有智能体交互，是提高效率与稳定性的关键。

**步骤：**

1. 运行命令：`Chat: Generate Workspace Instructions File`
2. 等待智能体分析代码库
3. 查看生成的指令（通常会偏长）
4. 继续输入：
   ```
   Compress down by half and add a mandatory development checklist 
   (lint, build, test) to the top
   ```
5. **提交** 指令文件

✅ **结果：** 之后的请求都能基于统一的工作区地图展开。

---

### 任务 2：用后台智能体并行处理

后台智能体运行在隔离的 git worktree 中，非常适合不需要你全程盯着的任务。

**步骤：**

1. 在 Chat 中点击 `+` → **New background agent**
2. 输入：
   ```
   Add linting rules for unused vars and async/await usage; fix any errors
   ```
3. 等待完成后 **Review** 并 **Apply** 变更
4. 完成后右键会话并删除

**再试一个云端智能体：**

1. 点击 `+` → **New cloud agent**
2. 输入：
   ```
   Make the README more engaging as a landing page to the project
   ```

✅ **结果：** lint 规则补齐、错误修复、README 优化，最后全部并回主分支。

---

### 任务 3：查看已有指令文件

仓库已包含预置指令，可帮助 AI 更快理解项目。

#### CSS 工具类指令

📄 查看 `.github/instructions/css-utilities.instructions.md`

该文件记录了此 Blazor 项目中可用的类 Tailwind CSS 工具类。

> 💡 **可选尝试：** 清空主要正文后重新运行提示词，观察重新生成效果

#### 前端设计指令

📄 查看 `.github/instructions/frontend-design.instructions.md`

其中的 “no purple gradients” 规则会推动智能体以设计师思维输出方案。

> 💡 **思考：** 你还可以针对哪些 AI 常见偏置做约束和引导？

---

## ✅ 第 1 部分完成！

你已经学会：
- 完成开发环境初始化
- 生成并精炼工作区指令
- 使用后台与云端智能体并行工作
- 理解现有指令文件的作用

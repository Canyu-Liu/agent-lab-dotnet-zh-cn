# 第 4 部分：多智能体开发

[🎮 在线演示](../docs/) • [📚 实验指南](../docs/step.html) • [← 第 3 部分](03-quiz-master.md)

---

> ⏱️ **时长：** 约 20 分钟

使用专长型智能体开发新功能：用 TDD 智能体保证质量，用设计智能体打磨 UI。

---

## 🧪 任务 1：寻宝模式（TDD 驱动）

通过自定义智能体交接复杂流程，把大任务拆成小步骤，同时保留关键决策控制权。

### 我们要构建什么

新增 **Scavenger Hunt（寻宝）** 模式：
- 使用与宾果相同的问题
- 以简洁清单形式展示
- 顶部显示进度条
- 点击即可标记完成

### 步骤

#### 阶段 1：Plan 规划

1. 在 **Plan Mode** 新建 Chat
2. 输入：
   ```
   Add a new Scavenger Hunt mode: same questions, but shown as a 
   simple list with checkboxes and a progress meter
   ```
3. **迭代计划**，确保它：
   - ✅ 在开始界面增加模式入口
   - ✅ 新建清单视图组件
   - ✅ 包含进度指示
   - ❌ 不要过度堆叠功能

#### 阶段 2：TDD Red（先写失败测试）

1. 选择 **TDD Red** 智能体
2. 点击 **Start**
3. 观察其生成测试，覆盖：
   - 组件渲染
   - 复选框交互
   - 进度计算
   - 状态管理

4. 在 VS Code 的 **Test Explorer** 查看失败测试

#### 阶段 3：TDD Green（让测试通过）

1. Red 完成后切换到 **TDD Green** 智能体
2. 观察其：
   - 以最小实现让测试通过
   - 每次变更后运行测试
   - 持续迭代直到全部通过

#### 阶段 4：Refactor（重构整理）

1. 选择 **TDD Refactor** 智能体
2. 在保持测试为绿色的前提下清理代码

### 检查点恢复

如果中途出问题：
1. 用 Chat **Checkpoints** 回退
2. 回到 “TDD Red” 之前的状态
3. 调整提示词后重试

> 💡 **加分项：** 试试 **TDD Supervisor**，可一键编排完整 TDD 流程

✅ **结果：** 用规范 TDD 流程完成并验证“寻宝模式”。

---

## 🎴 任务 2：卡组模式（设计驱动）

使用 **Pixel Jam** 智能体，在构建新功能时优先迭代 UI 体验。

### 我们要构建什么

新增 **Card Deck Shuffle（卡组洗牌）** 模式：
- 玩家进入游戏
- 点击后抽取随机卡片
- 卡片翻转动画展示
- 显示可讨论的问题

### 步骤

1. 新建 Chat
2. 选择 **Pixel Jam** 智能体
3. 输入：
   ```
   New mode: Card Deck Shuffle. Every player opens the game, 
   taps, and gets a random card with a question
   ```
4. 观察其对 UI 的迭代
5. 继续追问优化：
   ```
   Add a cool 3D flip animation when revealing the card
   ```
   ```
   Make the card styling match the cyberpunk theme
   ```
6. 满意后 **Commit**

### Pixel Jam 的特点

- 优先关注 **视觉设计**
- 在业务逻辑前先迭代 **UI/UX**
- 深度利用前端设计指令
- 输出更完整、可交付的动效界面

---

## 🔍 任务 3：UX 评审智能体

结合 MCP 工具、自定义流程与子智能体隔离能力，完成高质量体验评审。

### 步骤

1. 使用 **Pixel Jam** 新建 Chat
2. 输入：
   ```
   Run review
   ```
3. 提示时点击 **Allow for this Workspace**，授权 Playwright 工具
4. 观察其自动完成：
   - 页面截图
   - 可用性问题分析
   - 可访问性检查
   - 视觉一致性评估

### 评审维度

| 分类 | 检查项 |
|------|--------|
| **可用性** | 导航流程、按钮可理解性、反馈清晰度 |
| **可访问性** | 对比度、键盘导航、屏幕阅读器支持 |
| **视觉** | 一致性、间距、对齐 |
| **交互** | 触控热区、悬停状态、动画表现 |

### 评审后动作

评审结束后可继续输入：
```
File the critical findings as GitHub issues
```
```
Fix the accessibility issues you found
```
```
Assign the navigation bug to a background agent
```

✅ **结果：** 得到可执行的完整 UX 评审结论。

---

## 🎯 加分挑战

如果还有时间，可以继续尝试：

| 挑战 | 建议方式 |
|------|----------|
| 修复 UX 问题 | 委托后台或云端智能体 |
| 多主题切换 | 在开始页加入主题选择器 |
| 社交分享 | 在胜利页加入分享按钮 |
| 排行榜 | 记录并展示最高分 |
| 音效反馈 | 为交互添加音频提示 |

---

## ✅ 第 4 部分完成！

你已经学会：
- 使用 TDD 智能体推进测试驱动开发
- 用 Red-Green-Refactor 循环构建功能
- 使用 Pixel Jam 等设计导向智能体
- 执行系统化 UX 评审
- 组合多智能体处理复杂工作流

---

## 🎉 工作坊完成！

恭喜，你已完成 VS Code GitHub Copilot Agent Lab。

### 你构建了什么

- ✅ 完整重设计的社交宾果应用
- ✅ 自定义问答主题
- ✅ 寻宝模式（TDD 构建）
- ✅ 卡组洗牌模式（设计驱动）

### 你掌握了什么

1. **上下文工程**：让 AI 理解你的代码库
2. **智能体基础能力**：后台、云端与自定义智能体
3. **设计优先开发**：在 AI 协助下迭代 UI
4. **测试驱动开发**：通过 TDD 智能体保证可靠性

### 继续探索

- 📺 [VS Code YouTube](https://www.youtube.com/code)
- 📖 [VS Code Copilot 文档](https://code.visualstudio.com/docs/copilot/overview)
- 🌟 [Awesome Copilot](https://github.com/github/awesome-copilot)

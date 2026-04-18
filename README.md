# Soc Ops

适合线下交流活动的社交宾果游戏。找到符合题目的人，并连成 5 个即可获胜！

🎮 **[开始游戏](./docs/)** • 📚 **[查看实验指南](./docs/step.html?step=00-overview)**

**翻译说明**：此项目为社区翻译的版本，在 GitHub Copilot Dev Days Nanning 活动中使用。

---

## 📚 实验指南

| 部分 | 标题 |
|------|------|
| [**00**](./docs/step.html?step=00-overview) | 概览与检查清单 |
| [**01**](./docs/step.html?step=01-setup) | 环境搭建与上下文工程 |
| [**02**](./docs/step.html?step=02-design) | 先设计，后前端 |
| [**03**](./docs/step.html?step=03-quiz-master) | 自定义问答主持人 |
| [**04**](./docs/step.html?step=04-multi-agent) | 多智能体开发 |

> 📝 这些实验指南也可以在 [`workshop/`](workshop/) 文件夹中离线阅读。

---

## 前置条件

- [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) 或更高版本

## 运行

```bash
cd SocOps
dotnet run
```

## 构建

```bash
cd SocOps
dotnet build
```

推送到 `main` 分支后会自动部署到 GitHub Pages。

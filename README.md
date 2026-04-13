<img width="1507" height="864" alt="Screenshot 2026-04-13 at 1 36 53 PM" src="https://github.com/user-attachments/assets/ac267597-05ac-4f67-9ab7-a70329a1a1d5" /># Dify-Paper-Reading-Agent
中文版： 基于 Dify 搭建的 AI Agent 学术论文速读工作流，一键将 ArXiv 论文转化为结构化脑图。  English Version: An AI-powered workflow built on Dify that transforms ArXiv papers into structured mind maps with one click.
# 📚 论文速读 + 脑图生成器 | ArXiv Paper Digest & Mindmap Agent

> 基于 **Dify** 搭建的 AI Agent 自动化工作流，输入研究主题，一键输出结构化论文摘要与 XMind 脑图大纲。

[![Dify](https://img.shields.io/badge/Built%20with-Dify-blue)](https://dify.ai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## ✨ 核心功能

- **🔍 智能检索**：实时调用 ArXiv API 获取最新学术论文元数据。
- **🤖 AI 摘要**：利用大语言模型解析 XML 半结构化数据，提取核心论点、实验方法与关键数据。
- **🧠 格式转换**：自动将摘要重构为层级分明的 Markdown 列表，一键复制到 XMind 生成脑图。
- **⚡ 零代码编排**：全程通过 Dify 工作流画布拖拽搭建，逻辑透明、易于扩展。

## 🛠️ 技术栈与架构

| 节点 | 作用 | 关键技术 |
|:---|:---|:---|
| **开始** | 接收关键词输入 | Dify 变量定义 |
| **HTTP 请求** | 调用 ArXiv 公开 API | RESTful API, XML 解析 |
| **LLM (1)** | 提取论文核心信息 | Prompt Engineering, 语义理解 |
| **LLM (2)** | 转 XMind 可读列表 | Few-shot Prompt, 结构化输出 |
| **结束** | 输出最终结果 | Dify 输出变量映射 |

## 📁 仓库文件说明

- `paper_digest_workflow.yml` —— Dify 工作流 DSL 导出文件，可一键导入你的 Dify 实例。
- `screenshots/` —— 工作流画布与运行效果截图（可选）。

## 🚀 快速上手

### 方式一：在线体验（推荐）
> 点击下方链接直接运行 WebApp（无需登录）：
> **[👉 立即体验 WebApp]([https://your-dify-webapp-link.com](https://udify.app/workflow/I9rfuOUcY3F1Zn2s))**  
> *请将链接替换为你自己的 Dify 发布地址*

### 方式二：导入 DSL 文件
1. 注册/登录 [Dify.ai](https://cloud.dify.ai)。
2. 进入「工作室」→ 点击「导入应用」。
3. 上传本仓库中的 `paper_digest_workflow.yml` 文件。
4. 配置好你的模型供应商（如 DeepSeek、OpenAI API Key）。
5. 点击「发布」→「运行」即可使用。

## 📸 效果预览

### 工作流画布
![工作流画布](https://github.com/user-attachments/assets/c66d259d-836e-4846-88e5-ca2b3e9253b5)
)

### 运行结果示例

*<img width="1512" height="868" alt="Screenshot 2026-04-13 at 1 37 24 PM" src="https://github.com/user-attachments/assets/61b4dd03-5c42-4f35-a5c3-7f1881bd53b1" />*

## 💡 项目亮点

- **展示 AI 应用落地能力**：不局限于聊天框问答，通过 API 串联真实外部数据源。
- **体现自动化思维**：将“检索→阅读→整理→制图”手动流程压缩为分钟级自动化链路。
- **可复用性强**：更换 API 与 Prompt 即可迁移至新闻监控、竞品分析等场景。

## 📝 未来计划

- [ ] 支持批量处理多篇论文并生成对比脑图
- [ ] 集成 Notion API 实现自动存入知识库
- [ ] 增加 PDF 全文解析模块（突破仅依赖摘要的限制）

## 🤝 关于作者

此项目为个人学习与求职作品，旨在展示 **AI Agent 应用编排** 与 **自动化工作流设计** 能力。

如果有任何疑问或建议，欢迎通过 GitHub Issues 交流。

# cache —— 用 AI 构建的个人概念学习仓库

一个可公开访问、可持续迭代的个人学习仓库：它保存了一个**可复用的「概念学习资料生成」Skill**，以及由该 Skill 生成、并经本人核查的学习资料。既是本课程的作业成果，也可以作为后续项目与作品集的个人工具基础。

## 仓库用途

- 沉淀一个项目级 Skill：`concept-learner`，用于把任意概念整理成结构化学习资料。
- 保存由该 Skill 生成的三份概念学习资料 + 一份概念关系说明。
- 作为后续课程项目继续添加新 Skill、新学习资料的基础。

## 目录结构

```
cache/
├── .workbuddy/
│   └── skills/
│       └── concept-learner/
│           └── SKILL.md          # 项目级 Skill
├── learning-materials/
│   ├── agent.html                # 概念：Agent
│   ├── llm-context.html          # 概念：大模型的上下文
│   ├── skill.html                # 概念：Skill
│   └── concept-relationship.md   # 三者的关系说明（含 Mermaid 图）
├── README.md
└── .gitignore
```

## Skill 的存放路径

- 路径：`.workbuddy/skills/concept-learner/SKILL.md`
- 元数据：`name: concept-learner`，`description` 说明了「做什么 + 何时调用」。

## 如何在 WorkBuddy 中调用

1. 用 WorkBuddy 打开本仓库（本地克隆目录）。
2. 直接发一句类似下面的指令即可触发：

   > 帮我用 concept-learner 学习「RAG（检索增强生成）」

3. 也可以换成任意概念，例如「微调」「Transformer」「提示注入」等。Skill 会按 `SKILL.md` 中定义的步骤产出：个人解释、核心机制、应用场景、概念辨析、自测题、可核查来源。

> 说明：本作业的环境是 TraeCode，项目级 Skill 目录约定为 `.workbuddy/skills/`（与作业要求一致）。Skill 的格式遵循 Agent Skills 开放标准（`SKILL.md` + YAML frontmatter），因此也可用于 Claude Code、Cursor 等支持该标准的工具。

## 已生成的学习资料

| 文件 | 概念 | 说明 |
|------|------|------|
| `learning-materials/agent.html` | Agent（智能体） | 个人解释、核心机制、应用场景、易混淆点/边界、自测题、来源 |
| `learning-materials/llm-context.html` | 大模型的上下文 | 同上 |
| `learning-materials/skill.html` | Skill（技能） | 同上 |
| `learning-materials/concept-relationship.md` | 三者关系 | 文字 + 表格 + Mermaid 流程图 |

## 使用 AI 后的人工核查与修改

这些资料由 AI 辅助生成，本人做了以下人工核查与修改：

1. **理解并改写**：逐篇阅读生成内容，把「个人解释」改写为自己的话，未整段照搬 AI 对话结果。
2. **核对来源**：逐条打开来源链接验证真实可访问，去除了不确定或可疑的链接，只保留官方文档、论文与权威博客。
3. **修正概念辨析**：核对 Agent vs Workflow、上下文 vs 知识、Skill vs Prompt 等易混淆点，确保表述准确、不张冠李戴。
4. **补充边界**：为每个概念补充了「什么时候不该用」，避免只讲优点。
5. **统一结构**：让 Skill 的输出结构与三份资料的章节保持一致，便于复用和比对。

## 版本与安全

- 敏感信息（API Key、密码、私钥、`.env` 等）已通过 `.gitignore` 排除，未上传到仓库。
- 本仓库保持公开，提交记录可在 GitHub 上查看。

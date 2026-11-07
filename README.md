# H3 人物动作与节奏

这是一个用于 MiniMax H3 的 Codex Skill，帮助设计人物动作、对白节奏、参考帧与镜头衔接，并根据试片修正动作迟缓、僵硬、过快或不连贯的问题。

技能入口是 [SKILL.md](SKILL.md)，详细材料在 [references](references/) 中。已验证的项目案例、用户反馈和有待验证的建议分别标注；案例中的时长不能直接推广到所有动作。

## 使用

将仓库克隆到 Codex 的技能目录下，目录名为 `h3-motion-directing`。例如在 Windows PowerShell 中：

```powershell
git clone https://github.com/QWQcool/h3-motion-directing.git "$HOME/.codex/skills/h3-motion-directing"
```

目标目录应不存在；如果该技能已经安装，可在当前技能目录中使用 Git 同步。私有仓库需要拥有访问权限的 GitHub 账号。

在会话中使用 `$h3-motion-directing` 调用，并说明人物、动作、节奏、参考素材及希望获得的结果。编写 H3 最终提示词时建议配合 [MiniMax 官方 h3-prompt-writing 技能](https://github.com/MiniMax-AI/MiniMax-H3/tree/main/skills/h3-prompt-writing)；若本机已安装，技能会优先读取本地指南。

## 内容与范围

- `SKILL.md`：动作和节奏设计、提示词、验片与修正流程。
- `references/motion-patterns.md`：动作规划和示例提示词。
- [《赛后先哄你》](references/production-cases.md) 记录真人风格双人镜中的落座、接触与倾听。
- [《GPT 修好千问》](references/chibi-continuity.md) 记录 Q 版角色的收步与轻俯、连续尾帧接镜、对白归属，以及已认可表演上的局部修订。
- `references/production-checks.md`：生成、声音、补帧和交付检查。
- `references/sources.md`：官方和社区资料来源。

制作案例中的部分证据链接指向原项目在创建者电脑上的文件，仅在那台电脑上可用；案例摘要本身保存在仓库中。仓库不包含原项目的视频、图片或服务器凭据。

本仓库是技能文件的版本备份。本地更改需要通过 Git 提交并推送，才会同步到 GitHub。

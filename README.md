# H3 人物动作与节奏

这是一个用于 MiniMax H3 的 Codex Skill，帮助设计人物动作、对白节奏、参考帧与镜头衔接，并根据试片修正动作迟缓、僵硬、过快或不连贯的问题。

技能入口是 [SKILL.md](SKILL.md)，详细材料在 [references](references/) 中。内容为通用制作决策、技术边界和说明性示例，不依赖某个影片、人物或作者电脑上的项目文件。

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
- [表演问题诊断](references/acting-diagnostics.md)：落座、接触、动作过快或过慢的判断。
- [对白与动作连续性](references/dialogue-continuity.md)：身体支撑、口型归属、音画时间线和局部修订。
- [连续镜头与运动上下文](references/continuous-shots.md)：完整镜头、分任务延长、换机位及视频前缀。
- [提示词的动作负担](references/prompt-design.md)：动作约束、对白重叠和提示词审查。
- `references/production-checks.md`：生成、声音、补帧和交付检查。
- `references/sources.md`：官方和社区资料来源。

说明性示例不保证特定效果；动作时长和工作流参数按当前素材与部署核实。仓库不保存影片素材、项目验收记录或服务器凭据。

本仓库是技能文件的版本备份。本地更改需要通过 Git 提交并推送，才会同步到 GitHub。

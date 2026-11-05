# 来源与适用边界

查阅日期：2026-11-05。以下链接为作者或项目维护者发布的原始资料。社区技能作为可借鉴的方法，不构成 H3 效果保证；未安装或运行这些第三方技能的代码。

## MiniMax 官方 h3-prompt-writing

- [SKILL.md](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/SKILL.md)
- [基础模式指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/base-en.txt)
- [完整参考模式指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/ref-en.txt)
- 已安装本地版本：`<local-skill>/`。

用途：确定模式、提示词字段、首尾帧关系和参考标签。该技能与本技能配合使用。摄影机的运动幅度和速度要有明确指代；官方格式不提供可保证自然人物节奏的统一秒数。

## Square-Zero-Labs / video-prompting-skill

- [技能入口](https://github.com/Square-Zero-Labs/video-prompting-skill/blob/main/video-prompting/SKILL.md)
- [H3 专项说明](https://github.com/Square-Zero-Labs/video-prompting-skill/blob/main/video-prompting/references/models/minimax-h3/prompting.md)

借鉴：描述细节与新增动作是不同负担；检查动作数量能否容纳在时长内。超载时简化或分镜。使用动作参考时明确身体运动、构图和时间结构分别来自哪里。

本技能的取舍：保留 H3 官方格式，不套用其他模型的单行输出习惯；参考素材已经在上下文时直接使用。以上是社区方法，仍需在当前工作流试片。

## btwiuse / action-rhythm-editing

- [SKILL.md](https://github.com/btwiuse/video-skills/blob/main/ai-video-skills-v2-standard/action-rhythm-editing/SKILL.md)

借鉴：先确定身体路径，再分配时间；动作的接触、反应与收势影响可读性，速度变化比全程等速更有表现力。

适用边界：原技能重点包括打斗、追逐、武器与动作展示。本技能没有照搬其固定时长模板、强制蓄势、冲击停顿或结尾定格。日常互动按实际姿态、对白和情绪重新编排。

## 本地制作记录

见 [制作案例](production-cases.md)。其中自然落座、摸脸、近景倾听等有先前实际生成和检查记录；完整唇吻序列与 Ref2VA 动作迁移没有本项目成功验证。

本技能新写的泛化提示词未重新消耗 GPU 验证。框架与语义检查不代表渲染效果已经通过。后续实际制作发现新问题时，根据证据修订当前项目方案；更新此技能应在用户授权的技能维护任务中进行。

# 来源与适用边界

官方节点机制最近核对于2026-11-09。下列链接为项目维护者或原作者发布的资料入口；版本和部署不同会改变行为，实际执行前按当前schema与实现确认。社区方法不构成效果保证，也不要求自动安装其代码。

## 官方格式与推理能力

- [MiniMax h3-prompt-writing](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/SKILL.md)：基础与完整参考模式的字段、标签和首尾帧关系。
- [基础模式指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/base-en.txt)。
- [完整参考模式指南](https://github.com/MiniMax-AI/MiniMax-H3/blob/main/skills/h3-prompt-writing/references/ref-en.txt)。
- [ComfyUI H3指南](https://docs.comfy.org/tutorials/video/minimax/minimax-h3)：基础工作流、原生时长与多帧引导入口。
- [ComfyUI核心节点](https://github.com/Comfy-Org/ComfyUI/blob/master/comfy_extras/nodes_minimax_h3.py)：具体的首尾图、Add Guide、参考视频、帧数与时间索引行为。

这些资料说明模型或节点支持什么，不证明某段人物动作或声线在特定素材上已经成功。时间戳是意图，参考关系声明也不等于逐像素保留。

## 可借鉴的社区技能

- [Square-Zero-Labs / video-prompting-skill](https://github.com/Square-Zero-Labs/video-prompting-skill/blob/main/video-prompting/SKILL.md)：检查动作负担和时长容量。借鉴规划思路，最终仍按H3相应格式输出。
- [btwiuse / action-rhythm-editing](https://github.com/btwiuse/video-skills/blob/main/ai-video-skills-v2-standard/action-rhythm-editing/SKILL.md)：身体路径、接触、反应和收势。其动作戏停顿或固定时窗不能机械套到日常表演。
- [upr4k / h3-long-video](https://github.com/upr4k/comfy-tools/blob/main/minimax-h3/skills/h3-long-video/SKILL.md)：统一素材锚点与分段规划。不要采纳单末帧即可像素完美或必然无缝的过强表述。
- [teskor-hub / minimax-h3-skill](https://github.com/teskor-hub/minimax-h3-skill)：先测切点、再读素材和写表演。其特定依赖与工作流不是所有H3任务的必选路径。

## 连续运动的实现参考

- [ttulttul / H3 Continuation](https://github.com/ttulttul/ComfyUI-Minimax-H3-Continuation)：联合音画latent尾部引导、重叠去除和追加；作者明确说明不能保证无缝语义。
- [seitanism / Motion Context MultiRef](https://github.com/seitanism/ComfyUI-H3-Motion-Context-MultiRef)：运动上下文、音画延长与动作迁移，具体工作流的依赖和保留机制不同。

通用接线、时间和几何判断见 [连续镜头与运动上下文](continuous-shots.md)。前缀引导、参考输入和保留源latent的遮罩分别理解；不能因名字包含continuation就认为输入画面和运动必然保留。

## 技能与项目的边界

技能保存可迁移的判断、操作约束和说明性示例；项目保存素材、版本、运行参数、反馈和验片证据。使用本技能不需要取得作者电脑上的项目文件。示例和建议须按当前素材验证，文档及接线审查通过不能代替渲染或观感验收。

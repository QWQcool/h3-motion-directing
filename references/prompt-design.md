# 提示词的动作负担

目标是让一段可完成的表演读起来清楚，约束与引导彼此相容。提示词长短本身不是已证明的质量原因；优先检查内容是否压制行为、重复起点或提出冲突目标。以下改写是方法示例，尚需当前素材试片。

## 先写表演，再补必要约束

以一个连续镜头为单位写：当前构图和起始状态 → 人物想做什么 → 身体怎样移动或接触 → 对方怎样回应 → 对白与行为怎样重叠 → 相机如何观看。按所选模式使用官方字段，格式见配套提示词技能。

保留身份、服装、光线和空间锚点。每轮修改后重新整理最终意图，不把历史调试里的慢一点、快一点、保持不动和各种禁令一直累加。限制只针对已定位的风险及相应对象。

## 容易把人物写僵的约束

- **全身长期保持姿态，只准眼睛和嘴动**：适用于刻意克制或特定反应，不宜从模板继承到走近、接触或交谈。改写为可见行为，例如转向对方、把身体靠近、抬眼回应；仍允许静默和停顿承担剧情。
- **为了看清接触而全程放慢**：将接近速度、接触力度和情绪分开。可以日常速度抬手、轻轻接触，再随对白回应，而不是把温柔统一翻译成慢动作。
- **所有行为都逐渐发生**：只在需要犹豫或渐变时使用；明确是哪一次表情或动作渐变，不覆盖整镜。`quietly`或`softly`可能描述声音或力度，不能单凭词汇就判定它压慢身体。
- **短动作占满整个镜头**：主要动作可以提前完成，后半段用真实对白和反应承担；必要时缩短取用素材，不靠继续漂移或长时间摆姿势填满时长。
- **每句说完才允许下一个行为**：把可以同时发生的听、回应、转身、坐下和手势自然交叠。关键接触或笑点需要停顿时，再单独安排。

时间窗用于表达意图，不是毫秒保证。只标关键开始、接触或完成点，不为每次眨眼和呼吸排表。已有声音引导时，先量其实际说话与停顿，再安排可容纳的动作；不要要求台词与引导音频使用不同节奏。

## 摄影机与动作各写各的

固定机位可直接写明固定双人中近景及需要保持可见的脸、手或支撑点；演员仍按行动路径运动。不必为每个物件反复要求像素固定。

需要运镜时，只描述当前镜头有动机、可执行的相机路径及幅度。不要同时要求跟拍与背景像素固定，也不要用两个不相容机位的首尾图代替摄影机路径设计。

“不切镜”“不中途换姿”的要求能表达目标，却不能保证模型严格执行。出现问题时检查原生输出、约束和引导关系，而不是只重复更强烈的自然、流畅等形容词。

## 示例：一个镜头里的来回对白与落座

示例起点是两名成年人已经牵手、一人站在空坐垫前。动作和对白应依实际距离及声音时长重估；这段文本只演示怎样保留完整表演，不是固定分镜模板。

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Live-action. A fixed medium two-shot keeps both adults' faces, joined hands and the empty sofa cushion visible. Keep their appearance and the room lighting from the first frame. The woman turns toward the cushion, bends at the hips and knees, and sits beside the man in one continuous, ordinary-paced movement. Their joined hands follow her descent without a pull. While settling onto the cushion, she (S1) says in conversational Mandarin, <d>[Chinese] 今天可算忙完了。</d> He (S2) turns toward her and replies, <d>[Chinese] 辛苦了，先歇一会儿。</d> During his reply she releases his hand onto her lap, looks up at him and relaxes into a small smile; he notices and smiles back. Keep the action and conversation in one uninterrupted shot. Let the reply and her physical reaction overlap naturally.

overall_soundscape: Clear Mandarin conversation over quiet room air, with brief clothing movement and cushion compression.

non_diegetic_music: N/A
```

开始提交前检查起始牵手、松手和各自手臂归属是否明确，取景是否看得见落座过程，台词是否能按拟定镜长自然说完。若源图已经坐稳，改写为坐稳之后的交流，不重演这条动作链。

## 从操作层核对提示词

- 提示词指向的首图、尾图和动作参考，是否真的连接到采样所用条件。
- 单张首图、连续视频前缀、参考视频、声音引导的功能是否被正确区分。
- 台词、动作和引导时间是否共用同一任务时钟，重叠前缀是否计入长度。
- 上游取用镜头或剪点改变后，下游首图、前缀和声音是否同步更新。
- 当前轮改变了哪些变量；若同时改提示词、种子、引导、时长和剪辑，记录为组合修正，不宣布找到了唯一原因。

没有算力时可完成这套语义与接线审查，输出待试方案；不能由此给出渲染效果验收结论。

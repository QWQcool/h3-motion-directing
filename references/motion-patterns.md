# 动作规划与提示词示例

以下为可调整的写法示例，不是效果保证；具体文本未经当前素材渲染验证。人物、服装、动作距离、对白和秒数按任务替换，不依赖任何项目记录。

## 轻量镜头卡

按需要记录下面信息，不强制为简单任务输出完整表格：

```text
镜头目的 / 情绪变化：
首帧：谁在哪里、支撑点、手部状态、视线
主要动作：行动者 → 目标 → 可见路径
动作开始 / 接触 / 完成的大致时间：
对白与反应：哪些可以自然重叠
摄影机与取景：
末状态 / 下一镜如何承接：
参考用途 / 所选模式：
最需要验片确认的一点：
```

动作时长不需要填满整镜。选择能容纳表演的生成时长；多出的尾部可作为剪辑余量，不必要求演员一直缓慢移动。

## 自然落座：从身体路径安排时间

示例起点：人已经站在空坐垫前，脚有支撑，不需要跨越距离或绕行。下面试用约 1.6–2 秒动作窗；换起点、情绪或座位高度时重新估计，不把它当作推荐常数。

下面为 I2VA 写法示例，按约 6.6 秒镜头编排，包含牵手和两句对白；用于说明路径，不要求其他任务沿用这套先后顺序。若情绪和台词允许，说话可以与落座重叠：

```text
For the target video, at 0.00 seconds into the target video, <Picture 1> (from [Shot 1]) is fully referenced.

integrated_multimodal_description: [Shot 1] Live-action. A fixed medium shot shows the adult woman standing immediately in front of the empty left sofa cushion, with the adult man seated beside her, lightly holding her hand. Preserve their appearance, clothing and the room from the first frame. She begins one natural, slightly huffy sit-down immediately. Over about 1.6 to 2.0 seconds, she turns her hips toward the cushion, inclines her torso slightly forward for balance, bends her knees and moves her hips backward and down. Her descent briefly eases as her weight meets the cushion. Her feet stay supported, and his hand follows hers without pulling. By about 2 seconds she is comfortably seated; their joined hands rest low between them. At 2.2 to 3.6 seconds the woman (S1), in clear conversational Mandarin, says <d>[Chinese] 我还没消气呢。</d> He listens. At 4.0 to 5.5 seconds the man (S2), in a warm medium-low Mandarin voice, replies <d>[Chinese] 知道。我听着。</d> Her lips are closed during his reply; her brows relax as she meets his eyes. End with both seated and attentive.

overall_soundscape: Quiet room ambience, brief fabric movement and a soft cushion compression at contact, beneath clear conversational speech.

non_diegetic_music: N/A
```

若动作仍突然坠落，先看首帧与接触姿态是否相容、膝与重心过程是否存在，再增加运动时间或放松不相容的引导。不要只替换成 `slowly sits`。

## 抚脸：把轻接触与抬手速度分开

先判断手离脸的距离、是否经过遮挡以及眼镜位置，再给抬手和接触分配时间。只有确实需要约束接触位置时，才增加与动作路径相容的引导图。

用于动作段落的改写示例：

```text
As she finishes her question, he raises his right hand in one continuous movement and reaches her outer cheek over about 0.7 seconds. His fingertips make light contact below the eyeglass frame, then relax against the cheek. The approach is at ordinary human speed; the contact is gentle. He gives his reply while she listens, her gaze softening toward him.
```

这里约 0.7 秒仅是示例时间。首帧若手已在脸旁、远离身体或被遮挡，重新判断路径。不要把到达尾帧的时刻自动当作整个抬手动作的结束时刻。

## 近景倾听：用具体回应承担停顿

固定机位和身体已有支撑时，小幅表演可以合理。明确角色在听什么、何时改变表情，避免整镜只写“保持微笑”。

```text
The woman remains seated in close-up while the man speaks from off camera to her right. Her lips stay closed during his line. At his reassurance she glances briefly toward their joined hands, returns her gaze to his face and releases the tension in her eyebrows. A small smile appears before her reply.
```

这是新编写示例。不要机械添加眨眼、点头、看手、回望的全套动作；只保留与当前台词相关的反应。紧张、沉默或克制的角色可以有更长停顿，但应有剧情理由。

## 参考片中的切镜

先逐段确认参考是在连续表演，还是通过切镜跨过姿态变化。若后一镜已靠肩，生成它时首帧就处于靠肩姿态，并安排之后的情绪反应和台词。不要根据前后两张抽帧推断原片连续完成了转身、拥抱和靠肩。

如果用户要求连续镜头，检查路径并单独验证；不能擅自用切镜省略必须看见的动作。

## 动作迁移的适用条件

优先选能看清目标动作与接触关系的片段。身体动作需要看见关键支撑点，脸部表演需要足够近的面部画面；遮挡、切镜和变化很大的体型会增加判断难度。

核实 Ref2VA 支持后，按官方格式分别写清人物外观、动作参考、环境、摄影机和声音来源。需要保留参考节奏时，不再写另一套相冲突的动作顺序或任意加速时间窗。将“参考动作，重新设计节奏”与“保留动作和时间结构”说明白。

动作迁移的能力声明与当前素材上的验证分别记录，不能因节点支持参考视频就声称已解决全部动作问题。

## 常见反馈的修改方向

- **像慢动作**：查找长时间的接近过程、动作被平均铺满镜头、继承的慢速词和相隔过久的台词。明确完成窗及后续表演。
- **像静态照片**：检查首尾帧是否相同、姿态限制是否覆盖全身、动作是否在画外；增加与台词有关且当前景别能看见的行为。
- **太快或太硬**：检查是否省略平衡与收势、是否过早强制到达参考姿态、动作数量是否超出时长。
- **反复上下或来回移动**：对照引导图的时间顺序、透视和支撑点；必要时简化引导或重做不兼容的参考。
- **动作自然但片子无聊**：调整开场信息、景别、对白节奏和反应镜头；单纯加大动作速度未必改善吸引力。
- **转场突变**：先确定是生成片内的问题还是拼接点的问题，分别检查原生帧和补帧后素材。

这些是诊断入口，不是已证明的一一因果关系。

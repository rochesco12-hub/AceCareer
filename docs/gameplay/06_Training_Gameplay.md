# Ace Career Gameplay Bible
# 06 · Training Gameplay

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Training Gameplay 定义 Ace Career 中训练周的完整玩法。

训练不是：

点击一下。

↓

能力 +1。

而应该像现实职业球员一样：

制定训练计划。

↓

执行训练。

↓

观察成长。

↓

调整方向。

↓

迎接下一项赛事。

训练的意义不是短期提升能力。

而是决定：

未来几年，你会成长为什么样的球员。

---

# Design Goal

训练必须满足四个目标：

① 玩家每周都要思考训练什么

② 不存在万能训练方案

③ 每一次训练都会影响未来

④ 玩家能够明显感受到成长

训练不是填时间。

训练本身就是游戏。

---

# Training Philosophy

现实职业球员。

一年训练远远多于比赛。

真正决定职业高度的。

不是比赛。

而是长期训练。

因此：

Ace Career 中：

比赛负责验证实力。

训练负责创造实力。

---

# Training Loop

完整训练循环：

```text
Training Week
↓
Coach Analysis
↓
Set Weekly Goal
↓
Choose Training Blocks
↓
Complete Training
↓
Receive Feedback
↓
Attribute Growth
↓
Prepare Next Tournament
```

整个过程。

控制在一分钟左右完成。

---

# Weekly Training Goal

每个训练周开始。

玩家首先选择：

本周目标。

例如：

```text
Improve Serve
Improve Movement
Improve Endurance
Prepare Clay Season
Recover Body
Peak For Wimbledon
```

训练目标。

决定整个训练方向。

而不是每次重新选择。

---

# Coach Recommendation

进入训练周。

教练自动分析：

例如：

```text
Coach Report
Serve has become a weakness.
Recommend:
2 Serve Sessions
1 Recovery Session
```

或者：

```text
Movement is excellent.
Focus on Mental Training.
```

玩家：

可以采纳。

也可以完全忽略。

---

# Training Blocks

每周默认拥有：

3 个 Training Block。

例如：

```text
Monday
Serve
Wednesday
Strength
Friday
Recovery
```

不会细化到每天。

保持职业规划节奏。

---

# Training Categories

训练分为六类。

Technical

Physical

Mental

Recovery

Strategy

Serve

每一类都有：

不同成长。

不同疲劳。

不同伤病风险。

---

# Technical Training

例如：

```text
Forehand
Backhand
Volley
Slice
Return
```

特点：

成长稳定。

Fatigue 中等。

适合全年安排。

---

# Physical Training

例如：

```text
Strength
Speed
Endurance
Agility
```

特点：

成长快。

Fatigue 高。

伤病风险增加。

适合休赛期。

---

# Mental Training

例如：

```text
Focus
Confidence
Pressure
Composure
```

特点：

成长慢。

Fatigue 很低。

Grand Slam 前价值很高。

---

# Recovery Training

包括：

Stretch

Yoga

Mobility

Massage

Ice Bath

不会增加能力。

只负责：

恢复。

---

# Strategy Training

例如：

Opponent Analysis

Match Review

Serve Pattern

Return Position

未来：

影响 Match AI。

不是直接加能力。

---

# Training Intensity

每个 Block。

可以选择：

```text
Light
Medium
Heavy
Recovery
```

例如：

Heavy：

成长最高。

Fatigue 最大。

Recovery：

成长没有。

恢复最快。

不存在最佳方案。

---

# Training Preview

玩家确认之前。

系统自动预览。

例如：

```text
Serve
+0.8
Fatigue
+12
Injury Risk
+2%
```

玩家知道：

自己正在交换什么。

---

# Training Execution

确认以后。

系统自动完成训练。

Today 页面：

播放成长动画。

例如：

```text
Serve Practice Complete
Serve Accuracy
+1
Confidence
+2
```

整个过程：

十秒以内。

---

# Weekly Report

训练结束。

自动生成：

```text
Training Summary
Serve
+1
Forehand
+0
Endurance
+1
Confidence
+3
Fatigue
+15
```

帮助玩家理解：

训练成果。

---

# Visible Progress

成长必须：

肉眼可见。

例如：

不是：

Overall：

79 → 80。

而是：

```text
Serve Accuracy
84
↑1
First Serve %
76%
→79%
```

玩家更容易理解。

---

# Long-Term Development

连续训练。

形成：

职业特点。

例如：

连续一年：

Serve。

↓

Serve Bot。

连续一年：

Movement。

↓

Counter Puncher。

玩家不用选择打法。

打法自然形成。

---

# Seasonal Training

不同赛季。

推荐不同训练。

例如：

澳网前：

Hard Court。

法网前：

Endurance。

草地赛季：

Serve。

US Open：

Recovery。

整个训练。

围绕赛季变化。

---

# Peak Planning

训练真正的玩法。

来自：

Peak。

例如：

玩家知道：

三周后。

法网开始。

因此：

提前：

训练。

恢复。

减量。

最终：

法网达到：

最佳状态。

职业规划。

真正开始。

---

# Training During Tournament

比赛周。

依然可以训练。

但是：

只能：

Light。

Recovery。

不允许：

Heavy Training。

现实职业球员。

也不会：

比赛期间练力量。

---

# Injury Prevention

训练页面。

始终显示：

```text
Current Fatigue
68
Recommended
Recovery
```

如果继续 Heavy。

系统：

黄色提示。

不是禁止。

最终：

玩家决定。

---

# AI Training

AI 完全使用：

同一套系统。

不会：

自动：

能力 +1。

AI：

也要：

训练。

恢复。

成长。

整个世界公平。

---

# Emotional Feedback

完成一周训练。

玩家应该获得：

成长感。

而不是：

数值变化。

例如：

```text
Coach
Serve has improved significantly.
You are ready for Wimbledon.
```

一句评价。

往往比：

+1。

更有成就感。

---

# UX Rules

训练页面：

最多展示：

三个训练 Block。

所有成长：

可预览。

所有风险：

可预览。

整个流程：

一分钟完成。

避免：

复杂 Build。

复杂技能树。

---

# Success Metrics

训练玩法完成以后。

玩家应该：

期待训练周。

为了 Grand Slam。

主动安排训练。

开始真正规划赛季。

而不是：

随便点击。

如果玩家开始思考：

"这周我要不要练发球？"

而不是：

"随便练一下。"

那么：

Training Gameplay 就成功了。

---

# Definition of Done

✓ 每周拥有训练规划

✓ 教练自动提供建议

✓ 三个 Training Block 足够形成策略

✓ 不存在万能训练方案

✓ 长期形成不同打法

✓ Peak Planning 成为重要玩法

✓ AI 与玩家训练规则一致

✓ 玩家能够持续感受到成长

Training 不是能力提升系统。

Training 是职业球员成长的开始。

---

End of Document

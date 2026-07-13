# Ace Career Gameplay Bible
# 07 · Recovery Gameplay

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Recovery Gameplay 定义 Ace Career 中恢复周（Recovery Week）的完整玩法。

恢复不是：

等待。

更不是：

点击 Continue。

恢复本身就是职业规划的重要组成部分。

现实职业球员并不是：

训练越多越强。

比赛越多越强。

真正优秀的球员：

知道什么时候应该恢复。

什么时候应该停止。

什么时候应该为下一项赛事储备状态。

---

# Design Goal

Recovery Gameplay 必须满足：

① 恢复本身具有玩法

② 玩家愿意主动安排恢复

③ 恢复影响未来比赛

④ 不恢复一定会付出代价

恢复不是奖励。

而是一种职业选择。

---

# Recovery Philosophy

现实职业球员。

一年中真正比赛时间不到十分之一。

更多时间：

恢复。

旅行。

治疗。

调整状态。

因此：

Recovery 不是训练的附属品。

Recovery 是职业生涯的重要组成部分。

---

# Recovery Loop

完整恢复循环：

```text
Recovery Needed
↓
Health Analysis
↓
Choose Recovery Plan
↓
Recovery Week
↓
Physical Improvement
↓
Mental Recovery
↓
Ready For Next Tournament
```

整个过程：

控制在一分钟左右。

---

# When Recovery Starts

系统不会强制恢复。

而是在以下情况主动建议：

Fatigue > 70

连续比赛两周以上

Minor Injury

长途旅行结束

Grand Slam结束

连续多场三盘大战

玩家：

始终拥有选择权。

---

# Recovery Analysis

进入恢复周。

Today 自动生成：

Recovery Report。

例如：

```text
Recovery Report
Fatigue
76
Confidence
58
Body Status
Overloaded
Coach Recommendation
Recovery Week
```

让玩家知道：

为什么应该休息。

---

# Recovery Options

恢复不是唯一方案。

玩家拥有四种选择。

```text
Complete Rest
↓
Active Recovery
↓
Medical Recovery
↓
Mental Recovery
```

不同恢复。

效果不同。

---

# Complete Rest

完全休息。

特点：

Fatigue恢复最快。

Confidence小幅提升。

不会成长能力。

适合：

连续比赛后。

---

# Active Recovery

例如：

```text
Stretch
Mobility
Swimming
Yoga
```

恢复速度：

中等。

同时保持身体状态。

不会完全停滞。

---

# Medical Recovery

包括：

Physio

Massage

Ice Bath

Medical Treatment

恢复最快。

但需要：

花费现金。

不同医疗团队。

恢复效率不同。

---

# Mental Recovery

例如：

```text
Vacation
Family
Meditation
Sports Psychology
```

恢复：

Confidence。

减少：

Mental Fatigue。

Grand Slam失利后。

价值极高。

---

# Recovery Planning

玩家不是恢复一天。

而是规划：

这一周。

例如：

```text
Recovery Week
Monday
Massage
Wednesday
Yoga
Friday
Swimming
```

恢复拥有：

自己的节奏。

---

# Recovery Preview

玩家选择方案前。

自动显示：

```text
Fatigue
-28
Confidence
+5
Fitness
+2
Cost
$1,500
```

帮助玩家：

做职业选择。

---

# Coach Advice

恢复期间。

教练持续提供建议。

例如：

```text
Coach
Do not return too early.
You are still recovering.
```

玩家：

依然可以提前报名。

承担风险。

---

# Injury Recovery

如果存在伤病。

Today 自动切换：

Recovery Mode。

例如：

```text
Back Injury
Recovery Progress
63%
Estimated Return
2 Weeks
```

玩家每天（每周）都能看到恢复进度。

---

# Returning Too Early

这是恢复玩法的重要部分。

例如：

系统提示：

```text
Current Recovery
72%
Recommended
Wait One More Week
```

玩家可以：

提前复出。

但：

伤病复发概率增加。

真正形成：

职业决策。

---

# Recovery During Tournament

比赛期间。

恢复变成：

Between Match Recovery。

例如：

赢下：

Quarterfinal。

Today：

自动进入：

Recovery。

玩家选择：

Massage。

Ice Bath。

Recovery Training。

第二天：

Semifinal。

恢复质量。

影响下一场。

---

# Recovery Benefits

恢复不仅减少：

Fatigue。

还影响：

Confidence。

Injury Risk。

Training Efficiency。

Match Readiness。

长期恢复好的球员。

职业寿命更长。

---

# Seasonal Recovery

不同阶段。

恢复策略不同。

例如：

澳网后：

休息。

法网前：

保持训练。

温网后：

恢复身体。

ATP Finals后：

进入Off Season。

恢复开始服务：

整个赛季。

---

# Peak Recovery

恢复真正的玩法。

来自：

Peak。

例如：

玩家知道：

两周后：

温网。

于是：

连续恢复。

保持状态。

比赛当天：

Fatigue

18。

这是职业规划。

不是随机。

---

# Mental Recovery

输掉重要比赛以后。

系统推荐：

Mental Recovery。

例如：

```text
Confidence
43
Recommended
Sports Psychology
```

恢复以后：

Confidence：

缓慢提高。

而不是：

自动恢复。

---

# Financial Trade-Off

恢复需要成本。

例如：

普通按摩：

$300。

ATP级Physio：

$1,500。

Recovery Camp：

$5,000。

有钱。

恢复更快。

但：

长期现金流更紧张。

---

# Recovery Feedback

恢复结束。

Today：

自动生成：

```text
Recovery Complete
Fatigue
76 → 31
Confidence
58 → 67
Body Status
Excellent
```

玩家感受到：

身体真正恢复。

---

# Ready Status

恢复完成以后。

Today：

Primary Card：

自动变化。

例如：

```text
Ready For Competition
Next Tournament
Rome Masters
Entry Opens Tomorrow
```

恢复自然连接：

下一站赛事。

---

# Emotional Curve

恢复周。

情绪变化：

```text
疲惫
↓
决定休息
↓
身体恢复
↓
重新充满期待
↓
准备下一项赛事
```

恢复不是无聊。

而是：

重新积蓄力量。

---

# UX Rules

恢复页面：

保持安静。

减少：

红色。

增加：

绿色。

动画：

缓慢。

整个页面。

营造：

放松感。

区别于比赛周。

---

# Success Metrics

Recovery Gameplay 完成以后。

玩家应该：

主动安排恢复。

而不是：

被迫恢复。

甚至会开始思考：

"为了法网。

这一周值得休息。"

而不是：

"恢复就是浪费时间。"

---

# Definition of Done

✓ Recovery 成为独立玩法

✓ 玩家主动选择恢复方式

✓ Fatigue 合理下降

✓ Confidence 可以恢复

✓ 伤病恢复拥有阶段

✓ 提前复出拥有风险

✓ 恢复连接下一项赛事

✓ 玩家愿意主动安排 Recovery Week

Recovery 不是暂停游戏。

Recovery 是职业球员成长过程中最重要的一周。

---

End of Document

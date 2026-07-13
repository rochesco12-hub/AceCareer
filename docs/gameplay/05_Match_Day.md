# Ace Career Gameplay Bible
# 05 · Match Day

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Match Day 是 Ace Career 情绪价值最高的一天。

它不是点击：

Start Match

↓

Finish Match

而是职业球员真正的比赛日。

现实职业球员在比赛当天：

醒来。

↓

查看赛程。

↓

早餐。

↓

热身。

↓

教练会议。

↓

进入球场。

↓

比赛。

↓

采访。

↓

恢复。

↓

准备下一轮。

Ace Career 应该完整还原这种体验。

---

# Design Goal

Match Day 必须让玩家感受到：

> 今天是比赛日。

整个 Today 页面。

整个 UI。

整个节奏。

全部围绕：

今天这一场比赛。

比赛结束以后。

玩家应该真正感受到：

今天结束了。

而不是：

只是模拟了一场比赛。

---

# Design Philosophy

比赛。

不是玩法。

比赛日。

才是玩法。

真正让玩家期待的不是：

比分。

而是：

今天到底会发生什么。

所以：

整个 Match Day。

应该像：

F1 Race Weekend

Football Manager Match Day

Apple Sports

融合后的体验。

---

# Match Day Timeline

比赛日固定流程：

```text
Morning
↓
Coach Briefing
↓
Match Preparation
↓
Match
↓
Post Match
↓
Recovery
↓
Evening Summary
```

整个过程。

只需要一分钟。

但情绪必须完整。

---

# Match Day Entry

进入 Today。

整个页面自动变化。

例如：

```text
────────────────────
Match Day
Rome Masters
Quarterfinal
────────────────────
vs Carlos Alcaraz
Court Centrale
20:00
────────────────────
Start Match
────────────────────
```

玩家一眼知道：

今天只有这一件事。

---

# Match Header

顶部 Header：

只显示比赛信息。

例如：

```text
Rome Masters
Quarterfinal
```

右侧：

显示：

比赛倒计时。

例如：

```text
Starts In
3 Hours
```

不是：

Fatigue。

不是：

Money。

不是：

Coach。

比赛日。

聚焦比赛。

---

# Opponent Card

Primary Card：

永远展示：

对手。

例如：

```text
Carlos Alcaraz
World No.2
Age
24
Surface
Clay
Head To Head
2-3
Recent Form
WWWWW
```

玩家开始建立期待。

---

# Coach Briefing

比赛开始前。

自动生成：

Coach Brief。

例如：

```text
Coach Notes
His second serve is vulnerable.
Stay aggressive on return.
Avoid long rallies.
Confidence
High
```

这不是增加能力。

而是增加沉浸感。

---

# Match Conditions

比赛前。

展示当前状态。

例如：

```text
Confidence
83
Fatigue
29
Fitness
Excellent
Weather
Sunny
Court
Center Court
```

帮助玩家理解：

为什么这场比赛可能不同。

---

# Storyline

如果存在特殊剧情。

自动显示。

例如：

```text
Career First Masters Quarterfinal
Win Today
↓
Enter Top20
```

或者：

```text
Beat Him Today
↓
Career Head To Head
3-3
```

让比赛拥有意义。

---

# Media Focus

重大比赛。

自动生成媒体标题。

例如：

```text
Can Logan reach his first Masters semifinal?
```

或者：

```text
The biggest match of your career.
```

Grand Slam。

媒体更多。

ITF。

几乎没有。

---

# Warm-Up

比赛前。

允许一次：

Preparation。

例如：

```text
Focus
Serve
Return
Mental
Recovery
```

不是小游戏。

而是：

心理准备。

不同选择：

给予极小 Buff。

例如：

Confidence +2。

Fatigue -3。

---

# Start Match

点击：

Start Match。

进入比赛模拟。

整个 Match Engine 开始运行。

玩家无需操作击球。

重点始终是：

职业决策。

不是操作。

---

# Live Match

模拟过程中。

展示：

实时文字。

例如：

```text
First Set
4-3
Break Point
...
Ace
...
Tiebreak
...
Match Point
```

重要时刻：

暂停。

增强戏剧感。

而不是：

瞬间结束。

---

# Match Highlights

比赛结束。

自动生成：

Highlights。

例如：

```text
12 Aces
81%
First Serve
Saved
5/6
Break Points
Longest Rally
28 Shots
```

帮助玩家：

回顾比赛。

---

# Emotional Result

赢球。

Today：

自动切换。

例如：

```text
Victory
Into The Semifinal
Career Best
```

输球。

Today：

变成：

```text
Defeat
Quarterfinal Finish
Ranking
+4
```

输赢。

都必须拥有情绪反馈。

---

# Press Conference

重大赛事。

自动出现：

采访。

例如：

```text
How do you feel after today's victory?
```

玩家：

选择回答。

例如：

谦虚。

↓

自信。

↓

感谢团队。

不同回答。

影响：

媒体形象。

Confidence。

未来：

Sponsor。

---

# Recovery

比赛结束。

立即进入恢复阶段。

Today：

Primary Card：

自动切换。

例如：

```text
Recovery
Fatigue
61
Recommended
Massage
```

玩家决定：

恢复。

训练。

分析下一轮。

---

# Next Opponent

如果晋级。

立即显示：

下一轮。

例如：

```text
Semifinal
vs Jannik Sinner
```

形成新的期待。

玩家很自然：

继续下一天（下一周阶段）。

---

# Match Day Without Match

如果今天：

轮空。

或者：

休息。

Today：

显示：

Recovery Day。

例如：

```text
Practice Court
Recovery
Watch Opponent
```

依然有内容。

不会空。

---

# Grand Slam Match Day

Grand Slam。

整个 Today 自动升级。

例如：

背景。

动画。

奖杯。

观众。

新闻。

全部更隆重。

玩家能够：

一眼知道。

今天：

不是普通比赛。

---

# Career Milestones

如果今天：

可能创造纪录。

Today：

提前提示。

例如：

```text
Win Today
↓
First ATP Final
```

或者：

```text
Win Today
↓
World No.1
```

这种提示。

极大增加：

比赛张力。

---

# Match Day Emotion Curve

整个比赛日。

应该经历：

```text
期待
↓
分析
↓
紧张
↓
比赛
↓
释放
↓
恢复
↓
期待下一轮
```

而不是：

开始。

结束。

---

# UX Rules

比赛日。

Today 页面：

禁止出现：

训练计划。

长期统计。

复杂菜单。

所有视觉中心：

全部围绕：

今天这一场比赛。

---

# Success Metrics

Match Day 完成以后。

玩家应该：

打开 App。

↓

看到今天的比赛。

↓

期待开始。

↓

比赛结束获得巨大反馈。

↓

马上查看下一轮。

↓

继续 Career。

如果玩家会因为：

"今晚有比赛。"

而迫不及待打开 App。

那么 Match Day 就设计成功。

---

# Definition of Done

✓ 比赛日拥有独立 Today 布局

✓ 对手信息清晰

✓ 教练建议自然出现

✓ 比赛前拥有准备阶段

✓ 比赛后拥有恢复阶段

✓ 晋级后立即产生下一目标

✓ 输赢都推动 Career

✓ 每一场重要比赛都值得期待

Match Day 不只是打一场比赛。

它应该成为整个职业生涯中最令人期待的一天。

---

End of Document

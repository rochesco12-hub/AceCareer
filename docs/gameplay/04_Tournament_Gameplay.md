# Ace Career Gameplay Bible
# 04 · Tournament Gameplay

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Tournament Gameplay 定义玩家从决定报名一项赛事，到离开赛事的完整体验。

赛事不是一张签表。

也不是几场比赛。

它应该像现实 ATP 球员一样，是一次完整的"职业旅程（Tournament Journey）"。

玩家真正体验的是：

决定是否参赛

↓

来到比赛城市

↓

备战

↓

比赛

↓

恢复

↓

离开

而不是：

点击开始比赛。

↓

比赛结束。

↓

继续下一周。

---

# Design Goal

每一项赛事，都应该拥有自己的节奏。

无论是一站 ITF。

还是 Grand Slam。

玩家都应该感受到：

自己真正来到了一项赛事。

不同等级赛事。

体验应该明显不同。

---

# Tournament Journey

整个赛事生命周期：

```text
Tournament Available
↓
Entry Decision
↓
Acceptance
↓
Travel
↓
Arrival
↓
Tournament Week
↓
Tournament Finish
↓
Career Update
↓
Leave Tournament
```

玩家完整经历一次赛事。

而不是只打一场比赛。

---

# Stage 1

## Tournament Discovery

每周开放新的赛事。

Today 页面自动推荐：

例如：

```text
Recommended Tournament
ATP250 Doha
Hard Court
Prize Money
$620,000
Expected Result
Quarterfinal
Entry Deadline
3 Days
```

玩家首先看到的是：

"我有哪些选择。"

而不是：

"系统安排好了。"

---

# Stage 2

## Tournament Selection

玩家开始比较赛事。

例如：

```text
ATP250 Doha
Hard
预计积分
45
预计奖金
$28,000
预计胜率
61%
```

另一站：

```text
Challenger Phoenix
Hard
预计积分
80
预计奖金
$18,000
预计胜率
82%
```

第三站：

```text
休息一周
恢复
+35
伤病风险
-20%
```

真正的玩法来自：

比较。

而不是：

报名。

---

# Decision Psychology

报名时。

玩家应该思考：

我要冲积分？

还是赚钱？

还是恢复？

还是保排名？

任何选择。

都必须有代价。

---

# Stage 3

## Acceptance

报名结束后。

公布 Acceptance。

例如：

```text
Accepted
Seed 6
```

或者：

```text
Qualification
Seed 2
```

或者：

```text
Alternate
Waiting List #3
```

Acceptance 本身就是一种反馈。

而不是直接生成签表。

---

# Stage 4

## Travel

确认参赛以后。

进入旅行阶段。

例如：

```text
Travel
Barcelona
↓
Rome
```

旅行自动产生：

Fatigue

Travel Cost

Jet Lag（未来）

不同距离。

影响不同。

---

# Stage 5

## Arrival

抵达赛事。

Today 页面立即变化。

例如：

```text
Rome Masters
Tournament Week
Round Begins Tomorrow
```

下面出现：

Practice

Draw

Coach

Players

News

整个 Today 已经进入赛事模式。

---

# Arrival Feeling

玩家应该有：

"我来到了一项赛事。"

而不是：

"进入一个菜单。"

这是一种情绪变化。

---

# Stage 6

## Draw Release

签表公布。

玩家第一件事情：

不是比赛。

而是：

研究签表。

例如：

```text
Round1
Musetti
Round2
Rune
Quarterfinal
Sinner
Semifinal
Alcaraz
```

玩家开始思考：

这一站。

能走多远。

---

# Coach Briefing

签表公布后。

教练自动分析。

例如：

```text
Round1
Musetti
Clay Specialist
建议：
加强发球。
减少多拍。
```

玩家可以：

查看。

忽略。

或者调整训练。

---

# Practice Session

比赛开始前。

允许一次：

Practice。

不是小游戏。

而是：

选择重点。

例如：

```text
Serve
Return
Movement
Recovery
```

不同训练。

影响：

第一轮状态。

---

# Match Flow

比赛周。

Today 页面始终只关注：

下一场比赛。

例如：

```text
Next Match
Round 2
vs Jack Draper
Today
20:00
```

所有其它信息。

自动退居次要位置。

---

# Between Matches

比赛结束以后。

玩家不会立即进入下一轮。

而是进入：

Recovery。

Today 自动变化。

例如：

```text
Recovery Day
Fatigue
54
Recovery
Recommended
```

玩家决定：

恢复。

训练。

观看下一轮。

分析对手。

---

# Opponent Preview

下一轮确定以后。

自动生成：

Opponent Card。

例如：

```text
Carlos Alcaraz
World No.2
Hard Court
92%
Last Five
WWWWW
Head To Head
2-3
```

帮助玩家建立期待。

---

# Tournament Momentum

随着晋级。

整个赛事氛围变化。

例如：

Round1

普通。

Quarterfinal

媒体增加。

Semifinal

Today 页面更强调。

Final

背景动画。

奖杯。

新闻。

整个情绪不断升高。

---

# Elimination

如果输球。

整个赛事结束。

Today：

不会立刻进入下一站。

而是：

Tournament Summary。

例如：

```text
Rome Masters
Quarterfinal
Prize Money
$48,000
Points
180
Ranking
+9
```

输球。

依然获得反馈。

---

# Champion Moment

如果夺冠。

Today 完全变化。

例如：

```text
Champion
Rome Masters
Career Title
No.6
Ranking
#12
Career High
```

冠军：

应该拥有整个游戏最强反馈。

---

# Leaving Tournament

赛事结束。

玩家离开比赛城市。

系统自动：

恢复普通 Today。

新的赛事开始开放。

新的世界新闻出现。

新的目标出现。

职业生涯继续。

---

# Tournament Personality

不同赛事。

必须拥有不同体验。

例如：

ITF：

简单。

紧凑。

ATP250：

开始有媒体。

Masters1000：

世界顶级阵容。

Grand Slam：

整个 UI 都发生变化。

玩家必须能够感受到：

赛事等级。

---

# Tournament Identity

每项赛事：

拥有自己的特点。

例如：

Monte Carlo：

红土赛季开始。

Queen's：

草地热身。

Indian Wells：

第五大满贯。

US Open：

夜场。

不仅仅是：

积分不同。

---

# Emotional Curve

一项赛事。

应该拥有完整情绪。

```text
期待
↓
抽签
↓
紧张
↓
赢球
↓
恢复
↓
晋级
↓
决赛
↓
冠军
↓
满足
```

或者：

```text
期待
↓
抽签
↓
首轮出局
↓
失望
↓
重新规划
```

输球也是体验。

---

# UX Rules

赛事期间。

Today 页面：

禁止出现：

训练周内容。

禁止：

大量排行榜。

禁止：

复杂设置。

所有内容：

围绕赛事。

聚焦：

下一场比赛。

---

# Success Metrics

Tournament Gameplay 成功以后。

玩家应该：

期待每一站赛事。

记住不同赛事。

愿意规划赛季。

输球依然觉得：

"下一站继续。"

而不是：

只是完成几场模拟。

---

# Definition of Done

✓ 每项赛事拥有完整生命周期

✓ 报名具有真实决策价值

✓ 抽签形成期待

✓ 比赛之间拥有恢复阶段

✓ 不同赛事拥有不同氛围

✓ 冠军拥有强烈反馈

✓ 输球依然推动 Career

✓ 每项赛事都像一次真正的职业巡回赛经历

Tournament 不只是几场比赛。

Tournament 是职业生涯中一段值得记住的旅程。

---

End of Document

# Ace Career Gameplay Bible
# 10 · Career Goals

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Career Goals 定义玩家整个职业生涯的目标系统。

Ace Career 最大的问题不是：

玩家不知道怎么玩。

而是：

玩家不知道下一步为什么而努力。

Career Goals 的目的就是：

让玩家永远知道：

**自己现在为什么训练。**

**为什么比赛。**

**为什么休息。**

目标，是整个 Career 的驱动力。

---

# Design Goal

Career Goals 必须做到：

① 永远都有目标

② 短期目标容易完成

③ 长期目标值得奋斗

④ 完成一个目标以后，立即出现新的目标

整个职业生涯不能出现：

"我现在不知道该干什么。"

---

# Design Philosophy

现实职业球员。

每个阶段目标完全不同。

18岁：

进入职业巡回赛。

20岁：

进入Top200。

23岁：

进入Top100。

26岁：

赢ATP冠军。

29岁：

冲击Grand Slam。

33岁：

延长职业寿命。

Ace Career 也应该如此。

---

# Goal Pyramid

整个目标系统分为四层。

```text
Weekly Goal
↓
Season Goal
↓
Career Goal
↓
Legacy Goal
```

四层同时存在。

但只有一层是当前重点。

---

# Weekly Goal

玩家每周只有一个主要目标。

例如：

```text
Reach Quarterfinal
Recover From Injury
Improve Serve
Prepare For Wimbledon
Win First Match
```

完成以后。

立即获得反馈。

并生成下一目标。

---

# Weekly Goal Rules

每周目标：

必须满足：

- 一周内可以完成
- 与当前状态有关
- 不会过于困难
- 可以失败

例如：

排名300。

目标不会是：

赢法网。

---

# Season Goal

整个赛季只有一个核心目标。

例如：

```text
Finish Top100
Win Challenger Title
Qualify For Australian Open
Stay Inside Top50
Reach ATP Finals
```

赛季结束。

自动结算。

---

# Dynamic Season Goals

Season Goal：

不是固定。

而是根据：

当前排名。

年龄。

成长。

自动变化。

例如：

排名：

275。

系统推荐：

```text
Finish Top200
```

不是：

世界第一。

---

# Career Goals

Career Goal：

贯穿多年。

例如：

```text
First ATP Title
First Masters
First Grand Slam
World No.1
Olympic Gold
Hall Of Fame
```

这些目标。

完成周期：

数年。

---

# Legacy Goals

这是最终目标。

例如：

```text
Win 10 Grand Slams
300 Weeks No.1
100 Titles
Career Golden Slam
Become GOAT
```

不是所有玩家都会完成。

但永远存在。

---

# Goal Generation

系统自动生成目标。

依据：

Current Ranking

Age

Potential

Career Stage

Current Form

Coach Opinion

不会：

随机生成。

---

# Goal Recommendation

教练参与目标制定。

例如：

```text
Coach Recommendation
Top50 Is Realistic This Year.
```

或者：

```text
Forget Rankings.
Prepare For Clay Season.
```

目标开始具有职业感。

---

# Progress Visualization

所有目标。

必须拥有进度。

例如：

```text
Top50
Current
84
██████░░░░
84 → 50
```

玩家始终看到：

自己离目标还有多远。

---

# Milestone Goals

重大节点。

自动生成。

例如：

```text
Career First ATP Win
Win First Match
Progress
0/1
```

完成以后。

立刻庆祝。

---

# Hidden Goals

系统拥有：

隐藏目标。

例如：

连续三站八强。

连续二十场胜利。

一年不受伤。

玩家不知道。

完成以后：

突然解锁。

增强惊喜。

---

# Failure

目标允许失败。

例如：

赛季目标：

Top100。

最终：

112。

系统不会：

Game Over。

而是：

重新制定：

下一赛季目标。

失败也是成长。

---

# Adaptive Goals

如果玩家成长特别快。

目标自动提高。

例如：

原目标：

Top100。

提前完成。

系统立即调整：

Top50。

玩家不会失去动力。

---

# Personal Goals

玩家也可以：

自定义目标。

例如：

```text
Win Wimbledon
Beat Alcaraz
Become No.1 Before Age30
```

不会影响系统。

但会加入：

Career Timeline。

---

# Goal Rewards

完成目标。

奖励：

不是金币。

而是：

Career Feedback。

例如：

新闻。

媒体。

Coach Praise。

Confidence。

Hall Of Fame Progress。

Achievement。

整个职业世界认可你。

---

# Goal History

Career 自动记录：

```text
2027
Entered Top100
2028
Won First ATP Title
2029
Reached Top10
2031
World No.1
```

形成职业时间线。

---

# Goal Evolution

随着年龄增长。

目标变化。

例如：

年轻：

成长。

巅峰：

冠军。

老将：

纪录。

退役前：

Legacy。

整个职业目标不断变化。

---

# Today Integration

Today 页面：

永远展示：

唯一目标。

例如：

```text
Current Goal
Reach Top50
Progress
84 → 50
```

这是整个 Today 的长期方向。

---

# Career Psychology

目标最大的作用。

不是奖励。

而是：

每天告诉玩家：

为什么继续。

如果玩家知道：

"再赢两场。

我就进入Top50。"

那么：

继续下一周。

变得非常自然。

---

# Emotional Curve

目标系统：

应该形成：

```text
设定目标
↓
努力
↓
接近目标
↓
突破
↓
庆祝
↓
新的目标
```

玩家始终拥有：

前进方向。

---

# UX Rules

Today：

只显示：

一个主要目标。

不要：

同时出现：

十个任务。

玩家永远知道：

现在最重要的事情。

---

# Success Metrics

Career Goals 完成以后。

玩家应该：

每天知道：

为什么继续。

每个月完成：

一个中期目标。

每个赛季：

拥有一个长期目标。

每个职业生涯：

拥有一个传奇梦想。

---

# Definition of Done

✓ Weekly Goal 自动生成

✓ Season Goal 动态调整

✓ Career Goal 长期存在

✓ Legacy Goal 永远驱动玩家

✓ 目标始终具有进度反馈

✓ 失败不会终止 Career

✓ Today 永远展示当前目标

Career Goals 不是任务系统。

Career Goals 是整个职业生涯前进的意义。

---

End of Document

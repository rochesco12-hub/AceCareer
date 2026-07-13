# Ace Career Gameplay Bible
# 02 · Today Page

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Today Page 是 Ace Career 最重要的页面。

玩家打开 App 后，95% 的时间都应该停留在这里。

它不是首页。

它就是游戏本身。

如果 Today Page 做得不好，那么整个 Career Mode 都会变成：

打开 App

↓

找按钮

↓

找比赛

↓

找训练

↓

关闭 App

而不是：

打开 App

↓

立即知道今天发生了什么

↓

立即知道应该做什么

↓

做决定

↓

进入下一周

Today Page 的目标只有一句话：

> **让玩家在 5 秒内理解自己的职业生涯现在发生了什么。**

---

# Design Goals

Today 页面需要同时完成五件事情：

① 告诉玩家世界发生了什么

② 告诉玩家自己发生了什么

③ 告诉玩家本周最重要的事情

④ 提供最快的操作入口

⑤ 让玩家期待进入下一周

如果任何一个目标失败。

Today 页面就是失败的。

---

# Design Philosophy

Today 不是 Dashboard。

Today 是：

职业球员今天的生活。

玩家看到的不应该是：

二十多个按钮。

而应该像：

每天醒来。

打开自己的职业日程。

所以：

Today 更像：

Apple Calendar

+

Apple Fitness

+

Football Manager Inbox

+

Apple Sports

融合后的体验。

---

# The One Screen Principle

Today 永远遵守：

One Screen Principle。

默认情况下：

**第一页不允许纵向滚动。**

所有最重要的信息。

必须全部出现在一屏内。

如果需要更多信息。

使用：

Tab

Sheet

Bottom Sheet

Popover

而不是：

无限向下滚。

---

# Page Structure

Today 页面分为五个区域。

```text
────────────────────
Week Header
────────────────────
Primary Focus Card
────────────────────
Quick Status
────────────────────
Quick Actions
────────────────────
Bottom Tabs
────────────────────
```

整个页面：

控制在一个屏幕内。

---

# Week Header

顶部只保留最重要的信息。

例如：

```text
Week 18
ATP250 Doha
Season 2028
```

右侧：

世界排名。

```text
#84
↑6
```

点击：

进入完整 Ranking。

Header 不展示：

Fatigue。

Money。

Coach。

这些全部放下面。

Header 永远保持干净。

---

# Primary Focus Card

这是整个 Today 的核心。

占据页面最大面积。

它永远只展示：

**本周最重要的一件事情。**

例如：

比赛周：

```text
Quarterfinal
Doha ATP250
Tonight
vs Jack Draper
Start Match
```

训练周：

```text
Training Week
Serve Improvement
2 Sessions Left
```

恢复周：

```text
Recovery Week
Back Injury
Estimated Recovery
2 Weeks
```

休赛期：

```text
Off Season
Build For Next Season
```

玩家不用思考。

打开就知道：

现在最重要的事情是什么。

---

# Dynamic Focus

Primary Card：

不是固定。

它根据职业状态变化。

例如：

比赛周：

显示：

下一场比赛。

受伤：

显示：

Recovery。

赛季结束：

显示：

Season Summary。

世界第一：

显示：

Congratulations。

Grand Slam：

显示：

Tournament。

Today 永远围绕：

当前最重要事件。

---

# Quick Status

下面只有四个状态。

全部采用：

Apple Watch 风格。

```text
Health
🟢 Excellent
Ranking
#84
Money
$182,000
Confidence
82
```

点击：

进入详情。

默认：

只显示摘要。

---

# Quick Actions

Quick Action：

永远只有四个。

根据状态变化。

例如：

比赛周：

```text
Start Match
Training
Recovery
Calendar
```

恢复周：

```text
Recovery
Gym
Coach
Calendar
```

休赛期：

```text
Training
Travel
Coach
Next Week
```

按钮绝不能超过四个。

---

# Bottom Navigation

底部采用：

三个 Tab。

```text
News
Career
World
```

Today：

始终保持首页。

News：

查看职业新闻。

Career：

查看个人职业数据。

World：

查看赛历。

排名。

球员。

---

# News Tab

新闻不是单独首页。

而是：

Today 的延伸。

例如：

```text
Sinner wins Rome Masters
You reach Career High
Alcaraz withdraws
Djokovic retires
```

点击：

展开详情。

---

# Career Tab

Career：

显示：

长期目标。

例如：

Career High

Titles

Grand Slam

Legacy

Hall Of Fame Progress

这里不是操作页面。

而是：

长期反馈。

---

# World Tab

World：

展示：

整个职业巡回赛。

包括：

Calendar

Ranking

Tournament

Players

Records

这里更像：

ATP 官网。

---

# Week Modes

Today 根据不同 Week。

自动切换。

支持：

Match Week

Training Week

Recovery Week

Travel Week

Off Season

Grand Slam Week

每种状态：

布局不同。

但信息结构一致。

---

# Match Week

比赛周：

Primary Card：

显示：

下一场比赛。

Quick Action：

Start Match。

Coach Advice：

自动出现。

例如：

```text
Attack His Second Serve
Confidence
High
```

---

# Recovery Week

Primary：

Recovery。

下面：

Recovery Progress。

预计：

恢复：

2 Weeks。

按钮：

Recovery。

Massage。

Gym。

---

# Off Season

Primary：

Season Review。

按钮：

Training。

Coach。

Schedule。

Goals。

玩家开始规划下一赛季。

---

# Grand Slam Week

Primary Card：

明显放大。

例如：

```text
Australian Open
Round 3
vs Carlos Alcaraz
```

整个页面：

营造：

重大赛事氛围。

---

# Progress Feedback

Today 必须不断反馈成长。

例如：

本周：

```text
Ranking
84
↑6
Career High
New
```

或者：

```text
Serve
+1
Confidence
+3
```

成长：

必须每天可见。

---

# Coach Card

如果本周存在建议。

自动出现。

例如：

```text
Coach Recommendation
Rest This Week
Fatigue
83
```

点击：

查看分析。

玩家：

可忽略。

---

# Goal Card

长期目标：

始终可见。

例如：

```text
Current Goal
Enter Top50
Progress
84 → 50
```

完成以后。

自动切换：

下一目标。

---

# One More Week

Today 最下面。

始终存在：

Continue Week。

这是整个游戏：

最重要按钮。

所有内容：

都应该让玩家：

忍不住点击它。

---

# Empty State

如果本周：

没有比赛。

Today：

绝不能空。

而应该：

推荐：

训练。

恢复。

观看比赛。

分析对手。

规划赛程。

玩家始终有事可做。

---

# UX Rules

Today：

禁止：

二级菜单。

禁止：

超过四个主要按钮。

禁止：

长列表。

禁止：

复杂表格。

打开：

三秒内。

玩家必须知道：

现在。

应该做什么。

---

# Success Metrics

Today 页面完成以后。

玩家应该：

打开 App。

↓

五秒内。

理解本周。

↓

十秒内。

完成决策。

↓

一分钟内。

开始推进 Career。

如果玩家每天都会打开 Today。

即使没有比赛。

Today 就设计成功。

---

# Definition of Done

Today Page 完成标准：

✓ 首屏无滚动

✓ 当前目标唯一明确

✓ 四个以内 Quick Action

✓ 根据职业状态自动变化

✓ 每周都有成长反馈

✓ 每天打开都有新内容

✓ 引导玩家继续下一周

Today 不是首页。

Today 就是 Ace Career。

---

End of Document

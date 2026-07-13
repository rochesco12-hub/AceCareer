# Ace Career Gameplay Bible
# 15 · UX Flow

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

UX Flow 定义玩家打开 Ace Career 后，每一分钟应该发生什么。

它不是页面设计。

而是：

玩家行为设计（User Behavior Design）。

好的 UX。

不是按钮漂亮。

而是：

玩家永远知道：

下一步应该做什么。

---

# Design Goal

整个 UX 必须满足：

① 永远只有一个主要任务

② 不需要思考页面在哪里

③ 所有操作三步以内完成

④ 每次打开 App 都有新的反馈

玩家不会寻找功能。

功能主动来到玩家面前。

---

# Design Philosophy

Ace Career 采用：

**Flow First（流程优先）**

而不是：

**Page First（页面优先）**

玩家玩的不是页面。

玩家玩的是：

职业生涯。

所以：

页面只是流程中的一站。

不是目的。

---

# The 3 Second Rule

玩家打开 App。

三秒内必须知道：

① 我现在在哪一周

② 我现在最重要的事情是什么

③ 我应该点击哪里

如果三秒内还在找按钮。

UX 就失败了。

---

# Primary Flow

整个游戏。

只有一条主流程。

```text
Open App
↓
Today
↓
Decision
↓
Action
↓
Feedback
↓
Continue Week
```

所有功能。

最终都必须回到：

Today。

---

# Today Is Home

任何页面。

完成以后。

默认返回：

Today。

例如：

训练完成。

↓

Today。

比赛结束。

↓

Today。

恢复结束。

↓

Today。

玩家永远不会迷路。

---

# One Primary Action

任何时候。

Today 页面。

只有一个主按钮。

例如：

比赛周：

```text
Start Match
```

训练周：

```text
Start Training
```

恢复周：

```text
Recovery
```

休赛期：

```text
Plan Next Season
```

不要：

两个主按钮。

---

# Secondary Actions

除主按钮外。

最多三个快捷入口。

例如：

```text
Calendar
Coach
Ranking
```

四个已经是上限。

禁止：

八个按钮。

---

# Information Hierarchy

页面信息优先级：

```text
Current Goal
↓
Primary Action
↓
Status
↓
Quick Actions
↓
Secondary Information
```

任何统计。

都不能高于：

当前目标。

---

# No Dead Ends

任何页面。

都必须拥有：

下一步。

例如：

比赛结束。

不是：

Close。

而是：

```text
Recovery
↓
Next Match
↓
Continue Week
```

玩家自然继续。

---

# No Empty Pages

任何状态。

Today 都不能空。

例如：

没有比赛。

Today：

推荐训练。

恢复。

查看新闻。

规划赛程。

玩家永远有事可做。

---

# Progressive Disclosure

复杂内容。

逐层展开。

例如：

Today：

只显示：

```text
Coach Advice
```

点击。

展开：

完整分析。

默认：

永远简单。

---

# Navigation

整个游戏。

Bottom Tab：

固定四个。

```text
Today
Career
World
Profile
```

禁止：

超过四个。

News。

Calendar。

Ranking。

全部属于：

World。

---

# Sheet First

详情。

优先：

Bottom Sheet。

不要：

Push 新页面。

例如：

点击：

Coach。

↓

Bottom Sheet。

点击：

Ranking。

↓

Bottom Sheet。

尽量保持：

Today 不离开。

---

# Gesture Rules

支持：

Swipe：

切换 Week。

Long Press：

快捷操作。

Pull Down：

刷新世界。

尽量减少：

复杂手势。

---

# Animation Principles

动画：

服务信息。

不是炫技。

例如：

Ranking 上升。

数字滚动。

冠军。

奖杯动画。

恢复。

绿色渐变。

比赛。

速度更快。

恢复。

速度更慢。

不同状态。

拥有不同节奏。

---

# Feedback Timing

所有重要操作。

立即反馈。

例如：

训练。

结束。

↓

能力增长。

比赛。

结束。

↓

排名变化。

Recovery。

结束。

↓

Fatigue 下降。

不要：

延迟反馈。

---

# Error Prevention

尽量避免：

误操作。

例如：

Grand Slam 前。

玩家点击：

Heavy Training。

系统提示：

```text
Coach does not recommend this.
```

而不是：

直接禁止。

---

# Empty Time

如果玩家：

连续一分钟。

没有操作。

Today：

自动展示：

推荐内容。

例如：

```text
You are close to Top50.
```

或者：

```text
Entry closes tomorrow.
```

帮助玩家继续。

---

# Session Length

一次游玩。

建议：

5~10 分钟。

完成：

一到两周。

不会：

一周玩一小时。

保持：

移动端节奏。

---

# Notification Design

通知。

只提醒：

真正重要的事情。

例如：

报名截止。

Grand Slam。

世界第一。

重大伤病恢复。

不要：

每天推送。

---

# Widget Integration

Widget。

直接对应：

Today。

例如：

```text
Week 18
Rome Masters
Tonight
vs Sinner
```

点击 Widget。

直接进入：

Today。

不是：

首页。

---

# Apple Watch

Apple Watch：

只展示：

今天最重要事件。

例如：

```text
Recovery Complete
Next Match Tomorrow
```

不允许：

复杂操作。

---

# Flow Example

一个完整 Session。

```text
Open App
↓
Today
↓
See Ranking
↓
Coach Advice
↓
Start Match
↓
Win
↓
Ranking Up
↓
Continue Week
↓
Close App
```

整个过程。

无需寻找任何功能。

---

# Emotional UX

UX 不只是效率。

还包括：

情绪。

例如：

冠军。

震动。

奖杯。

动画。

新闻。

恢复。

绿色。

安静。

Grand Slam。

更加隆重。

整个 UI。

跟随职业生涯变化。

---

# UX Red Lines

禁止：

超过三级页面。

禁止：

连续弹窗。

禁止：

空白页面。

禁止：

十个以上按钮。

禁止：

滚动才能看到主按钮。

---

# Success Metrics

UX 完成以后。

玩家应该：

打开 App。

↓

3 秒知道目标。

↓

10 秒开始行动。

↓

5 分钟完成一次 Session。

↓

自然继续下一周。

整个过程。

没有迷路。

没有思考：

按钮在哪里。

---

# Definition of Done

✓ Today 成为唯一入口

✓ 三秒知道下一步

✓ 一个主按钮

✓ 四个以内快捷入口

✓ 所有页面都能回到 Today

✓ 所有操作立即反馈

✓ Session 控制在 5~10 分钟

✓ 玩家始终保持 Flow

Ace Career 的 UX。

不是让玩家寻找功能。

而是让职业生涯自然流动。

---

End of Document

# Ace Career Gameplay Bible
# 14 · Onboarding

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Onboarding 定义玩家第一次打开 Ace Career 的完整体验。

它不是新手教程。

而是：

玩家第一次成为职业网球运动员。

Onboarding 的目标不是介绍所有功能。

而是让玩家：

5 分钟内爱上 Career。

---

# Design Goal

整个 Onboarding 必须做到：

① 五分钟进入职业生涯

② 不需要阅读大量文字

③ 每一步都有即时反馈

④ 第一小时就体验完整 Career Loop

玩家应该觉得：

"原来职业网球是这样。"

而不是：

"这个游戏怎么这么复杂。"

---

# Design Philosophy

现实中没有职业球员。

会先学习所有规则。

再开始比赛。

他们都是：

边打。

边成长。

Ace Career 也是如此。

功能。

应该随着职业生涯逐步解锁。

不是一次全部出现。

---

# First Launch

第一次打开 App。

不是主菜单。

直接进入：

Career Creation。

背景：

世界巡回赛。

中央一句话：

> **Every Champion Starts Somewhere.**

下面只有一个按钮：

```text
Start Your Career
```

---

# Career Creation

创建流程控制在一分钟内。

玩家只需要选择：

- 姓名
- 国家
- 左/右手
- 单反/双反
- 初始打法（可选）

不选择：

能力值。

身高。

体重。

这些由系统自动生成。

减少决策压力。

---

# Introduction

创建完成以后。

播放约 15 秒动画。

展示：

```text
Junior Tour
↓
ITF
↓
Challenger
↓
ATP
↓
Grand Slam
↓
World No.1
```

告诉玩家：

未来会经历什么。

而不是：

怎么玩。

---

# First Today

第一次进入 Today。

整个页面极简。

只有：

```text
Week 1
Welcome To Professional Tennis
Goal
Win Your First Match
Start Training
```

其他功能。

全部隐藏。

---

# Guided Training

第一次训练。

只有一个按钮。

```text
Start Training
```

系统自动完成。

结束后：

展示成长。

例如：

```text
Serve
+1
Confidence
+5
```

让玩家立刻获得：

成长反馈。

---

# First Tournament

训练结束。

自动推荐：

第一站 ITF。

Today 页面出现：

```text
ITF Cairo
Entry Open
Recommended
```

玩家只需要：

点击报名。

不用理解：

Acceptance。

Seed。

Draw。

---

# First Draw

第一次抽签。

自动生成。

系统用一句话解释：

```text
This is your position in the tournament.
```

结束。

不要：

介绍所有规则。

---

# First Match

第一场比赛。

系统自动降低难度。

目标：

不是挑战。

而是：

体验。

比赛结束。

立刻展示：

积分。

奖金。

排名变化。

让玩家理解：

职业循环。

---

# First Victory

如果赢球。

展示：

```text
Career First Win
Congratulations!
```

生成：

第一条新闻。

让玩家觉得：

世界注意到了自己。

---

# First Defeat

如果输球。

绝不能 Game Over。

Coach 自动出现：

```text
Every Champion Starts With Losses.
Let's Prepare For Next Week.
```

玩家立即进入：

Recovery。

继续 Career。

---

# Progressive Unlock

随着成长。

功能逐渐开放。

例如：

Top500：

解锁 Coach。

Top200：

解锁 Sponsor。

Top100：

解锁 Legacy。

Top50：

解锁 Media。

玩家不会被复杂系统淹没。

---

# First Season

第一赛季。

系统自动提供：

三个目标。

```text
Win Your First Match
Enter Top500
Reach One Quarterfinal
```

全部容易完成。

持续给予成就感。

---

# Coach Guidance

前四周。

Coach 建议：

几乎每周出现。

例如：

```text
This Week
Recovery Is Recommended.
```

随着玩家熟悉。

逐渐减少提示。

---

# Empty States

如果玩家不知道下一步。

Today 永远显示：

```text
Recommended Next Step
Enter ITF Cairo
```

玩家永远不会迷路。

---

# First Achievement

第一小时内。

至少获得：

三个 Achievement。

例如：

```text
First Training
First Match
First Ranking
```

不断强化：

成长体验。

---

# First Season Ending

赛季结束。

自动生成：

Season Review。

例如：

```text
Matches
18
Wins
11
Ranking
876 → 412
Next Goal
Top250
```

让玩家期待：

第二赛季。

---

# Skip Tutorial

老玩家。

可直接跳过。

所有引导。

只保留：

Career Creation。

---

# UX Rules

Onboarding：

禁止：

超过两分钟连续阅读。

禁止：

一次解释多个系统。

坚持：

Learn By Playing。

边玩边学。

---

# Success Metrics

Onboarding 完成以后。

玩家应该：

30 秒创建角色。

5 分钟完成第一周。

15 分钟完成第一项赛事。

60 分钟理解整个 Career Loop。

并愿意继续第二赛季。

---

# Definition of Done

✓ 创建流程小于一分钟

✓ 五分钟进入比赛

✓ 第一小时体验完整 Career Loop

✓ 功能逐步解锁

✓ 玩家不会迷路

✓ 输球不会劝退玩家

✓ 第一赛季结束后愿意继续

Onboarding 的目标不是教会玩家所有功能。

而是让玩家爱上职业网球人生。

---

End of Document

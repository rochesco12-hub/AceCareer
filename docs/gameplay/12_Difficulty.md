# Ace Career Gameplay Bible
# 12 · Difficulty

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Difficulty System 定义 Ace Career 的整体难度设计。

Ace Career 的难度。

绝不能通过：

AI Overall +10

玩家 Overall -10

这种方式实现。

真正优秀的职业模拟游戏。

难度来自：

更真实的职业世界。

而不是：

更强的 AI。

---

# Design Goal

Difficulty 必须满足：

① AI 不作弊

② 玩家始终公平竞争

③ 难度来自职业决策

④ 不同玩家都能找到适合自己的体验

玩家输球。

应该认为：

"我没有规划好。"

而不是：

"AI 开挂了。"

---

# Design Philosophy

现实职业网球。

最大的挑战不是：

每个人都特别强。

而是：

职业管理。

例如：

恢复。

赛程。

旅行。

训练。

伤病。

心理。

因此：

Ace Career 的难度。

应该增加：

职业压力。

而不是：

比赛难度。

---

# Difficulty Levels

游戏默认提供四个难度。

```text
Easy
↓
Normal
↓
Hard
↓
Legend
```

每个难度。

改变的是：

世界规则。

不是：

球员能力。

---

# Easy

适合：

第一次接触职业模拟玩家。

特点：

- Recovery 更快
- Injury 更少
- Coach 建议更明确
- Money 更充足
- Goal 更容易完成
- AI 决策较保守

重点：

体验 Career。

---

# Normal

推荐默认难度。

特点：

完全按照：

设计平衡。

Recovery。

训练。

旅行。

全部保持：

标准体验。

这是：

官方推荐玩法。

---

# Hard

适合：

熟悉 Career 的玩家。

变化：

AI 更善于规划赛季。

AI 更合理安排恢复。

AI 更少犯错。

世界竞争更加激烈。

玩家必须真正规划赛季。

---

# Legend

最高难度。

不是：

AI 更强。

而是：

整个职业世界更加真实。

例如：

Recovery 更慢。

旅行成本更高。

赞助更难获得。

Top100 更稳定。

Grand Slam 更难爆冷。

真正体验：

职业体育。

---

# What Difficulty Changes

Difficulty 会影响：

Recovery

Coach

Economy

Injury

Travel

Media

Goal

AI Planning

不会影响：

击球能力。

不会影响：

模拟概率。

---

# Recovery

例如：

Easy：

Fatigue

恢复：

+25%。

Legend：

恢复：

标准值。

玩家必须：

主动安排恢复。

---

# Injury

Easy：

Minor Injury：

明显减少。

Legend：

完全真实。

长期过度比赛。

一定受伤。

---

# Economy

Easy：

奖金充足。

赞助更容易。

Legend：

资金压力明显增加。

玩家需要：

合理规划。

---

# Coach

Easy：

Coach 会直接告诉玩家：

应该怎么做。

例如：

```text
Skip This Tournament.
```

Legend：

Coach：

只提供分析。

最终：

完全由玩家决定。

---

# Goal System

Easy：

系统推荐：

简单目标。

Legend：

目标更加真实。

例如：

排名：

120。

不会：

推荐：

世界第一。

而是：

Top100。

---

# AI Planning

Hard 与 Legend。

最大的区别：

AI 职业规划。

例如：

AI 会：

为了 Wimbledon。

主动放弃：

ATP250。

而不是：

所有赛事都报名。

---

# Ranking Difficulty

Legend：

Top10 更稳定。

Top100 更难进入。

Grand Slam 冠军：

更加集中。

职业世界：

更接近现实。

---

# Tournament Difficulty

不是：

对手：

能力更高。

而是：

Acceptance。

排名。

签表。

更加困难。

例如：

ATP500。

更容易遇见：

Top Player。

---

# Financial Pressure

Legend：

需要真正管理：

现金流。

例如：

连续受伤。

可能无法：

聘请高级教练。

职业规划：

更加重要。

---

# Psychological Difficulty

高难度。

媒体压力更大。

例如：

连续失败。

新闻更多。

Confidence 恢复更慢。

玩家需要：

主动调整。

---

# Dynamic Difficulty

未来支持：

Adaptive Difficulty。

例如：

连续：

五站冠军。

系统：

逐渐提高：

AI 职业规划质量。

保持挑战。

不是：

偷偷增加能力。

---

# Custom Difficulty

未来：

支持：

自由组合。

例如：

```text
Recovery
Easy
Economy
Hard
Injury
Legend
Coach
Easy
```

玩家创造：

自己的职业体验。

---

# Difficulty Recommendation

第一次 Career。

推荐：

Normal。

完成一次 Career。

推荐：

Hard。

真正体验：

职业体育。

推荐：

Legend。

---

# UX Rules

创建 Career。

只解释：

不同职业体验。

不要：

展示：

大量数字。

例如：

```text
Legend
The most authentic professional tennis career experience.
```

而不是：

Recovery

-13%。

---

# Success Metrics

Difficulty 完成以后。

玩家应该：

输球。

不会觉得：

AI 太强。

而会觉得：

"我的赛季安排出了问题。"

如果玩家能够：

通过职业规划。

战胜世界。

那么：

Difficulty System 就成功了。

---

# Definition of Done

✓ AI 永不作弊

✓ 难度来自职业管理

✓ Recovery 随难度变化

✓ Economy 随难度变化

✓ AI Planning 随难度变化

✓ 玩家拥有公平体验

✓ Legend 接近真实职业巡回赛

Ace Career 的难度。

来自职业生涯。

不是来自作弊的 AI。

---

End of Document

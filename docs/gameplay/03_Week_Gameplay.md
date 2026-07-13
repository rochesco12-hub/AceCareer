# Ace Career Gameplay Bible
# 03 · Week Gameplay

Version: 1.0
Status: Draft
Priority: P0

---

# Overview

Week Gameplay 定义 Ace Career 最核心的玩法单位。

整个游戏不以：

天（Day）

作为推进单位。

也不以：

比赛（Match）

作为推进单位。

而是：

Week。

这是整个 Career Mode 最重要的设计之一。

现实 ATP/WTA 巡回赛就是以周为单位运作。

因此玩家也应该像真正职业球员一样：

每周规划。

每周比赛。

每周成长。

---

# Design Goal

每进入一周。

玩家必须经历：

世界变化

↓

信息获取

↓

职业决策

↓

执行计划

↓

获得反馈

↓

下一周

而不是：

Continue

↓

Continue

↓

Continue

Week 本身就是游戏。

---

# Why Week Instead of Day

Day 有三个问题。

第一。

推进速度太慢。

例如：

一项 ATP250。

现实需要七天。

玩家需要点击七次。

非常无聊。

第二。

每天发生的事情太少。

职业球员很多天只是：

训练。

恢复。

媒体。

旅行。

拆成七天。

会产生大量空内容。

第三。

赛历天然就是 Week。

ATP Calendar：

Week18

Week19

Week20

Grand Slam

全部都是以 Week 为单位。

所以：

Week 才是真正适合职业模拟的时间尺度。

---

# Weekly Structure

每一周固定拥有六个阶段。

```text
World Update
↓
Career Review
↓
Planning
↓
Execution
↓
Weekly Summary
↓
Next Week
```

玩家每周都会完整经历一次。

---

# Phase 1

## World Update

进入 Week 后。

世界先变化。

不是玩家先行动。

例如：

新的冠军诞生。

新的世界第一。

新的新闻。

新的退役。

新的新秀。

新的赛事开放。

玩家第一眼看到的是：

世界不是静止的。

---

# Phase 2

## Career Review

随后。

玩家查看自己的变化。

例如：

```text
Ranking
#84
↑5
Money
+$12,400
Confidence
+4
Fatigue
38
Coach
Rest Recommended
```

所有变化集中反馈。

形成：

成长感。

---

# Phase 3

## Weekly Planning

这是一周最重要的阶段。

玩家真正开始玩游戏。

需要决定：

参加哪项赛事。

是否训练。

是否恢复。

是否旅行。

是否更换团队。

是否冲排名。

所有选择都会影响未来。

---

# Planning Priority

Planning 永远遵循：

Tournament

↓

Health

↓

Training

↓

Finance

↓

Coach

比赛永远优先。

恢复永远高于训练。

---

# Phase 4

## Execute Week

系统开始模拟这一周。

例如：

比赛周：

Arrival

↓

Practice

↓

Round1

↓

Round2

↓

Quarterfinal

↓

Recovery

↓

Semifinal

↓

Final

非比赛周：

Training

↓

Recovery

↓

Gym

↓

Coach Meeting

↓

Travel

整个过程。

玩家只关注关键决策。

系统自动完成重复流程。

---

# Phase 5

## Weekly Summary

Week 结束。

统一结算。

例如：

```text
Champion
ATP250 Doha
Prize Money
+$36,000
Ranking
#84 → #71
Confidence
+8
Fatigue
+17
Legacy
+2
```

所有奖励。

一次性爆发。

形成高潮。

---

# Phase 6

## Continue Week

最后。

出现：

Continue Week。

整个 Today 页面已经发生变化。

新的赛事。

新的新闻。

新的目标。

玩家自然继续。

形成：

One More Week。

---

# Different Week Types

Week 不完全一样。

支持：

Tournament Week

Training Week

Recovery Week

Travel Week

Grand Slam Week

Off Season Week

不同 Week。

玩法完全不同。

---

# Tournament Week

重点：

比赛。

玩家关注：

对手。

签表。

恢复。

教练建议。

媒体。

整个页面围绕：

下一场比赛。

---

# Training Week

重点：

成长。

玩家决定：

练什么。

练多少。

是否 Peak。

是否准备下一项赛事。

成长。

成为主反馈。

---

# Recovery Week

重点：

恢复。

玩家关注：

Fatigue。

伤病。

医疗团队。

恢复速度。

不是能力成长。

而是：

身体恢复。

---

# Travel Week

重点：

赛程规划。

例如：

欧洲。

↓

北美。

↓

亚洲。

旅行：

增加疲劳。

也影响预算。

玩家必须提前规划。

---

# Grand Slam Week

这是全年最特殊的一周。

整个 UI。

自动变化。

例如：

背景。

标题。

动画。

新闻数量。

媒体采访。

全部增加。

让玩家感受到：

这是 Grand Slam。

---

# Off Season Week

休赛期。

不是：

空白。

而是：

整个职业规划。

例如：

更换教练。

调整训练。

查看总结。

制定目标。

准备下一赛季。

这里是：

Career Management。

---

# Weekly Decisions

一周最多：

四个重要决定。

例如：

报名。

↓

训练。

↓

恢复。

↓

教练。

超过四个。

玩家开始疲劳。

---

# Weekly Feedback

Week 必须产生反馈。

包括：

排名。

奖金。

成长。

新闻。

纪录。

关系。

目标。

至少三项变化。

否则：

这一周没有意义。

---

# Weekly Emotion Curve

每一周应该拥有情绪节奏。

```text
期待
↓
思考
↓
紧张
↓
高潮
↓
满足
↓
期待下一周
```

而不是：

一直平淡。

---

# Long-Term Connection

Week 会影响：

Month。

Month 会影响：

Season。

Season 会影响：

Career。

因此：

任何一周都不是独立存在。

例如：

这一周休息。

可能帮助：

三周后的温网。

Week 是长期策略的一部分。

---

# UX Rules

Week 页面：

禁止出现：

超过四个主要操作。

禁止连续弹窗。

禁止玩家重复确认。

Week 必须：

打开。

思考。

决定。

推进。

整个过程：

一分钟内完成。

---

# Success Metrics

Week Gameplay 完成以后。

玩家应该：

每进入新 Week。

都会产生：

"这周我要干什么？"

而不是：

"继续。"

如果玩家每推进一周。

都会产生新的职业故事。

Week Gameplay 就成功了。

---

# Definition of Done

✓ Week 成为核心玩法单位

✓ 每周都有新的决策

✓ 每周都有成长反馈

✓ 每周都有新的目标

✓ 不同 Week 拥有不同玩法

✓ 一分钟完成一周管理

✓ 玩家期待进入下一周

Week 不是时间单位。

Week 就是 Ace Career 最基本的游戏单位。

---

End of Document

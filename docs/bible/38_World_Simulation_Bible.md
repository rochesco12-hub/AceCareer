# Ace Career Engine Bible
# 38 · World Simulation Bible

Version: 1.0
Status: Final
Priority: P0

---

# Overview

World Simulation 是整个 Ace Career 最重要的 Engine。

它决定整个职业网球世界是否真正"活着"。

玩家不是世界的中心。

玩家只是这个世界里的其中一名职业球员。

即使玩家永远不进入比赛。

整个世界也应该继续运行：

- 球员成长
- 球员退役
- 世界排名变化
- Grand Slam冠军诞生
- 新闻更新
- 教练更换
- 新秀进入巡回赛

如果玩家关闭游戏一年。

再次打开。

世界应该已经完全不同。

---

# Design Goal

World Simulation 必须满足：

✓ 世界独立于玩家运行

✓ 每一周都会发生大量事件

✓ AI 永远不会停止成长

✓ 排名持续变化

✓ 球员不断进入与退出职业巡回赛

✓ 玩家只是世界的一部分

整个世界必须拥有生命。

---

# Simulation Philosophy

Ace Career 不是：

玩家推动世界。

而是：

世界持续运转。

玩家参与其中。

整个 ATP 世界。

每一周都在发生数千件事情。

玩家只能看到其中极少部分。

---

# World Scale

默认职业世界：

```text
Active Players
2200
Junior Players
400
Retired Players
History Archive
ATP Tournaments
全年完整赛历
News Database
持续增长
Historical Records
永久保存
```

玩家看到排行榜前100。

实际上：

世界拥有2200名职业球员。

---

# World Layers

世界分为四层。

```text
Player Layer
↓
Tournament Layer
↓
World Layer
↓
History Layer
```

每一层。

每周都会更新。

---

# Weekly Simulation

整个世界。

每推进一周。

都会完整模拟一次。

流程固定。

```text
Week Begins
↓
Generate Events
↓
AI Decision
↓
Tournament Entry
↓
Acceptance
↓
Travel
↓
Training
↓
Recovery
↓
Tournament
↓
Ranking
↓
Prize Money
↓
Career Update
↓
News
↓
History
↓
Week Ends
```

整个 Engine 永远按照这个顺序。

---

# Step 1

## World Events

首先。

生成世界事件。

例如：

- 新赛事开放
- Grand Slam开始
- 球员生日
- 新赞助
- 新纪录
- 新伤病
- 新教练

世界开始变化。

---

# Step 2

## AI Decision

2200名球员。

全部进行思考。

决定：

参加赛事。

恢复。

训练。

旅行。

更换教练。

退赛。

整个世界开始行动。

---

# Step 3

## Tournament Entry

AI 开始报名。

例如：

```text
ATP250
Entry
31 Players
Masters
96 Players
ITF
32 Players
```

报名结束。

进入 Acceptance。

---

# Step 4

## Acceptance

系统自动生成：

Accepted

Qualifying

Alternate

Rejected

整个报名过程。

完全模拟。

不是直接生成签表。

---

# Step 5

## Travel

报名成功以后。

AI 开始旅行。

系统计算：

距离

↓

飞行时间

↓

Fatigue

↓

Jet Lag

↓

Arrival

旅行也是模拟的一部分。

---

# Step 6

## Training

没有比赛的球员。

自动训练。

训练内容：

由 AI Decision 决定。

例如：

Serve

Movement

Recovery

Mental

整个世界都在成长。

---

# Step 7

## Recovery

Fatigue 高。

自动恢复。

伤病球员。

自动治疗。

整个 Recovery System。

与玩家一致。

---

# Step 8

## Tournament Simulation

所有赛事。

同步模拟。

例如：

```text
Australian Open
128
Masters
96
ATP500
32
Challenger
32
ITF
32
```

每项赛事。

完整模拟。

冠军自然产生。

---

# Step 9

## Ranking Update

赛事结束。

统一计算：

积分

↓

保分

↓

失分

↓

奖金

↓

排名

不会：

每场比赛更新。

统一周结算。

---

# Step 10

## Career Update

所有球员：

更新：

Age

Confidence

Fatigue

Career Stats

Titles

Ranking High

Relationship

整个 Career 持续成长。

---

# Step 11

## News Generation

系统筛选：

世界最重要新闻。

例如：

```text
Sinner Wins Wimbledon
New World No.1
Djokovic Retires
Logan Reaches Top100
Teenager Wins Challenger
```

新闻来自世界。

不是脚本。

---

# Step 12

## History

永久保存：

冠军

↓

纪录

↓

退役

↓

Career Milestone

整个职业历史。

越来越丰富。

---

# Population System

职业世界：

默认保持：

2200±50

任何时候。

世界人口保持稳定。

例如：

```text
Retired
72
↓
New Rookie
80
↓
Current
2208
```

世界不会：

越来越少。

也不会：

无限增加。

---

# Ranking Distribution

世界排名：

始终完整。

例如：

```text
1-10
Elite
11-50
World Class
51-100
ATP
101-250
ATP/Challenger
251-500
Challenger
501-1200
ITF
1200+
Junior Transition
```

不会出现：

只有15个人。

---

# Tournament Population

例如：

ATP250。

不会出现：

世界第600。

也不会出现：

世界第1全部参加。

系统自动平衡。

每项赛事。

符合现实。

---

# Dynamic World

世界永远变化。

例如：

连续几年。

可能出现：

新王朝。

也可能：

群雄争霸。

整个世界：

没有固定剧本。

---

# Historical Archive

所有赛季。

永久保存。

例如：

```text
2028
Australian Open
Champion
Alcaraz
2029
Champion
Logan
2030
Champion
Rune
```

未来几十年。

仍然可以查看。

---

# Retirement

退役。

不会删除。

进入：

History。

Hall Of Fame。

Career Archive。

世界拥有真正历史。

---

# Rookie Generation

每年。

生成：

新的年轻球员。

例如：

17岁。

18岁。

19岁。

拥有：

随机国籍。

随机打法。

随机潜力。

未来：

成为：

世界第一。

也可能：

永远停留ITF。

---

# World Stability

任何 Simulation。

必须保证：

世界始终成立。

例如：

Masters：

一定96签。

Grand Slam：

一定128签。

ITF：

一定32签。

系统自动补齐。

不会因为：

玩家存在。

破坏世界。

---

# Debug Mode

开发模式。

支持查看：

```text
Current Week
World Population
2207
ATP Events
14
Players Training
1394
Players Traveling
238
Players Recovering
317
Players Competing
258
Retired This Week
2
New Players
3
```

方便开发。

---

# Acceptance Criteria

✓ 世界独立运行

✓ 2200名职业球员持续存在

✓ 排名完整

✓ 每周完整模拟

✓ AI 同步成长

✓ 新闻自动生成

✓ 历史永久保存

✓ 玩家不是世界中心

---

# Final Principle

Ace Career 最重要的不是玩家。

而是：

整个职业网球世界。

每天都在继续前进。

即使没有玩家。

这个世界。

依然精彩。

---

End of Document

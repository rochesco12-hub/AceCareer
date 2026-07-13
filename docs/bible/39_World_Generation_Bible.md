# Ace Career Engine Bible
# 39 · World Generation Bible

Version: 1.0
Status: Final
Priority: P0

---

# Overview

World Generation 定义当玩家创建一个全新的 Career 时，整个职业网球世界是如何被生成的。

它不是生成玩家。

而是生成：

整个 ATP 世界。

一个真正的职业生涯，不应该开始于：

玩家出生。

而应该开始于：

一个已经存在几十年的职业巡回赛。

玩家只是进入了这个世界。

而不是创造这个世界。

---

# Design Goal

World Generation 必须做到：

✓ 世界拥有完整历史

✓ 世界拥有完整人口

✓ 世界拥有完整排名

✓ 世界拥有完整赛历

✓ 世界拥有完整纪录

✓ 世界拥有真实的发展潜力

玩家第一次进入世界时。

应该感觉：

这个世界已经运行很多年。

---

# Design Philosophy

现实世界不会因为玩家出生。

才开始存在。

Ace Career 也是一样。

玩家创建 Career 时。

世界已经拥有：

几十年的巡回赛。

数千名球员。

完整的排名。

完整的冠军。

完整的历史。

玩家只是其中一员。

---

# Generation Flow

创建 Career 时。

世界生成流程固定：

```text
Generate World Seed
↓
Generate Calendar
↓
Generate Population
↓
Generate Rankings
↓
Generate History
↓
Generate Current Season
↓
Generate News
↓
Generate Player
↓
Enter World
```

整个流程。

只执行一次。

之后全部交给 World Simulation。

---

# Step 1

## World Seed

首先生成：

World Seed。

例如：

```text
World Seed
483912847
```

整个世界：

全部依赖这个 Seed。

保证：

同一个 Seed。

永远生成同一个世界。

方便：

Debug。

分享。

重放。

---

# Step 2

## Calendar Generation

生成完整赛历。

包括：

Australian Open

Indian Wells

Miami

Monte Carlo

Madrid

Rome

Roland Garros

Queen's

Wimbledon

Canada

Cincinnati

US Open

Asia Swing

Indoor Season

ATP Finals

所有赛事。

一次生成。

---

# Step 3

## Population Generation

生成：

2200 名职业球员。

例如：

```text
Top100
100
ATP
150
Challenger
450
ITF
1100
Junior Transition
400
```

每个人：

独立生成。

---

# Player Generation

每位球员拥有：

- 国籍
- 年龄
- 身高
- 持拍
- 正反手
- 发球倾向
- 技术特点
- 性格
- 潜力
- 当前能力
- 成长曲线
- 伤病倾向
- 教练
- 职业目标

没有两个球员完全一样。

---

# Age Distribution

世界年龄必须合理。

例如：

```text
17-19
8%
20-23
24%
24-28
38%
29-33
22%
34+
8%
```

整个巡回赛。

始终保持正常年龄结构。

---

# Nationality Distribution

国籍不是随机平均。

应该参考现实。

例如：

```text
USA
Spain
Italy
France
Germany
Australia
Argentina
China
Japan
...
```

不同国家。

拥有不同人才密度。

---

# Potential Generation

每位球员。

拥有隐藏潜力。

例如：

```text
Potential
62
Current
58
```

也可能：

```text
Potential
97
Current
43
```

未来：

成为世界第一。

或者：

默默无闻。

---

# Playing Style Generation

自动生成打法。

例如：

Serve Bot

Baseline Aggressor

Counter Puncher

Clay Specialist

All Court

Defensive Player

未来成长。

围绕打法。

而不是：

随机成长。

---

# Step 4

## Ranking Generation

生成完整排名。

例如：

```text
World No.1
↓
World No.2200
```

每个排名。

对应：

真实能力。

不会出现：

世界第300。

能力比世界第20高。

---

# Step 5

## Tournament History

生成过去：

10 年历史。

例如：

```text
Australian Open
2020
Champion
...
2021
Champion
...
...
2029
Champion
```

玩家进入世界时。

纪录已经存在。

---

# Historical Rankings

生成：

历年世界第一。

Masters 冠军。

Grand Slam 冠军。

ATP Finals。

Olympics。

整个世界：

拥有历史厚度。

---

# Records

生成初始纪录。

例如：

```text
Most Grand Slams
Most Weeks No.1
Most ATP Titles
Longest Winning Streak
```

玩家未来。

可以不断刷新。

---

# Step 6

## Current Season

生成：

当前赛季。

例如：

Week18。

已经结束：

17 周。

未来：

还有：

34 周。

世界不是：

Week1。

固定开始。

---

# Step 7

## News Generation

根据当前世界。

生成新闻。

例如：

```text
World No.1 Defends Rome
Teenager Wins Challenger
Veteran Announces Retirement
```

玩家第一次进入。

世界已经发生很多事情。

---

# Step 8

## Player Creation

最后。

生成玩家。

玩家不是：

世界第一。

默认：

18 岁。

排名：

800~1200。

准备开始职业生涯。

整个世界：

不会因为玩家改变。

---

# Dynamic Balance

每个世界。

都不同。

例如：

某个世界：

Alcaraz 王朝。

另一个世界：

Rune 崛起。

另一个世界：

新秀提前统治。

不会：

完全固定。

---

# Rookie Pipeline

生成：

未来五年。

新秀池。

例如：

```text
Age17
92 Potential
Spain
Age16
88 Potential
USA
Age18
95 Potential
Italy
```

未来：

逐渐进入职业巡回赛。

---

# Retirement Pipeline

生成：

未来可能退役球员。

例如：

```text
Age37
Probability
82%
```

世界自然更新。

---

# Data Integrity

任何世界。

必须保证：

- 排名连续
- 球员唯一
- 冠军唯一
- 赛事完整
- 历史完整
- 数据一致

任何生成失败。

重新生成。

---

# Save Strategy

World Generation。

只执行一次。

之后：

World Simulation。

负责全部变化。

任何世界。

都不会：

重新生成。

---

# Debug Mode

开发模式支持：

```text
World Seed
483912847
Players
2200
History Years
10
Grand Slam Records
Generated
Future Rookies
400
Current Week
18
```

方便开发。

---

# Acceptance Criteria

✓ 世界拥有2200名职业球员

✓ 世界拥有完整历史

✓ 世界拥有完整赛历

✓ 世界拥有完整排名

✓ 世界拥有未来新秀

✓ 世界拥有未来退役

✓ 玩家进入的是已有世界

✓ World Generation 只执行一次

---

# Final Principle

Ace Career 不应该让玩家创造世界。

而应该让玩家进入一个已经存在、正在运转、拥有过去、拥有未来的职业网球世界。

玩家不是世界的开始。

玩家只是这个世界历史中的一部分。

---

End of Document

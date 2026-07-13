# Ace Career Engine Bible
# 37 · AI Decision Bible

Version: 1.0
Status: Final
Priority: P0

---

# Overview

AI Decision Bible 定义整个 Ace Career 中所有 AI 球员的决策逻辑。

它回答的问题只有一个：

> **如果世界里没有玩家，这个职业网球世界还能正常运转吗？**

如果答案是否定的。

那么整个 Career 都是不真实的。

AI 绝不能只是：

随机报名。

随机训练。

随机成长。

每一位 AI 都必须像真正的职业球员一样：

思考。

规划。

成长。

衰退。

退役。

---

# Design Goal

AI 必须做到：

✓ 每周自主决策

✓ 拥有长期职业规划

✓ 不作弊

✓ 不依赖玩家存在

✓ 每个人拥有不同职业轨迹

玩家应该感觉：

自己只是 ATP 世界里的其中一个人。

---

# AI Philosophy

AI 不是 NPC。

AI 是：

Professional Tennis Player。

他们拥有：

- 自己的目标
- 自己的团队
- 自己的训练
- 自己的恢复
- 自己的旅行
- 自己的职业生涯

整个世界：

2200 名职业球员。

2200 个独立 Career。

---

# AI Brain

每位 AI 每周都会执行一次完整思考。

流程如下：

```text
Current Situation
↓
Evaluate Goals
↓
Evaluate Health
↓
Evaluate Ranking
↓
Evaluate Schedule
↓
Choose Tournament
↓
Choose Training
↓
Choose Recovery
↓
Execute Week
```

所有 AI 使用完全相同流程。

---

# AI Personality

每位 AI 生成时拥有隐藏人格。

例如：

Professionalism

Aggressiveness

Patience

Confidence

Discipline

Risk Preference

Ambition

Financial Awareness

Home Preference

Travel Tolerance

这些属性终身存在。

不会改变。

---

# Example

例如：

Professionalism

95

↓

训练积极

恢复合理

很少退赛

例如：

Risk

90

↓

喜欢挑战 Masters

即使容易首轮出局。

例如：

Risk

15

↓

更喜欢 Challenger

稳定拿分。

---

# AI Career Goals

AI 永远拥有目标。

例如：

Top100

Top50

ATP Champion

Grand Slam

World No.1

Veteran

Retirement

不同阶段。

目标不同。

---

# Tournament Decision

AI 不会：

看到有赛事。

就报名。

而是计算：

```text
Tournament Value
=
Points
+
Prize Money
+
Expected Win Rate
+
Surface Fit
+
Travel Cost
+
Fatigue
+
Season Goal
```

最后。

选择：

价值最高。

---

# Tournament Entry Rules

系统必须严格限制。

```text
Top20
几乎不会报名 Challenger
绝不会报名 ITF

Top50
不会报名 ITF
偶尔ATP250

Top100
ATP250
ATP500
Masters
Grand Slam

Top250
ATP250
Challenger

Top500
Challenger
ITF

500+
ITF
Junior
```

这是整个世界真实性的重要规则。

---

# Surface Preference

AI 拥有：

Surface Bias。

例如：

Clay Specialist

↓

更愿意参加：

红土赛事。

Serve Bot

↓

更喜欢：

草地。

Indoor Player

↓

更喜欢：

室内赛。

不会：

所有赛事都一样。

---

# Travel Decision

AI 会计算：

旅行成本。

例如：

欧洲连续四站。

↓

继续留在欧洲。

而不是：

飞东京。

再飞巴黎。

旅行也是职业规划。

---

# Recovery Decision

Fatigue：

>70。

AI：

优先恢复。

Fatigue：

<30。

AI：

继续比赛。

不会：

无限连续参赛。

---

# Injury Decision

Minor Injury：

不同人格。

不同选择。

例如：

Aggressive

↓

继续比赛。

Professional

↓

休息一周。

Risk Preference：

决定职业轨迹。

---

# Training Decision

AI 每周都会训练。

训练目标来自：

弱项。

赛季。

教练建议。

例如：

草地前。

更多：

Serve。

法网前。

更多：

Endurance。

---

# Coach Influence

每位 AI 同样拥有教练。

教练影响：

赛事选择。

恢复。

训练。

长期规划。

AI 不会忽略教练。

但也不会完全听从。

---

# Ranking Awareness

AI 会关注：

自己排名。

例如：

当前：

102。

距离：

Top100。

只差：

18分。

AI：

更愿意报名：

容易拿分赛事。

而不是：

Masters。

---

# Money Awareness

低排名 AI。

现金不足。

可能：

放弃远距离比赛。

优先：

附近赛事。

职业生涯：

不仅只有积分。

---

# Confidence

连续赢球。

Confidence：

提高。

AI：

更容易挑战高等级赛事。

连续输球。

Confidence：

下降。

AI：

更加保守。

---

# Rival Decision

长期输给某位球员。

AI：

可能主动避开。

或者：

更加希望复仇。

不同人格。

行为不同。

---

# Retirement Decision

AI 不会：

固定35岁退役。

综合：

年龄。

伤病。

排名。

奖金。

动力。

家庭（Future）。

自动决定。

---

# Rookie Development

年轻 AI。

更加激进。

老将。

更加稳定。

职业风格。

随着年龄变化。

---

# Decision Priority

AI 永远遵循：

```text
Health
↓
Career Goal
↓
Tournament
↓
Training
↓
Finance
↓
Travel
```

健康。

永远第一。

---

# No Cheating

AI 禁止：

能力瞬间提升。

无限恢复。

无限金钱。

无限体力。

所有成长。

全部遵守：

玩家规则。

---

# World Diversity

2200 名 AI。

不会：

2200 个一样。

例如：

有人：

疯狂打比赛。

有人：

长期恢复。

有人：

只打红土。

有人：

喜欢 ATP250。

整个世界。

自然丰富。

---

# Debug

开发模式支持：

查看任意 AI。

例如：

```text
Current Goal
Top50
Reason
Need 180 Points
Next Tournament
Rome Masters
Coach
Recovery Recommended
Decision
Ignore Coach
```

方便调试。

---

# Acceptance Criteria

✓ AI 拥有完整职业规划

✓ AI 自主报名

✓ AI 自主恢复

✓ AI 自主训练

✓ AI 不作弊

✓ AI 具有不同人格

✓ 世界无需玩家即可运行

---

# Final Principle

玩家不是唯一会思考的人。

整个 ATP 世界。

2200 名职业球员。

每一个人。

都在努力实现自己的梦想。

---

End of Document

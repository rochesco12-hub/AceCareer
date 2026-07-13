# Ace Career Game Design Document
## AI Tournament Decision System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

AI Tournament Logic（AI赛事决策系统）负责决定：

整个世界所有 AI 球员：

- 报什么比赛
- 为什么报
- 是否退赛
- 是否休息
- 是否降级打 Challenger
- 是否冲击 ATP
- 如何规划整个赛季

AI 不能随机报名。

必须像真实职业球员一样制定职业规划。

---

# 2. Design Goal

AI 应该让玩家产生：

"这些球员真的在规划自己的职业生涯。"

而不是：

"AI 只是随机出现在签表里。"

AI 每周都要做决策。

每一个决定都必须有原因。

---

# 3. AI Decision Pipeline

每进入新的 Week。

AI 必须执行：

```text
Update Ranking
↓
Update Health
↓
Update Fatigue
↓
Update Confidence
↓
Generate Candidate Tournaments
↓
Evaluate Each Tournament
↓
Choose Best Tournament
↓
Entry
↓
Schedule Recovery
↓
Save Plan
```

所有 AI 使用同一套流程。

---

# 4. AI Personality

每个 AI 拥有长期人格。

例如：

Aggressive

Balanced

Conservative

Surface Specialist

Home Preference

Money First

Ranking First

Career First

人格影响：

整个职业生涯。

不是：

一场比赛。

---

# 5. Decision Factors

AI 对每站赛事计算：

Tournament Score。

Tournament Score =

```text
Points Value
+
Prize Money
+
Surface Preference
+
Travel Distance
+
Fatigue
+
Ranking Goal
+
Confidence
+
Injury Risk
+
Home Bonus
+
Season Goal
```

得分最高：

自动报名。

---

# 6. Ranking Goal

不同排名。

目标不同。

例如：

世界排名：

350。

目标：

进入 Top250。

系统：

优先：

ITF M25。

不是：

ATP250。

世界排名：

92。

目标：

保住 Top100。

优先：

ATP250。

不是：

ITF。

AI 必须符合职业逻辑。

---

# 7. Surface Preference

每位 AI：

拥有：

Surface Rating。

例如：

Clay

95

Grass

60

Hard

88

Indoor

75

进入：

Clay Season。

AI：

更倾向：

报名 Clay。

不是：

随机。

---

# 8. Fatigue

疲劳：

影响：

赛事选择。

Fatigue：

80+

AI：

主动休息。

Fatigue：

60。

AI：

可能降级：

打 Challenger。

Fatigue：

20。

允许：

连续比赛。

---

# 9. Injury

Minor Injury：

AI：

降低比赛数量。

Major Injury：

AI：

直接退出赛事。

进入：

Recovery Plan。

AI 不会：

带重伤：

连续比赛。

---

# 10. Confidence

Confidence：

影响：

风险偏好。

Confidence：

90。

AI：

更愿意挑战：

ATP500。

Confidence：

25。

AI：

更愿意：

打 ITF。

恢复信心。

---

# 11. Home Preference

部分 AI：

拥有：

Home Bonus。

例如：

日本球员。

Tokyo ATP。

Tournament Score：

增加。

现实职业球员：

经常如此。

---

# 12. Travel Logic

AI：

计算：

连续旅行。

例如：

Rome

↓

Toronto

↓

Tokyo

若：

连续跨洲。

Travel Cost：

增加。

AI：

更可能：

休息。

而不是：

继续飞。

---

# 13. Season Planning

AI：

不是：

只规划：

这一周。

而是：

未来：

4~8 周。

例如：

知道：

法网：

还有：

5 周。

AI：

减少：

Hard Court。

开始：

Clay。

提前准备。

---

# 14. Withdraw Decision

AI：

满足：

以下情况。

允许：

Withdraw。

- Major Injury
- Fatigue > 90
- Grand Slam 准备
- Travel Impossible
- Better Tournament

不是：

随机退赛。

---

# 15. Skip Week

AI：

允许：

主动：

休息。

例如：

连续：

4 周比赛。

Week5：

Recovery。

保持：

长期状态。

---

# 16. Tournament Priority Example

例如：

AI：

世界排名：

145。

候选：

ITF M25

Score

61

Challenger50

84

ATP250

18

最终：

报名：

Challenger50。

---

# 17. AI Archetypes

支持：

Grinding Player

↓

不停比赛。

Young Talent

↓

冲排名。

Veteran

↓

保护身体。

Clay Specialist

↓

重点打 Clay。

Big Match Player

↓

Grand Slam 优先。

Money Hunter

↓

奖金优先。

未来：

支持：

更多人格。

---

# 18. AI Memory

AI 保存：

Career Memory。

例如：

去年：

Rome：

夺冠。

今年：

更愿意：

再次参赛。

去年：

连续伤病。

今年：

减少：

比赛数量。

AI：

拥有：

长期学习能力。

---

# 19. Data Model

```text
AITournamentPlan
PlayerID
CurrentGoal
PreferredSurface
PreferredRegion
Fatigue
Confidence
TravelBudget
TargetRanking
CurrentTournament
NextTournament
PlannedWeeks
```

---

# 20. Acceptance Criteria

完成后：

✓ AI 每周自动规划赛事

✓ AI 不随机报名

✓ AI 会休息

✓ AI 会退赛

✓ AI 会根据 Surface 调整赛程

✓ AI 会提前准备 Grand Slam

✓ AI 与玩家遵循相同规则

✓ AI 支持 20+ Season

---

End of Document

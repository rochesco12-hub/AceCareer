# Ace Career Game Design Document
## Match Simulation System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Match Simulation System（比赛模拟系统）负责模拟每一场网球比赛。

它不是简单随机胜负。

而是根据：

- 球员能力
- 当前状态
- 场地
- 疲劳
- 心理
- 战术
- 比赛经验

共同决定比赛结果。

所有比赛：

AI vs AI

Player vs AI

Player vs Player（未来）

全部使用同一套模拟规则。

---

# 2. Design Goal

比赛模拟必须做到：

- 看起来真实
- 允许爆冷
- 强者长期更强
- 弱者偶尔获胜
- 数据可解释

玩家不能感觉：

"系统随机让我输。"

---

# 3. Simulation Pipeline

```text
Match Start
↓
Read Player Stats
↓
Apply Surface Bonus
↓
Apply Fatigue
↓
Apply Confidence
↓
Apply Injury
↓
Calculate Match Rating
↓
Generate Match Events
↓
Determine Winner
↓
Generate Statistics
↓
Update Career
```

---

# 4. Match Rating

每名球员生成：

Match Rating。

计算：

```text
Overall Ability
+
Current Form
+
Surface Bonus
+
Confidence
+
Physical Status
+
Mental Status
+
Experience
-
Fatigue
-
Injury Penalty
```

不是：

Overall 高。

一定赢。

---

# 5. Surface Modifier

不同球员：

不同 Surface。

例如：

```text
Hard
90
Clay
75
Grass
82
```

进入：

Clay。

自动：

使用：

Clay Rating。

不是：

Overall。

---

# 6. Current Form

最近：

10 场比赛。

生成：

Form。

例如：

WWWWW

95

WLWLW

63

LLLLL

28

Form：

直接影响：

Match Rating。

---

# 7. Confidence

Confidence：

影响：

关键分。

Confidence：

90。

抢七表现：

更稳定。

Confidence：

20。

容易：

连续失误。

---

# 8. Fatigue

Fatigue：

降低：

移动。

耐力。

专注。

恢复。

Fatigue：

90+

容易：

第三盘崩盘。

---

# 9. Injury

Minor Injury：

能力：

-5%

Moderate：

-15%

Major：

禁止比赛。

---

# 10. Match Momentum

比赛拥有：

Momentum。

例如：

连续破发。

Momentum：

增加。

Confidence：

提高。

Momentum：

不是能力。

只是：

比赛走势。

---

# 11. Upset System

系统必须允许：

爆冷。

但：

概率合理。

例如：

世界第一。

输给：

世界第120。

概率：

约：

5%。

不是：

50%。

---

# 12. Match Statistics

每场比赛生成：

ACES

Double Fault

First Serve %

Break Points

Winners

Unforced Errors

Net Points

Match Time

未来：

支持：

完整技术统计。

---

# 13. Match Length

根据：

比分。

自动计算：

Duration。

例如：

6-2 6-2

约：

65 分钟。

7-6 7-6

约：

150 分钟。

Duration：

影响：

Fatigue。

---

# 14. Retirement

比赛中。

若：

Health：

低于阈值。

可能：

Retirement。

Ret：

记录：

历史。

新闻。

统计。

---

# 15. Match Importance

不同赛事。

心理压力不同。

Grand Slam：

Pressure

+20%

ATP250：

+5%

压力：

影响：

Mental。

---

# 16. AI Match Behaviour

AI：

拥有：

Aggressive

Balanced

Defensive

Serve First

Baseline

Net Rush

不同风格：

影响：

Statistics。

未来：

可扩展。

---

# 17. Result Generation

比赛结束：

输出：

Winner

Loser

Score

Statistics

Duration

Highlights

MVP

全部进入：

History。

---

# 18. Data Model

```text
MatchSimulation
MatchID
PlayerA
PlayerB
Winner
Score
Duration
Surface
Statistics
MomentumLog
CompletedAt
```

---

# 19. Edge Cases

支持：

- Walkover
- Retirement
- Medical Timeout
- Rain Delay（Future）
- Injury During Match
- Super Tie-break
- Final Set Tie-break
- Grand Slam Rules

---

# 20. Acceptance Criteria

✓ 比赛结果合理

✓ 强者长期更强

✓ 爆冷存在但合理

✓ Statistics 完整生成

✓ Fatigue 正确增加

✓ Injury 正确影响比赛

✓ AI 与玩家统一模拟规则

✓ 长期 Career 稳定运行

---

End of Document

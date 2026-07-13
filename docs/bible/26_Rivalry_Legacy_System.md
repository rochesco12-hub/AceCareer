# Ace Career Game Design Document
## Rivalry & Legacy System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Rivalry & Legacy System（宿敌与传奇系统）负责记录整个职业生涯最重要的人物关系。

它不仅记录数据。

更记录：

- 伟大的对手
- 伟大的时代
- 伟大的纪录
- 伟大的传奇

当玩家回顾 Career 时。

记住的不应该只是：

冠军数量。

而是：

"我和阿尔卡拉斯打了 38 场。"

"我连续三年在温网决赛击败辛纳。"

这才是真正的职业生涯。

---

# 2. Design Goal

系统必须做到：

- 自动形成 Rival
- 自动记录时代
- 自动记录纪录
- 自动形成 Legacy
- AI 与玩家一致

玩家无需主动创建 Rival。

系统自动分析。

---

# 3. Rival Generation

系统持续分析：

Head To Head。

若：

满足：

```text
交手 ≥ 5 次
+
双方排名接近
+
重要赛事交手
+
双方胜率接近
```

自动建立：

Rival。

---

# 4. Rival Level

每组 Rival：

拥有等级。

Level 1

Regular Rival

↓

Level 2

Strong Rival

↓

Level 3

Career Rival

↓

Level 4

Legendary Rival

等级：

自动升级。

---

# 5. Rival Score

系统计算：

```text
Rival Score
=
Head To Head
+
Grand Slam Meetings
+
Final Meetings
+
Ranking Competition
+
Winning Streak
+
Media Attention
```

Score：

越高。

关系越传奇。

---

# 6. Head To Head

保存：

```text
Matches
Wins
Losses
Clay
Grass
Hard
Indoor
Grand Slam
Final
Longest Match
```

Career：

永久保存。

---

# 7. Era Detection

系统自动判断：

是否进入：

某个时代。

例如：

```text
2030~2034
Player
vs
Sinner Era
```

条件：

双方长期：

Top10。

连续：

多年交手。

---

# 8. Legacy Score

玩家拥有：

Legacy Score。

来源：

```text
Grand Slam
+
Masters1000
+
Weeks No.1
+
Titles
+
Win Rate
+
Career Earnings
+
Records
+
Olympics（Future）
```

Legacy：

决定：

历史地位。

---

# 9. Hall of Fame Rating

退役后。

系统自动评分：

例如：

```text
GOAT
Legend
Hall Of Fame
Great Champion
Top Player
Tour Player
```

不是：

只有冠军数。

综合：

Career。

---

# 10. Career Records

系统记录：

Career：

所有纪录。

例如：

```text
Most Titles
Most Grand Slams
Most ATP500
Longest Win Streak
Longest Clay Streak
Longest Grass Streak
Most Weeks No.1
Career Earnings
Career Wins
Career Finals
```

永久保存。

---

# 11. Tournament Records

每项赛事：

拥有：

独立纪录。

例如：

Rome Masters。

保存：

```text
Most Titles
Most Wins
Youngest Champion
Oldest Champion
Fastest Final
Longest Final
```

未来：

不断刷新。

---

# 12. World Records

世界纪录：

例如：

```text
Youngest World No.1
Oldest Grand Slam Champion
Longest Winning Streak
Most Consecutive Finals
Most Career Titles
Most Career Wins
```

所有纪录：

世界共享。

---

# 13. Dynamic Commentary

媒体：

自动生成：

例如：

```text
This is the 17th meeting between Player and Alcaraz.
One of the greatest rivalries of this generation.
```

增强沉浸感。

---

# 14. Legacy Timeline

Career：

自动生成：

时间轴。

例如：

```text
2026
Turned Pro
↓
2027
First ITF Title
↓
2029
Top100
↓
2031
First ATP Title
↓
2033
First Grand Slam
↓
2035
World No.1
↓
2042
Retired
```

无需玩家维护。

---

# 15. Hall of Fame

退役。

自动进入：

Hall Of Fame。

保存：

全部 Career。

未来：

玩家：

可浏览：

所有传奇。

进行：

跨时代比较。

---

# 16. GOAT Ranking

系统：

自动生成：

历史排名。

综合：

```text
Legacy Score
Grand Slam
Weeks No.1
Titles
Win Rate
Strength of Era
Records
```

不是：

只看：

冠军数。

---

# 17. UI

新增：

Career 页面。

包括：

Career Timeline

↓

Hall Of Fame

↓

Records

↓

Rivals

↓

Legacy

↓

Awards

全部：

可浏览。

---

# 18. Data Model

```text
Rival
PlayerA
PlayerB
Matches
Wins
Losses
RivalLevel
RivalScore
StartedSeason
```

```text
Legacy
PlayerID
LegacyScore
HallOfFameLevel
GOATRank
CareerRecords
CareerTimeline
```

---

# 19. Edge Cases

支持：

- Rival 退役
- Rival 复出（Future）
- 三人时代
- 黄金时代
- 单方面统治
- 无 Rival Career

---

# 20. Acceptance Criteria

✓ 自动生成 Rival

✓ 自动建立 Career Timeline

✓ 自动统计所有纪录

✓ 自动计算 Legacy

✓ 自动进入 Hall Of Fame

✓ 自动生成 GOAT Ranking

✓ AI 与玩家一致

✓ 支持无限 Career

---

End of Document

# Ace Career Game Design Document
## Endgame & Retirement System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Endgame System（职业生涯终局系统）负责管理球员职业生涯最后阶段。

Career 不应该无限进行而没有意义。

玩家可以一直继续游戏。

但职业生涯一定会结束。

真正结束的是：

职业。

不是：

世界。

玩家退役以后：

世界仍继续运行。

可以继续观看整个 ATP 世界的发展。

---

# 2. Design Goal

系统必须满足：

- 自然退役
- 主动退役
- AI 自动退役
- Legacy 永久保存
- 世界继续运行
- 可以创建第二职业生涯

---

# 3. Retirement Philosophy

现实职业球员：

最终都会退役。

不会：

40 岁。

依旧：

世界第一。

年龄。

身体。

动力。

家庭。

伤病。

共同决定：

退役时间。

---

# 4. Retirement Pipeline

```text
Career Active
↓
Retirement Decision
↓
Retirement Ceremony
↓
Career Summary
↓
Legacy Evaluation
↓
Hall Of Fame
↓
World Continue
```

---

# 5. Retirement Conditions

满足任意条件：

可以退役。

年龄：

35+

或

重大伤病。

或

长期低排名。

或

玩家主动选择。

AI：

自动判断。

---

# 6. Suggested Retirement

系统：

自动建议。

例如：

```text
You are 38 years old.
Current Ranking
156
Recent Injury
Major Knee Injury
Coach recommends retirement.
```

玩家：

可接受。

也可继续。

---

# 7. Forced Retirement

默认：

没有强制退役。

玩家：

理论可以：

45 岁继续比赛。

但：

能力。

恢复。

伤病。

会严重下降。

实际上很难继续竞争。

---

# 8. Retirement Ceremony

退役当天：

生成：

新闻。

职业总结。

视频（Future）。

包括：

Career Timeline

Career Records

Career Earnings

Titles

Grand Slams

World No.1 Weeks

Hall Of Fame Score

---

# 9. Career Summary

生成：

完整 Career Report。

包括：

```text
Years On Tour
Career Wins
Career Losses
Win Rate
Titles
Grand Slams
Masters
ATP500
ATP250
Career Earnings
Highest Ranking
Weeks At No.1
Best Rival
Most Successful Surface
Longest Winning Streak
```

永久保存。

---

# 10. Legacy Evaluation

系统：

自动计算：

Legacy。

例如：

```text
Legend
Hall Of Fame
GOAT Candidate
Great Champion
Tour Veteran
```

生成：

最终评分。

---

# 11. Hall Of Fame

退役。

自动加入：

Hall Of Fame。

保存：

全部 Career。

玩家：

未来：

可以查看：

任何传奇球员。

---

# 12. Continue World

退役以后。

世界：

不会停止。

AI：

继续：

比赛。

成长。

退役。

新秀。

玩家：

可以：

继续观看。

或者：

开始第二 Career。

---

# 13. Second Career

支持：

New Career。

世界：

重新生成。

不是：

覆盖旧档。

旧 Career：

永久保存。

---

# 14. Records Comparison

退役后：

自动比较：

```text
GOAT Rank
Titles Rank
Grand Slam Rank
Career Earnings Rank
Winning Percentage Rank
Longest Winning Streak Rank
```

帮助玩家了解历史地位。

---

# 15. Awards

退役时：

生成：

Career Awards。

例如：

Most Improved

King Of Clay

Grass Legend

Iron Man

Comeback Player

Big Match Player

全部进入：

History。

---

# 16. Retirement News

自动生成：

例如：

```text
Former World No.1 announces retirement after 18-year career.
```

进入：

News Archive。

---

# 17. Retirement UI

退役页面：

包括：

Career Timeline

↓

Awards

↓

Hall Of Fame

↓

Records

↓

Career Summary

↓

Continue Watching World

↓

Start New Career

---

# 18. Data Model

```text
Retirement
PlayerID
RetiredSeason
RetiredWeek
Age
Reason
LegacyScore
HallOfFameLevel
CareerSummary
Awards
```

---

# 19. Edge Cases

支持：

- 提前退役
- 重伤退役
- 世界第一退役
- 无冠军退役
- AI 集体退役
- Hall Of Fame 满员（理论无限）

---

# 20. Acceptance Criteria

✓ 玩家可自然退役

✓ AI 自动退役

✓ Career Summary 自动生成

✓ Hall Of Fame 自动建立

✓ Legacy 永久保存

✓ 世界继续运行

✓ 支持无限 Career

---

End of Document

# Ace Career Game Design Document
## Tournament Week System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Tournament Week（比赛周）是 Career 中最重要的游戏循环。

Week Mode 属于经营阶段。

Tournament Week 属于比赛阶段。

玩家进入赛事后，游戏自动切换到 Tournament Mode。

玩家退出赛事后，自动恢复 Week Mode。

整个切换过程必须自动完成。

玩家无需手动切换模式。

---

# 2. Design Goal

Tournament Week 必须做到：

- 比普通周节奏更慢
- 更强调比赛体验
- 玩家每场比赛都有决策
- AI 与玩家同步推进
- 保持真实 ATP 比赛节奏

---

# 3. Tournament Mode Entry

进入条件：

```text
Tournament Status
↓
Draw Released
↓
Player Accepted
↓
Travel Completed
↓
Enter Tournament Mode
```

满足条件后：

Today 页面自动切换。

---

# 4. Tournament Timeline

完整赛事流程：

```text
Arrival
↓
Practice
↓
Draw Released
↓
Round 1
↓
Recovery
↓
Round 2
↓
Recovery
↓
Quarterfinal
↓
Recovery
↓
Semifinal
↓
Recovery
↓
Final
↓
Award Ceremony
↓
Tournament Summary
↓
Return Week Mode
```

所有赛事都遵循此流程。

---

# 5. Arrival

进入赛事城市。

系统自动：

- 更新地点
- 更新时区
- 更新天气（预留）
- 更新场地
- 更新球场

长距离旅行：

增加疲劳。

短距离旅行：

影响较小。

---

# 6. Practice Day

比赛开始前：

玩家拥有 Practice。

可选择：

- 发球训练
- 底线训练
- 网前训练
- 战术训练
- 轻度恢复

Practice：

不会提升大量能力。

主要作用：

提高：

Match Readiness。

---

# 7. Match Readiness

新增：

比赛准备度。

范围：

```text
0 ~ 100
```

影响：

- 发挥稳定性
- 开局状态
- 失误率

准备度来源：

- Practice
- Recovery
- Confidence
- Fatigue

---

# 8. Match Day

进入比赛。

Today 页面：

显示：

```text
Round
Opponent
Court
Surface
Start Time
Weather（预留）
```

玩家点击：

开始比赛。

进入：

Match System。

---

# 9. Recovery Day

比赛结束后。

自动进入：

Recovery。

玩家选择：

完全休息

↓

理疗

↓

轻度训练

↓

观看录像

↓

媒体采访

不同选择：

影响：

- 疲劳
- 信心
- Match Readiness
- Injury Risk

---

# 10. Injury During Tournament

若：

比赛受伤。

系统判断：

Minor

↓

继续比赛

Major

↓

Medical Timeout

↓

Retirement

玩家拥有：

继续

或

退赛。

AI 同样。

---

# 11. Tournament Schedule

默认：

一天：

只进行：

一轮。

特殊情况：

允许：

双赛日（预留）。

例如：

雨天延期。

Grand Slam。

ATP 官方特殊安排。

---

# 12. Player Decisions

Tournament Week：

玩家主要决策：

- Practice
- Recovery
- Match
- Withdraw
- Press
- Coach Meeting（预留）

不能：

高强度力量训练。

不能：

长期旅行。

---

# 13. AI Behaviour

AI：

每天：

自动：

- Practice
- Recovery
- Match
- Medical
- Press

AI：

不会：

永远满状态。

AI：

同样受到：

Fatigue。

Injury。

Confidence。

影响。

---

# 14. Match Result

比赛结束。

系统更新：

- Ranking Points（暂存）
- Prize Money
- Match Statistics
- Confidence
- Fatigue
- Injury
- News

正式 ATP 排名：

下一 Week。

统一更新。

---

# 15. Elimination

若：

玩家出局。

Tournament Week：

立即结束。

进入：

Tournament Summary。

随后：

Week Mode。

玩家可以：

提前规划：

下一站赛事。

---

# 16. Champion

若：

获得冠军。

系统：

播放：

Award Ceremony。

生成：

冠军新闻。

更新：

Career Statistics。

加入：

History。

---

# 17. Tournament Summary

赛事结束：

显示：

- 最终成绩
- 获得积分
- 奖金
- 当前排名
- 排名变化
- 胜负记录
- 技术统计
- 下一站推荐赛事

玩家点击：

继续下一周。

返回：

Week Mode。

---

# 18. UI

Today：

Tournament Mode：

顶部：

```text
ATP250 Doha
Quarterfinal
```

中部：

Opponent Card。

底部：

Quick Actions：

- Practice
- Recovery
- Match
- Tournament Draw
- Statistics

首页：

始终保持：

单屏。

---

# 19. Data Model

```text
TournamentWeek
TournamentID
CurrentRound
CurrentMatch
CurrentCity
ArrivalDate
PracticeCompleted
RecoveryCompleted
Status
```

---

# 20. State Machine

```text
Travel
↓
Arrival
↓
Practice
↓
Match
↓
Recovery
↓
Next Round
↓
Champion
↓
Summary
↓
Week Mode
```

不得：

跳过：

Recovery。

不得：

直接：

Round1

↓

Final。

---

# 21. Edge Cases

必须支持：

- Injury Before Match
- Injury During Match
- Walkover
- Retirement
- Rain Delay（预留）
- Medical Timeout
- Bye
- Lucky Loser Opponent
- Opponent Withdrawal
- Final Cancelled（预留）

---

# 22. Acceptance Criteria

完成后：

✓ Week 自动切换 Tournament Mode

✓ 比赛结束自动恢复 Week Mode

✓ Recovery 正常运行

✓ Practice 正常运行

✓ Fatigue 正常累计

✓ Injury 正常处理

✓ Tournament Summary 正常生成

✓ Champion Ceremony 正常生成

✓ AI 与玩家同步推进

✓ 支持所有赛事级别

---

End of Document

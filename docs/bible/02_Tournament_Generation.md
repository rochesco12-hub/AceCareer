# Ace Career Game Design Document
## Tournament Generation System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Tournament Generation System 负责生成整个职业网球世界的赛事。

它不是生成玩家赛事。

而是生成整个世界未来所有赛事。

所有 AI 与玩家共享同一份赛事数据库。

整个世界只有一个 Tournament Database。

---

# 2. Design Goal

整个世界任何时候都应该让玩家感觉：

> 「世界一直在举办比赛。」

玩家永远不会遇到：

- 没有比赛
- 没地方报名
- 世界停下来等待玩家

Calendar 每推进一周。

Tournament Generator 自动生成新的赛事窗口。

---

# 3. Generation Philosophy

Tournament Generator 必须满足：

### Rule 1

真实。

参考 ATP Calendar。

不能随机生成：

北京 ATP500

放到六月。

这种情况禁止。

---

### Rule 2

持续。

世界不会因为玩家退赛而取消赛事。

---

### Rule 3

多选择。

每周必须拥有多个赛事。

绝不能：

Week 15

只有：

一个 ITF。

---

### Rule 4

层级完整。

同一周必须同时存在：

ITF

↓

Challenger

↓

ATP

不同层级。

供不同排名球员选择。

---

# 4. Weekly Tournament Pool

默认：

每一周：

系统生成：

ITF M15

3~5站

ITF M25

1~3站

Challenger

1~2站

ATP250

按真实赛历

ATP500

按真实赛历

Masters1000

按真实赛历

Grand Slam

按真实赛历

玩家排名决定：

可报名范围。

不是：

赛事是否存在。

---

# 5. Tournament Database

所有赛事进入：

Tournament Database。

字段：

TournamentID

Season

Week

Category

Surface

City

Country

PrizeMoney

ChampionPoints

DrawSize

QualifyingSize

Status

EntryOpenWeek

StartWeek

EndWeek

AIPlayers

PlayerEntries

Champion

HistoryID

数据库：

整个世界共享。

---

# 6. Tournament Creation Pipeline

Calendar

↓

读取 Week

↓

检查真实赛历

↓

创建 Tournament

↓

加入 Database

↓

开放报名

↓

AI开始规划

↓

玩家收到通知

整个流程：

自动执行。

无需玩家参与。

---

# 7. Tournament Categories

### ITF

新人赛事。

积分低。

奖金低。

竞争弱。

适合：

新人。

恢复信心。

---

### Challenger

晋级赛事。

连接：

ITF

ATP。

主要目标：

冲击 Top100。

---

### ATP250

职业巡回赛。

奖金明显增加。

竞争激烈。

---

### ATP500

世界高手大量参加。

成为：

Top30。

主要战场。

---

### Masters1000

全年重点。

积分巨大。

AI：

优先级极高。

---

### Grand Slam

全年最重要赛事。

最高奖金。

最高积分。

最大曝光。

所有 AI：

优先参加。

---

# 8. Tournament Priority

AI 为每项赛事计算：

Priority Score。

例如：

Priority

=

Points

+

Prize

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

最终：

选择：

Priority 最大赛事。

---

# 9. Geographic Distribution

赛事不能全部：

欧洲。

系统按照：

真实地区。

生成：

Australia

Europe

North America

Asia

South America

Middle East

Africa

不同赛季。

不同地区。

避免：

连续：

欧洲。

欧洲。

欧洲。

降低旅行真实性。

---

# 10. Surface Distribution

每个阶段：

Surface 固定。

例如：

Clay Season。

所有主要赛事：

Clay。

Grass Season。

主要赛事：

Grass。

玩家需要：

制定赛季计划。

AI 同样。

---

# 11. Tournament Availability

玩家：

并不是：

所有赛事。

都能报名。

例如：

世界排名：

850。

系统：

推荐：

ITF。

ATP250：

显示：

Ranking Too Low。

赛事：

仍然存在。

只是：

不能报名。

---

# 12. AI Tournament Planning

AI：

提前：

4周。

开始规划。

例如：

Week18。

AI：

已经知道：

Week22。

法网。

AI：

可能：

减少比赛。

提前恢复。

现实职业球员：

也是这样。

---

# 13. Replacement Logic

Withdrawal。

以后。

系统：

自动：

Waiting List。

↓

Lucky Loser。

↓

重新生成：

Acceptance。

不允许：

Bracket：

空缺。

---

# 14. History

每一站赛事结束。

自动进入：

History。

保存：

冠军

亚军

四强

奖金

积分

新闻

比赛记录

永久保存。

---

# 15. Acceptance Criteria

Tournament Generation 完成后：

✓ 每周拥有多个赛事

✓ 世界不会缺少赛事

✓ AI 自动规划

✓ 地区正确轮换

✓ Surface 正确轮换

✓ Tournament Database 永久增长

✓ 历史完整保存

✓ 支持20+赛季

---

End of Document

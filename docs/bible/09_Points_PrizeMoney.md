# Ace Career Game Design Document
## Ranking Points & Prize Money System

Version: 1.0
Status: Draft
Priority: P0

---

# 1. Purpose

Points & Prize Money System（积分与奖金系统）负责管理整个职业生涯中的：

- ATP Ranking Points
- ATP Race Points
- Prize Money
- Career Earnings
- Ranking Defence
- Financial Growth

它决定：

- 球员世界排名
- 是否能够参加更高级别赛事
- 职业收入
- 职业发展速度

---

# 2. Design Goal

系统必须满足：

- 基于真实 ATP 积分体系
- 支持长期 Career
- 奖金与积分独立计算
- AI 与玩家完全一致
- 支持未来自定义积分规则

---

# 3. Tournament Reward Pipeline

```text
Tournament Completed
↓
Determine Final Position
↓
Award Ranking Points
↓
Award Race Points
↓
Award Prize Money
↓
Update Career Earnings
↓
Update Season Earnings
↓
Update Ranking History
↓
Generate News
```

所有奖励必须一次性结算。

不得分批结算。

---

# 4. Ranking Points

每项赛事拥有固定积分。

例如：

| Tournament | Champion |
|------------|----------:|
| ITF M15 | 15 |
| ITF M25 | 25 |
| Challenger 50 | 50 |
| Challenger 75 | 75 |
| Challenger 100 | 100 |
| ATP250 | 250 |
| ATP500 | 500 |
| Masters1000 | 1000 |
| Grand Slam | 2000 |

后续支持 ATP 官方积分表更新。

---

# 5. Round Points

不同轮次对应不同积分。

例如：

ATP250

Champion

250

Runner-up

165

Semifinal

100

Quarterfinal

50

Round2

25

Round1

0

积分表可配置。

不是写死。

---

# 6. ATP Race

ATP Race 独立计算。

特点：

- 每赛季重新开始
- 不计算保分
- 用于 ATP Finals

Career Ranking

≠

ATP Race

两个榜单必须独立维护。

---

# 7. Career Ranking

Career Ranking：

采用 Rolling 52 Weeks。

只统计：

过去 52 周积分。

进入新 Week：

自动删除：

53 周以前积分。

无需玩家操作。

---

# 8. Ranking Defence

系统自动记录：

去年同期获得积分。

例如：

2026 Week18：

冠军

250 Points

2027 Week18：

必须保分。

若提前出局。

自动扣除：

去年积分。

这是 ATP 排名最重要规则之一。

---

# 9. Live Ranking

赛事期间：

显示：

Live Ranking。

例如：

目前即时排名：

67

预计夺冠：

58

正式排名：

下一 Week 更新。

Live Ranking：

仅供参考。

---

# 10. Prize Money

每站赛事拥有奖金池。

奖金按照轮次发放。

例如：

ATP250：

Champion

$95,000

Runner-up

$55,000

Semifinal

$32,000

Quarterfinal

$18,000

奖金未来可同步真实 ATP 数据。

---

# 11. Career Earnings

Career 保存：

Career Earnings。

永久累计。

例如：

Career Earnings

$18,450,000

退役后：

永久保存。

Hall of Fame：

显示：

Career Prize Money。

---

# 12. Season Earnings

每赛季：

单独统计。

例如：

2027 Earnings

$1,250,000

赛季结束：

清零。

Career：

不清零。

---

# 13. Taxes（预留）

未来版本：

支持：

税务。

例如：

奖金：

100,000

税：

20%

最终收入：

80,000

Alpha：

暂不启用。

---

# 14. Sponsor Bonus

未来：

赞助合同：

根据：

成绩。

自动发放奖金。

例如：

进入 Grand Slam 四强。

奖励：

$80,000

属于：

商业收入。

不属于：

Prize Money。

---

# 15. Appearance Fee

部分赛事：

允许：

Appearance Fee。

例如：

ATP250。

邀请 Top10。

给予：

Appearance Fee。

AI：

同样适用。

---

# 16. Financial Summary

每周结束：

生成：

Financial Report。

包括：

Prize Money

Sponsor Income

Coach Salary

Travel Cost

Medical Cost

Net Income

Cash Balance

帮助玩家管理职业生涯。

---

# 17. UI

比赛结束：

显示：

获得积分

↓

奖金

↓

Career Earnings

↓

Live Ranking

↓

Official Ranking（Next Week）

首页：

显示：

Career Earnings

Current Ranking

Race Ranking

---

# 18. Data Model

```text
TournamentReward
RewardID
TournamentID
Round
RankingPoints
RacePoints
PrizeMoney
```

```text
CareerFinance
CareerEarnings
SeasonEarnings
CashBalance
TotalTax
SponsorIncome
PrizeMoneyIncome
```

---

# 19. Edge Cases

支持：

- Withdrawal
- Walkover
- Retirement
- Qualification Points
- Lucky Loser
- Protected Ranking
- Tournament Cancelled
- Shared Prize（预留）

---

# 20. Acceptance Criteria

完成后：

✓ ATP Points 正确结算

✓ ATP Race 独立维护

✓ Rolling 52 Weeks 正常运行

✓ Ranking Defence 自动计算

✓ Live Ranking 正常显示

✓ Prize Money 正确发放

✓ Career Earnings 永久保存

✓ AI 与玩家统一规则

✓ 支持长期 Career

---

End of Document

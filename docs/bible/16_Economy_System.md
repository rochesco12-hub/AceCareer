# Ace Career Game Design Document
## Career Economy System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Economy System（经济系统）负责模拟职业球员整个职业生涯的财务管理。

它不仅统计奖金。

更重要的是：

让玩家真正经营自己的职业生涯。

收入与支出都会影响未来的发展。

---

# 2. Design Goal

经济系统必须满足：

- 奖金 ≠ 最终收入
- 玩家必须管理现金流
- AI 与玩家遵循同一套经济规则
- 收入、支出、资产全部可追踪
- 支持 20+ 赛季

---

# 3. Economy Pipeline

```text
Tournament Finish
↓
Prize Money
↓
Sponsor Income
↓
Expenses
↓
Tax
↓
Cash Balance
↓
Financial Report
```

所有经济变化必须记录。

---

# 4. Income Sources

收入包括：

- Tournament Prize Money
- Sponsor Income
- Appearance Fee
- National Team Bonus（预留）
- Year-end Bonus（预留）

所有收入进入：

Career Wallet。

---

# 5. Expense Sources

支出包括：

- Coach Salary
- Fitness Coach
- Physio
- Sports Psychologist
- Travel
- Hotel
- Training Base
- Equipment
- Medical Treatment

职业球员不能只有收入。

---

# 6. Cash Balance

玩家拥有：

```text
Current Cash
```

所有消费：

直接扣除。

若余额不足：

无法：

- 聘请高级团队
- 升级训练基地
- 购买高级恢复方案

---

# 7. Team Salary

团队采用周薪。

例如：

| Staff | Weekly Cost |
|--------|------------:|
| Coach | $2,000 |
| Fitness Coach | $1,200 |
| Physio | $1,500 |
| Psychologist | $1,000 |

每周自动扣款。

---

# 8. Travel Cost

旅行费用根据：

- 距离
- 舱位
- 地区

计算。

例如：

欧洲境内：

$300

欧洲 → 北美：

$2,200

亚洲 → 澳洲：

$1,800

未来支持：

经济舱 / 商务舱。

---

# 9. Hotel Cost

住宿根据赛事等级自动推荐。

例如：

ITF：

$80 / 天

Challenger：

$120 / 天

ATP：

$220 / 天

玩家可升级酒店。

提高恢复效率。

---

# 10. Equipment

装备包括：

- 球拍
- 球线
- 鞋
- 护具

装备拥有：

耐久度。

需要定期更换。

未来可接入品牌赞助。

---

# 11. Medical Cost

受伤后：

玩家可选择：

普通治疗

↓

高级治疗

↓

顶级医疗团队

费用越高：

恢复越快。

---

# 12. Sponsor System（预留接口）

赞助商根据：

- 世界排名
- 成绩
- 曝光度

主动提供合同。

合同包括：

- 固定收入
- 成绩奖金
- 品牌要求

---

# 13. Financial Report

每周结束：

自动生成：

```text
Income
Prize Money
Sponsor
Expenses
Travel
Coach
Medical
Net Income
Cash Balance
```

方便玩家了解现金流。

---

# 14. Bankruptcy Rule

现金低于：

0。

不会 Game Over。

系统自动：

降低消费。

解除高薪团队。

推荐低级赛事。

帮助玩家恢复现金流。

---

# 15. AI Economy

AI 同样拥有：

收入。

支出。

团队。

旅行成本。

AI 不允许无限资金。

---

# 16. Data Model

```text
Economy
PlayerID
CashBalance
CareerIncome
CareerExpense
SeasonIncome
SeasonExpense
WeeklyExpense
SponsorIncome
PrizeMoneyIncome
TravelExpense
MedicalExpense
```

---

# 17. Edge Cases

支持：

- Sponsor Lost
- Team Contract End
- Medical Emergency
- Cash Negative
- Tournament Cancelled
- Appearance Fee Cancelled

---

# 18. Acceptance Criteria

完成后：

✓ 收支完整记录

✓ 每周自动生成财务报表

✓ 团队薪资自动扣除

✓ 差旅自动计算

✓ AI 与玩家统一规则

✓ 长期 Career 稳定运行

---

End of Document

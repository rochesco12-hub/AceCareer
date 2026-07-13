# Ace Career Development Bible
# 55 · Economy Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Economy Engine 定义整个 Ace Career 的职业经济系统。

经济系统不是金币系统。它模拟职业网球真正的商业运作：奖金、赞助、团队开支、旅行费用、税务、投资。所有收入与支出共同决定一位球员职业生涯的发展质量。不是为了赚钱，而是为了支持职业发展。

---

# Design Goals

✓ 真实职业经济 ✓ 长期成长 ✓ Config Driven ✓ AI/玩家一致 ✓ 不变成经营游戏 ✓ 百年稳定 ✓ 未来商业玩法

---

# Eight Economy Components

Prize Money / Sponsors / Appearance Fees / Staff Salary / Travel / Medical / Training / Investment（未来）

---

# Cash Flow

```
Income - Expenses = Cash Flow
```

---

# Net Worth

```
Cash + Investment + Contracts = Net Worth
```

---

# Financial Health Levels

Critical → Stable → Comfortable → Wealthy → Elite

---

# Key Features

- **Prize Money**：Grand Slam/Masters/ATP500/250/Challenger/ITF（全部读取 Config）
- **Sponsor Income**：Equipment/Apparel/Luxury/Technology/Nutrition（长期稳定收入）
- **Appearance Fees**：Popularity 95 → $300,000（高人气球员赛事邀请）
- **Staff Expenses**：Coach/Fitness/Physio/Doctor/Nutritionist/Agent（每周自动结算）
- **Travel Expenses**：Flights/Hotels/Transportation（高级团队成本更高）
- **Medical Expenses**：Treatment/Rehabilitation/Surgery（重大伤病经济压力增加）
- **Training Expenses**：Facilities/Equipment/Training Camp（投入越高成长效率越高）
- **Investment System**（未来）：Property/Business/Stocks/Foundations（退役后财富来源）
- **Budget Planning**：Training/Medical/Staff/Travel 预算自主设置
- **AI Economy**：AI 同样需要 Pay Staff/Choose Coach/Upgrade Team（无限资源）
- **Financial Events**：Big Sponsor/Luxury Contract/Financial Crisis/Career Investment → Story
- **Economy Impact**：不直接提高能力，但间接影响 Coach/Recovery/Training/Staff/Travel Quality
- **Retirement Wealth**：Career Prize/Sponsor Income/Net Worth/Career Expenses（职业财务总结）

---

# Config Files

economy.json / expenses.json / income.json / investment.json

---

# Performance

- Weekly Settlement <10ms
- Career Finance Realtime
- 2200 Players Stable

---

# Definition of Done

✓ 完整职业经济循环 ✓ AI/玩家一致 ✓ 收支平衡 ✓ 商业故事联动 ✓ Career 财务总结 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

职业球员真正需要管理的不是银行账户，而是自己的整个职业生涯。

Economy Engine 让每一次冠军奖金都真正拥有价值。

---

End of Document

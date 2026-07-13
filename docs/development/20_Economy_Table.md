# Ace Career Development Bible
# 20 · Economy Table

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Economy Table 定义整个 Ace Career 的职业经济系统。

它回答的核心问题："职业球员如何靠网球生存。" 经济不仅影响玩家，更影响整个 AI 世界。

---

# Design Goals

✓ 职业真实 ✓ 长期稳定 ✓ Config Driven ✓ AI 可理解 ✓ 无需 Grind ✓ 支持未来赞助/团队经营

---

# 收入来源 vs 支出

| 收入 | 支出 |
|------|------|
| Prize Money | Coach Salary（Amateur $0~300 → Elite $15,000+/周）|
| Sponsor | Travel（距离×航班×酒店×地区×赛事等级）|
| Appearance Fee | Medical（Massage/Recovery/MRI/Surgery）|
| National Team Bonus | Equipment（球拍/球线/鞋/配件）|
| Achievement Bonus | Training Camp（西班牙学院/佛罗里达/高原训练）|

---

# 经济阶层

- **Top10**：极高收入（奖金+赞助）
- **Top100**：稳定收入
- **Top300**：勉强收支平衡
- **500+**：可能亏损，需自担机票/酒店/教练

---

# 每站赛事净利润

```
Prize - Travel - Coach - Hotel - Medical = Net Income
```

---

# Key Features

- **Sponsor 收入**受 Ranking / Titles / Popularity / Nationality / Media Exposure 共同影响，不是固定收入
- **AI 受经济压力驱动**：余额不足 → 优先附近赛事，避免跨洲旅行
- **Bankruptcy**（未来）：不会 Game Over，但需降级教练/打 ITF
- **年度 Inflation**：Prize +2% / Coach +2% / Travel +1.5%
- **Career 页面**显示 Career Prize Money / Expenses / Net Worth / Largest Prize

---

# Config Files

economy.json / coach_cost.json / travel_cost.json / sponsor.json / prize_money.json

Engine 不保存任何金额。

---

# Performance

- Income Calculation <2ms
- Season Summary <10ms
- Career Finance Realtime

---

# Definition of Done

✓ 职业收入完整 ✓ 职业支出完整 ✓ AI 理解经济压力 ✓ 长期经济稳定 ✓ Config 驱动 ✓ 支持未来经营玩法

---

# Final Principle

真正的职业生涯不仅要赢得冠军，还要学会经营自己的职业人生。奖金不是数字，而是职业选择的结果。

---

End of Document

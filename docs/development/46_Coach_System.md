# Ace Career Development Bible
# 46 · Coach System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Coach System 定义整个 Ace Career 的教练系统。

教练不是装备、不是 Buff、不是数值插件。教练是职业生涯中最重要的伙伴之一。Coach System 不直接增加 Overall，而是影响整个 Career Loop：训练方向、恢复质量、比赛准备、职业规划。

---

# Design Goals

✓ 长期合作 ✓ 数据驱动 ✓ AI/玩家一致 ✓ Config Driven ✓ 不同执教风格 ✓ 教练成长 ✓ 百年稳定

---

# Eight Coach Categories

| Category | 擅长 |
|----------|------|
| Technical | Serve / Forehand / Backhand / Volley |
| Tactical | Match Strategy / Surface Adaptation / Big Match |
| Fitness | Endurance / Strength / Movement / Recovery |
| Mental | Confidence / Pressure / Focus / Resilience |
| Development | Potential Growth / Training Efficiency（年轻球员）|
| Veteran | Decline↓ / Recovery↑ / Consistency↑（延长巅峰）|
| Specialist | 特定 Surface / 特定打法 |
| Legendary | Career Planning ★5 / Training ★5 / Mental ★5（极少/极高费用）|

---

# Coach Levels

Local → Regional → National → Professional → Elite → Legendary

---

# Key Features

- **Coach Relationship**（0~100）：长期合作→默契提高→训练效率提升
- **Coach Loyalty**：5 Years Together → Loyalty↑
- **Coach Change**：Hire / Renew / Upgrade / Dismiss（AI 同样遵循）
- **Coach Salary**：Weekly Salary + Bonus + Performance Bonus → 进入 Economy
- **Coach Reputation**：Coached 5 Slam Champions → Legendary Coach
- **Coach Growth**：Young Coach→Experience→Elite Coach（AI 世界持续成长）
- **Coach Retirement**：教练同样退役（未来传奇教练继续执教）
- **AI Coach**：AI 根据 Economy/Goal/Results 自动决定 Hire/Upgrade/Fire/Keep
- **Match Preparation**（未来）：Opponent Analysis→Surface Plan→Match Strategy
- **Story Connection**：New Coach/Historic Partnership/Coach Split/Legendary Duo
- **Media Connection**：传奇教练加盟自动生成 News→Career Timeline→Story

---

# Config Files

coach.json / coach_levels.json / styles.json / salary.json

---

# Performance

- Coach Update <5ms
- Relationship Update Realtime
- Coach Search Realtime

---

# Definition of Done

✓ 多类型教练 ✓ AI 自动聘请教练 ✓ 长期合作关系 ✓ 教练成长 ✓ Story 深度联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

伟大的冠军很少独自诞生。每一位传奇球员的背后几乎都有一位同样伟大的教练。

Coach System 负责塑造职业生涯中最重要的伙伴关系。

---

End of Document

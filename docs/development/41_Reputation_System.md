# Ace Career Development Bible
# 41 · Reputation System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Reputation System 定义整个 Ace Career 的职业声望系统。

Reputation 不等于 Popularity。Popularity 是大众喜欢程度，Reputation 是职业圈对你的评价。它影响赛事邀请、赞助等级、媒体关注、AI 态度、Hall of Fame、Legacy。

---

# Design Goals

✓ 长期积累 ✓ 难以获得 ✓ 容易失去 ✓ Story Driven ✓ AI/玩家一致 ✓ Config Driven ✓ 百年稳定

---

# Reputation Levels

Unknown → Recognized → Respected → Elite → Legendary → Iconic

---

# Eight Reputation Categories

| Category | 来源 |
|----------|------|
| Professional | Attendance / Withdrawals / Training / Professionalism / Conduct |
| Champion | Big Titles / Final Wins / Major Performances |
| Sportsmanship | Fair Play / Respect / Code Violations（未来更丰富）|
| Big Match | Grand Slam Finals / Pressure Performance |
| Consistency | Top10 8 Seasons（长期稳定 >> 一年爆发）|
| Legend | Career Milestones / Historic Moments |
| Media | Results + Behavior + Story + Interviews |
| Global | Career Slam / Olympic Champion → Global Icon |

---

# Reputation Score

```
Results + Ranking + Titles + Consistency + Sportsmanship + Historic Moments = Reputation Score
```

不是 Popularity。

---

# Key Features

- **Growth Curve**：20→40 容易，80→90 极难（长期目标）
- **Loss**：Repeated Withdrawals / Bad Sportsmanship → Reputation↓（下降快于成长）
- **AI Perception**：Legend→Respect / Young Player→Challenge
- **Tournament Impact**：高 Reputation 球员更容易获得 Wildcard
- **Sponsor Impact**：赞助优先考虑 Reputation 而不仅是 Ranking（传奇老将仍拥有高价值赞助）
- **Story Connection**：Respected Veteran vs Young Challenger
- **Legacy Connection**：Reputation → Legacy → Hall Of Fame → GOAT
- **Reputation Timeline**：Unknown→Recognized→Elite→Legendary

---

# Config Files

reputation.json / sportsmanship.json / media.json / professionalism.json

---

# Performance

- Update Reputation <5ms
- Career Query Realtime
- AI Lookup Realtime

---

# Definition of Done

✓ Reputation 长期积累 ✓ Story 深度联动 ✓ AI 感知 Reputation ✓ Legacy 自动引用 ✓ Hall Of Fame 使用 Reputation ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

冠军赢得的是比赛。Reputation 赢得的是整个职业网球世界的尊重。

当一位球员走进球员通道，所有人都知道他是谁——这就是 Reputation。

---

End of Document

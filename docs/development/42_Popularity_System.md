# Ace Career Development Bible
# 42 · Popularity System

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Popularity System 定义整个 Ace Career 的人气系统。

Popularity ≠ Reputation。Reputation 来自职业圈的尊重，Popularity 来自公众的喜爱。它影响门票销量、社交媒体关注、商业价值、媒体曝光、比赛关注度、品牌合作。世界第一未必拥有最高人气——很多球员因为打法/性格/故事/国家拥有远超排名的人气。

---

# Design Goals

✓ 长期积累 ✓ 可快速增长 ✓ 可快速下降 ✓ Story 驱动 ✓ AI/玩家一致 ✓ Config Driven ✓ 未来社交媒体

---

# Popularity Levels

Unknown → Rising → Recognized → Popular → Superstar → Global Icon

---

# Six Popularity Categories

| Category | 内容 |
|----------|------|
| Performance | Winning Streak / Grand Slam / Epic Match（持续时间有限）|
| Story | Comeback / Underdog / Historic Rivalry / Teen Champion（传播最快）|
| Personality | (未来) Charismatic/Funny/Calm/Passionate/Reserved → 不同球迷 |
| Nationality | Home Slam Champion → Popularity↑（网球传统越强增长越快）|
| Media Exposure | Grand Slam Final ★5 / ATP250 R1 ★1 |
| Entertainment | Big Server → Highlight Player → Popularity↑ |

---

# Popularity Score

```
Performance + Story + Media + Nationality + Titles + Historic Moments = Popularity
```

并非 Ranking。

---

# Key Features

- **Growth Curve**：100→1000 容易，1M→10M 困难（非线性）
- **Decay**：长期无曝光→Popularity↓（传奇球员下降更慢）
- **Fan Base**（未来）：Local/Global/Hardcore/Casual → 不同价值
- **Home Crowd**：Nationality = Tournament Country → Popularity Bonus
- **Social Media**（未来）：Followers/Engagement/Trending/Viral Moments
- **Sponsor Connection**：Global Icon → Luxury Brand（商业价值远高于普通球员）
- **Ticket Sales**：Player Popularity → Attendance → Revenue
- **Broadcast Value**：宿敌大战天然加成 TV Rating/Streaming/Highlights
- **Reputation Independence**：Popularity 95 + Reputation 72（球迷喜欢但职业圈评价一般 → 两者永远独立）
- **Timeline**：First Viral Match→Global Superstar→Most Popular Player

---

# Config Files

popularity.json / media.json / fans.json / social.json

---

# Performance

- Popularity Update <5ms
- Fan Query Realtime
- Media Query Realtime

---

# Definition of Done

✓ Reputation 完全独立 ✓ Story 自动提升人气 ✓ 球迷系统 ✓ 未来社交媒体 ✓ Sponsor 深度联动 ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

有些球员赢得冠军。有些球员赢得全世界。

Popularity System 负责记录每一位球员在球迷心中的位置。

---

End of Document

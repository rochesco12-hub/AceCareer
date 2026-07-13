# Ace Career Development Bible
# 45 · Personality Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Personality Engine 定义整个 Ace Career 的人格系统。

同样的能力值，因为 Personality 不同，职业生涯也会完全不同。Personality 不只一个标签——它影响 AI 决策、比赛风格、职业规划、媒体形象、训练偏好、宿敌关系、球迷喜爱程度。

---

# Design Goals

✓ 长期稳定 ✓ 缓慢成长 ✓ AI/玩家一致 ✓ Config Driven ✓ 深度影响世界 ✓ 支持 Story ✓ 百年稳定

---

# 九维人格（0~100）

| Dimension | 影响 |
|-----------|------|
| Confidence | Big Matches / Pressure / Comebacks / Momentum（高→更容易逆转）|
| Discipline | Training / Recovery / Lifestyle / Fatigue（高→成长更稳定）|
| Aggression | Match Style / Shot Selection / Risk / Media Image |
| Resilience | Losing Streak / Injury / Pressure / Comeback（高→更容易东山再起）|
| Professionalism | Recovery / Coach / Training / Consistency（长期决定 Career）|
| Charisma | Popularity / Media / Sponsors / Fans（不是实力而是人格魅力）|
| Patience | Career Planning / Training / Recovery / Tournament Choice（高→更少冒险）|
| Risk Taking | Schedule / Shot Choice / Coach Change / Tournament Entry |
| Competitiveness | Rivalry / Important Matches / Training / Goals（越强越追求冠军）|

---

# Key Features

- **Personality Growth**：Young Low Confidence → Grand Slam Champion → Confidence↑（但不会从 10→90）
- **Personality Events**：Career-ending Injury → Resilience↓ Confidence↓（Story 推动成长）
- **Personality Types**：系统自动生成标签（Ice Man / Showman / Workhorse / Fighter / Veteran Leader / Silent Killer）来自九维人格，不是单独存储
- **AI Personality**：Risk Taking 95 → Skip Recovery → Play More Events（形成不同职业路线）
- **Player Personality**：未来支持通过赛后采访/比赛决策逐渐塑造
- **Media Connection**：Calm Champion vs Aggressive Challenger vs Veteran Leader
- **Sponsor Connection**：Charismatic→Luxury Brands / Professional→Technology Brands
- **Story Connection**：Never Gives Up → Legendary Comeback

---

# Config Files

personality.json / traits.json / growth.json / events.json

---

# Performance

- Personality Update <2ms
- AI Query Realtime
- Story Lookup Realtime

---

# Definition of Done

✓ 九维人格模型 ✓ AI 完全读取人格 ✓ Story 自动影响人格 ✓ 支持玩家成长 ✓ Config 驱动 ✓ 商业系统联动 ✓ 百年稳定

---

# Final Principle

真正让球迷记住一位球员的，从来不只是他的冠军数量，而是他的性格。

Personality Engine 让每一位球员都拥有属于自己的灵魂。

---

End of Document

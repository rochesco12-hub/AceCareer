# Ace Career Development Bible
# 32 · Narrative Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Narrative Engine 是整个 Ace Career 的叙事引擎。

Story Engine 负责产生故事。News Engine 负责报道故事。Narrative Engine 负责把所有故事串联成一段真正的职业生涯。这是整个 Career Mode 最具有沉浸感的系统。

现实体育从来不是一件件孤立事件，而是故事推动故事。第一次输→连续三次失败→终于复仇→成为宿敌→多年后共同退役。四场比赛，被 Narrative 变成一段传奇。

---

# Design Goals

✓ 长期连续 ✓ 自动组织 ✓ 不依赖 AI ✓ Config Driven ✓ 所有球员 ✓ 世界历史 ✓ 百年稳定

---

# Story vs Narrative

- **Story**：一个事件（Won Wimbledon）
- **Narrative**：一系列 Story（Lost Final→Lost Semi→Lost Final→Won Championship→Defended Title），拥有完整情绪曲线

---

# Narrative Lifecycle

```
Beginning → Development → Turning Point → Climax → Ending → Legacy
```

---

# 12 种 Narrative 类型

| Type | 示例 |
|------|------|
| Rise | ITF→Challenger→Top100→Top20→Grand Slam→No.1 |
| Fall | No.2→Injury→Top80→Confidence Lost→Outside Top200 |
| Comeback | Major Injury→Miss 1 Year→Return→Top10→Champion |
| Rivalry | 多年多次在 AO/Rome/US Open/ATP Finals 连续相遇 |
| Dynasty | 4 Years + 8 Grand Slams + No.1 → 时代 |
| Redemption | Lost Final×3 → Finally Won |
| Collapse | Champion→Injury→Ranking Drop→Coach Leave→Retirement |
| Transition | Federer Retired→Nadal Decline→New No.1→New Era |
| Era | Big Three Era→Young Generation→Next Generation |
| Journey | 长期跨国多赛季的完整职业旅程 |
| Breakthrough | 单赛季内从无名到突破性成就 |
| Legacy | Career Slam / Golden Slam / Historic Rivalry |

---

# Key Features

- **Narrative Builder**：持续监听 Story→Story→Story，足够时才 Build Narrative
- **Narrative Memory**：Won French Open → 5 Years Later → Still Clay King
- **Narrative Conflict**：Young Star vs Old Champion same tournament → Story 自动升级
- **Narrative Evolution**：Villain→Champion→Legend，职业生涯不断演化
- **Narrative End**：结束后不删除，进入 History→Legacy→Hall Of Fame 永久保存
- **World Narrative**：Spanish Era→American Revival→Asian Breakthrough
- **AI Narrative**：AI 同样拥有完整 Narrative（Unknown Junior→Grand Slam Champion→Legend）

---

# Narrative Weight

Legendary / Historic / Major / Normal / Minor → 决定 News/Timeline/首页 展示频率

---

# Config Files

narrative.json / arc.json / timeline.json / legacy.json / importance.json

---

# Performance

- Narrative Detection <15ms
- Weekly Update <40ms
- 100 Years Stable

---

# Definition of Done

✓ 自动生成职业叙事 ✓ Story 自动连接 ✓ 支持 Career Arc ✓ 支持世界历史 ✓ AI 拥有完整 Narrative ✓ Config 驱动 ✓ 百年稳定

---

# Final Principle

一场比赛可以创造一个冠军。一段叙事才能创造一个传奇。

Narrative Engine 负责把一场场比赛编织成一段值得铭记的职业人生。

---

End of Document

# Ace Career Development Bible
# 31 · Story Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Story Engine 是整个 Ace Career 最重要的系统。

新闻描述事实。Story 解释事实。玩家多年以后记住的不是"2036年第17周ATP500冠军世界排名第8"，而是"那一年我终于击败了宿敌""那一年我结束了连续两年的伤病"。

Story Engine 负责创造这些记忆。

---

# Design Goals

✓ 长期连续 ✓ 自动生成 ✓ 不依赖 AI ✓ Config Driven ✓ 世界所有球员共享 ✓ 可扩展 ✓ 百年稳定

---

# Story 五层架构

```
Point → Match → Tournament → Season → Career
```

越往上，故事跨度越长。

---

# Story Lifecycle

```
Trigger → Develop → Peak → Resolution → History
```

宿敌不是一场比赛，而是十年的故事。

---

# 12 种 Story 类型

| Type | 示例 |
|------|------|
| Breakthrough | First ATP Win → Top100 → Top10 → Grand Slam → No.1 |
| Rivalry | Logan vs Carlos 连续交手/比分接近/重要赛事相遇 → 自动升级 |
| Dynasty | 4 Grand Slams + 80 Weeks No.1 → Dynasty |
| Comeback | Major Injury → Ranking 185 → Return → Top10 |
| Collapse | Top5 → Lose 12 Matches → Outside Top80 |
| Injury | 伤病→错过大满贯→复出→首胜→完成 |
| Underdog | No.98 连续击败 No.6→No.4→No.2→Champion |
| Dominance | 25 Wins + 3 Titles + No.1 → Dominant Season |
| Retirement | Final Season→Farewell Tour→Last Match→Hall Of Fame（持续一年）|
| Legacy | 200 Wins→500 Wins→1000 Wins→Hall Of Fame |
| Record | Longest Streak / Fastest Serve / Youngest/Oldest Champion |
| Historic | Career Slam / Golden Slam / Historic Rivalry（最高等级）|

---

# Story Importance

S: Legendary / A: Historic / B: Major / C: Minor / D: Daily

---

# Key Features

- **Player Story Timeline**：2027 ATP Debut→2028 Top100→2030 First Slam→2035 No.1
- **World Story Timeline**：Djokovic Retired→Logan Era Begins→Youngest No.1→Historic Rivalry
- **Story Memory**：Won Wimbledon → 5 Years Later → Defending Champion Story
- **Story Chain**：Top100→Top10→No.1→Grand Slam→Dynasty（形成 Career Arc）
- **Story Expiration**：Winning Streak→Lost→Story Closed（传奇故事永远保留）
- **Story Hooks**：输出到 News / Timeline / Commentary / Replay / Achievements / Legacy

---

# Config Files

story.json / story_trigger.json / story_weight.json / legacy.json / records.json

---

# Performance

- Story Detection <10ms
- Weekly Story Update <30ms
- 100 Years Stable

---

# Definition of Done

✓ 自动生成长期故事 ✓ 支持 Career Arc ✓ 支持世界故事 ✓ Story 不依赖 AI ✓ Config 驱动 ✓ 百年稳定 ✓ 所有新闻都有 Story 来源

---

# Final Principle

玩家不会记住每一场比赛，但一定会记住属于自己的故事。

Story Engine 不是记录职业生涯，而是赋予职业生涯意义。

---

End of Document

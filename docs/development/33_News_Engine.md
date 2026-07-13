# Ace Career Development Bible
# 33 · News Engine

Version: 1.0
Status: Final
Priority: P0

---

# Overview

News Engine 定义整个 Ace Career 的新闻系统。

News 不是随机生成的文字，也不是简单复述比赛结果。News 是整个世界的信息传播系统，它决定玩家如何感知这个世界。新闻不是流水账——新闻必须具有价值、优先级、时效性。

---

# Design Goals

✓ 世界级新闻流 ✓ 自动生成 ✓ Story 驱动 ✓ AI 可扩展 ✓ Config Driven ✓ 长期连续 ✓ 百年稳定

---

# News Pipeline

```
World Events → Story Engine → Narrative Engine → News Engine → Importance Ranking → News Feed → Player Timeline
```

News 永远来自 Story，不是直接来自比赛。

---

# 12 种 News Categories

Tournament / Ranking / Career / Records / Transfer / Injury / Retirement / Rivalry / Milestone / Historic / Junior / World

---

# News Score

```
Story Weight × Tournament Level × Player Fame × Historical Value = News Score
```

---

# News Levels

| Level | 首页 | 推送 | 示例 |
|-------|------|------|------|
| Breaking | 置顶 | ✓ | No.1 Injured / Retirement / Historic Champion |
| Major | 卡片 | 可选 | Grand Slam Champion / Top10 Debut |
| Featured | 卡片 | — | Historic Upset / Record |
| Normal | Feed | — | ATP250 Champion / Top200 Entry |
| Minor | Feed | — | Qualifier Won / Junior Champion |

---

# Key Features

- **Personalization**：玩家看到的新闻优先 Player→Rivals→Tournament→World
- **News Lifetime**：Breaking 7天 / Major 30天 / Historic 永久 / Minor 3天
- **Duplicate Prevention**：相同 Story 禁止连续报道，只保留最高质量
- **Follow-up News**：Injury→Surgery→Recovery→Return→Champion，形成新闻专题
- **AI Writing Hook**：News Engine 输出 Headline/Summary/Story Tags/Context/Importance → AI 负责润色
- **Archive**：所有新闻永久进入 Season/Career/World Archive
- **Localization**：支持 Chinese/English/Japanese/Spanish

---

# Config Files

news.json / importance.json / headline_rules.json / news_weight.json

---

# Performance

- News Generation <20ms
- Weekly Feed <40ms
- Search Realtime

---

# Definition of Done

✓ 新闻全部来源于 Story ✓ 自动计算重要性 ✓ 个性化 Feed ✓ 长期专题 ✓ Config 驱动 ✓ AI 负责润色而非决定内容 ✓ 百年稳定

---

# Final Principle

新闻的意义不是告诉玩家发生了什么，而是告诉玩家：这个世界今天真正值得关注的是什么。

News Engine 就是整个职业网球世界的声音。

---

End of Document

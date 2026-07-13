# Ace Career AI Prompt Bible
# 13 · Social Media Prompt Specification

Version: 1.0
Status: Final
Priority: P1

---

# Overview

Social Media Prompt Specification 定义整个 Ace Career 社交媒体 AI Prompt。

News 是官方媒体。Commentary 是赛事直播。Social Media 代表整个世界的声音——球迷、记者、退役球员、赛事官方、赞助商，整个职业网球社区。它让玩家真正感受到世界正在关注自己。

---

# Design Goals

✓ Facts First ✓ Community Driven ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 内容简洁 ✓ 多样化表达

---

# Prompt Inputs / Outputs

**Inputs**：Match / Tournament / Statistics / Story Tags / Ranking / Records / History / Achievements / Player Popularity / Recent Events

**Outputs**：Post Type / Author Type / Post Content / Sentiment / Priority（所有内容都是独立帖子）

---

# Seven Author Types

Fans / Journalists / Tournament / ATP / Sponsors / Former Players / Analysts

---

# Post Categories + 示例

| Category | 示例 |
|----------|------|
| Match Reaction | "Another impressive performance from Logan today." |
| Tournament Updates | "The semifinal lineup is now complete."（偏官方）|
| Story Posts | "Nine straight wins. The streak continues."（引用 Story）|
| Record Posts | "Career win No.500. Another milestone reached."（克制）|
| Fan Reactions | "Can't wait for the final. That tie-break was unreal."（允许轻微情绪，禁止攻击）|
| Analyst Posts | "Serve efficiency continues to improve this season."（引用 Statistics）|
| Former Player Posts | "That level of consistency is difficult to maintain over an entire season."（专业评价）|

---

# Key Rules

- **Sentiment Levels**：Positive/Neutral/Concern/Historic（不无限放大情绪）
- **Popularity Impact**：Popularity 95→20 Posts / 40→5 Posts（世界自然关注明星）
- **Trending Topics**：#WorldNo1 / #Wimbledon / #Comeback / #Masters1000 / #CareerHigh（全部来自 Story）
- **Style**：Short/Natural/Professional/Modern（ATP 官方/BBC Sport/The Athletic 风格）
- **Forbidden**：政治/辱骂/攻击/网络暴力/博彩/阴谋论/私人生活/虚假采访
- **Vocabulary**：✅ Impressive/Consistent/Solid/Historic/Remarkable/Confident ❌ GOAT!!/OMG!!/Destroyed!!/Crazy!!
- **Length**：40~120 characters（极少数长帖 200 characters）

---

# Config Files

social_prompt.json / author_types.json / sentiment.json / hashtags.json

---

# Definition of Done

✓ 社区视角 ✓ Facts First ✓ Story 自动融合 ✓ Author 多样化 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正鲜活的职业世界不仅有比赛，还有讨论比赛的人。

Social Media Prompt 负责让整个职业网球世界拥有属于自己的声音。

---

End of Document

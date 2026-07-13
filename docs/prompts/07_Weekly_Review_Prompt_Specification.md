# Ace Career AI Prompt Bible
# 07 · Weekly Review Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Weekly Review Prompt Specification 定义整个 Ace Career 每周总结 AI Prompt。

Weekly Review 不是流水账，不是把七天新闻拼起来。而是回答："过去七天，职业网球世界最值得记住的事情是什么。" 它帮助玩家重新建立整个世界的上下文。

---

# Design Goals

✓ Facts First ✓ Story Driven ✓ 世界视角 ✓ AI/玩家一致 ✓ Never Hallucinate ✓ Config Driven ✓ 2 分钟读完

---

# Prompt Inputs / Outputs

**Inputs**：Weekly Matches / Tournament Results / Ranking Changes / Story Tags / Achievements / Records / News / Calendar / Player Progress / World Events

**Outputs**：Week Summary / Your Week / World Highlights / Ranking Watch / Story Watch / Looking Ahead

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Week Summary | 一句话总结整个世界（30~50 words）✅ "The clay season continued with several major upsets and a new Masters champion." |
| Your Week | 聚焦玩家（Matches/Wins/Losses/Training/Ranking/Achievements）保持客观 |
| World Highlights | 3~5 件世界事件（New Champion/Historic Upset/Major Injury/Retirement/Record）依据 World Importance |
| Ranking Watch | Top10 Changes/No.1 Race/Race To Finals/Top100 Debuts（无变化则省略）|
| Story Watch | 本周 Story 引用（Winning Streak/Comeback/Historic Rivalry/Teen Champion）无则不生成 |
| Looking Ahead | 下一周重点（Next Tournament/Potential Rival/Ranking Opportunity）不预测只提醒 |

---

# Additional Watches

- **Achievement Watch**：Player/AI Achievement + Historic Milestone（500 Wins/1000 Aces/First Masters）
- **Injury Watch**：重大伤病自动生成（保持职业报道风格）

---

# Dynamic Focus

如果玩家本周没有比赛 → 自动增加 Training/Recovery/World News（不是空白）

---

# Style Rules

- **Tone**：Professional / Concise / Weekly Magazine（ATP Weekly/The Athletic Weekly/Apple News Weekly 风格）
- **Vocabulary**：✅ Progress/Momentum/Rise/Challenge/Opportunity ❌ 疯狂/爆炸/史诗/神迹
- **Length**：300~500 words（Grand Slam Week 600 words）

---

# Config Files

weekly_review.json / review_structure.json / weekly_style.json / weekly_priority.json

---

# Definition of Done

✓ 世界视角 ✓ 玩家视角 ✓ Story 自动融合 ✓ Ranking 自动总结 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正优秀的周报不是告诉玩家这一周打了几场比赛，而是让玩家知道：过去七天，整个职业网球世界发生了哪些值得铭记的变化。

---

End of Document

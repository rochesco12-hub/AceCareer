# Ace Career AI Prompt Bible
# 08 · Today Summary Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Today Summary Prompt Specification 定义整个 Ace Career Today 页面每日摘要 AI Prompt。

It's not "what happened today" but "if you could only tell the player one thing today, what would it be." Today Summary is the first AI content players see every day — it should answer: what happened, what matters most, and what should I do.

---

# Design Goals

✓ Today First ✓ Action Driven ✓ Facts First ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 30 秒读完

---

# Prompt Inputs / Outputs

**Inputs**：Current Date / Calendar / Today's Match / Tournament / Training Plan / Recovery Status / Fatigue / Ranking / Story Tags / Notifications / Upcoming Events / Recent Results

**Outputs**：Today's Focus / Current Situation / Recommendation / Watch List

---

# 四段式结构

| 段 | 内容 |
|----|------|
| Today's Focus | 一句话（15~25 words）today's most important thing ✅ "Today marks your Wimbledon quarterfinal." |
| Current Situation | 当前状态（Fatigue/Recovery/Ranking/Form/Confidence）解释意义而非重复数据 |
| Recommendation | 系统建议（Prioritize Recovery/Train Serve/Prepare For Clay）来自 Decision Engine |
| Watch List | 今天需关注（Top10 Debut/Next Opponent/Coach Contract）最多两条 |

---

# Daily Priority（每天只允许一个 Primary Focus）

Match Day / Recovery Day / Training Day / Travel Day / Rest Day — 不能同时强调五件事

---

# 各模式规则

- **Match Day**：聚焦 Opponent/Tournament/Preparation，其他内容降优先级
- **Recovery Day**：聚焦 Fatigue/Recovery/Injury Risk，非新闻
- **Travel Day**：聚焦 Destination/Jet Lag/Preparation
- **Training Day**：聚焦 Training Focus/Growth/Weakness/Coach Advice
- **Off Season**：聚焦 Recovery/Planning/Training/Career Goals

---

# Style Rules

- **Tone**：Supportive/Professional/Calm/Focused（像职业教练，不是新闻主播）
- **Story**：Winning Streak/Comeback/Historic Rivalry/Career High（存在时自然融合）
- **Vocabulary**：✅ Focus/Prepare/Maintain/Continue/Monitor/Recover ❌ Urgent/Critical/Disaster/Amazing/Incredible
- **Forbidden**：必须/一定/你应该/不要失败/冠军属于你 — Today 不命令玩家，只提供建议
- **Length**：80~150 words（任何情况不超过 180 words）

---

# Config Files

today_summary.json / daily_focus.json / recommendation_rules.json / today_style.json

---

# Definition of Done

✓ Today First ✓ 单一核心重点 ✓ 建议来自 Decision Engine ✓ Story 自动融合 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

优秀的 Today Summary 不是告诉玩家今天有很多事情，而是告诉玩家：今天真正值得关注的，只有这一件。

---

End of Document

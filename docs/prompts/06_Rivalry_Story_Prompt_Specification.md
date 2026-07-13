# Ace Career AI Prompt Bible
# 06 · Rivalry Story Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Rivalry Story Prompt Specification 定义整个 Ace Career 宿敌故事 AI Prompt。

Rivalry 并不是 H2H 数据。真正伟大的 Rivalry 是一段持续数年的职业叙事（Federer vs Nadal / Djokovic vs Nadal / Agassi vs Sampras）。这些故事远远超过了比分。

---

# Design Goals

✓ Facts First ✓ Story Driven ✓ Never Hallucinate ✓ 自动生成 ✓ AI/玩家一致 ✓ Config Driven ✓ 长期演化

---

# Prompt Inputs / Outputs

**Inputs**：Player A/B / H2H / Timeline / Classic Matches / Story Tags / Statistics / Ranking / Titles / History

**Outputs**：Headline / Overview / History / Turning Points / Current Chapter / Legacy

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Headline | 8~16 words / 强调宿敌关系 ✅ A Rivalry That Defined A Generation |
| Overview | First Meeting/Years Active/H2H/Major Finals（快速建立背景）|
| History | Timeline 回顾：First Meeting→First Final→Grand Slam Battle→No.1 Race→Recent Match |
| Turning Points | 关键节点（First Slam Win/Historic Comeback/Five-set Epic/Record-breaking Final）来自 Timeline |
| Current Chapter | Winning Streak/Ranking Race/Recent Form（不预测未来）|
| Legacy | 历史意义：Defined The Clay Era/Produced Six Grand Slam Finals/Inspired A Generation |

---

# Style Rules

- **Playing Style Contrast**：Big Server vs Elite Returner / Aggressive Baseliner vs Counter Puncher（依据 Statistics）
- **H2H Context**：不简单展示数字，解释意义。✅ "Logan leads overall, but Carlos has dominated their Grand Slam meetings."
- **Story Integration**：Revenge/Passing The Torch/Comeback/Golden Era（存在时自然融合）
- **Vocabulary**：✅ Rivalry/Contest/Battle/Chapter/Duel/Encounter ❌ Hatred/Enemy/Destroy/Crush/War（保持体育精神）
- **Dynamic Evolution**：First Match→20 Matches→40 Matches→Retirement→Historic Rivalry（AI 自动更新）
- **Rivalry Completion**：双方退役后生成最终版本 → 永久保存 → History
- **Forbidden**：心理活动/赛前对话/更衣室/私人关系/采访/未来预测

---

# Config Files

rivalry_prompt.json / rivalry_story.json / chapters.json / legacy_rules.json

---

# Definition of Done

✓ Facts First ✓ Story 自动生成 ✓ Timeline 自动引用 ✓ Legacy 自动评价 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

伟大的宿敌从来不是因为他们打了很多场比赛，而是因为他们共同定义了一个时代。

Rivalry Prompt 负责把这段持续多年的竞争讲述成职业网球历史上最精彩的故事。

---

End of Document

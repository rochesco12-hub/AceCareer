# Ace Career AI Prompt Bible
# 09 · Hall of Fame Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Hall of Fame Prompt Specification 定义整个 Ace Career 名人堂 AI Prompt。

这是整个 AI Bible 中最庄重的一篇 Prompt。因为它只会生成一次，并且会永久保存在 Hall of Fame、History Archive、Career Documentary、Player Biography、Legacy。它不是新闻，也不是传记，而是一份历史评价。

---

# Design Goals

✓ Facts First ✓ Legacy First ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 永久保存 ✓ 仪式感

---

# Prompt Inputs / Outputs

**Inputs**：Career / Timeline / Statistics / Legacy / Hall Qualification / Achievements / Records / Story / History / Biography

**Outputs**：Opening / Career Journey / Career Achievements / Legacy / Historical Evaluation / Closing

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Opening | 一句话定义职业生涯 ✅ "Logan Du leaves the sport as one of the defining players of his generation." ❌ 不得直接称 GOAT（除非 Legacy Engine 已确认）|
| Career Journey | 成长历程：Debut→Top100→First Masters→Grand Slam→No.1→Retirement（依据 Timeline）|
| Career Achievements | 最具代表性的成就（Grand Slams/Masters/Titles/Weeks No.1/Wins/Prize Money）不需全部列举 |
| Legacy | 为什么伟大：Consistency/Dominance/Longevity/Sportsmanship/Influence（引用 Legacy Engine）|
| Historical Evaluation | 历史背景：One of the greatest hard-court players of his era/Defined an entire generation（依据 Era/History/Records）|
| Closing | 职业意义总结。克制/庄重。✅ "His achievements will remain part of the sport's history for generations to come." |

---

# Style Rules

- **Style**：Historical/Elegant/Objective/Respectful（Hall of Fame Citation / Olympic Hall / ATP Legends）
- **Tone**：允许庄严，禁止煽情。✅ "His legacy continues to influence future generations." ❌ "The world cried as he walked away."
- **Story Integration**：Great Comeback/Historic Rivalry/Golden Era/Career Slam（存在时自动引用）
- **Statistics**：22 Grand Slams / 301 Weeks No.1 / 98 Titles（必须来自 Statistics Engine）
- **Legacy**：必须引用 Legacy Score/GOAT Ranking/Career Grade/Hall Tier（不自己评价）
- **Vocabulary**：✅ Recognized/Established/Remembered/Defined/Inspired/Respected ❌ Greatest Ever/Perfect/Invincible/God/Immortal（除非系统确认）
- **Forbidden**：采访/家人/童年/梦想/心理活动/未来幻想
- **Length**：600~900 words（不超过 1200 words）
- **退役后内容永久锁定**

---

# Config Files

hall_prompt.json / legacy_prompt.json / hall_style.json / hall_structure.json

---

# Definition of Done

✓ Legacy First ✓ Timeline 自动生成 ✓ Statistics 自动引用 ✓ Never Hallucinate ✓ Hall 永久保存 ✓ Config Driven

---

# Final Principle

冠军属于那个赛季。纪录属于那个时代。而 Hall of Fame 属于整个历史。

这篇文字不是写给今天的玩家，而是写给几十年后的职业网球世界。

---

End of Document

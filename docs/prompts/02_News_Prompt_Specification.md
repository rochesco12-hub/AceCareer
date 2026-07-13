# Ace Career AI Prompt Bible
# 02 · News Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

News Prompt Specification 定义整个 Ace Career 新闻系统的 AI Prompt。

News 是整个职业世界的信息入口。它不仅告诉玩家发生了什么，更告诉整个世界为什么这件事值得关注。

---

# Design Goals

✓ Facts First ✓ Story Driven ✓ Never Hallucinate ✓ AI/玩家一致 ✓ 多语言 ✓ 可配置 ✓ 长期维护

---

# Prompt Inputs / Outputs

**Inputs**：Match / Tournament / Player / Statistics / Timeline / Story Tags / Records / Ranking / Career / History

**Outputs**：Headline / Subheadline / Body / Context / Related Story Tags

---

# 五段式 Body 结构

| 段 | 内容 |
|----|------|
| Lead | Who + What + Where（不要背景和情绪描写）|
| Match Summary | Score/Duration/Key Stats/Opponent（全部来自 Statistics）|
| Turning Point | Saved Break Points/Won Tie-break/Dominated Third Set（引用 Story Engine）|
| Impact | Ranking/Titles/Records/Legacy/Story（不能自己推测）|
| What's Next | Next Tournament/Ranking Goal/Upcoming Rival（保持职业报道）|

---

# Headline Rules

8~18 words / 一句话 / 直接说明事件 / 不夸张

✅ Logan Wins First Grand Slam Title / Carlos Returns To World No.1

❌ 震惊！史诗！神了！封神！

---

# Style Rules

- **Tone**：Professional / Objective / Elegant / Concise（ATP Tour/The Athletic/BBC Sport 风格）
- **Vocabulary**：✅ Claimed/Defeated/Advanced/Captured/Secured ❌ Destroyed/Humiliated/Crazy/Legendary
- **Statistics**：精确引用（18 Aces / 78% 1st Serve / 6/8 Break Points），不能估算
- **Story Rules**：存在 Story Tags 时自然引用，没有时不得创造
- **Ranking**：必须写 Current Ranking/Career High/Change，不能预测未来
- **Records**：只有 Records Engine 确认后才能写
- **Forbidden**：幻想采访/心理/未来/观众/更衣室/社交媒体（全部禁止）
- **Multi-language**：相同结构，翻译新闻而非翻译 Prompt
- **Regeneration**：允许不同措辞但事实必须完全一致

---

# Config Files

news_prompt.json / headline_rules.json / news_style.json / news_length.json

---

# Definition of Done

✓ Facts First ✓ Story Driven ✓ Never Hallucinate ✓ Professional Tone ✓ 五段式结构 ✓ Config Driven

---

# Final Principle

新闻的职责不是制造传奇，而是记录传奇发生的那一天。

---

End of Document

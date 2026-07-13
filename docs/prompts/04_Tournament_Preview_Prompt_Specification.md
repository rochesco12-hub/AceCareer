# Ace Career AI Prompt Bible
# 04 · Tournament Preview Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Tournament Preview Prompt Specification 定义整个 Ace Career 赛事前瞻 AI Prompt。

前瞻不是预测，不是竞猜。而是帮助读者理解：这项赛事开始之前，整个职业世界正在发生什么。

---

# Design Goals

✓ Facts First ✓ Story Driven ✓ 不预测结果 ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 可读性优先

---

# Prompt Inputs / Outputs

**Inputs**：Tournament / Surface / Category / Location / Draw / Seeds / Rankings / Story Tags / History / Records / Recent Form / Calendar（禁止未来数据和冠军预测）

**Outputs**：Headline / Overview / Players To Watch / Storylines / Records To Watch / Tournament Outlook

---

# 六段式结构

| 段 | 内容 |
|----|------|
| Headline | 8~16 words / 描述赛事 / 不制造悬念 ✅ The Clay Season Continues In Rome |
| Overview | Tournament/Category/Surface/Location/Historical Importance |
| Players To Watch | 3~5 位球员（依据 Ranking/Recent Form/Story/Popularity/Home Advantage，非世界前五固定）|
| Storylines | Champion Returns/Winning Streak/Historic Rivalry/Teenage Breakthrough/Home Favorite/Comeback（全部来自 Story Engine）|
| Records To Watch | Career Slam/100th Win/Top10 Debut/No.1 Race（不存在则不生成）|
| Outlook | 总结值得期待的原因 / 不预测冠军 |

---

# Style Rules

- **Favorite**：✅ Leading Contender/Top Seed/In-form Player/Defending Champion ❌ Guaranteed Champion/Will Win/Cannot Lose
- **Recent Form**：引用 Winning Streak/Recent Titles/Season Record/Last Five Matches（不凭感觉）
- **Tournament History**：Most Titles/Defending Champion/Historic Finals（必须来自 History Engine）
- **Surface Analysis**：依据 Surface Statistics 描述 Clay Specialists/Grass Experts/Indoor Players
- **Ranking Context**：说明 No.1 Race/Top8 Race/Top100 Entry/Seed Changes（不预测未来排名）
- **Vocabulary**：✅ Arrives/Returns/Leads/Highlights/Features/Awaits ❌ Epic/Legendary/Insane/Unbelievable
- **Forbidden**：冠军预测/比分预测/心理分析/虚构采访/博彩/赔率
- **Length**：250~450 words（Grand Slam 600 words）

---

# Config Files

tournament_preview.json / preview_structure.json / story_priority.json / preview_style.json

---

# Definition of Done

✓ Facts First ✓ Story Driven ✓ 不预测结果 ✓ 自动识别 Story ✓ 专业媒体风格 ✓ Config Driven

---

# Final Principle

真正优秀的赛事前瞻不是告诉读者谁会夺冠，而是告诉读者：为什么这一周整个职业网球世界都会把目光投向这里。

---

End of Document

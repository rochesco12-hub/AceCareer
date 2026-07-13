# Ace Career AI Prompt Bible
# 14 · Interview Prompt Specification

Version: 1.0
Status: Final
Priority: P1

---

# Overview

Interview Prompt Specification 定义整个 Ace Career 赛后采访 AI Prompt。

职业球员在公开采访中几乎不会说"我今天太神了"，更多时候会感谢团队、称赞对手、分析比赛、展望下一场。Ace Career 必须保持这种职业感。

---

# Design Goals

✓ Facts First ✓ Personality Driven ✓ Never Hallucinate ✓ AI/玩家一致 ✓ Config Driven ✓ 尊重职业体育文化 ✓ 长期一致性

---

# Prompt Inputs / Outputs

**Inputs**：Match / Tournament / Round / Opponent / Statistics / Story Tags / Player Personality / Current Form / Ranking / Achievements

**Outputs**：Opening Quote / Match Reflection / Opponent Comment / Looking Ahead / Closing Quote

---

# 五段式结构

| 段 | 内容 |
|----|------|
| Opening Quote | 回应比赛结果 ✅ "I'm really happy with today's performance." |
| Match Reflection | 评价比赛（依据 Statistics：Serve/Return/Momentum/Pressure Moments）|
| Opponent Comment | 评价对手 ✅ "He played a very high level today." 永远保持尊重 |
| Looking Ahead | 谈下一场 ✅ "I'll recover well and prepare for the next match." 不预测冠军 |
| Closing Quote | 感谢支持 ✅ "Thank you to everyone who supported me today." |

---

# Personality Integration（来自 Personality Engine）

| Personality | Style |
|-------------|-------|
| Professional | Short / Calm / Respectful |
| Showman | Energetic / Confident / Positive |
| Reserved | Minimal / Focused / Quiet |

所有 Personality 都不能改变事实。

---

# Context Rules

- Grand Slam Final ≠ ATP250 R1（语气不同）
- **Story Integration**：Comeback/Winning Streak/Historic Rivalry（允许引用但不直接复述）
- **Emotional Levels**：Win→Positive / Loss→Respectful / Historic→Reflective / Retirement→Emotional
- **Defeat**：✅ "He played better today. I'll learn from this match." ❌ "I was terrible. I don't deserve to win."
- **Victory**：✅ "I'm happy with the result. There's still work to do." ❌ "Nobody can beat me."

---

# Style Rules

- **Forbidden**：攻击对手/政治观点/博彩/私人生活/更衣室内幕/虚假采访/不存在人物
- **Vocabulary**：✅ Proud/Happy/Respect/Prepare/Compete/Recover ❌ Destroy/Humiliate/Hate/Impossible/Perfect
- **Length**：150~350 words（Grand Slam Final 500 words）

---

# Config Files

interview_prompt.json / personality_quotes.json / interview_style.json / emotion_rules.json

---

# Definition of Done

✓ Personality 驱动 ✓ Facts First ✓ Story 自动融合 ✓ 尊重职业体育文化 ✓ Never Hallucinate ✓ Config Driven

---

# Final Principle

真正优秀的赛后采访不会因为赢球而狂妄，也不会因为输球而失态。

它代表的不是一个人的情绪，而是一位职业运动员的风度。

---

End of Document

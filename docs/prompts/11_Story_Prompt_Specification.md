# Ace Career AI Prompt Bible
# 11 · Story Prompt Specification

Version: 1.0
Status: Final
Priority: P0

---

# Overview

Story Prompt Specification 定义整个 Ace Career 故事生成 AI Prompt。

Story 并不是新闻，也不是 Biography。Story 是整个 Career 世界的叙事引擎。News/Today/Replay/Documentary 都会引用 Story。Story 是所有 AI 内容的源头。

---

# Design Goals

✓ Story First ✓ Facts First ✓ Never Hallucinate ✓ 自动演化 ✓ AI/玩家一致 ✓ Config Driven ✓ 长期连续性

---

# Prompt Inputs / Outputs

**Inputs**：Story Tags / Timeline / Statistics / Ranking / History / Records / Career / Achievements / Recent Matches / World State

**Outputs**：Story Title / Type / Current Chapter / Summary / Next Possible Chapter / Priority

Story 本身不是文章，而是 Narrative Object。

---

# 16 种 Story Types

Comeback / Winning Streak / Losing Streak / Underdog / Breakthrough / Dominance / Dynasty / Passing The Torch / Historic Rivalry / Final Chance / Career Revival / Teen Sensation / Late Bloomer / Golden Generation / Record Chase / GOAT Debate（全部配置化）

---

# Story Lifecycle

```
Trigger → Developing → Peak → Resolution → Archive
```

Story 不会永远存在。

---

# Key Rules

- **Trigger**：必须由事件触发（Win 5 Matches→Winning Streak / Lose 6→Crisis / 3 Finals→Breakthrough / No.1→New King）禁止随机生成
- **Current Chapter**：说明目前发展到哪一步（Chapter 2: Winning Streak Continues）不是重新讲完整故事
- **Priority**：Critical/High/Medium/Low → Today 只展示最高优先级
- **Conflict Required**：Champion→Injury / Comeback→Final（没有冲突 Story 很快结束）
- **Resolution**：Completed/Failed/Interrupted → 进入 History
- **Multi-story Limit**：最多 1 Primary + 2 Secondary（避免信息过载）
- **World Stories**：Golden Generation / Clay Era / Rise Of Asia / Dominant Champion（整个世界也拥有 Story）
- **Narrative Continuity**：❌ Comeback→Champion→Comeback→Champion ✅ Comeback→Recovery→Final→Champion
- **Forbidden**：幻想人物关系/梦想/采访/家庭/媒体评论

---

# Length

- Story Summary：20~40 words
- Narrative：80~150 words（不是长文章）

---

# Config Files

story_prompt.json / story_types.json / story_priority.json / story_lifecycle.json

---

# Definition of Done

✓ Story 自动生成 ✓ 生命周期完整 ✓ Timeline 深度融合 ✓ Never Hallucinate ✓ Story 可持续发展 ✓ Config Driven

---

# Final Principle

冠军只是一个结果。故事才是玩家真正记住职业生涯的原因。

Story Prompt 负责把一连串真实发生的事件编织成一个值得铭记几十年的传奇。

---

End of Document

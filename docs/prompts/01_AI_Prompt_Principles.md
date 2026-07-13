# Ace Career AI Prompt Bible
# 01 · AI Prompt Principles

Version: 1.0
Status: Final
Priority: P0

---

# Overview

AI Prompt Bible 定义整个 Ace Career 所有 AI 输出的统一规范。

Prompt 不是一段文本，而是整个世界的语言规则。未来所有 AI 输出（News/Story/Commentary/Today/Weekly Review/Hall of Fame/Biography/Documentary/Interview/Rivalry）全部遵守这一套规范。

---

# Design Goals

✓ 世界观统一 ✓ 风格统一 ✓ 不幻想 ✓ 不重复 ✓ 长期可维护 ✓ Config Driven ✓ 多语言兼容

---

# Golden Rule

```
Facts First. Narrative Second.
```

先事实。后叙事。

---

# Source Priority

```
Statistics → Timeline → Story Tags → Records → Career → History
```

禁止凭空补充。

---

# Never Hallucinate

禁止：猜测/幻想/补充不存在的人物/比赛/采访/数据

所有事实必须来自 Engine。

---

# Narrative Rule

AI 可以解释，不能编造。

✅ "这是他连续第三次进入四强。"（事实）

❌ "他一直梦想这一刻。"（如果没有记录）

---

# Tone

Professional / Objective / Elegant / Calm / Confident

像 ATP 官网 / Apple Newsroom / The Athletic，不是微博热搜。

---

# 风格规则

- **Emotional Level**：允许情绪，禁止煽情。✅ "他完成了一次令人印象深刻的逆转。" ❌ "他创造了人类历史最伟大的奇迹！"
- **Length**：Today 80w / News 250w / Biography 500w / Hall 600w / Documentary 1000w
- **Readable > Accurate > Beautiful**（可读性永远第一）
- **World Consistency**：禁止出现"游戏/玩家/系统/模拟/NPC/AI"等词汇
- **Career Perspective**：✅ "本赛季已经取得 42 场胜利。" ❌ "玩家已经完成任务。"
- **Player Respect**：即使世界第 900 也保持职业表达
- **AI Neutrality**：不偏向玩家，AI 球员同样待遇

---

# 智能规则

- **Timeline Awareness**：如果 Timeline 已有冠军，不能说"首次夺冠"
- **Statistics Awareness**：引用数据必须来自 Statistics，不能自己计算
- **Story Awareness**：Comeback→文章重点复出；Winning Streak→重点状态火热
- **Avoid Repetition**：禁止连续使用"传奇/伟大/历史/震撼/经典"
- **Dynamic Vocabulary**：Won/Defeated/Beat/Overcame/Claimed（自然度）
- **Forbidden Words**："史上最/无敌/神/爆炸/封神/炸裂/碾压/毁灭/逆天"（除非世界历史真的如此）

---

# Config Files

prompt_rules.json / style.json / forbidden_words.json / tone.json

---

# Definition of Done

✓ Facts First ✓ Never Hallucinate ✓ World Consistency ✓ Professional Tone ✓ Story Driven ✓ Config Driven

---

# Final Principle

AI 不负责创造传奇。传奇已经发生。

AI 的职责只是用最准确、最克制、最有温度的方式把它讲述出来。

---

End of Document

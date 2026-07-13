# Ace Career Development Bible
# 34 · AI News Writing Bible

Version: 1.0
Status: Final
Priority: P0

---

# Overview

AI News Writing Bible 定义整个 Ace Career 中 AI 新闻生成的写作规范。

News Engine 决定写什么。AI Writer 决定怎么写。AI 是 ATP Tour / ESPN / BBC Sport / The Athletic 风格的综合体：报道事实、突出重点、保留情绪、绝不夸张。

---

# Design Goals

✓ 媒体化 ✓ 客观 ✓ 简洁 ✓ 富有故事性 ✓ 长期一致 ✓ 多语言统一 ✓ 不胡编乱造

---

# Writing Principles

```
Fact First → Context Second → Emotion Last
```

---

# Hallucination Rule（绝对禁止）

禁止 Invent Match / Score / Injury / Quote / Record。所有内容必须来自 Engine。

---

# 五段式结构

```
Headline → Summary → Body → Background → What's Next
```

---

# 各段规则

| 段 | 规则 |
|----|------|
| **Headline** | 12~20 字（中文）/ 40~70 chars（英文），唯一重点。✅ Logan 首夺温网冠军 ❌ 过于冗长 |
| **Summary** | 一句话：Who + What + Why Important |
| **Body** | 倒金字塔：最重要→支撑事实→统计→历史背景 |
| **Tone** | Professional / Objective / Confident / Calm。禁止 OMG/Amazing/Crazy/Unbelievable |
| **Emotion** | 来自事实不是形容词。不说"惊天逆转"，说"在先丢两盘后连赢三盘完成逆转" |
| **Numbers** | 永远具体。"12 连胜"不是"连续很多场" |
| **Statistics** | 只引用真正重要的数据（25 Aces/1st Serve%/Winner 数），不写"第17个制胜分"|

---

# Context Rules

- **为什么重要**："职业生涯首座大师赛冠军"不只"赢得冠军"
- **Historical Context**："近十年来最年轻的温网冠军"（来自 History）
- **Story Continuity**："在连续三次止步四强后终于完成突破"（来自 Narrative）
- **Player Identity**：World No.1/Young Star/Veteran/Former Champion
- **Tournament Language**：Grand Slam 更庄重 / ATP250 更简洁 / Olympics 更具国家荣誉感
- **Rivalry Language**：自动加入 H2H/Recent Meetings/Winning Streak

---

# Length Rules

| Type | Words |
|------|-------|
| Breaking | 40~80 |
| Featured | 120~250 |
| Major Story | 250~500 |
| Historic | 500~800 |

---

# 禁忌

禁止：小说化 / 过度夸张 / 主观评价 / AI 猜测 / 重复词汇 / 网络热梗 / Emoji

---

# 正确 vs 错误

✅ "Logan 在决赛击败 Carlos，首次赢得法网冠军，并首次进入世界前三。这场胜利也结束了他此前三次法网四强出局的纪录。"

❌ "太励志了！Logan 终于圆梦法网！这一刻实在令人泪目！"

---

# Prompt Pipeline

AI 输入：Headline / Story Tags / Narrative / Statistics / Context / Historical Facts

AI 输出：Headline / Summary / Article

不允许访问数据库。

---

# Performance

- Headline <100 Tokens
- Summary <50 Tokens
- Article <500 Tokens

---

# Definition of Done

✓ 新闻风格统一 ✓ 不产生幻觉 ✓ Story 连续 ✓ Narrative 一致 ✓ 多语言统一 ✓ AI 不创造事实 ✓ 长期质量稳定

---

# Final Principle

优秀的体育新闻从来不是华丽辞藻，而是在最短的篇幅里准确记录一个值得被历史记住的瞬间。

AI Writer 应该像一位真正的职业体育记者，而不是一个会写作文的 AI。

---

End of Document

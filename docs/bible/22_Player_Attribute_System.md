# Ace Career Game Design Document
## Player Attribute System

Version: 1.0
Status: Draft
Priority: P1

---

# 1. Purpose

Player Attribute System（球员属性系统）定义所有球员能力值。

它是整个 Career 最核心的数据之一。

Training、Match、Ranking、AI、Scouting、Progression 等所有系统都依赖 Attribute。

任何比赛结果都必须由 Attribute 推导，而不是随机决定。

---

# 2. Design Goal

属性系统必须满足：

- 易于理解
- 长期成长
- 不存在万能属性
- 每种打法都有优势
- AI 与玩家完全一致

Attribute 不只是 Overall。

每项能力都有实际作用。

---

# 3. Attribute Categories

所有属性分为六大类：

Technical

Physical

Mental

Serve

Movement

Hidden

每个类别影响不同系统。

---

# 4. Technical Attributes

包括：

Forehand

Backhand

Volley

Slice

Return

Drop Shot

Passing Shot

Lob

每项：

范围：

```text
1 ~ 99
```

不会直接显示 Overall。

---

# 5. Serve Attributes

包括：

First Serve Power

First Serve Accuracy

Second Serve

Kick Serve

Slice Serve

Serve Variety

Ace Rate

Serve Consistency

共同影响：

发球局胜率。

---

# 6. Physical Attributes

包括：

Strength

Speed

Acceleration

Agility

Endurance

Reaction

Flexibility

Balance

影响：

移动。

恢复。

连续比赛。

---

# 7. Mental Attributes

包括：

Confidence

Focus

Composure

Pressure Resistance

Competitive Spirit

Work Ethic

Leadership

影响：

关键分。

抢七。

决胜盘。

---

# 8. Movement Attributes

包括：

Court Coverage

Recovery Speed

Split Step

Footwork

Net Approach

影响：

防守。

跑动。

救球。

---

# 9. Hidden Attributes

默认：

玩家不可见。

包括：

Potential

Consistency

Big Match Player

Injury Proneness

Learning Speed

Professionalism

Temperament

Media Personality

未来：

通过球探逐渐发现。

---

# 10. Overall Rating

Overall：

不是平均值。

而是：

根据打法动态计算。

例如：

Serve Bot：

Serve 权重更高。

Clay Specialist：

Movement 权重更高。

All Court：

技术均衡。

Overall：

只作为参考。

不是胜负依据。

---

# 11. Attribute Growth

成长来源：

训练

+

比赛

+

经验

+

教练

+

年龄

+

潜力

成长：

缓慢。

不会一周：

+5。

---

# 12. Attribute Decay

年龄增长。

部分属性：

下降。

例如：

Acceleration

↓

Speed

↓

Endurance

Mental：

下降较慢。

Experience：

持续增加。

---

# 13. Surface Bonus

不同 Surface：

调用不同属性。

Hard：

Serve

Forehand

Return

Clay：

Endurance

Footwork

Topspin（未来）

Grass：

Serve

Volley

Reaction

系统：

自动切换权重。

---

# 14. Playing Style Mapping

系统根据属性：

自动判断打法。

例如：

Serve > 92

Volley > 85

↓

Serve & Volley

Forehand > 94

Movement > 91

↓

Aggressive Baseliner

Endurance > 95

Defense > 92

↓

Counter Puncher

无需玩家选择。

---

# 15. Match Usage

比赛模拟：

不会：

直接读取：

Overall。

而是：

读取：

所有相关 Attribute。

例如：

发球：

读取：

Serve。

接发：

读取：

Return。

底线：

读取：

Forehand。

Backhand。

因此：

能力更加真实。

---

# 16. Attribute History

所有成长：

永久保存。

例如：

2027

Serve

82

↓

84

↓

86

未来：

Career Graph。

展示成长曲线。

---

# 17. Data Model

```text
PlayerAttribute
PlayerID
Forehand
Backhand
Volley
ServePower
ServeAccuracy
Return
Strength
Speed
Agility
Endurance
Confidence
Focus
Composure
Potential
Overall
```

---

# 18. Edge Cases

支持：

- 长期伤病降低能力
- 老将能力衰退
- 天赋兑现失败
- 快速成长
- 心理崩盘
- 状态低迷

---

# 19. Future Expansion

未来可增加：

Topspin

Slice Quality

Net Instinct

Return Position

Court IQ

Shot Selection

Spin Rate

Serve Placement

所有新增属性：

不得影响旧存档。

---

# 20. Acceptance Criteria

✓ 所有能力拥有实际用途

✓ Overall 不决定比赛

✓ Match 调用真实 Attribute

✓ 长期成长合理

✓ AI 与玩家一致

✓ 支持 30+ Season

---

End of Document

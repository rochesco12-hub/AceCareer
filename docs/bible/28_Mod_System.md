# Ace Career Game Design Document
## World Configuration & Mod System

Version: 1.0
Status: Draft
Priority: P2

---

# 1. Purpose

Mod System（世界配置系统）负责让 Ace Career 的整个世界可以被配置，而不是写死。

所有核心内容：

- ATP Calendar
- Tournament
- Points
- Prize Money
- Countries
- Surfaces
- Coaches
- Equipment
- Sponsors
- AI Personality

未来都应该支持配置。

而不是修改代码。

---

# 2. Design Goal

整个 Career 必须做到：

- 数据驱动（Data Driven）
- 不修改代码即可增加内容
- 支持官方更新
- 支持社区 Mod（Future）
- 保证旧存档兼容

---

# 3. Configuration Philosophy

所有固定数据：

禁止写死。

例如：

错误：

```swift
ATP250 Champion = 250
```

正确：

```text
TournamentConfig
ChampionPoints
250
```

任何数值都来自配置文件。

---

# 4. Config Categories

系统支持：

TournamentConfig

CalendarConfig

SurfaceConfig

CountryConfig

CoachConfig

SponsorConfig

EquipmentConfig

DifficultyConfig

WorldConfig

UIConfig

全部独立维护。

---

# 5. Tournament Config

每项赛事：

拥有：

```text
TournamentID
Category
Name
Country
Surface
PrizeMoney
Points
DrawSize
QualifyingSize
Week
Indoor
Altitude
```

修改配置。

无需重新开发。

---

# 6. Points Config

积分：

全部来自：

PointsConfig。

例如：

```text
ATP250
Champion
250
RunnerUp
165
Semi
100
```

未来：

官方积分变化。

只更新配置。

---

# 7. Calendar Config

Calendar：

完全配置化。

例如：

```text
Week18
Barcelona
ATP500
Clay
Spain
```

未来：

新增赛事。

无需修改代码。

---

# 8. Surface Config

Surface：

拥有独立配置。

例如：

```text
Clay
Bounce
92
Speed
65
MovementPenalty
12
```

未来：

支持：

不同球场。

不同品牌。

---

# 9. Country Config

国家：

保存：

```text
Population
TennisPopularity
TalentRate
HomeTournament
WeatherBias
```

未来：

动态调整。

---

# 10. Coach Config

所有教练：

来自配置。

例如：

```text
Coach
ServeBonus
RecoveryBonus
Salary
Nationality
Level
```

新增教练：

无需更新程序。

---

# 11. Equipment Config

装备：

例如：

球拍。

球鞋。

球线。

护腕。

全部配置。

未来：

支持品牌。

---

# 12. Difficulty Config

不同难度：

通过配置。

例如：

Easy

Recovery

+20%

Hard

AI Learning

+15%

而不是：

写死。

---

# 13. World Config

世界参数：

例如：

```text
Population
2000
RetirementAge
37
RookiePerSeason
80
WeatherEnabled
False
```

未来：

自由调整。

---

# 14. Save Compatibility

所有 Config：

拥有：

Version。

旧 Save：

自动：

Migration。

配置变化：

不会：

导致坏档。

---

# 15. Future Mod Support

未来：

开放：

Mod。

例如：

新增：

Laver Cup。

ATP NextGen。

UTS。

全部：

通过：

Config。

不是：

修改程序。

---

# 16. Data Structure

```text
Config
Version
Category
Key
Value
UpdatedAt
```

所有配置：

统一读取。

---

# 17. Developer Rules

新增系统。

必须：

优先：

Config。

禁止：

Magic Number。

例如：

禁止：

```swift
if points == 250
```

必须：

读取：

Config。

---

# 18. Edge Cases

支持：

- Config 升级
- Config 回滚
- Config 缺失
- Config 校验失败
- Save 使用旧 Config

---

# 19. Acceptance Criteria

✓ 所有固定数据配置化

✓ 官方更新无需改代码

✓ Save 保持兼容

✓ 支持未来 Mod

✓ 支持长期维护

---

End of Document

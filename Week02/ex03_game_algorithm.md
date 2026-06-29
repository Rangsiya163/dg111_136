โจทย์ A — ระบบ Combat

```mermaid
flowchart TD
Start([Start]) --> Input[/รับ player_attack, enemy_defense,
enemy_hp/]
Input --> Calc["damage = max(player_attack - enemy_defense,
1)"]
Calc --> Reduce["enemy_hp = enemy_hp - damage"]
Reduce --> D1{enemy_hp <= 0?}
D1 -->|Yes| Win[/แสดง Victory!/]
D1 -->|No| Show[/แสดง enemy_hp ที่เหลือ/]
Win & Show --> End([End])
```

โจทย์ B — ระบบ Level Up


```mermaid
flowchart TD
Start([Start]) --> Input[/รับ current_xp,xp_needed,level/]
Input --> D1{current_xp >= xp_needed?}
D1 -->|Yes| D11[level = level = 1 ]
D11 --> D12[xp_needed = xp_needed x1.5]
D12 --> D13[current_ xp = 0]
D13 --> Show
D1 -->|No| Show[/แสดง level และ current_xp/]
Show --> End([End])
```


โจทย์ C (ท้าทาย) — Simple AI Patrol


```mermaid
flowchart TD
Start([Start]) --> Input[pos = A,dir = forward]
Input --> D1{ระยะถึง player < 100?}
D1 -->|Yes| D11[/chase player/]
D11 --> End([End])

D1 -->|No| DN1[เลื่อน enemy ตาม dir]
DN1--> DN11{ถึงจุด B?}
DN11 -->|Yes| DN11C[dir = กลับไป A]
DN11C --> D1
DN11 -->|No| DN12C{ถึงจุด A?}
DN12C-->|Yes| DN12C1[dir = กลับไป B]
DN12C1 --> D1
DN12C -->|No| D1
```

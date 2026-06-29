เอา Ex01 มาเขียนใหม่ โดยใช้รูปแบบ

BEGIN [ชื่อ algorithm]
INPUT ...
IF ... THEN
...
ELSE
...
END IF
OUTPUT ...
END

โจทย์ A — ตรวจสอบเกรด

```mermaid
flowchart TD
Start([Start]) --> Input[/รับคะแนน score/]
Input --> D1{score >= 80?}
D1 -->|Yes| A[เกรด = A]
D1 -->|No| D2{score >= 70?}
D2 -->|Yes| B[เกรด = B]
D2 -->|No| D3{score >= 60?}
D3 -->|Yes| C[เกรด = C]
D3 -->|No| D4{score >= 50?}
D4 -->|Yes| D[เกรด = D]
D4 -->|No| F[เกรด = F]
A & B & C & D & F --> Output[/แสดงเกรด/]
Output --> End([End])
```

BEGIN [Grade Calculator Algorithm]
INPUT score >= 80 THEN grade = "A"
ELSE IF score >= 70 THEN grade = "B"
ELSE IF score >= 60 THEN grade = "C"
ELSE IF score >= 50 THEN grade = "D"
ELSE grade = "F"
END IF
OUTPUT grade

โจทย์ B— หาค่าสูงสุดจาก 2 ตัวเลข

```mermaid
flowchart TD
Start([Start]) --> Input[/รับ a และ b/]
Input --> Check{a > b?}
Check -->|Yes| Even[เกรด a]
Check -->|No | Odd[เกรด b]
Even & Odd--> End([End])
```

BEGIN [หาค่าสูงสุดจาก 2 ตัวเลข]
INPUT a , b

IF a > b THEN เกรด a

ELSE เกรด b

END IF

END

โจทย์ C — นับ 1 ถึง N

```mermaid
flowchart TD
Start([Start]) --> Input[/รับ N /]
Input --> Process[i=1]
Process --> D1{i <= N?}
D1 --> |Yes| T1[/พิมพ์ i/]
T1 --> T2[i = i+1]
T2 --> D1
D1 --> |No| End([End])
```

BEGIN [นับ 1 ถึง N]

INPUT N

i = 1

IF  i <= N THEN

    พิมพ์ i

    i = i + 1

ELSE 

END IF

END

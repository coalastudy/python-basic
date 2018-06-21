---
description: 자율과제 2의 모범 답안입니다.
---

# 모범 답안

## 해적통 게임

{% code-tabs %}
{% code-tabs-item title="games/pirate\_game.py" %}
```python
import random

print("해적통 게임 프로그램입니다!")

# 벌칙 번호 생성
oops = random.randint(1, 18)
oops2 = oops
while oops2 == oops:
    oops2 = random.randint(1, 18)

# 상태 초기화
status = ["01", "02", "03", "04", "05", "06", "07", "08", "09", "10", "11", "12", "13", "14", "15", "16", "17", "18"]

your_choice = -1
while your_choice != oops and your_choice != oops2:
    print('''
         ---------
        |+++++++++|
        ___________
        |  O   @  |
        |    o    |
         ---===---
           |   |
    ---------------------
    | {0} | {1} | {2} | {3} |
  --------------------------
  | {4} | {5} | {6} | {7} | {8} |
  --------------------------
  | {9} | {10} | {11} | {12} | {13} |
  --------------------------
    | {14} | {15} | {16} | {17} |
    ---------------------
    '''.format(status[0], status[1], status[2], status[3], status[4],
               status[5], status[6], status[7], status[8], status[9],
               status[10], status[11], status[12], status[13], status[14],
               status[15], status[16], status[17],))
    # 유저 입력 받기
    your_choice = input("칼 꽂을 번호를 입력하세요 : ")
    your_choice = int(your_choice)

    status[your_choice - 1] = "/\\"

print('''
         ---------
        |+++++++++|
        ___________
        |  O   @  |
        |    o    |
         ---===---
           |   |
           ~ /  
           \ ~ /
            \ 
           /   ~\ 
             \ ~
          ~~  ~ 
퐁~~~~ 당신이 걸렸습니다!''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}


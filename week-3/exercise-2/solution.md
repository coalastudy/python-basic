---
description: 자율과제 2의 모범 답안입니다.
---

# 모범 답안

## 가위 바위 보 게임

{% code-tabs %}
{% code-tabs-item title="game/rps\_game.py" %}
```python
import random

while True:

    player = input('''
무엇을 낼 껀가요?!
1. 가위
2. 바위
3. 보
''')

    computer = random.randint(1, 3)
    computer = str(computer)

    if player == "1":
        player = "가위"
    elif player == "2":
        player = "바위"
    elif player == "3":
        player = "보"

    if computer == "1":
        computer = "가위"
    elif computer == "2":
        computer = "바위"
    elif computer == "3":
        computer = "보"

    print("\n플레이어는 {0}를 내셨습니다.".format(player))
    print("컴퓨터는 {0}를 냈습니다.\n".format(computer))

    if computer == player:
        print("둘 다 {0}로 비겼습니다.".format(computer))
    elif computer == "가위":
        if player == "바위":
            print("플레이어가 {0}로 승리하였습니다!".format(player))
            break
        elif player == "보":
            print("컴퓨터가 {0}로 승리하였습니다!".format(computer))
    elif computer == "바위":
        if player == "보":
            print("플레이어가 {0}로 승리하였습니다!".format(player))
            break
        elif player == "가위":
            print("컴퓨터가 {0}로 승리하였습니다!".format(computer))
    elif computer == "보":
        if player == "가위":
            print("플레이어가 {0}로 승리하였습니다!".format(player))
            break
        elif player == "바위":
            print("컴퓨터가 {0}로 승리하였습니다!".format(computer))
    else:
        print("잘못된 입력입니다. 프로그램을 종료합니다.")
        break
```
{% endcode-tabs-item %}
{% endcode-tabs %}


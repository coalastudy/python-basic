---
description: 자율과제 2의 모범 답안입니다.
---

# 모범 답안

## 가위 바위 보 게임 만들기

{% code-tabs %}
{% code-tabs-item title="rps\_game.py" %}
```python
first_player = input('''
첫번째 플레이어 무엇을 낼 껀가요?!
1. 가위
2. 바위
3. 보
''')

second_player = input('''
두번째 플레이어 무엇을 낼 껀가요?!
1. 가위
2. 바위
3. 보
''')

if first_player == "1":
    first_player = "가위"
elif first_player == "2":
    first_player = "바위"
elif first_player == "3":
    first_player = "보"
else:
    first_player = "잘못된 입력"

if second_player == "1":
    second_player = "가위"
elif second_player == "2":
    second_player = "바위"
elif second_player == "3":
    second_player = "보"
else:
    second_player = "잘못된 입력"

print("\n첫번째 플레이어는 {0}를 내셨습니다.".format(first_player))
print("두번째 플레이어는 {0}를 내셨습니다.\n".format(second_player))

if second_player == first_player:
    print("둘 다 {0}로 비겼습니다.".format(second_player))
elif second_player == "가위":
    if first_player == "바위":
        print("첫번째 플레이어가 {0}로 승리하였습니다!".format(first_player))
    elif first_player == "보":
        print("두번째 플레이어가 {0}로 승리하였습니다!".format(second_player))
elif second_player == "바위":
    if first_player == "보":
        print("첫번째 플레이어가 {0}로 승리하였습니다!".format(first_player))
    elif first_player == "가위":
        print("두번째 플레이어가 {0}로 승리하였습니다!".format(second_player))
elif second_player == "보":
    if first_player == "가위":
        print("첫번째 플레이어가 {0}로 승리하였습니다!".format(first_player))
    elif first_player == "바위":
        print("두번째 플레이어가 {0}로 승리하였습니다!".format(second_player))
else:
    print("잘못된 입력입니다. 프로그램을 종료합니다.")
```
{% endcode-tabs-item %}
{% endcode-tabs %}


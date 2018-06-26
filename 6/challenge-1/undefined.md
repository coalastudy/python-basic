---
description: Challenge 1의 모범 답안입니다.
---

# 모범 답안

## 모듈화하기

{% code-tabs %}
{% code-tabs-item title="games/\*" %}
```python
def play_game():
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## main.py

{% code-tabs %}
{% code-tabs-item title="main.py" %}
```python
import calculators.grade_calculator
import calculators.normal_calculator
from calculators import obesity_calculator
from calculators.pay_calculator import calculate_pay
from games.beskin_rabins_game import validate_input
from games import baseball_game
from games import beskin_rabins_game
from games import crocodile_game
from games import rps_game

if __name__ == "__main__":

    while True:

        print('''
실행하고자 하는 번호를 입력해주세요.
0. 종료
1. 학점 계산기
2. 일반 계산기
3. 비만도 계산기
4. 급여 계산기
5. 야구 게임
6. 베스킨라빈스31 게임
7. 악어 게임
8. 가위바위보 게임
        ''')

        choice = validate_input("선택 : ", ['0', '1', '2', '3', '4', '5', '6', '7', '8'])

        if choice == 1:
            calculators.grade_calculator.calculate_grade()
        elif choice == 2:
            calculators.normal_calculator.calculate_two_numbers()
        elif choice == 3:
            obesity_calculator.calculate_obesity()
        elif choice == 4:
            calculate_pay()
        elif choice == 5:
            baseball_game.play_game()
        elif choice == 6:
            beskin_rabins_game.play_game()
        elif choice == 7:
            crocodile_game.play_game()
        elif choice == 8:
            rps_game.play_game()
        elif choice == 0:
            print("프로그램을 종료합니다.")
            break
```
{% endcode-tabs-item %}
{% endcode-tabs %}


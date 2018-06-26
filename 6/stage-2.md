---
description: '메인 함수를 선언하는 방법을 배우고, 반복문을 사용하여 여러분만의 프로그램을 완성시켜 봅니다.'
---

# Stage 2 - 메인 함수 만들기

## 나만의 프로그램

우리가 지금까지 만든 모든 파일들을 모듈로 만들어서 메인 프로그램 한군데에서 실행시킬 수 있도록 만들어볼 것 입니다. 필요할 때 마다 코딩을 이용해서 여러분의 프로그램을 더욱 확장시켜보세요. 조그만 것 부터 시작하다보면 어느샌가 대단한 무언가를 만들고 있을 것 입니다.

![&#xBA54;&#xC778; &#xD504;&#xB85C;&#xADF8;&#xB7A8;](../.gitbook/assets/image%20%2843%29.png)

## 메인 함수 선언하기

### 메인 함수의 의미 

우리는 이제서야 처음으로 메인 함수라는 단어를 들었습니다. 그러나 다른 언어를 배우게 되면, 일반적으로 가장 처음 시간에 메인 함수에 대해 배우게 됩니다. 메인 함수는 프로그램의 시작점이 되는 곳을 알려주는 역할을 합니다. 생각해보니 시작점을 알려주는 것이 합리적이죠? 우리가 지금까지 만든 프로그램은 시작점이 없어서 파일을 처음부터 끝까지 통째로 실행하게 되는 것 입니다. 메인 함수를 만들어 조금 더 명확한 시작의 의미를 가지도록 프로그램을 만들어 봅시다.

### 메인 함수 만들기 

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
if __name__ == "__main__":
```
{% endcode-tabs-item %}
{% endcode-tabs %}

파이썬에서 메인 함수는 위와 같이 선언하면 됩니다. 기존에 함수를 선언할 때, 'def'를 사용한 것과는 좀 다른 모양입니다. if문을 사용하여 파이썬에 미리 지정된 '\_\_name\_\_'이란 변수와 비교하여 메인 함수임을 파악합니다.

![&#xC120;&#xC5B8;&#xD55C; &#xBAA8;&#xC2B5;](../.gitbook/assets/image%20%2890%29.png)

선언하게 되면 왼쪽에 초록색 실행 아이콘이 보일 것 입니다. 이곳에서부터 실행할 수 있다는 의미입니다.

## 반복하여 실행하기 

### 반복문 사용하기 

사용자가 종료한다는 입력을 주기 전까지 계속해서 프로그램을 수행시킬 수 있도록 while문을 사용하여 메인 함수를 반복적으로 만들어봅시다.

### 입력받아 원하는 모듈 실행하기 

사용자에게 번호에 따른 안내문을 제공하고, 원하는 수행을 할 수 있도록 조건문을 사용하여 만들어봅시다.

{% code-tabs %}
{% code-tabs-item title="main.py" %}
```python
import calculators.grade_calculator
import calculators.normal_calculator
from calculators import obesity_calculator
from calculators.pay_calculator import calculate_pay
from games.beskin_rabins_game import validate_input


if __name__ == "__main__":

    while True:

        print('''
실행하고자 하는 번호를 입력해주세요.
0. 종료
1. 학점 계산기
2. 일반 계산기
3. 비만도 계산기
4. 급여 계산기
        ''')

        choice = validate_input("선택 : ", ['0', '1', '2', '3', '4'])

        if choice == 1:
            calculators.grade_calculator.calculate_grade()
        elif choice == 2:
            calculators.normal_calculator.calculate_two_numbers()
        elif choice == 3:
            obesity_calculator.calculate_obesity()
        elif choice == 4:
            calculate_pay()
        elif choice == 0:
            print("프로그램을 종료합니다.")
            break
```
{% endcode-tabs-item %}
{% endcode-tabs %}


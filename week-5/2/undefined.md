---
description: 자율과제 2의 모범 답안입니다.
---

# 모범 답안

## 일반 계산기

{% code-tabs %}
{% code-tabs-item title="calculators/normal\_calculator.py" %}
```python
print("일반계산기 프로그램입니다!")


def add(a, b):
    return a + b


def sub(a, b):
    return a - b


def mul(a, b):
    return a * b


def div_int(a, b):
    return a // b


def div_float(a, b):
    return a / b


def reminder(a, b):
    return a % b


while True:
    first = input("계산할 첫번째 값을 입력해주세요 : ")
    second = input("계산할 두번째 값을 입력해주세요 : ")
    way = input('''
    원하는 연산을 선택하세요.
    1. 더하기
    2. 빼기
    3. 곱하기
    4. 정수나누기
    5. 실수나누기
    6. 나머지 구하기
    7. 계산기 종료
    ''')

    first = int(first)
    second = int(second)

    # 결과 출력
    print("\n\n두 개의 값 : {0} 와 {1}\n".format(first, second))

    if way == "1":
        print("더하기 값 (a + b) : {0}".format(add(first, second)))
    elif way == "2":
        print("빼기 값 (a - b) : {0}".format(sub(first, second)))
    elif way == "3":
        print("곱하기 값 (a * b) : {0}".format(mul(first, second)))
    elif way == "4":
        print("정수 나누기 값 (a // b) : {0}".format(div_int(first, second)))
    elif way == "5":
        print("실수 나누기 값 (a / b) : {0}".format(div_float(first, second)))
    elif way == "6":
        print("나머지 값 (a % b) : {0}".format(reminder(first, second)))
    elif way == "7":
        print("프로그램을 종료합니다.")
        break
    else:
        print("잘못된 연산입니다.")
```
{% endcode-tabs-item %}
{% endcode-tabs %}


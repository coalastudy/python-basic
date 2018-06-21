---
description: >-
  숫자 4개를 가지고 자리와 수의 크기를 비교하여 스트라이크와 볼을 판단하는 게임을 만들어봅니다. 이전까지 배운 변수, 할당연산자, 입출력,
  조건문, 반복문, 랜덤 라이브러리 등을 활용합니다.
---

# Stage 2 - 야구 게임 만들기

## 야구 게임 코딩하기 

본격적으로 야구 게임을 만들어보겠습니다. 이번 Stage를 통하여 이전 시간에 그렸던 순서도에서 난수를 발생하여 문제를 출제하는 부분과 사용자로부터 정답을 입력받는 부분까지 코딩할 것 입니다. 잘 따라오세요!

![&#xC57C;&#xAD6C; &#xAC8C;&#xC784;](../.gitbook/assets/image%20%2814%29.png)

## 난수 발생하기

### 랜덤 라이브러리 활용

로또 발생기를 기억하시죠?! 로또 발생기와 아주 똑같습니다. 다만 여기서 조금 달라진 부분이 있다면, 로또 발생기는 7자리지만 야구 게임은 4자리라는 것과 랜덤 라이브러리에서 randrange문이 아닌 randint문을 사용해서 좀 더 직관적으로 범위를 설정한 것 입니다. 아래와 같이 코딩하여 난수를 생성해 봅시다.

{% code-tabs %}
{% code-tabs-item title="games/baseball\_game" %}
```python
import random

print("야구 게임 프로그램입니다!")

new_number = random.randint(0, 9)
print(new_number)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 중복 제거하기

이번에는 'answer'라는 정답 리스트 변수를 하나 선언하고 정답 리스트 안에 새로운 숫자가 있는지 중복여부를 파악하여 4자리의 숫자를 만들어주는 과정까지 코딩해보겠습니다.

{% code-tabs %}
{% code-tabs-item title="games/baseball\_game" %}
```python
import random

print("야구 게임 프로그램입니다!")

# 랜덤하게 4자리의 숫자 만들기 (각 자리의 수는 중복 불가)
answer = list()

while len(answer) != 4:
    new_number = random.randint(0, 9)
    if new_number not in answer:
        answer.append(new_number)

print(answer)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## 정답 입력받기

### 사용자로부터 정답 입력받기

위의 과정을 통해 4자리의 정답 리스트를 생성했습니다. 이번에는 사용자로부터 답을 맞추는 과정을 입력받아 그 안의 값을 하나하나 조회해보는 과정입니다.

먼저는 input문을 통해 4자리의 값을 입력받습니다. 입력받은 4자리의 숫자는 문자열 자료형입니다. 문자열 자료형도 enumerate문에 넣어서 반복문을 실행하면 값과 인덱스를 하나하나 조회할 수 있습니다. 아래와 같이 코딩해보세요.

{% code-tabs %}
{% code-tabs-item title="games/baseball\_game" %}
```python
# 유저에게 입력 받음
your_answer = input("답을 맞추어 보세요 : ")

# 스트라이크, 볼 검사
for index, value in enumerate(your_answer):
    print("index : {0}, value : {1}".format(index, value))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% page-ref page="../week-2/stage-4.md" %}


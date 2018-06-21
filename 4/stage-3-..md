---
description: 게임의 중요한 논리적 구조는 완성하였습니다. 이를 반복하는 일이 남았습니다. 반복적으로 게임을 만들어봅시다.
---

# Stage 4 - 루프속으로 빠져봅시다.

## 야구 게임 완성하기 

이제 게임을 완성하고 즐기는 시간만 남았습니다. 반복적으로 사용자에게 입력을 받아서 4 스트라이크가 나올 때까지 반복하면 되는데요. 함께 코딩해봅시다!

![&#xC644;&#xC131;&#xB41C; &#xC57C;&#xAD6C; &#xAC8C;&#xC784;](../.gitbook/assets/image%20%2863%29.png)

## 루프 돌리기

### 반복 범위 정하기

먼저는 반복되는 범위를 현재 우리가 작성한 코드에서 파악해보는 것이 중요합니다. 그래야 TAB을 통해서 반복할 부분을 컴퓨터에게 알려줄 수 있으니까요.

무엇이 반복되는지 생각해봅시다. 난수의 생성은 한 번이면 충분합니다. 반복하지 않아도 됩니다. 유저의 숫자 입력은 어떻죠? 반복이 되네요! 그렇다면 유저가 입력하는 곳부터 반복을 시작하면 좋겠네요. 현재 우리가 작성한 숫자를 판별하는 것도 반복되서 알려주어야 사용자가 그 힌트를 가지고 숫자를 맞힐 수 있겠죠. 그래서 반복 범위는 아래와 같이 될 것 입니다.

![&#xBC18;&#xBCF5; &#xBC94;&#xC704; &#xC815;&#xD558;&#xAE30;](../.gitbook/assets/image%20%2886%29.png)

### 반복 조건 정하기

언제까지 반복해야 될까요? 어렵지 않습니다. 4 스트라이크가 될 때까지 반복하면 되겠죠! 그러면 조건이 'strike != 4'가 되겠네요! 여기서 주의해야할 점은, 위의 코드에서 while문을 바로 써준다면, 'strike 변수가 while문 내부에 있어서 처음 while문이 시작될 때 strike가 없어서 문제가 발생합니다. 그래서 우리는 while문 이전에 'strike' 변수를 선언해주어야 합니다.

{% code-tabs %}
{% code-tabs-item title="games/baseball\_game.py" %}
```python
import random

print("야구 게임 프로그램입니다!")

# 랜덤하게 4자리의 숫자 만들기 (각 자리의 수는 중복 불가)
answer = list()

while len(answer) != 4:
    new_number = random.randint(0, 9)
    if new_number not in answer:
        answer.append(new_number)

# print(answer)

strike = 0

while strike != 4:
    # 유저에게 입력 받음
    your_answer = input("답을 맞추어 보세요 : ")

    strike = 0
    ball = 0

    # 스트라이크, 볼 검사
    for index, value in enumerate(your_answer):
        print("index : {0}, value : {1}".format(index, value))
        if int(value) == answer[index]:
            strike += 1
        elif int(value) in answer:
            ball += 1

    if strike == 0 and ball == 0:
        print("Out!!!!!!!!!!!")
    else:
        print("{0} 스트라이크 {1} 볼입니다.".format(strike, ball))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## 결과 출력하기

### 카운트 변수 추가

마지막으로 게임을 종료하고 몇번의 시행만에 정답을 맞추었는지 알려주기 위해서 카운트해주는 변수를 추가할 것 입니다. 

카운트 변수를 선언해주어야 하는데, 어디에 선언하면 좋을까요? 일단, 카운트 변수는 반복문 안에서 초기화 되어서는 안됩니다. 왜냐하면 반복하는 행위를 몇 번 했는지 세야하는 것인데, 그 안에서 초기화가 된다면 계속 초기화 값에 머물러 있겠죠. 따라서 반복문 밖에서 초기화 해줍니다.

결국 시행이란 것은 사용자가 수를 입력하는 행위를 의미합니다. 그래서 카운트 변수는 사용자가 입력할 때 1씩 증가해야합니다.

그리고 마지막에 모든 반복문이 종료되고 카운트 정보를 출력합니다.

{% code-tabs %}
{% code-tabs-item title="games/baseball\_game.py" %}
```python
import random

print("야구 게임 프로그램입니다!")

# 랜덤하게 4자리의 숫자 만들기 (각 자리의 수는 중복 불가)
answer = list()

while len(answer) != 4:
    new_number = random.randint(0, 9)
    if new_number not in answer:
        answer.append(new_number)

# print(answer)

strike = 0
count = 0

while strike != 4:
    # 유저에게 입력 받음
    your_answer = input("답을 맞추어 보세요 : ")

    count += 1
    strike = 0
    ball = 0

    # 스트라이크, 볼 검사
    for index, value in enumerate(your_answer):
        # print("index : {0}, value : {1}".format(index, value))
        if int(value) == answer[index]:
            strike += 1
        elif int(value) in answer:
            ball += 1

    if strike == 0 and ball == 0:
        print("Out!!!!!!!!!!!")
    else:
        print("{0} 스트라이크 {1} 볼입니다.".format(strike, ball))
        
print("{0}번만에 정답을 맞추셨습니다!".format(count))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### Enjoy Your Game! 

이전에 코딩하면서 불필요한 출력들이 있었습니다. 그것들을 다 지우고 게임을 즐기시길 바랍니다! 위의 코드 상에서 13, 28번째 줄.


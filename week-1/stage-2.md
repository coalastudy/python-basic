---
description: '파이썬으로 모니터에 문자를 출력하는 방법을 배워봅니다. 먼저는 ''Hello World!''를 출력해보고, 메뉴판까지 만들어봅니다.'
---

# Stage 2 - 출력과 실행

## 메뉴판 그려보기

간단한 출력 연습을 해보고, 고급 과정으로 메뉴판 그리기를 해 볼 것 입니다. 이미 나는 좀 알아 하시는 분들은 당장 메뉴판을 그려보셔도 좋아요. 여러분이 가게를 차린다고 생각하시고 정성껏 메뉴판을 작성해보아요!

![&#xBA54;&#xB274;&#xD310; &#xCD9C;&#xB825; &#xACB0;&#xACFC;](../.gitbook/assets/image%20%2827%29.png)

## Hello World! 출력하기

Hello World!는 여러분이 모든 프로그래밍 언어를 배울 때 접하게 될 것입니다. 컴퓨터의 세상으로 온 여러분에게 컴퓨터가 인사를 하는 것이 아닐까 생각되네요. 차근차근 따라하며 컴퓨터와 인사하는 시간을 가져봐요!

### print문 알아보기

'print'는 번역하면 '출력하다'라는 뜻이죠. 파이썬에서 print문을 사용하여 모니터에 우리가 원하는 문자들을 출력할 수 있습니다. 우리가 파이썬 파일에 print문을 쓰면 컴퓨터는 출력하라는 명령을 받아서 우리가 보는 모니터 화면에 print문 안의 내용을 보여주게 됩니다.

![print&#xC758; &#xC0AC;&#xC6A9;](../.gitbook/assets/image%20%2836%29.png)

### Hello World!

Stage 1에서 만든 main.py로 들어가보세요. main.py에 아래와 같은 코드를 작성해주세요.

{% code-tabs %}
{% code-tabs-item title="main.py" %}
```python
print("Hello World!")
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 실행하기

main.py를 우클릭하고 Run 'main'을 클릭합니다.

![main.py&#xB97C; &#xC2E4;&#xD589;](../.gitbook/assets/image%20%281%29.png)

## 파일 이름 출력하기

print문을 조금 더 연습해봅시다. 이번에는 각각의 파일에 들어가서 print문을 써본 뒤 각각의 파일을 실행시켜보도록 할 것 입니다. 비만도 계산기 파일을 예시로 들어서 설명할테니 여러분은 나머지 5개의 파일에서도 똑같이 해보세요.

### 프로그램 설명문 작성하기

obesity\_calculator.py를 열어 아래의 코드를 작성해주세요.

{% code-tabs %}
{% code-tabs-item title="obesity\_calculator.py" %}
```python
print("비만도 계산기 프로그램입니다.")
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 실행하기

main.py를 실행했던 것 처럼, 이번에는 obesity\_calculator.py에서 우클릭하여 Run 'obesity\_calculator'를 클릭합니다.

![obesity\_calculator.py&#xB97C; &#xC2E4;&#xD589;](../.gitbook/assets/image%20%2831%29.png)

{% hint style="info" %}
메뉴막대에 보시면 Run이라는 항목이 있습니다. 그 안에 첫번째 Run과 세번째 Run, Run이 2개가 존재하는데, 큰 차이점이 있습니다. 첫번째 Run 이전에 실행시켰던 파일이 있으면 해당 파일을 또 다시 시작합니다. 따라서 이전에 실행 기록이 없다면 비활성화 됩니다. 세번째 Run은 초기 상태에서 실행하기 때문에 파일을 선택하는 과정이 추가됩니다.
{% endhint %}

## 메뉴판 출력하기

### format문 알아보기

문장을 출력하게 될 때, 우리는 좌우로, 가운데로 정렬도 하고 싶고, 반복되는 문구를 출력해야 될 수도 있고, 문자만 출력하는게 아니라 숫자를 출력해야 될 때도 있습니다. 그래서 우리는 이러한 문장의 형태를 편리하게 표현하기 위해 파이썬에서 제공하는 format문을 사용합니다.

###  format 예시

#### 2개 이상의 값 넣기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"I love {0}, you love {1}.".format("apple", "me")
# I love apple, you love me
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 숫자 넣기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"I have {0} dollars".format(100000)
# I have 100000 dollars
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 이름으로 넣기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"you give me {gift}, he loves {gift}".format(gift="shoes")
#you give me shoes, he loves shoes
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 왼쪽 정렬하기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"{0:<10}".format("hi")
#'hi        '
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 가운데 정렬하기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"{0:^10}".format("hi")
#'    hi    '
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 오른쪽 정렬하기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"{0:>10}".format("hi")
#'        hi'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 공백 채우기

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
"{0:!<10}".format("hi")
#'hi!!!!!!!!'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 메뉴판 그리기

print문, format문에 대하여 학습하였습니다. 이제 여러분의 메뉴판을 작성해봅시다. 제가 만든 메뉴판을 예시로 삼아 여러분의 메뉴판을 만들어보세요.

{% code-tabs %}
{% code-tabs-item title="lunch\_recommander.py" %}
```python
print("점심 추천기 프로그램입니다!")

print('''
메뉴판
======================
{0:<10}{1:>10}{won} 
{2:<10}{3:>10}{won}
{4:<10}{5:>10}{won}
{6:<10}{7:>10}{won}
{8:<10}{9:>10}{won}
{10:<10}{11:>10}{won}
{12:<10}{13:>10}{won}
======================
'''.format('갈비탕', 10000,
           '떡볶이', 7000,
           '오뎅', 5000,
           '감자탕', 8000,
           '김치찌개', 8000,
           '제육볶음', 7000,
           '김치볶음밥', 5000, won="원"))
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
print문 안에 따옴표 3개로 감싸면 줄바꿈에 관계없이 그대로 출력됩니다. 기존 따옴표 안에서 줄바꿈을 하려면 '\n' 문자를 사용합니다.
{% endhint %}




---
description: '코딩에서 중요한 변수의 개념에 대해 이해하고, 할당연산자가 무엇인지 배워봅니다. 이를 가지고 급여 계산기를 만들어봅니다.'
---

# Stage 3 - 급여 계산기 만들기

## 급여 계산기 만들어보기

알바하느라 힘드시죠? 이렇게 일해서 한달에 얼마를 벌 수 있을지... 번 돈으로 무엇을 할 수 있을지 궁금하지 않으신가요? 이 모든 것 한방에 빠르게 보여주는 급여 계산기를 한번 만들어봐요!

![&#xAE09;&#xC5EC; &#xACC4;&#xC0B0;&#xAE30; &#xC644;&#xC131;](../.gitbook/assets/2018-06-17-11.07.27.png)

## 변수란 무엇인가?

### 변수란?

변수는 값을 담는 그릇입니다. 밥을 먹을 때 많은 음식들이 그릇에 담겨져 나오죠? 그릇에 김치가 담겨져 나올 수도 있고, 불고기가 담겨져 나올 수 있고, 빈대떡이 담겨져 나올 수 있습니다. 이처럼 변수는 값을 담습니다. 숫자 1이 담길 수도 있고, 1000이 담길 수도 있고, 94923이 담길 수도 있고, 문자 'I love you'가 담길 수도 있습니다.

![&#xBCC0;&#xC218; = &#xAC12;&#xC744; &#xB2F4;&#xB294; &#xADF8;&#xB987;](../.gitbook/assets/image%20%28139%29.png)

### 급여 계산기에서 필요한 변수

급여를 계산하기 위해서 우리는 필요한 정보들이 있습니다. 우선은 내가 시급이 얼마인지 알아야겠죠. 그리고 하루에 몇시간을 근무하는지, 한달에 몇 일을 근무하는지 알아야 한달 급여를 계산할 수 있습니다. 시급이 얼마인지 담는 그릇, 일일근무시간을 담는 그릇, 한달근무일수를 담는 그릇 이렇게 3개의 그릇이 필요합니다.

```text
pay -> 시급
time_of_day -> 일일근무시간
day_of_month -> 한달근무일수
```

## 할당연산자란 무엇인가?

### 할당연산자란?

할당이란 말이 조금 낯설죠? 위의 변수에서 설명했던 용어로 대신하면 담는 행위로 생각하시면 됩니다. 변수라는 그릇에 값을 '담다'이 바로 '할당하다' 입니다. 

수학에서 '='은 '같다'라는 의미로 사용됩니다. 그러나 코딩에서는 '할당', 즉 '담는다'의 의미입니다. 왼쪽\(좌항\)의 변수에 오른쪽\(우항\)의 값을 담는 의미입니다.

 

![&#xD560;&#xB2F9;&#xC5F0;&#xC0B0;&#xC790;](../.gitbook/assets/image%20%2890%29.png)

### 변수에 할당하기

급여 계산기에서 3개의 변수에 값을 담아보도록 하겠습니다. 시급 7000원, 일일근무시간 8일,  한달근무일수는 19일로 담아봅시다.

{% code-tabs %}
{% code-tabs-item title="calculators/pay\_calculator.py" %}
```python
pay = 7000
time_of_day = 8
day_of_month = 19
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## 급여 계산기 완성하기

### 한달 급여 계산하기

한달 급여를 어떻게 계산하면 될까요?

{% hint style="info" %}
한달 급여 = 시급 \* 일일근무시간 \* 한달근무일수
{% endhint %}

위와 같은 식이 성립되겠죠. 위 식을 코드로 옮겨보겠습니다.

{% code-tabs %}
{% code-tabs-item title="calculators/pay\_calculator.py" %}
```python
# 월급 계산
profit = pay * time_of_day * day_of_month
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 출력하기

앞서 배운 print문과 format문을 사용하여 출력해보도록 하겠습니다.

아래의 코드는 완성된 코드입니다.

{% code-tabs %}
{% code-tabs-item title="calculators/pay\_calculator.py" %}
```python
print("급여계산기 프로그램입니다!")

pay = 7000
time_of_day = 8
day_of_month = 19

# 월급 계산
profit = pay * time_of_day * day_of_month

# 결과 출력
print("예상 월급은 : {0}원입니다.\n\n".format(profit))
print("{0}원으로 무엇을 할 수 있을까요?".format(profit))
print("PC방 (1200원 기준) : {0}시간".format(profit // 1200))
print("점심 (7000원 기준) : {0}끼".format(profit // 7000))
print("영화 (11000원 기준) : {0}편".format(profit // 11000))
print("노래방 (20000원 기준) : {0}시간".format(profit // 20000))

print('''
열심히 일하시는 당신에게...
비록 세상이 그대를 속일지라도
슬퍼하거나 노여워하지 말아라
슬픈 날은 참고 견디라
기쁜 날이 오고야 말리니.''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% hint style="info" %}
'//'는 정수 나눗셈을 의미합니다. '/' 파이썬3에서는 실수 나눗셈을 적용합니다.
{% endhint %}


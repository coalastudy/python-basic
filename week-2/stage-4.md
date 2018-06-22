---
description: >-
  주민번호 앞자리를 통해 생년월일을 알 수 있고, 뒷자리의 첫번째 자리로 성별을 판별할 수 있습니다. 사용자로부터 주민번호 정보를 입력받고
  주민번호의 내용을 분석하여 조건문을 통해 정보를 뽑아내도록 하겠습니다.
---

# Stage 4 - 주민번호 인적사항 판별하기

## 주민번호 분석기

주민번호 앞자리는 생년월일을 뒷자리에서 첫번째는 성별을 나타냅니다. 그런데 뒷자리가 가지는 또 다른 의미를 아시나요? 뒷자리의 나머지 자리는 여러분이 출생한 장소를 지역코드로 나타내는데요. 이번 Stage와 Challenge를 통해서 주민번호를 완전히 파헤쳐보도록 하겠습니다.

이번 시간에는 앞자리와 뒷자리의 첫번째를 가지고 정보를 파악해서 생년월일과 성별을 판별해내겠습니다.

![&#xC8FC;&#xBBFC;&#xB4F1;&#xB85D; &#xBD84;&#xC11D;&#xAE30;](../.gitbook/assets/image%20%28116%29.png)

## 문자열 분석하기

### 문자열은 어떻게 구성되는가?

주민등록을 사용자로부터 입력받으면 문자열 형태로 주민번호가 들어옵니다. 그러면 생년월일을 알기 위해선 앞의 6자리를 각각 2자리씩 끊어서 생각해야 합니다. 이를 위해 우리는 문자열이 어떻게 구성되어 있는지 알아야 합니다. 그런데 전혀 어렵지 않습니다. 각각의 문자열에는 문자 하나하나마다 순서대로 숫자가 부여되어 있습니다. 우리는 그 문자가 문자열에서 몇번째 문자인지만 알면 우리가 원하는 문자를 가져올 수 있습니다.

![&#xBB38;&#xC790;&#xC5F4;&#xC758; &#xAD6C;&#xC131;](../.gitbook/assets/image%20%2852%29.png)

이렇게 각 문자마다 숫자가 부여된 것을 문자열 인덱싱이라고 합니다.

### 문자열 인덱싱 알아보기

문자열 인덱싱에 대해 이해하셨으면, 이제는 파이썬에서 문자열 인덱싱을 사용해보도록 하겠습니다. 아래의 코드를 통해 이해해보도록 합시다.

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
a = "I love you"

print(a[0])
# 'I' 출력

print(a[8])
# 'o' 출력

print(a[-1])
# 'u' 출력

print(a[-3])
# 'y' 출력

print(a[10])
# error 범위를 넘어감

print(a[-11])
# error 범위를 넘어감
```
{% endcode-tabs-item %}
{% endcode-tabs %}

* 인덱싱은 대괄호\(\[\]\)안에 문자에 해당하는 숫자\(인덱스\)를 넣어주어 원하는 문자를 가져옵니다.
* 인덱싱은 음수로도 가능합니다. -1번째는 마지막 문자를 인덱싱합니다.
* 문자열의 범위를 넘어가면 안됩니다.

### 문자열 슬라이싱 알아보기

인덱싱을 알아보았습니다. 하지만 인덱싱은 문자열 내에서 연속된 여러개의 문자를 가져오지는 못합니다. 단 하나의 문자만 가져올 수 있지요. 그래서 슬라이싱이란 것이 있습니다. 말 그대로 문자열을 더 작은 조각으로 자르는 행위입니다. 어떻게 할 수 있는지 예문을 통해 살펴보겠습니다.

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
a = "I love you"

print(a[0:3])
# 'I l' 출력

print(a[7:-1])
# 'yo' 출력

print(a[3:])
# 'ove you' 출력

print(a[:4])
# 'I lo' 출력력
```
{% endcode-tabs-item %}
{% endcode-tabs %}

* ':' 콜론으로 범위를 지정합니다.
* 콜론 앞의 숫자\(인덱스\)부터 마지막 숫자\(인덱스\) 앞의 문자까지 가져니다.
* 콜론 앞에 숫자\(인덱스\)가 없으면 문자열의 처음부터 가져니다.
* 콜론 뒤에 숫자\(인덱스\)가 없으면 문자열의 끝까지 가져옵니다.

## 주민번호로 인적사항 판별하기

### 정보 뽑아내기

앞서 배운 문자열 슬라이싱을 사용하여 생년월일과 성별에 대한 정보를 가져와봅시다.

{% code-tabs %}
{% code-tabs-item title="resident\_number\_analyzer.py" %}
```python
print("주민등록번호 분석기 프로그램입니다!")

resident_number = input("주민번호를 입력해주세요 : ")

# 생년 월일 탐색
birth_year = resident_number[0:2]
birth_month = resident_number[2:4]
birth_day = resident_number[4:6]
sex = resident_number[6]
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 성별 비교하기

조건문을 가지고 성별을 비교합니다.

{% code-tabs %}
{% code-tabs-item title="resident\_number\_analyzer.py" %}
```python
# 성별 탐색
if sex == '1' or sex == '3':
    sex = '남자'
elif sex == '2' or sex == '4':
    sex = '여자'
else:
    sex = '중성'
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 출력하기

{% code-tabs %}
{% code-tabs-item title="resident\_number\_analyzer.py" %}
```python
# 주민번호로부터 정보 출력
print("\n생년월일 : {0}년 {1}월 {2}일".format(birth_year, birth_month, birth_day))
print("성별 : {0}".format(sex))
```
{% endcode-tabs-item %}
{% endcode-tabs %}


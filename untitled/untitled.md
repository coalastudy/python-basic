---
description: 파이썬에 내장되어 있는 random이라는 것을 사용하여 점심을 추천해주는 점심 추천기를 완성합니다.
---

# Stage 2 - 점심으로 뭘 먹지?

## 점심 추천기

직장인 여러분! 매일매일 최대의 난제죠. 아 오늘 점심 뭐먹지... 이상하게도 우리 회사 주변에 혹은 동네에 음식점은 엄청나게 많은데 먹을 것이 없죠. 참 이상한 이상한 일이에요. 그래서 더 이상 고민을 그만하기 위해서 랜덤으로 메뉴를 추천해주는 점심 추천기를 만들어 볼 것 입니다. 여러분이 마음 껏 응용해서 사용할 수 있으니까, 여러분의 실생활에서 사용해보면 좋겠네요!

![&#xC810;&#xC2EC; &#xCD94;&#xCC9C;&#xAE30; &#xC644;&#xC131;](../.gitbook/assets/image%20%2837%29.png)

## 내장 함수와 외장 함

### 함수란 무엇인가?

여러분이 이제껏 코딩을 하면서 사용했던 대부분의 것들이 바로 함수입니다. 함수는 6주차때 더 자세히 배웁니다. 지금 시간에는 '아 우리가 했던게 함수구나' 이 정도만 알아두시면 됩니다. 그래서 무엇이 함수냐? print문, input문, format문, len문 등 단어 다음에 소괄호가 오는 것이 함수입니다. 우리가 사용했던 함수는 모두 내장 함수로서 파이썬을 만든 사람이 사용하기 편하도록 파이썬 내부에 심어놓은 코드들을 우리는 편하게 사용하는 것입니다.

![&#xD568;&#xC218; &#xC0AC;&#xC6A9;&#xC758; &#xC608;&#xC2DC;](../.gitbook/assets/image%20%2858%29.png)

### 내장 함수, 외장 함수의 차이점

#### 내장 함수

아무런 설정이 필요없이 파이썬을 설치만 하면 기본적으로 사용할 수 있는 함수를 의미합니다.

#### 외장 함수

외장 함수를 알기 위해서는 먼저 '라이브러리'란 것을 알아야 합니다. 라이브러리는 도서관이라는 뜻이죠. 맞습니다. 책 대신에 함수들이 모여있는 도서관입니다. 그래서 우리는 외장 함수를 사용하려면 먼저 라이브러리를 코드에 심어주어야 합니다. 그리고 그 라이브러리에서 우리가 사용하고자 하는 함수를 찾아서 사용하면 되는 것 입니다.

![&#xB0B4;&#xC7A5; &#xD568;&#xC218;&#xC640; &#xC678;&#xC7A5; &#xD568;&#xC218;](../.gitbook/assets/image%20%2823%29.png)

### random 파헤치기

파이썬에 수많은 라이브러리가 있지만, 우리는 random 라이브러리를 가져와서 사용할 것 입니다. 왜냐하면, 점심 추천기를 만들 때 임의로 추천할 메뉴를 골라주기 위해서죠. random 말고도 수많은 라이브러리가 있으니, 여러분이 무엇인가 필요하시다면 구글링을 통해 라이브러리를 찾아보시길 권합니다. 이번 시간을 통해 random을 예제로 라이브러리를 가져와 외장 함수를 사용하는 법을 배우는 것 입니다.

#### random 라이브러리 가져오기

아래와 같은 코드를 파이썬 파일 최상단에 선언함으로써 random 라이브러리를 가져올 수 있습니다.

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
import random
```
{% endcode-tabs-item %}
{% endcode-tabs %}

random 라이브러리가 지원하는 함수 예제입니다.

#### randrange\(a, b\)

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
import random
num = random.randrange(1, 10)
print(num)
# 1 <= num < 10 범위에서 난수를 생성
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### randint\(a, b\)

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
import random
num = random.randint(1, 10)
# 1 <= num <= 10 범위에서 난수를 생성
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### shuffle\(list\)

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
import random
my_list = [1, 2, 3, 4, 5]
random.shuffle(my_list)
print(my_list)
# [4, 1, 5, 2, 3] 등 리스트를 마구 섞음
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### choice\(list\)

{% code-tabs %}
{% code-tabs-item title="example" %}
```python
import random
my_list = [1, 2, 3, 4, 5]
result = random.choice(ㅣ)
print(result)
# my_list의 요소들 중 하나를 무작위로 선택
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## 점심 추천기 만들기

### random 사용하여 숫자 뽑아내기

### 추천 결과 출력하


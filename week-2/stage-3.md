---
description: 학점 계산기를 만들어보면서 조건문에 대해 더욱 깊이 이해합니다.
---

# Stage 3 - 학점 계산하기

## 학점 계산기

시험이 끝나면 내 평균학점은 어떻게 될까? 궁금하고 초조하시죠? 그래서 우리는 학점 계산기로 우리의 예상 점수를 입력하고 결과를 받아보곤 하는데요. 아직은 우리가 여러 과목을 입력받아 학점을 계산하기에는 무리가 있습니다. 그래서 우선은 한 과목만 입력받고, 만점 방식을 선택하여 학점에 대한 점수가 몇 점인지 계산하는 프로그램을 만들어보도록 하겠습니다.

![&#xC644;&#xC131;&#xB41C; &#xD559;&#xC810; &#xACC4;&#xC0B0;&#xAE30;](../.gitbook/assets/image%20%281%29.png)

## 다중 조건문

### 다중 조건문이란 무엇인가?

다중 조건문은 조건문안에 또 조건문이 들어가는 것을 의미합니다. A라는 조건에 의하여 코드가 수행되는데 그 안에서 또 조건문에 있게 되는 것이지요. 그래서 머릿속으로 어떻게 결과가 나오는지 고민하다보면 어려움에 봉착하게 됩니다. 예를 들어, 어떤 사물에 대하여 사물이 무엇인지 판단하려고 합니다. '귤'이라는 사물이 있다고 했을 때, 사물을 판별하기 위해 사물의 카테고리를 나누겠죠? 음식, 가전제품, 의류 등으로 말이죠. '귤'은 음식이기 때문에, 음식으로 들어오게 되겠죠. 그러면 그 음식 안에서 또 카테고리가 나뉩니다. 육류, 채소류, 과일류 등으로 말이죠. 그럼 '귤'은 과일로 들어가겠죠. 그 중에 귤, 바나나, 포도, 오렌지 등 여러 과일들이 존재하는거고요. 이런 식으로 조건 안에 조건이 있는 경우에 대해 다중 조건문이라고 합니다.

![&#xB2E4;&#xC911; &#xC870;&#xAC74;&#xBB38; &#xC608;&#xC2DC;](../.gitbook/assets/image%20%2820%29.png)

### 다중 조건문은 어떻게 사용하나요?

다중 조건문의 사용은 간단합니다. 이전 시간에 배웠던 것 처럼 TAB으로 구분된 조건문 안에 원하는 위치에 TAB을 정렬하여 사용하면 됩니다. 아래의 코드는 위의 것에 대한 예시입니다.

![&#xC608;&#xC2DC; &#xCF54;&#xB4DC;](../.gitbook/assets/image%20%2846%29.png)

## 학점 계산기 만들기

본격적으로 학점 계산기를 만들어보겠습니다. 과목명, 당신의 점수, 취득 학점을 입력받고, 만점 방식에 대해 입력받습니다. 만점 방식에 따라 당신의 점수를 계산하는 방법이 달라집니다. 그 방법은 아래와 같습니다.

```text
4.5 만점
    A+ - 4.5점
    A - 4.0점
    A- - 없음
    B+ - 3.5점
    B - 3.0
    B- - 없음
    C+ - 2.5점
    C - 2.0점
    C- - 없음
    F - 0
    
4.3 만점
    A+ - 4.3점
    A - 4.0점
    A- - 3.7
    B+ - 3.5점
    B - 3.0
    B- - 2.7
    C+ - 2.5점
    C - 2.0점
    C- - 1.7
    F - 0    
```

### 입력받기

과목명, 당신의 점수, 취득한 학점, 학점 계산 방식을 입력받아 봅시다.

{% code-tabs %}
{% code-tabs-item title="grade\_calculator.py" %}
```python
print("학점계산기 프로그램입니다!")

subject_name = input("과목명을 입력해주세요 : ")
subject_score = input("당신의 점수를 입력해주세요 : ")
subject_grade = input("취득한 학점을 입력해주세요 : ")

calculating_way = input('''
학점 계산 방식을 선택해주세요.
1. 4.5 만점
2. 4.3 만점
''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 다중 조건문으로 점수 계산하기

점수를 계산하고, 정보를 출력하세요.

{% code-tabs %}
{% code-tabs-item title="grade\_calculator.py" %}
```python
score = 0

if calculating_way == '1':
    if subject_score == 'A+':
        score = 4.5
    elif subject_score == 'A':
        score = 4.0
    elif subject_score == 'A-':
        score = "There is no value"
    elif subject_score == 'B+':
        score = 3.5
    elif subject_score == 'B':
        score = 3.0
    elif subject_score == 'B-':
        score = "There is no value"
    elif subject_score == 'C+':
        score = 2.5
    elif subject_score == 'C':
        score = 2.0
    elif subject_score == 'C-':
        score = "There is no value"
    elif subject_score == 'F':
        score = 0
    else:
        score = "There is no value"

    print('''
과목 이름 : {0}
당신의 점수 : {1}
변환한 점수 : {2}
당신의 취득학점 : {3}
'''.format(subject_name, subject_score, score, subject_grade))

elif calculating_way == '2':
    if subject_score == 'A+':
        score += 4.3
    elif subject_score == 'A':
        score += 4.0
    elif subject_score == 'A-':
        score += 3.7
    elif subject_score == 'B+':
        score += 3.3
    elif subject_score == 'B':
        score += 3.0
    elif subject_score == 'B-':
        score += 2.7
    elif subject_score == 'C+':
        score += 2.3
    elif subject_score == 'C':
        score += 2.0
    elif subject_score == 'C-':
        score += 1.7
    elif subject_score == 'F':
        score += 0
    else:
        score = "There is no value"

    print('''
과목 이름 : {0}
당신의 점수 : {1}
변환한 점수 : {2}
당신의 취득학점 : {3}
'''.format(subject_name, subject_score, score, subject_grade))

else:
    print("잘못된 연산 방법 입니다. 프로그램을 종료합니다.")
```
{% endcode-tabs-item %}
{% endcode-tabs %}


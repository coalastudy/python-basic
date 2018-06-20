---
description: 급여 계산기에 세금을 적용해봅니다. 세금 적용시에는 3가지의 조건이 있습니다. 조건이 3개가 붙을 때 어떻게 처리하는지 알아봅니다.
---

# Stage 2 - 급여에 세금 적용하기

## 세금 적용하기

납세의 의무를 잘 지키고 계신가요? 알바라도 주 15시간 이상, 월 60시간 이상 근무하는 근무자에게는 4대 보험 가입이 필수인데요. 4대 보험도 한 달 급여에서 제외되는 경우가 있죠. 그래서 이를 고려해보고요. 4대 보험으로 내는 세금 뿐만 아니라 소득세 공제를 위해 급여에서 빠지는 부분이 있을 수도 있죠. 이렇게 되면 한 달 열심히 일해도 왜 이거밖에 안들어왔지? 하고 의심이 가게 됩니다. 이번에는 세금에 관한 부분을 적용시켜보도록 하겠습니다.

![&#xC138;&#xAE08; &#xC801;&#xC6A9; &#xACB0;&#xACFC;](../.gitbook/assets/image%20%285%29.png)

## 세가지 조건을 처리해보기

### elif문 알아보기

Stage 1을 통하여 if문과 else문에 대해서 알아보았습니다. if문과 else문 밖에 없다면 코딩을 하는데 큰 어려움을 겪게 될 것입니다. 예를 들어, 일반 계산기를 만들때 덧셈을 할지, 뺄셈을 할지, 곱셈을 할지, 나눗셈을 할지 적어도 4개의 조건이 필요합니다. 그런데 if문과 else문을 가지고는 2가지 밖에 만들 수 없지요. 그래서 이를 보완하기 위해 elif문이 있습니다. elif문은 'else if'의 줄인 표현입니다. '그 외의 경우이고 만약에~' 이 정도로 해석할 수 있겠죠. elif문은 if문과 else문 사이에 원하는 만큼 집어넣을 수 있습니다. 아래와 같이 말이죠.

![elif&#xBB38; &#xC608;&#xC2DC;](../.gitbook/assets/image%20%2842%29.png)

## 세금 적용하기

### 조건에 대한 정리

세금에 대하여 4가지 조건으로 나누겠습니다.

```text
1. 미적용
2. 4대 보험만 적용 (8.41%)
3. 소득세 공제만 적용 (3.3%)
4. 모두 적용
```

### 세금 적용여부 입력받기

세금 적용하는 부분도 수습 적용하는 부분과 마찬가지로 입력 받습니다.

{% code-tabs %}
{% code-tabs-item title="pay\_calculator.py" %}
```python
# 세금 적용 여부
tax = input('''
세금을 적용하나요?
1. 미적용
2. 4대 보험료 공제
3. 소득세 공제
4. 모두 적용
''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}

숫자로 비교하기 위해 형변환합니다.

{% code-tabs %}
{% code-tabs-item title="pay\_calculator.py" %}
```python
# 세금 변수 추가
tax = int(tax)
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### 세금 적용하기

4가지의 경우를 비교하여 세금으로 나가는 비용을 계산해보세요.

{% code-tabs %}
{% code-tabs-item title="pay\_calculator.py" %}
```python
# 세금 적용
if tax == 2:
    tax_price = profit * 841 // 10000
elif tax == 3:
    tax_price = profit * 33 // 1000
elif tax == 4:
    tax_price = profit * 841 // 10000 + profit * 33 // 1000
else:
    tax_price = 0

profit = profit - tax_price
```
{% endcode-tabs-item %}
{% endcode-tabs %}


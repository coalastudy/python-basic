---
description: Challenge 2의 모범 답안입니다.
---

# 모범 답안

## 비만도 계산

{% code-tabs %}
{% code-tabs-item title="obesity\_calculator.py" %}
```python
print("비만도계산기 프로그램입니다!")

# 정보 입력
sex = input('''
성별이 어떻게 되십니까?
1. 남자
2. 여자
''')
height = input("신장을 입력해주세요 : ")
weight = input("체중을 입력해주세요 : ")
age = input("나이를 입력해주세요 : ")

# 숫자로 변환
height = int(height)
weight = int(weight)

# BMI 계산
BMI = weight / (height * height / 10000)

# 결과 출력
print("당신의 BMI 수치는 {0}입니다.".format(BMI))

print('''
괜찮아요...
눈에 보이는게
전부는 아니잖아요.''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}




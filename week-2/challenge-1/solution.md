---
description: Challenge 1의 모범 답안입니다.
---

# 모범 답안

## 비만도 계산기

{% code-tabs %}
{% code-tabs-item title="calculators/obesity\_calculator.py" %}
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
print("당신의 BMI 수치는 {0}입니다.\n".format(BMI))

# 결과 출력
if BMI < 18.5:
    print("저체중이십니다. 살 좀 찌셔야겠어요.")
elif BMI < 23:
    print("정상이십니다.")
elif BMI < 25:
    print("과체중이십니다. 살을 조금만 빼시면 좋겠어요.")
elif BMI < 30:
    print("비만이세요. 꼭 살을 빼세요!")
elif BMI < 35:
    print("중등도 비만이십니다. 2단계 비만입니다. 약간 위험해요!")
else:
    print("고도비만이십니다. 건강이 위험해요! 꼭 살을 빼세요!")

print('''
괜찮아요...
눈에 보이는게
전부는 아니잖아요.''')
```
{% endcode-tabs-item %}
{% endcode-tabs %}


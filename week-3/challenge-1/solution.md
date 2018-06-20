---
description: challenge 1의 모범 답안입니다.
---

# 모범 답안

## 중복 허용되는 로또 번호 발생기

{% code-tabs %}
{% code-tabs-item title="life/lotto\_numbers\_creator.py" %}
```python
import random

print("로또 번호 생성기 프로그램입니다!")

lotto_numbers = list()

lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))
lotto_numbers.append(random.randrange(1, 46))

print('''
랜덤 로또 발생기 입니다. (중복이 가능합니다)
당첨 번호 : {0}, {1}, {2}, {3}, {4}, {5}
2등 보너스 볼 : {6}
'''.format(lotto_numbers[0],
           lotto_numbers[1],
           lotto_numbers[2],
           lotto_numbers[3],
           lotto_numbers[4],
           lotto_numbers[5],
           lotto_numbers[6]))
```
{% endcode-tabs-item %}
{% endcode-tabs %}


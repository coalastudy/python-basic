---
description: Challenge 2의 모범 답안입니다.
---

# 모범 답안

## practice\_xlsxwriter.py

{% code-tabs %}
{% code-tabs-item title="practice\_xlsxwirter.py" %}
```python
import xlsxwriter

workbook = xlsxwriter.Workbook('hello.xlsx')
worksheet = workbook.add_worksheet()

for value in range(1, 101):
    worksheet.write('A'+str(value), value)

workbook.close()
```
{% endcode-tabs-item %}
{% endcode-tabs %}


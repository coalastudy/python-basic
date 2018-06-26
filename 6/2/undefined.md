---
description: 자율과제 2의 모범 답안입니다.
---

# 모범 답안

## practice\_xlsxwriter.py

{% code-tabs %}
{% code-tabs-item title="practice\_xlsxwriter.py" %}
```python
import xlsxwriter

workbook = xlsxwriter.Workbook('hello.xlsx')
worksheet = workbook.add_worksheet()

for value in range(1, 51):
    worksheet.write('A'+str(value), 'A'+str(value))
    worksheet.write('B'+str(value), 'B'+str(value))
    worksheet.write('C'+str(value), 'C'+str(value))
    worksheet.write('D'+str(value), 'D'+str(value))

workbook.close()
```
{% endcode-tabs-item %}
{% endcode-tabs %}


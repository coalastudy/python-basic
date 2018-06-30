---
description: xlsxwriter 패키지를 설치해보고 튜토리얼을 해봅니다.
---

# Stage 4 - 엑셀 관련 패키지 사용하기

## xlsxwriter 패키지 

엑셀 문서를 파이썬으로 작업할 수 있도록 도와주는 패키지입니. 문서를 참고해서 여러분이 더 심화작업도 해보면 재밌을 꺼에요!

![hello.xlsx](../.gitbook/assets/image%20%2825%29.png)

## 터미널이란

### 터미널은 무엇인가 

컴퓨터 관련 영화나 개발자들을 생각하면 검은 화면에 일반 사람들이 알 수 없는 말들을 막 치는 것이 상상이 됩니다. 바로 그 검은화면! 그곳이 터미널입니다! \(물론 색을 바꿀 수 있습니다.\)

터미널은 사람이 컴퓨터와 직접적으로 의사소통 할 수 있도록 만든 창구 역할을 합니다. 앞서 배운 pip를 사용하려면 터미널에서 사용해야 합니다. pip를 통해 직접적으로 컴퓨터에 파이썬 패키지를 설치하기 때문입니다.

![&#xD130;&#xBBF8;&#xB110; &#xBAA8;&#xC2B5;](../.gitbook/assets/image%20%2873%29.png)

## xlsxwriter 패키지 튜토리얼 

### xlsxwriter 패키지 다운로드 

터미널에서 xlsxwriter 패키지를 설치할 것 입니다. 파이참에서는 터미널 기능을 제공합니다.

파이참에서 터미널을 실행합니다.

![](../.gitbook/assets/image%20%2836%29.png)

터미널에서 xlsxwriter 패키지를 설치합니다.

![xlsxwriter &#xD328;&#xD0A4;&#xC9C0; &#xC124;&#xCE58;](../.gitbook/assets/image%20%28120%29.png)

### 코드 작성 및 실행 

practice\_xlsxwriter.py 파일을 만들어 아래의 코드를 복사하여 붙여넣고 실행합니다.

{% code-tabs %}
{% code-tabs-item title="practice\_xlsxwriter.py" %}
```python
import xlsxwriter

workbook = xlsxwriter.Workbook('hello.xlsx')
worksheet = workbook.add_worksheet()

worksheet.write('A1', 'Hello world')

workbook.close()
```
{% endcode-tabs-item %}
{% endcode-tabs %}


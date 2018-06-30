---
description: Challenge 2의 모범 답안입니다.
---

# 모범 답안

## 주민번호 분석기

{% code-tabs %}
{% code-tabs-item title="life/resident\_numbers\_analyzer.py" %}
```python
print("주민등록번호 분석기 프로그램입니다!")

resident_number = input("주민번호를 입력해주세요 : ")

# 생년 월일 탐색
birth_year = resident_number[0:2]
birth_month = resident_number[2:4]
birth_day = resident_number[4:6]

# 성별 탐색
if resident_number[6] == '1' or resident_number[6] == '3':
    sex = '남자'
elif resident_number[6] == '2' or resident_number[6] == '4':
    sex = '여자'
else:
    sex = '중성'

# 지역 탐색
local_code = resident_number[7:9]
local_code = int(local_code)

if 0 <= local_code <= 8:
    local = '서울특별시'
elif 9 <= local_code <= 12:
    local = '부산광역시'
elif 13 <= local_code <= 15:
    local = '인천광역시'
elif 16 <= local_code <= 25:
    local = '경기도'
elif 26 <= local_code <= 34:
    local = '강원도'
elif 35 <= local_code <= 39:
    local = '충청북도'
elif local_code == 40:
    local = '대전광역시'
elif 41 <= local_code <= 43 or 45 <= local_code <= 47:
    local = '충청남도'
elif local_code == 44 or local_code == 96:
    local = '세종특별자치시'
elif 48 <= local_code <= 54:
    local = '전라북도'
elif 57 <= local_code <= 66:
    local = '전라남도'
elif 55 <= local_code <= 56:
    local = '광주광역시'
elif 67 <= local_code <= 70:
    local = '대구광역시'
elif 71 <= local_code <= 81:
    local = '경상북도'
elif 82 <= local_code <= 84 or 86 <= local_code <= 90:
    local = '경상남도'
elif local_code == 85:
    local = '울산광역시'
else:
    local = '제주특별자치도'

# 주민번호로부터 정보 출력
print("\n생년월일 : " + birth_year + "년 " + birth_month + "월 " + birth_day + "일")
print("성별 : " + sex)
print("출생지역 : " + local)
```
{% endcode-tabs-item %}
{% endcode-tabs %}


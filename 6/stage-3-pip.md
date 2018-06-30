---
description: 모듈과 패키지의 개념에 대해 배웠습니다. 이제는 훌륭한 개발자들이 만들어놓은 모듈과 패키지를 함께 공유하고 사용하는 흐름에 대해 배워봅니다.
---

# Stage 3 - pip에 대하여

## pip install...

위대한 프로그램들은 한 사람이 다 만들 수 있을까요? 절대 그럴 수 없습니다. 여러분이 많이 사용하시는 유투브도 일부는 파이썬을 제작되었습니다. 여러분도 잘 아시겠지만, 유투브를 관리하는 사람이 한 명일까요? 아니죠. 구글이라는 엄청 큰 회사죠. 위대한 프로그램을 만들려면 다른 사람들이 내가 쓴 프로그램을 잘 사용할 수 있도록, 다른 사람이 만든 프로그램을 내가 잘 사용하는 것이 중요합니다. pip란 것을 이해하고, 다른 사람들이 만들어 놓은 것을 가져와 사용해봅시다.

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip install turtle
>>> pip install django
>>> pip install xlsxwriter
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## 오픈소스 

### 오픈소스란 무엇인가 

코딩에 관심이 많으신 분들이라면 오픈소스라는 단어는 한번쯤 들어보셨을 것 입니다. 오픈소스는 우리가 이전에 만들었던 프로그램의 원시 코드를 누구나 열람할 수 있도록 오픈하여 누구나 사용할 수 있도록 한 것 입니다. 대표적인 오픈소스 사이트로는 GitHub가 있습니다.

## PyPI란

### PyPI란 무엇인가 

Python Package Index의 줄임말로 파이썬으로 만든 패키지들을 관리하고 열람할 수 있는 저장소입니다. Index는 우리가 이전에 문자열과 리스트를 다루면서 들어보셨습니다. PyPI는 파이썬 패키지에 Index를 붙여 관리하는 모습을 상상하시면 됩니다. 

앱스토어를 다들 이용해보셨죠? 스마트폰에서 앱을 설치하려면 앱스토어에서 개발자들이 올린 앱을 다운받습니다. PyPI는 앱스토어와 같은 역할을 한다고 생각하시면 훨씬 이해하는데 도움이 되실 것 같습니다.

![PyPI&#xC758; &#xBAA8;&#xC2B5;](../.gitbook/assets/image%20%28112%29.png)

## pip란

### pip란 무엇인가

파이썬으로 작성된 패키지를 설치하고 관리해주는 역할을 합니다. 앱스토어에서는 스토어에 들어가서 다운받기 버튼을 누르면 스마트폰에 앱이 설치됩니다. 이와 같은 역할을 해주는 것이 pip 입니다. pip를 통해 PyPI에서 우리가 원하는 패키지를 가져와 사용해야 합니다.

pip는 파이썬 3를 설치하면 동시에 함께 설치되기 때문에 설치하는 문제는 걱정하지 않아도 된다. 이것은 마치 스마트폰을 사면 앱스토어가 설치되어 있는 것과 유사하다.

### pip 사용법

PyPI로 부터 패키지를 설치, 삭제, 버전관리, 목록을 조회하는 방법을 알아봅니다.

#### 패키지 설치 

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip install 패키지 이름 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 패키지 삭제 

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip uninstall 패키지 이름 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 특정 버전 설치 

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip install 패키지 이름 == 1.0.0
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 패키지 버전 업그레이드 

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip install --upgrade 패키지 이름 
```
{% endcode-tabs-item %}
{% endcode-tabs %}

#### 설치한 패키지 조회 

{% code-tabs %}
{% code-tabs-item title="example" %}
```bash
>>> pip list 
```
{% endcode-tabs-item %}
{% endcode-tabs %}




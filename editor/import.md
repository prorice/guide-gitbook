# 콘텐츠 참조 {#콘텐츠-참조}

콘텐츠 참조\(conref\)는 다른 파일이나 책들에서 콘텐츠를 재사용하기 편리한 메커니즘이다.

## 현재 책의 다른 파일에 있는 컨텐츠 참조 {#현재-책의-다른-파일에-있는-컨텐츠-참조}

다른 파일에 있는 콘텐츠를`include`테그를 이용하여 정말 쉽게 참조할 수 있다.

```
{% include "./test.md %}

```

## 다른 책의 파일에 있는 컨텐츠 참조 {#다른-책의-파일에-있는-컨텐츠-참조}

깃북은 또한 git테그를 사용하여 다른 책의 파일에 있는 컨텐츠를 참조할 수 있다.

```
{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}

```

git url의 형태는 다음과 같다.

```
git+https://user@hostname/project/blah.git/file#commit-ish

```

실제 git url은 반드시`.git`로 끝나야 한다. 그리고 가져올 파일이름은`.git`뒤에 나와야 한다.

`commit-ish`및 어떠한 테그, sha, 또는 브랜치를 지정할 수 있다.`git checkout`인자값으로. 그리고 기본은`master`이다.

## 상속 {#상속}

템플릿 상속은 재사용 탬플릿을 쉽게 만드는 방법이다. 템플릿을 쓸 때 너는 "blocks"를 정의 할 수 있고, 자식 탬플릿은 이것을 오버라이드 할 수 있다. 상속은 원하는 만큼 가능하다.

`block`은 템플릿의 구역과 식별자를 정의한다. 식별자는 이름이다. 부모 템플릿은 특수한 블록들이다. 그리고 자식 템플릿들은 새로운 컨탠츠로 오버라이드 할 수 있다.

```
{% extends "./mypage.me" %}

{% block pageContent %}
# 이것은 내 페이지 콘텐츠이다
{% endblock %}

```

`mypage.md`파일에는 반드시 블록을 정의해야 한다.

```
{% block pageContent %}
이것은 기본 콘텐츠이다
{% endblock %}

# License

{% import "./LICENSE" %}
```




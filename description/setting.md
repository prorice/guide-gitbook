# 설정 {#설정}

모든 설정들은`book.json`에 저장된다.

[jsonlint.com](http://jsonlint.com/)에서 문법을 검사한 뒤 너의`book.json`에 붙여넣기 할 수 있다.

모든 필드는 일부 추출된 값으로 옵션이거나 기본이다.

## 필드 {#필드}

### gitbook {#gitbook}

```
{ "gitbook": "2.x.x" }

```

이 옵션은 깃북의 버전을 찾는데 사용된다. 이것은 책을 생성하는데 사용된다. 이 형태는[시멘틱](http://semver.org/)조건을 따른다.

### 제목 {#제목}

```
{ "title": "내 놀라운 책" }

```

이 옵션은 책의 제목을 정의한다. 기본값은 README 첫 번째 제목을 따른다.

**gitbook.com**의 이 값은 플렛폼에 입력 타이틀에서 정의된다.

> 역주
>
> `book.json`을 수정하는 것 보다[https://www.gitbook.com/book/\[아이디\]/\[책이름\]/details](https://www.gitbook.com/book/[%EC%95%84%EC%9D%B4%EB%94%94]/[%EC%B1%85%EC%9D%B4%EB%A6%84]/details)
>
> 페이지의 setting 에 들어가서 설정하는 것이 더 확실히 반영됩니다.

### 설명 {#설명}

```
{ "discription": "이 책은 좋은 책이다!" }

```

이 옵션은 책에대한 설명을 정의한다. 기본 값은 README의 첫 번째 절을 따른다.

**gitbook.com**의 이 값은 설정된 내용에 따르거나 특정 언어에서 정의된다.

### 방향 {#방향}

```
{ "direction": "rtl" }

```

이 옵션은 언어의 출력방향을 변경할 때 사용된다. 이것은`language`의 언어에 따라 올바른 텍스트 방향으로 설정하는것을 권장한다.

### 스타일 {#스타일}

이 옵션은 커스텀 css를 책에서 사용할 때 쓰인다.

예:

```
{
    "styles": {
        "website": "styles/website.css",
        "ebook": "styles/ebook.css",
        "pdf": "styles/pdf.css",
        "mobi": "styles/mobi.css",
        "epub": "styles/epub.css"
    }
}

```

### 플러그인 {#플러그인}

```
{ "plugins": ["mathjax"] }

```

책에서 쓰이는 플러그인 리스트의 시작은 'book.json' 설정에 정의된다.

### 플러그인 설정 {#플러그인-설정}

```
{
    "plugins": ["myplugin"],
    "pluginsConfig": {
        "myPlugin": {
            "message": "Hello World"
        }
    }
}

```

이 옵션은 모든 플러그인들의 설정들을 포함한다.

### 구조 {#구조}

이 옵션은 GitBook의 파일경로를 덮는데 사용된다.

예를들어 만역`INTRO.md`파일을`README.md`대신 사용하길 원한다면

```
{
    "structure": {
        "readme": "INTRO.md"
    }
}

```

구조 타입은`readme`,`langs`,`summary`,`glossary`이다.

### 변수 {#변수}

```
{
    "variables": {
        "myTest": "Hello World"
    }
}

```

변수에 대한 자세한 정보는[템플릿](https://bluekms21.gitbooks.io/gitbookhelp_kr/content/1.9.%20%ED%85%9C%ED%94%8C%EB%A6%BF.md)을 참조하라.


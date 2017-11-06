# 플러그인 {#플러그인}

플러그인은 GitBook이나 ebook 그리고 웹 사이트의 기능을 포함하는 최고의 방법이다. 플러그인들은 그 종류도 다양하다. 수학함수 출력이나 Google Analytic과 같은...

## 플러그인 찾는 방법 {#플러그인-찾는-방법}

플러그인은[plugins.gitbook.com](https://bluekms21.gitbooks.io/gitbookhelp_kr/content/plugins.gitbook.com)에서 쉽게 찾을 수 있다.

## 플러그인 인스톨 방법 {#플러그인-인스톨-방법}

플러그인을 추가하고 싶다면`book.json`에 다음과 같이 쓰면 된다.

```
{
    "plugins": ["myPlugin", "anotherPlugin"]
}
```

너는 또한 특정한 버전을 지정하여 사용할 수도 있다.`myPlugin@0.3.1`이것은 구 버전 Gitbook등을 사용할 때 유용하다.

만약 책을 로컬에서 빌드하고 싶다면 다운로드 하고 플러그인을 준비하여`gitbook install`하는것으로 간단하게 할 수 있다.


# 챕터와 서브챕터 {#챕터와-서브챕터}

GitBook은 SUMMARY.md 파일을 사용하여 책에 쓰일 챕터와 서브챕터를 정의할 수 있다.

SUMMARY.md 파일은 일반적으로 책의 컨텐츠 테이블을 만드는데 사용된다.

SUMMARY.md 의 포멧은 간단한 링크들의 목록이다.  
링크의 이름은 챕터 이름으로 사용된다. 그리고 타겟은 챕터파일의 경로이다.

서브챕터는 부모 챕터에 속한 리스트 형태로 간단히 정의할 수 있다.

## 간단한 예제 {#간단한-예제}

```
# Summary

* [Chapter 1](chapter1.md)
* [Chapter 2](chapter2.md)
* [Chapter 3](chapter3.md)
```

## 서브챕터 예제 {#서브챕터-예제}

```
# Summary

* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

# 역주 {#역주}

챕터와 서브챕터에는 넘버링을 하지 않아도 자동으로 넘버링 된다.

```
[제목](파일링크) 로 작성하면 된다.

* [형식](1. 형식.md)
  * [출력](1.1. 출력.md)
  * [Readme로 책 소개](1.2. Readme로 책 소개.md)

위와 같이 작성하면 실제 표시되는 챕터에는

1. 형식
  1.1. 출력
  1.2. Readme로 책 소개

로 표시된다.
```




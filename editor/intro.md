# Readme로 책 소개 {#readme로-책-소개}

네 책의 첫번째 페이지는 README.md 이다. 만약 요약 파일이 제공되지 않는다면 이 파일은 첫번째 엔트리로 추가된다.

# 다른 파일을 README.md로 사용하기 {#다른-파일을-readmemd로-사용하기}

깃허브에서 호스팅되는 일부 책들의 소개 페이지 대신 README.md를 유지하라.

깃허브 버전 2.0.0 이상부터 사용하던 README를`book.json`으로 정의하는것이 가능해졌다.

```
{
    "structure": {
        "readme": "myIntro.md"
    }
}
```




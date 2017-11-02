# 문서 내용 작성하기 {#문서-내용-작성하기}

## 작업할 문서 열고 Sync 하기 {#open}

이미 내 컴퓨터에 Clone을 통해 받아온 책은 Open 하기만 하면 작업이 가능합니다. GitBook Editor에서 \[GitBook Editor\]-\[Open...\] 메뉴를 이용해 작업할 책을 여십시오. 책이 있는 폴더를 선택하시면 됩니다.

![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/gitbook_open.png)

하지만,**문서를 열자 마자 GitBook Editor에서 \[Book\]-\[Sync\] 메뉴를 눌러주십시오.**지금 우리가 하는 작업은 혼자 하는 저술 활동이 아닌 공동작업이기에 Git을 이용한 분산개발에서 작업 시작 전에 Fetch, Pull을 해야 하듯이 자신의 작업을 시작하기 전에 원격저장소의 변경사항을 Sync 해 주어야 합니다. Sync 기능을 수행하면 Git의 Pull과 Push 기능이 한 동작으로 수행되어 원격저장소와 로컬을 동일하게 동기화 해 줍니다.

Sync 기능을 처음 수행하면 GitHub.com의 계정을 물어봅니다. 앞의 단계에서 GitHub의 Issue 기능을 통해 관리자에게 권한을 요청한 바로 그 계정 정보를 입력하시면 됩니다.

![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/github_login.png)

다시 한번 강조합니다. 문서를 열고나면 반드시 Sync 기능을 실행해 원격저장소의 변경사항을 받아 오십시오.

책을 작업하는 화면은 일반적인 문서편집기와 유사합니다. 문단양식, 강조, 그림삽입, 링크, 각주, 수식 등 간단한 편집을 지원하며 소스코드에 대한 강조 기능등도 있습니다. 하지만, 문단양식별로 표현을 변경하거나 글자의 색을바꾸는 기능은 지원하지 않습니다. 이런 문서 표현에 관한 것들은 조판\(Publish\)시에 결정되게 됩니다. 이럴게 컨텐츠 작성과 표현이 분리됨으로 하나의 소스로 HTML, PDF, ePub 등 다양한 형태의 출판물을 만들 수 있다는 장점이 있습니다.![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/open_book.png)

## 새 챕터 만들기 {#newchaptor}

공동 작업시의 충돌을 줄이기 위해 각 저자는 작성 내용을 별도의 챕터\(Article\)로 분리하여 작업해 주시기를 부탁드립니다. 작성 원하는 챕터를 \[Add an article\] 기능을 이용해 만들어 줍니다. 물론 이미 챕터를 만드셨다면 단순히 GitBookEditor의 왼쪽 TOC에서 해당 챕터를 글릭하시기만 하시면 열리게 됩니다.

새 챕터를 만들때 중요한 주의사항이 있습니다. 챕터의 이름을 처음에는 반드시 영문과 언더바를 이용해 가능한 짧으면서도 의미가 통하게 만들어 주십시오. 이 챕터 이름이 md 파일의 이름이 되기 때문에 그렇습니다. 만일 챕터를 만들때의 이름으로 한글을 쓰게 되면 한글은 모두 무시되 '.md'라는 .으로 시작하는 파일이 생성되어 숨겨진 파일로 간주되어 편집작업을 할 수 없게 되는 문제가 생깁니다. 또 문서들간의 링크 생성시 이 md 파일의 이름이 사용되므로 지나치게 길거나 공백이 있으면 문제가 발생할 수 있습니다.

새 챕터를 만들때의 표준 작업방식은 다음과 같습니다.

1. \[+Add an article\] 버튼을 눌러 챕터 추가를 시작합니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/add_article.png)

2. 가능한 한 짧은 영문으로 Title을 입력합니다. 저는 '추가정보' 라는 챕터를 위해 'more\_info'라고 했습니다. \[Add\]를 누르면 실제로 파일이 생깁니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/article_title.png)

3. 영문으로 생성된 챕터명의 오른쪽에 가면 연필모양 편집버튼이 생깁니다. 이를 눌러 챕터명을 한글로 수정합니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/chapter_rename.png)

4. 문서 편집기 부분으로 가서 제일 상단에 챕터명을 적고 이를 Heading1 문단형식으로 바꿉니다. 툴바 혹은 단축키 &lt;Shft-Ctl-1&gt;을 이용하면 됩니다. 그 아래에는 저자명을 적어 줍니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/chptor_h1.png)

5. FILES 탭에 가보면 more\_info.md 파일이 생긴 것을 확인할 수 있습니다. 이제 내가 작성하는 내용은 이 파일에 기록될 것입니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/article_files.png)

6. 챕터를 만들었으면 즉시 \[Save\]와 \[Sync\] 버튼을 눌러 저장하고 원격저장소에 올려주십시오. 파일의 리스트는 SUMMARY.md 파일에 저장되는데 이 파일이 충돌이 가장 많이 발생하므로 새 챕터 생성 즉시 원격저장소에까지 올려주셔야 공동작업시의 충돌을 줄일 수 있습니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/chaptor_save_sync.png)

다시 한번 강조합니다. 새 챕터를 만드실 때는 우선 간단한 영문으로 이름을 만드시고, 한글로 변경하십시오. 또한 새 챕터 생성을 하시자마자 저장과 씽크를 해 주십시오.

## 내용 작성하기 {#write}

자신이 작성하는 챕터의 내용을 작성하고 저자가 작성의 작은 단위가 끝났다 판단할 때 \[Save\] 합니다. GitBook에서의 Save는 Git의 Commit과 의미가 거의 유사합니다. Commit시의 메시지는 기본적으로 자동 생성되고 실제로 Git의 이력으로 모두 남아 복구나 브랜치 병합 등이 모두 가능합니다.

이렇게 Save가 Commit의 의미를 가지기 때문에 의미있는 한 단락의 작성이 끝나면 \[Save\]를 눌러 Commit을 생성해 주시는 것이 좋습니다. 또한 가능한 한 여러 파일에 걸친 변경후에 저장하는 일을 지양해 주십시요. Commit의 단위가 불명확해져 복구 등의 작업에 어려움이 있을 수 있습니다.

### 챕터별 제목과 하부 문단 지정 {#챕터별-제목과-하부-문단-지정}

각 챕터의 첫 줄은 챕터의 제목을 써주시고 이를 Hedaing 1 스타일로 지정해 주십시요. 툴바의 문단형식 버튼을 이용해도 되지만, &lt; Shift-Ctrl-1&gt; 키를 누르는 것이 더 빠릅니다.

![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/paragraph-style.png)

두번째 줄에는 각 챕터를 맏은 분의 이름을 기록해 주시길 부탁드립니다. 각 챕터는 작성자의 실명\(혹은 별명\)을 확히 밝혀 출판될 예졍입니다.

챕터 내에 새부적인 장절이 필요한 경우 Heading 2, 3, 4등을 사용하여 제목을 세부 제목을 적어주시면 됩니다. 이 때 각 장절의 번호는 적지 않는 것을 원칙으로 합니다. 장절의 번호는 추후 편집시 만들 예정입니다.

실제 내용을 작성시에는 Paragraph를 선택하시면 됩니다. 즉 문서 양식이 없는 상태로 작성해주시면 나중에 일괄적으로 양식을 잡을 것입니다. 실제 작성예는 다음과 같습니다.

![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/paragraph.png)

### 그림 삽입하기 {#그림-삽입하기}

그림은 잘 쓴 글 이상으로 내용을 잘 설명하는 도구입니다. GitBook에서는 다양한 방법으로 그림을 삽입할 수 있고, 그 기능이 매위 뛰어납니다.

제가 가장 많이 사용하는 방법은 원하는 그림을 캡처 툴로 캡처하거 웹 페이지에서 복사하여 GitBook Editor에서 붙여넣기 하는 방법입니다. 일반적으로 하듯이 그림 &lt;Ctl-C&gt;, &lt;Ctl-V&gt;하시면 되는 것입니다. 그러면 그림이 실제 파일로 자동으로 만들어 집니다.

그림을 붙여넣기 하면 자동으로 'Create New Image' 창이 열리고, 파일의 이름을 지정할 수 있습니다. 이 이름을 기존 파일의 이름과 겹치면 저장이 안됩니다. 파일이름은 가능한 한 영문으로 의미있는 이름을 부여해 주시길 부탁드립니다. 또한 그림이 저장되는 폴더는 기본적으로 assets 폴더이지만 사용자가 설정할 수도 있습니다.

![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/import_image.png)

이 뿐 아니라 PC에 있는 파일이나 인터넷상의 URL을 이용해 그림을 삽입하실 수 있습니다. 이 기능은 툴바의 그림모양 아이콘인 Insert Image 버튼을 이용하면 됩니다.

### 링크 삽입하기 {#링크-삽입하기}

하이퍼링크도 전자문서에서 매우 중요한 요소입니다. 다른 챕터에서 상세한 내용을 설명하거나 참조가 필요한 URL이 있는 경우 이를 링크로 만들어 줍니다.

링크는 툴바의 \[Insert Iink\] 버튼으로 만들 수 있습니다. GitBook Editor에서 링크를 걸기를 원하는 텍스트를 선택하고 Insert Link 버튼을 눌러 나오는 창에서 링크 주소를 입력해 간단히 만들어 줄 수 있습니다.

만약 링크 하려는 주소가 인터넷 URL이 아니라 GtiBook 내의 각 챕터별 파일이나 챕터 내의 세부 장절이라도 링크가 가능합니다. 예를 들어 '구체적인 문서 작성법'이라는 문장에 본 탭터인 '문서내용 작성하기'의 '내용 작성하기' 절에 링크하고 싶다면, 다음과 같이 하시면 됩니다.

1. 먼저 '문서 내용 작성하기' 챕터의 '내용 작성하기'하는 절 제목에 무우스를 가져가면 줄의 오른쪽에 엥커를 만들수 잇는 핀 버튼이 생깁니다. 이 버튼을 눌러 앵커의 명칭을 입력해 주세요.
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/create_anchor.png)
2. '구체적인 문서 작성법' 이라는 부분을 선택하고 \[Insert Link\] 버튼을 누른 후
3. 챕터의 제목을 입력하면 유사한 챕터가 나오면 해당 문서를 선택합니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/create_link1.png)

4. 문서 내 절까지 링크를 지정하기 위해서는 다시 챕터 제목을 선택하시면, 챕터 제목이 실제 파일명으로 변하고, 이 파일명 뒤에 \#과 앵커 명을 입력하시면 됩니다.  
   ![](https://jangbi882.gitbooks.io/gitbook-guide/content/assets/create_link2.png)

5. 이제 해당 링크를 누르면 링크된 챕터의 절로 이동합니다.

## 공동작업자를 위해 Sync 하기 {#sync}

하루의 작업을 끝낼 때, 혹은 그보다 더 자주 \[Sync\] 기능을 이용해 GitHub의 저장소에 올려 공동 작업자들이 받을 수 있게 합니다. 주의 할 것이 GitBook은 충돌 발생시 기본적으로 가장 마지막에 저장한 내용으로 덮어 써 충돌을 복구한는으로 것으로 보입니다\(확실치는 않고 추가 확인 필요\). 때문에 가능한 한 저자별로 작업하는 챕터\(article\)을 분리하여 작업하는 것이 바람직 합니다.

그러니, 가능한 한 자주 Sync 버튼을 눌러 공동 저장소와 동기화 새 주십시오. 그리고, 하루 작업을 마치실 때는 반드시 Sync 해 주십시오.

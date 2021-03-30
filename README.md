# 20182651 컴퓨터학부 전종원

## ***Table***
      | Header      | Title       |
      | ----------- | ----------- |
      | Syntax      | Description |
  -> 위 예시의 결과는 다음과 같다.
| Header      | Title       |
| ----------- | ----------- |
| Syntax      | Description | 
  
-> 세 개 이상의 하이픈(---)을 사용하여 각 열의 헤더를 만들고 파이프(|)를 사용하여 각 열을 구분하여 표를 추가할 수 있다.

-> 한 열의 셀 길이가 일치 할 필요는 없다.
   
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

-> 콜론(:)을 하이픈의 왼쪽, 오른쪽 또는 양쪽에 추가하면 열의 텍스트를 왼쪽, 오른쪽 또는 가운데로 정렬할 수 있다.

  | f\|oo  |
  | ------ |
  | b `\|` az |
  | b **\|** im |

-> 이스케이프 처리를 통해 셀의 컨텐츠에 파이프를 포함할 수 있다.
  
  | abc | def |
  | --- | --- |
  | bar | baz |
  > bar
  
-> 테이블은 빈 줄이나 다른 블록 구조의 시작에서 나뉘게 된다. 
   
      | abc | def | 
      | --- |
      | bar |
    
-> 헤더 행은 셀 수의 구분 기호 행과 일치해야한다. 그렇지 않으면 테이블로 인식되지 않는다.

  | abc | def |
  | --- | --- |
  | bar |
  | bar | baz | boo |

-> 그러나 테이블 행의 나머지 부분은 헤더 행의 셀 수보다 적은 수의 셀이 있으면 자동으로 부족한 곳에 빈 셀이 삽입된다. 반대로 헤더 행보다 클 경우 무시된다. 

| abc | def |
| --- | --- |

-> 테이블 본문에 행이 없으면 헤더행만 존재하는 테이블이 생성된다.

## Strikethrough
```
~~The world is flat.~~ We now know that the world is round.
```
-> 위 예시의 결과는 다음과 같다.

~~The world is flat.~~ We now know that the world is round.

-> 위와 같이 단어 앞 뒤에 물결표 두개를 사용하면 취소 선을 그릴 수 있다.

    Hello. My ~~Name

    is~~

-> 위의 예시와 같이 새 단락과는 취소 선을 이을 수 없다.
## Task List items
```
- [x] pragraph1
- [ ] pragraph2
- [ ] pragraph3
```
-> 위 예시의 결과는 다음과 같다.
- [x] pragraph1
- [ ] pragraph2
- [ ] pragraph3

-> 대시(-) + 공백 + 대괄호([])를 추가하면 확인란이 있는 항목 목록을 만들 수 있다.

-> 이 때 대괄호 안에 X 기호를 추가하여 확인란을 선택한다. 

- [x] pragraph1
- [ ] pragraph2
  - [ ] pragraph3
  - [ ] pragraph4
- [ ] pragraph5
` 
- [x] pragraph1
- [ ] pragraph2
  - [ ] pragraph3
  - [ ] pragraph4
- [ ] pragraph5 `

-> 이처럼 항목 목록을 중첩하여 사용할 수 있다.

## Automatic URL Linking
`www.naver.com`을 입력하면
www.naver.com
이와 같은 결과를 얻을 수 있다.
-> 이처럼 대부분의 마크다운 프로세서는 자동으로 URL을 링크로 변환한다.

-> www. 다음에 유효한 도메인이 있을 시에 http가 자동으로 삽입된다.

-> 이메일 주소가 텍스트 노드 내에서 인식 될 때 이메일을 자동 링크로 변환한다.


## Disallowed Raw HTML
    <title>
    <textarea>
    <style>
    <xmp>
    <iframe>
    <noembed>
    <noframes>
    <script>
    <plaintext>
    
  -> GFM은 태그필터 HTML 출력을 렌더링 할 때 위에 기재된 HTML 태그 필터링을 활성화한다.
  
  -> 다른 모든 HTML 태그는 허용된다.

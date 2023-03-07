# 3_7

html : 구조(레이아웃) / CSS : 표현(스타일링) / JS : 동작(인터렉션)

### HTML

: hyper text markup language

- Hyper Text
  
  - 참조(하이퍼링크)를 통해 사용자가 한 문서에서 다른 문서로 즉시 접근할 수 있는 텍스트

- Markup Language
  
  - 태그 등을 이용하여 문서나 데이터의 구조를 명시하는 언어
    
    - 대표적인 예 - HTML, Markdown

- 즉, 웹 페이지를 작성(구조화)하기 위한 언어

- # MDN, W3Schools에서 정보찾기

### HTML 기본 구조

- html : 문서의 최상위(root) 요소

- head : 문서 메타데이터 요소
  
  - 문서 제목, 인코딩, 스타일, 외부 파일 로딩 등
  
  - 일반적으로 브라우저에 나타나지 않는 내용
  
  - example)
    
    - <title> : 브라우저 상단 타이틀
    
    - <link> : 외부 리소스 연결 요소 (CSS 파일 등)
    
    - <style> : CSS 직접 작성
    
    ![](assets/2023-03-07-09-20-53-image.png)

- body : 문서 본문 요소
  
  - 실제 화면 구성과 관련된 내용

- 요소(element)
  
  - `<h1>` contents `</h1>`
  
  - HTML의 요소는 태그와 내용(contents)으로 구성되어 있다.
  
  - 열었으면 닫아야하며 모든 내용은 태그로 감싸져 있어야 한다.
  
  - HTML 요소는 시작 태그와 종료 태그 그리고 태그 사이에 위치한 내용으로 구성
    
    - 태그(element, 요소)는 컨텐츠(내용)를 감싸는 것으로 그 정보의 성격과 의미를 정의
  
  - 내용이 없는 태그들
    
    - br, hr, img, input, link, meta
  
  - 요소는 중첩(nestsed)될 수 있음
    
    - 요소의 중첩을 통해 하나의 문서를 구조화
    
    - 여는 태그와 닫는 태그의 쌍을 잘 확인해야함
      
      - 오류를 반환하는 것이 아닌 그냥 레이아웃이 깨진 상태로 출력되기 때문에, 디버깅이 힘들어 질 수 있음.

- 속성(attribute)
  
  - `<a href(속성명) = "https://google.com"(속성값)></a>`
  
  - 각 태그별로 사용할 수 있는 속성이 다르다.
  
  - 속성은 속성명과 속성값으로 이루어져 있다.
  
  - 속성을 작성할 때 공백은 없어야하며 `""`만을 이용한다.
  
  - 속성을 통해 태그의 부가적인 정보를 설정할 수 있음
  
  - 요소는 속성을 가질 수 있으며, 경로나 크기와 같은 추가적인 정보를 제공
  
  - 요소의 시작 태그에 작성하며 보통 이름과 값이 하나의 쌍으로 존재
  
  - 태그와 상관없이 사용 가능한 속성(HTML Global Attribute)들도 있음
  
  - ### HTML Global Attribute
    
    - 모든 HTML 요소가 공통으로 사용할 수 있는 대표적인 속성
      
      - (몇몇 요소에는 아무 효과가 없을 수 있음)
      
      - id : 문서 전체에서 유일한 고유 식별자 지정
      
      - class : 공백으로 구분된 해당 요소의 클래스의 목록 (CSS, JS에서 요소를 선택하거나 접근)
      
      - style : inline 스타일
      
      ![](assets/2023-03-07-09-29-22-image.png)

### HTML 텍스트 요소

![](assets/2023-03-07-09-51-39-image.png)

### HTML 그룹 컨텐츠

![](assets/2023-03-07-09-52-23-image.png)

- form
  
  - `<form>`은 사용자의 정보(데이터)를 제출하기 위한 영역

- input
  
  - 다양한 타입을 가지는 입력 데이터 유형과 위젯이 제공됨
  
  - `<input>` 대표적인 속성
  
  - 장고에서
  
  ![](assets/2023-03-07-10-06-52-image.png)

- input label
  
  - label을 클릭하여 input 자체의 초점을 맞추거나 활성화 시킬 수 있음
    
    - 사용자는 선택할 수 있는 영역이 늘어나 웹 / 모바일(터치) 환경에서 편하게 사용할 수 있음
    
    - label과 input 입력의 관계가 시각적 뿐만 아니라 화면리더기에서도 label을 읽어 쉽게 내용을 확인할 수 있도록 함
    
    ![](assets/2023-03-07-10-09-52-image.png)

### CSS

cascading style sheets

- 구문
  
  - h1 {
    
        color : blue; (선언(declaration))
        font-size : 15px; ( 속성 : 값 )
    
    }

- CSS 구문은 선택자를 통해 스타일을 지정할 HTML 요소를 선택

- 중괄호 안에서는 속성과 값, 하나의 쌍으로 이루어진 선언을 진행

- 각 쌍은 선택한 요소의 속성, 속성에 부여할 값을 의미.
  
  - 속성 (property) : 어떤 스타일 기능을 변경할지 결정
  
  - 값 (value) : 어떻게 스타일 기능을 변경할지 결정

- 정의 방법
  
  - 인라인(inline)
  
  - 내부 참조(embedding) - `<style>`
  
  - 외부 참조(link file) - 분리된 CSS 파일

- 선택자 정리
  
  - 요소 선택자
    
    - HTML 태그를 직접 선택
  
  - 클래스 선택자
    
    - 마침표(.)문자로 시작하며, 해당 클래스가 적용된 항목을 선택
  
  - 아이디 선택자
    
    - `#` 문자로 시작하며, 해당 아이디가 적용된 항목을 선택
    
    - 일반적으로 하나의 문서에 1번만 사용. 여러 번 사용해도 동작하지만, 단일 id를 사용하는 것을 권장

- 적용 우선순위
  
  - 중요도 - 사용시 주의
    
    - !important
  
  - 우선순위 (specificity)
    
    - inline > id > class, attribute > element
    
    - css파일에서 같은 순위가 있다면 아래에 있는 것이 나중에 적용됨

### CSS 상속

- CSS는 상속을 통해 부모 요소의 속성을 자식에게 상속한다.
  
  - 속성(property) 중에는 상속이 되는 것과 되지 않는 것들이 있다.
  
  - 상속되는 것 예시
    
    - ex) text 관련 요소(font, color, text-align), opacity, visibility 등
  
  - 상속되지 않는 것 예시
    
    - ex) Box model 관련 요소(width, height, margin, padding, border, box-sizing, display), position 관련 요소(position, top/right/bottom/left, z-index 등)

[[VSCode]유용한 단축키 모음](https://inpa.tistory.com/entry/VS-Code-%E2%8F%B1%EF%B8%8F-%EC%9C%A0%EC%9A%A9%ED%95%9C-%EB%8B%A8%EC%B6%95%ED%82%A4-%EC%A0%95%EB%A6%AC)

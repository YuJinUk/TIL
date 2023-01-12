# MarkDown

- 제목
  
  - '#', '##' h1/h2 => 모든 마크다운 문서의 기본 틀 / 골격

- list
  
  - 순서x => '*' or '-'
  
  - 순서o => 1,2,3
    
    - python
      
      - List
        
        - 연속된 인덱스를 가진 iterable한 자료구조
      
      - Tuple
      
      - dictionary

- code block
  
  - 문장 한 가운데 `print('abd')`
  
  - ```python
    abd = 11
    print(abd)
    ```

- url & image
  
  - "[string](google.com)"
  
  - ![string]()

- 테이플
  
  | 제목1 | 제목2 | 제목3 |
  | --- | --- | --- |
  | 1   | 2   | 3   |

## Git의 기초

> 분산 버전 관리 프로그램
> 
> > 중앙 집중식 관리가 아닌 서버 및 개발자 개인의 pc에서도 버전이 동시에 관리하여 리소스를 분산적으로 관리하는 것.

1. 백업

2. 복구

3. 협업
   
   ### Git 문법
   
   1. git 시작하기
      
      1. 초기화 : `git init` : git local repository 초기화
         
         1. local repository 생성 후 버전으로 관리할 파일을 `git add` 로 최소한 한번이라도 staging area로 옮겨줘야 한다.
            
            why? `git init` 을 실행하더라도 git은 어떤 파일의 버전을 관리해야하는지 모르기 때문
         
         2. 파일의 상태
            
            1. 최초 생성 시 : untracked
            
            2. git add 후 : staged
            
            3. git commit : tracked
            
            4. 파일의 수정이 있을 때 : modified
            
            5. 최신이면 : up-to-date
      
      2. `git add` 
         
         1. git add . : 현재 위치한 w.d(working directory)에 생긴 모든 변화 사항을 stage에 올림
         
         2. git add {file_name} : file을 지정해서 stage에 올림
      
      3. `git commit -m "commit message"`
         
         1. commit message는 해당 버전이 어떤 목적에서 생성되었는지 적는 용도
            
            1. 길이 제한 o
      
      **여기까지가 Local Repository의 일들**
      
      ___
      
      ### Remote Repository (원격 레포지토리 / 깃허브)
      
      - repository에 연결하기 : `git remote add origin URL`
      
      - `git push origin master` : local > remote로 upload
        
        - 인증 (본인 확인)
      
      - add > commit > push 순으로 진행해야만 한다.

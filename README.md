# blog 만들기
 
## 1. 어떻게 만들까?
  - 사용 요구 조건
    - 글 포스팅
    - 글 카테고리
    - 카테고리를 트리 구조로 정리
    
  - 기술 조건 파악
    - 다양한 테마를 이용할 수 있어야 함.
    - 커스터마이징 할 여지가 있어야 함.
    - 만들기 쉬워야 함. 

## 2. 다양한 시도(삽질)
### 2-1. Jekyll 테마를 그대로 가져와서 활용.
 - 문제점
   - 제일 많이 쓰는 테마를 골랐다.
   - 내 저장소에 config.yml 과 index.html을 만들고 테마를 가져오는 방식을 택했다.
   - 안 예쁘다
   - 안 예쁜데 어떻게 고쳐야 할지 모르겠다. -> 커스터마이징을 한번쯤 꼭 하겠구나라고 생각...
   - 직접 코드를 만져서 테마를 고르는 과정을 거치자 -> ruby 는 초반 진입장벽이 높단다.
   - 검색 결과, 그나마 헬로월드도 찍어본 go language를 이용하는 Hugo를 사용하자.

### 2-2. hugo를 설치해보자
 - 과정
  - chocolately를 사용해서 설치 -> cmd 창에서 간편하게 사용할 수 있지만, 어떤건지는 자세하게 모른다.
  - go langauge 설치
  * test 소스(헬로 월드)를 만들고 go build 로 build 해서 실행시켜보자

## 3. hugo 를 사용해서 블로그를 만들어보자!
### 3-1. github 저장소를 두개 생성한다.
 - 소스 파일이 담길 저장소를 생성
 - 렌더링 된 결과물이 담길 페이지를 생성
 
### 3-2. local 저장소 생성, github 저장소와 연동
 - 소스 파일의 local 저장소를 hugo 명령을 통해 생성.
 - 소스 파일의 local 저장소의 remote 저장소로 github 저장소(blog)를 등록
  $ git remote add origin git@github.com:gringrape/blog.git
 - 렌더링 된 결과물의 local 저장소를 submodule 로 설정해서 remote 저장소와 연동
  $ git submodule add -b masater git@github.com:integerous/integerous.github.io.git public

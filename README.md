# JPA

## 실습 환경 구축

문서를 참조하여 실습 환경을 구축한다.

### 1단계 - 엔티티 매핑

1. 요구 사항
    - [x] 제시된 DDL(Data Definition Language)을 보고 유추하여 엔티티 클래스와 리포지토리 클래스 작성
    - [x] `@DataJpaTest`를 사용하여 학습 테스트
2. 기능 목록
    - [x] 엔티티 클래스 생성
    - [x] `@DataJpaTest` 학습 테스트 생성
        - [x] Answer 학습 테스트 생성
        - [x] DeleteHistory 학습 테스트 생성
        - [x] Question 학습 테스트 생성
        - [x] User 학습 테스트 생성

### 2단계 - 연관 관계 매핑

1. 요구 사항
    - [x] JPA 실제 도메인 모델을 어떻게 구성하고 객체와 테이블을 어떻게 매핑할지 정의
        - [ x 객체의 참조와 테이블의 외래 키를 매핑해서 객체에서는 참조를 사용하고 테이블에서는 외래 키를 사용할 수 있도록 정의
2. 기능 목록
    - [x] DDL 쿼리를 보고 연관관계 유추
        - [x] Answer의 Question 다대일 매핑
        - [x] Answer의 Writer 다대일 매핑
        - [x] DeleteHistory의 Deleter 다대일 매핑
        - [x] Question의 Writer 다대일 매핑

### 3단계 - 질문 삭제하기 리팩터링

1. 요구 사항
    - [ ] 질문 데이터 삭제 상태로 변경
    - [ ] 로그인 사용자와 질문한 사람이 같은 경우 삭제 가능
    - [ ] 답변이 없는 경우 삭제 가능
    - [ ] 질문자와 답변 글의 모든 답변자 같은 경우 삭제 가능
    - [ ] 질문을 삭제 할 때 답변 또한 삭제해야 하며, 답변의 삭제 또한 삭제 상태 변경
    - [ ] 질문자와 답변자가 다른 경우 삭제 불가
    - [ ] 질문과 답변 삭제 ㅇ력에 대한 정보를 history에 남겨야 함
2. 기능 목록
    - [ ] 코드 정리 및 삭제 시 상태 변경
        - [ ] 관련 테스트 코드 생성
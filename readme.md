# 금융 상품 데이터 수집

## 공통 요구사항

- 외부 API 를 사용하여 데이터를 받아오기
- 데이터를 원하는 형태로 가공하기
- 요구사항에서 사용할 API 는 금융상품통합비교공시 API

[오픈 API 소개 | 오픈API개요 | 오픈API | 금융감독원 금융상품통합비교공시 금융상품한눈에](https://finlife.fss.or.kr/finlife/main/contents.do?menuNo=700029)

- 제공하는 API 중 **정기예금 API 를 활용**합니다
- 공식 문서를 보고 **데이터의 구조를 먼저 파악**한 후 요구사항을 구현합니다.

## 세부 요구사항

1. 데이터 추출 - Key 값 출력하기
2. 데이터 추출 – 전체 정기예금 상품 리스트
3. 데이터 가공 - 전체 정기예금 상품들의 옵션 정보 리스트
4. 데이터 가공 - 상품과 옵션 정보들을 담고 있는 새로운 값을 만들어 반환하기

## 프로젝트 소감

1. 금융 프로젝트의 1~3번까지의 내용은 생각보다 쉬워서 금방금방 했는데, 4번에서 너무 막혔다. 
2. 4번에서 막힌 이유는 url주소를 틀려서 처음 받아오는 정보들이 프로젝트 내용과 달라서였다.
3. 앞으로 항상 개발 전부터 세세한 것도 신경쓰도록 하자(특히 주소나 url url url)
4. 딕셔너리 사용이 아직 익숙하지 못한 것 같다.
5. 딕셔너리 값 추가, 딕셔너리 값 수정 등을 좀 더 연습하자
6. 항상 안되면 이유를 좀 많이 고민해보자, 몇번하다가 맨탈나가지 말고
7. json 파일 열었으면 로드도 해야지..

```python
books_json = open('data/books.json', encoding='utf-8')
books_list = json.load(books_json)
```
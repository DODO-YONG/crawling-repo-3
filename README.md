# Crawling Project - 네이버 우리 (도)지역 주간 베스트 콘텐츠 알림 서비스
(Fast Campus DSS 14th Crawling-3조)
조원 : 정성용, 여영웅

크롤링을 활용하여 웹 데이터를 불러와 판다스 데이터프레임을 활용하여 전처리하고 SQL 데이터베이스로 저장
이후 데이터베이스로 KAKAO API, AWS Lambda, Crontab등을 활용하여 서비스를 구축하는 활동

- 일 단위로 제공되는 네이버 우리 지역(도) 베스트 콘텐츠를 취합하여 주간 베스트 콘텐츠를 선정하여 카카오톡 알림 서비스 제공
  - 좋아요 갯수와 블로그 게시일로 가중치를 주어 가장 포인트가 높은 5개 컨텐츠 선정
- 바쁜 일상 속 멀지 않은 거주 지역(도) 내에서 주말 여가 시간 활용을 할 수 있게끔 컨텐츠를 제공하는 취지로 진행

## Goals

크롤링을 활용하여 네이버 우리동네 데이터 불러와서 저장하는 클래스 생성
 (네이버 우리동네판의 지역별 제목, 링크, 좋아요 갯수, 블로그 게시일, 지역) 
 셀레니움, 스크래피를 활용하여 크롤링 함수 생성하여 데이터 프레임으로 저장
 해당 데이터프레임을 지역별로 불러와 병합
 Sequal Pro Database로 저장

생성한 클래스 패키지 모듈 형태로 설정하여 설치
 setup.py를 통해 만든 naver module 설치
 크론탭 설정하여 매일 9시에 패키지 모듈에 포함된 함수 실행되게끔 설정

서비스화
 데이터베이스를 불러와 전처리 후 점수를 측정하여 주간 상위 5개 컨텐츠 선정
 카카오 API를 활용하여 선정한 주간 베스트 컨텐츠 카카오톡 알림 서비스 제공
 Flask를 활용하여 웹프레임워크 구축하여 우리지역 주간 베스트 콘텐츠 검색 서비스 구축
 
 ## 팀구성
- 담당
  - 정성용 : 카카오톡 및 웹 프레임워크 서비스 구축
  - 여영웅 : 크롤링, 데이터프레임 전처리 및 데이터베이스 관리

## 결과물
   ###
   ![image](https://github.com/dss-14th/crawling-repo-3/blob/main/1.png)

## 우여곡절 

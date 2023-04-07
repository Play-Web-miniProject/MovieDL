# Show Me The Credit!💰   

### 팀 소개
|구분|이름|내용|
|--|--|--|
|팀명||5OS(오링스)|
|팀원||안태현, 오성진, 오수연, 유정현, 이예지|
|역할|안태현|데이터 수집 및 기초 전처리, 딥러닝 (회귀) 모델 선정 및 학습, <br>파라미터 조정, 웹구현(js)|
||오성진|데이터 전처리, 딥러닝 (회귀) 모델 선정 및 파라미터 조정, <br>웹구현(HTML)|
||오수연|데이터 전처리, 점수화, 딥러닝 (회귀, 분류) 모델 선정 및 <br>파라미터 조정, 보고서 작성|
||유정현|데이터 전처리, 점수화, 딥러닝 (회귀, 분류) 모델 선정 및 <br>파라미터 조정, 보고서 작성|
||이예지|추가 분석용 웹 크롤링, 크롤링 데이터 전처리, <br>딥러닝 (분류) 모델 선정 및 파라미터 조정, 보고서 작성|

### data 설명
|순번|파일명(/final/0_data/)|설명|
|--|--|--|
|1|KOBIS_개봉일람_2023-03-23.csv|KOBIS 개봉일람(연도별) 2003년~2023년 <br>영화 정보 데이터(2023-03-23 기준)|
|2|preprocessing.csv|누락 데이터 제외, 컬럼별 전처리, 데이터 타입 <br>변경된 파일|
|3|naver_crawling_data.csv|네이버 영화 API에서 크롤링으로 배우, 평점, <br>네이버 영화 url 추가 수집한 파일|
|4|resizing_all.csv|‘전국 스크린 수’ 50 초과, ‘전국 관객수’ 1,000명 초과 / <br>연도별 ‘총 관객수’, ‘코로나’ 컬럼 추가 (4168개 데이터)|
|5|resizing_reg.csv|‘전국 스크린 수’ 50 초과, ‘전국 관객수’ 10,000명 초과 <br>100,000명 미만의 데이터 / 연도별 ‘총 관객수’, ‘코로나’ <br>컬럼 추가 (1603개 데이터)|
|6|resizing_cls.csv|‘전국 스크린 수’ 50 초과, ‘전국 관객수’ 800,000명 초과하는 데이터 / <br>연도별 ‘총 관객수’, ‘코로나’ 컬럼 추가 (744개 데이터)|
|7|movie_resize_merged_all.csv|resizing_all.csv파일과 크롤링 파일을 합친 파일|
|8|movie_resize_merged_reg.csv|resizing_reg.csv파일과 크롤링 파일을 합친 파일|
|9|movie_resize_merged_cls.csv|resizing_cls.csv파일과 크롤링 파일을 합친 파일|
|10|movie_resize_ranking.csv|movie_resize_merged_all.csv파일에서 <br>‘전국 관객수’ 기준 상위 300개 데이터|
|11|movie_total_people.csv|연도별 ‘총 관객수’ 데이터|
|12|movie_final_reg.csv|movie_resize_merged_reg.csv파일에서 ‘감독’, ‘배급사’, ‘주연배우’ <br>점수화 컬럼을 추가한 회귀 학습용 최종 파일 (1413개 데이터)|
|13|movie_final_cls.csv|movie_resize_merged_cls.csv파일에서 ‘감독’, ‘배급사’, ‘주연배우’ <br>점수화 컬럼을 추가한 분류 학습용 최종 파일 (708개 데이터)|
|14|DL model/cls_model.h5, reg_model.h5|분류 모델(cls_model.h5)과 <br>회귀 모델(reg_model.h5)을 학습시킨 모델링 파일|
|15|requirements.txt|install이 필요한 모듈&모듈 버전 리스트|

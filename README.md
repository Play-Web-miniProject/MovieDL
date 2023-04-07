# Show Me The Credit!💰   

### 팀 소개
|구분|이름|내용|
|:--:|:--:|--|
|팀명||5OS(오링스)|
|팀원||안태현, 오성진, 오수연, 유정현, 이예지|
|역할|안태현|데이터 수집 및 기초 전처리, 딥러닝 (회귀) 모델 선정 및 학습, <br>파라미터 조정, 웹구현(js)|
||오성진|데이터 전처리, 딥러닝 (회귀) 모델 선정 및 파라미터 조정, <br>웹구현(HTML)|
||오수연|데이터 전처리, 점수화, 딥러닝 (회귀, 분류) 모델 선정 및 <br>파라미터 조정, 보고서 작성|
||유정현|데이터 전처리, 점수화, 딥러닝 (회귀, 분류) 모델 선정 및 <br>파라미터 조정, 보고서 작성|
||이예지|추가 분석용 웹 크롤링, 크롤링 데이터 전처리, <br>딥러닝 (분류) 모델 선정 및 파라미터 조정, 보고서 작성|

### data 설명
|순번|파일명(/final/0_data/)|설명|
|:--:|--|--|
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

## 1. 프로젝트 소개 
   
### 1) 주제
국내 개봉 영화 데이터를 활용한 영화 관람객수 예측 DL모델 개발   
   
### 2) 배경
(1) 영화 산업은 지속적인 성장을 거듭하며 2019년 매출액 2조 5093억 원의 최고 수준을 기록함.   
(2) Covid-19의 확산으로 2020년 매출액 전년 대비 58% 감소하며 지난 10년 간 가장 적은 규모를 보임.   
(3) 2022년 한국 영화산업 결산 보고서에 따르면 매출액과 전체 관객 수 모두 회복세에 접어들었음.   
(4) 코로나19 팬데믹으로 3년간 침체된 영화산업의 성장을 기대하며 어떤 요소들이 영화 흥행에 영향을 주는지 알아보고자 함.   
   
### 3) 목적 및 기대효과
(1) 영화 투자자의 관점에서, 영화가 개봉되었을 때 기대되는 수익에 대해 합리적인 기준이 있다면 투자 규모 등의 중요한 의사 결정을 내릴 때 도움이 될 것.   
(2) 머신러닝/딥러닝을 통해 영화 관람객 수 예측 모델을 도출함으로써, 영화 투자사에 가이드라인을 제시할 수 있고, 영화 제작사의 입장에서는 영화 투자 제안 및 홍보에 전략적 수단이 될 것이라 기대함.   
(3) 소비자의 입장에서 흥행 가능성이 높은 작품을 확인함으로써 관람 전 기대감을 높이고 관람 후 만족도가 상승할 것으로 기대함.   
   
### 4) 프로젝트 수행기간
2023년 4월 3일 ~ 2023년 4월 7일   
   
### 프로젝트 참여 구성인원
안태현, 오성진, 오수연, 유정현, 이예지   
   
### 개발환경
(1) 시스템 : VSCode, jupyter notebook, Google colaboratory   
(2) 언어 : Python, HTML, CSS, JavaScript   
(3) 라이브러리 : Cmake, BeautifulSoup4, Pandas, Pandas-profiling,  Numpy, Numpydoc,  Matplotlib, Seaborn, Sklearn(Scikit-Learn), Tensorflow, TensorJs, Urllib, Xmltodict   
(4) 알고리즘 : DNN(Deep Neural Network), Batch Normalization   
   
## 2. 프로젝트 전 과정
   
### 0. Data Collecting
KOBIS 공식 통계 자료: 연도별 영화 정보 및 통계 데이터   
https://www.kobis.or.kr/kobis/business/stat/offc/searchOfficHitTotList.do?searchMode=year   
    
네이버 API 영화 데이터 크롤링: 배우, 평점, 네이버 영화 정보 url 데이터 추가 수집   
https://developers.naver.com/docs/serviceapi/search/movie/movie.md   



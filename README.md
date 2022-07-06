# vgames_analysis
vgames게임 데이터를 이용하여 게임시장을 분석
--------------------------------------------------------------------------------------------------------------------



# 프로젝트 기획 배경
### 1. 판매량을 통하여 시대별 게임에 대한 관심도를 파악해 보고자 하였다.
### 2. 지역별로 선호하는 게임의 장르, 플랫폼이 다르다면 그 지역에서 선호하는 것은 어떤 것인지 파악해 보고자 하였다.
3. 

# 프로젝트 목표
### 지역별, 장르별, 선호하는 플랫폼을 찾아 분석 후 추후 관심있을 가능성이 높은 게임을 예측하여 보고자 하였다.

# Data
### datafile : vgames2.csv

dataset --
<img width="470" alt="image" src="https://user-images.githubusercontent.com/90304674/177641927-a90c1548-61a9-4db4-9171-7a97068190e3.png">

Name : 게임 이름

Platform : 플랫폼

<img width="598" alt="image" src="https://user-images.githubusercontent.com/90304674/177643361-fddafdc6-79ba-4f8d-a315-eee380504505.png">


Year : 출시 연도

<img width="553" alt="image" src="https://user-images.githubusercontent.com/90304674/177643606-720c7178-de68-4e65-9222-e78cbda1fcc2.png">


Genre : 게임 장르

<img width="556" alt="image" src="https://user-images.githubusercontent.com/90304674/177643540-9b54ac4e-58d0-43d4-8a4d-9fce6b67eb3a.png">


Publisher : 출판사

NA_Sales : 북미지역 판매량

EU_Sales : 유럽지역 판매량

JP_Sales : 일본지역 판매량

Other_Sales : 기타지역 판매량

# 데이터 전처리
### 결측치 확인 및 제거

<img width="227" alt="image" src="https://user-images.githubusercontent.com/90304674/177644008-4f1a4efb-5a0d-4266-be5e-dfa0105849bf.png">

<img width="121" alt="image" src="https://user-images.githubusercontent.com/90304674/177644085-22f4307c-f12c-4332-89fa-6ab25999b5c1.png">

### 출시 연도 수정
출시 연도가 두 자리 수(ex. 9, 97, 11, 15, 3)로 되어있는 경우가 있어 비디오 게임이 상용화된 1970년대와 현재 시점인 2022년을 감안하여 23을 기준으로 적은 것은 +2000, 큰 것은 +1990을 해주었다.

### 판매량 단위 통일
각 지역의 판매량 데이터가 중간중간 'K', 'M'의 문자로 되어있는 경우가 있어 'M'은 제거하고, 'K'는 *0.001로 대체하여 'M'단위로 통일하였다.

### 타입 수정
연도는 int, 각 지역 판매량은 float으로 타입을 변환하여 주었다.

# 시각화
### 연도별 게임 판매량
<img width="491" alt="image" src="https://user-images.githubusercontent.com/90304674/177646607-ed242fc0-7303-4c9b-bbf1-09d23c28e436.png">

### 장르별 게임 판매량
<img width="567" alt="image" src="https://user-images.githubusercontent.com/90304674/177646717-5e7c73c2-4748-4cb3-9f39-d2e5f329fc43.png">

### 플랫폼별 게임 판매량
<img width="925" alt="image" src="https://user-images.githubusercontent.com/90304674/177647693-407f039e-e213-490c-92b6-f5f48874df3c.png">

### 장르별 총 판매량
<img width="538" alt="image" src="https://user-images.githubusercontent.com/90304674/177648109-f3c6c5d4-b8e2-48db-babb-996809ef6b91.png">

### 플랫폼별 총 판매량 (TOP5)
<img width="414" alt="image" src="https://user-images.githubusercontent.com/90304674/177648194-c6c7ee6b-fa1f-49ff-9ddb-d86b6c112d49.png">


# 한계점
### 현재 2022이지만 데이터는 2020년 까지라 현재 시점에서의 분석의 정확도는 부족할 수 있다.

# 개선점
### 현재까지의 게임 데이터를 추가로 수집하여 추가 분석을 하고자하며 최종적으로는 시계열 모델인 ARIMA 등을 통하여 추후 게임 시장을 예측해 보고자 함.








<h2 align="center">☀️2021 날씨 빅데이터 콘테스트<br><br>🍚날씨 최적화 식단 설계 및 추천 플랫폼: 뭉게뭉게 냉장고</h2>

<h2>🍚 1. 개요</h2>

- 공모전: 2021년 기상청에서 개최한 [2021 날씨 빅데이터 콘테스트](https://bd.kma.go.kr/contest/main.do)

- 주제: 날씨 최적화 식단 설계 및 추천 플랫폼: 뭉게뭉게 냉장고

- 수행기간: `2021.05.13 ~ 2021.06.28`

- 수행인원: 구병모, 김미섭, 정예린, 김효주

- 담당역할: 데이터 전처리 (Feature Engineering, 결측치 처리), 상관분석, 모델링

<h2>🍚 2. 분석 배경</h2>

<p align = "center"><img src = "Images/1. 배경.JPG" width = "1000" height = "400"></p>

- 식품은 날씨와 기후의 영향을 크게 받는 상품군

- 코로나 19 바이러스로 인해 격리시설에 있는 환자와 같이 주어진 식단을 먹어야하는 분들께 먹고 싶은 식단을 제공해주자 

<h2>🍚 3. 분석 목표</h2>

#### 날씨변수의 소비에 대한 영향력 판별

- 기상요소에 따라 사람들의 소비패턴이 유의미한 변화를 보이는가

#### 기상요소에 민감한 상품군의 선별

- 서로 다른 상품군을 어떻게 조합하면 날씨의 영향을 긍정적으로 수용하면서 사람들의 선호도가 높도록 구성할까

#### 데이터의 종합을 통한 맞춤형 서비스 제공

- 날씨 + 영양성분 + 가격 데이터를 추가적으로 고려하여 적합한 `날씨 맞춤형` 식단 조합 및 추천 서비스를 제공

<h2>🍚 4. 분석 프로세스</h2>

<p align = "center"><img src = "Images/2. 프로세스.JPG" width = "1000" height = "300"></p>

<h2>🍚 5. 분석 내용</h2>

### 1. 데이터 전처리

- (1) 변수 설정

<img src = "Images/3. 변수설정.JPG" width = "800" height = "300">

- (2) 결측치 처리

<img src = "Images/4. 결측치.JPG" width = "800" height = "300">

- (3) 새로운 변수 생성

<img src = "Images/5. 새로운 변수.JPG" width = "800" height = "300">

- (4) 데이터 표준화

<img src = "Images/6. 최종 데이터 변수.JPG" width = "800" height = "300">

- 설명변수: 각 변수별로 범위가 달라 모델에 적용했을 때 큰 값을 가지는 변수의 영향이 크게 작용할 수 있음 > 각 변수의 평균이 0, 표준편차가 1이 되도록 표준화

- (5) 이상치 제거

<img src = "Images/7. 이상치.JPG" width = "800" height = "300">

- (6) 상관 분석

<img src = "Images/8. 상관분석.JPG" width = "800" height = "300">

- 상관계수가 높게 나타나는 변수들의 VIF를 구하여 다중공선성이 있는지 판단하여 제거해줌

### 2. 데이터 모델링

<img src = "Images/9. 모델링.JPG" width = "1000" height = "400">

- Xgboost, Random Forest, LightGBM, Ridge 회귀 비교

- 다양한 모델에서 R-square 값을 기준으로 어느 정도 예측이 가능한 식품군을 선택해서 식단을 구성하고자 함

<img src = "Images/10. 예측.JPG" width = "1000" height = "400">

- 모델링 과정을 통해 식품별로 사람들의 선호도를 예측

- 그 후 사람들의 선호도가 가장 높게 나오는 식단을 구성

<h2>🍚 6. 활용방안</h2>

<p align = "center"><img src = "Images/11. 플랫폼.JPG" width = "800" height = "400"></p>

- 플랫폼 아이디어 제시

<p align = "center"><img src = "Images/12. 식단.JPG" width = "900" height = "400"></p>

- 식단은 위와 같은 카테고리로 구성

<p align = "center"><img src = "Images/13-1. 솔루션.JPG" width = "1000" height = "400"></p>

<p align = "center"><img src = "Images/13-2. 솔루션.JPG" width = "1000" height = "400"></p>

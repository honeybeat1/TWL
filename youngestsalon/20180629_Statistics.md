# 데잇걸즈 4일차 (2018.06.28.) TIL


### Introduction
1. 통계가 필요한 이유
- 자료의 신뢰성
- 의사결정의 근거 제시
- 현상을 분석하여 실증자료를 제시

2. 통계학
- 자료의 수집과정을 설계, 자료를 요약/해석하여 결론을 이끌어내거나 일반화하는 원리 및 방법론을 제공
- 모집단 전수조사하기에는 시간/공간적 제약 존재 -> 표본을 통한 데이터 수집 및 모집단 특성 추론 필요
- 통계량이 모수와 어느 정도 일치할 지에 대한 확률이 필연적임

3. 통계의 한계
- 표본에서 결과를 얻기 때문에 정확한 결론을 내지 못함
- 확률이 없으면 의미가 없음 (Ex. 오차범위)
- 항상 틀릴 가능성을 내포함 (Ex. 신뢰구간)
- 차원의 저주 : 차원(변수의 숫자 p)이 증가하면 그것을 표현하기 위한 데이터 양(observation : n)이 기하급수적으로 증가 or 데이터의 밀도가 희박해짐
    * 일정 차원을 넘으면 분류기의 성능은 점점 감소
    * 각 차원(변수)에서 20%를 샘플링하기 위해 개별 변수에서 추출해야 하는 데이터의 비율 : 1차원 = 20%, 2차원 = 45%, 3차원 = 58%, 10차원 = 85%
    * 각 차원의 데이터 밀도가 희박해지면 모델링을 할 시 과적합(Overfitting)의 문제가 발생

4. 변수가 (과도하게) 많을 때 줄이는 법
- Missing 비율이 큰 변수 지우기
- 현업과 상의해서 변수 제거 (추천)
- PCA (추후 배울 예정)
- lasso (추후 배울 예정)

5. 데이터 분석가들이 많이 사용하는 데이터 분석 도구 : Python / R / Excel
- Python : 프로그래밍 언어이지만 다양한 데이터 분석 라이브러리가 존재. 오픈소스(=무료). 프로그래밍 실력이 분석 결과의 품질을 좌우함.
- R : 통계분석을 주 목적으로 만들어진 언어. 다양한 데이터 분석 라이브러리가 존재. 오픈소스(=무료).
- 엑셀 : 사용이 쉬움. 애드인(Add-ins) 프로그램을 통해 다양한 데이터 편집/고급 분석 가능. 대용량 데이터 처리 불가. 상용 SW는 비용 발생.

6. 기타
- 분석 프로세스 : SEMMA (Sample, Explore, Modify, Model, Assess. 솔루션 업체인 SAS사 주도로 만들어진 방법론. Explore가 제일 중요.)

7. EDA : Exploratory Data Analysis
- 데이터가 가진 정보를 데이터의 탐색만으로 얻는 방법. 즉, 탐색적 자료 분석. 데이터 분석의 첫 단계.
- 데이터로부터 정보를 얻기 위한 다양한 방법을 시도 -> 데이터의 패턴/규칙을 파악.

8. 자료의 분류 : 수치형 변수 (연속형 변수 & 이산형 변수) / 범주형 변수 (명목형 변수 & 순위형 변수)
- 연속형 변수 : 실수(Floating)와 같이 딱 떨어지는 숫자가 아닌 경우. (Ex. 키, 몸무게, 온도, 거리)
- 이산형 변수 : 정수(Interger)와 같이 딱 떨어지는 숫자. (Ex. 수강생의 수, 카페의 개수)
- 명목형 변수 : 순서(정렬?)가 없는 범주형 변수. (Ex. 혈액형, 성별, 통신사)
- 순위형 변수 : 순서가 있는 범주형 변수. (Ex. 학년, 등급, 설문지 척도)

9. 범주형 자료의 요약 : 도수 분포표, 원형그래프, 막대그래프, 파레토 그림
- 이 경우, 범주의 종류에 관심을 두며 각 범주가 나타내는 횟수를 요약함
- 도수분포표 : 범주와 그 범주에 대응하는 도수 및 상대도수를 나열한 표. 전체 자료의 개요를 파악하기 쉬움.
      * 도수 : 각 범주에 속하는 관측값의 개수
      * 상대도수 : 도수를 자료의 전체 개수로 나눈 비율
- 원형그래프 : 상대도수에 비례하여 중심각을 나누어 조각을 나눈 것과 같은 형태를 그림
- 파레토그림 : 막대그래프의 일종. 상대도수의 크기가 큰 순서로 범주를 왼쪽 -> 오른쪽으로 배열하여 만듦.
              범주의 순서가 의미가 있는 순위형 자료와 같은 경우에는 유용하지 않음.

10. 통계는 왜 중요할까? (by 영웅님)
- 현재 우리나라에 빅데이터 수집/분석이 가능할만큼 큰 기업은 많지 않음.
- but, 데이터의 패턴을 정확히 파악해서 해석하기 위해 통계 기초에 대한 이해는 필수!
- EDA = 데이터를 탐색하기 위한 모의고사를 반복하는 작업.
- 데이터, Prediction, Sampling, EDA에 대해 시간 여유가 있을때 검색해 보세요.

11. 연속형 자료의 요약 : 점도표, 도수 분포표, 히스토그램, 줄기-잎 그림.
- 점도표 : 수평선을 긋고 눈금을 표시한 후 각 관측값에 해당하는 위치에 점을 찍어 표시. 전체 자료의 개요 파악에 용이하나, 엑셀에서는 못 그림.
- 도수분포표 : 모든 관측값을 포함하는 범위를 몇 개의 구간으로 나누어 작성함.
      * 계급 : 나뉘어진 각 부분
      * 계급구간 : 각 계급에 포함되는 값의 범위
      * 계급구간의 폭 : 각 계급구간의 크기
- 히스토그램 : 각 계급에 대하여 범주형 자료에서의 막대그래프와 같은 모양의 그림. 연속형 자료를 요약할 시 가장 많이 사용(중요함!)
      * 막대의 높이 : 상대도수를 계급구간의 폭으로 나눈 값.
      * 데이터 값의 범위, 빈도의 집중 영역, 대칭성을 알 수 있음.
- 줄기-잎 그림 : 자료의 분포를 시각적으로 쉽게 파악하면서 각 관측값을 유지할 수 있음. 최댓값/최솟값/특정 관측값의 위치 파악이 용이함.
- (참조) 지도 : Google Spreadsheet의 Chart 기능에는 '지도' 기능이 있음 (실습파일 'GNP' 탭 참조)

12. 수치 요약
- 중심 위치의 측도 : 평균(엑셀 'average'), 중앙값(엑셀 'median')
    * 중심 위치를 통해서는 퍼진 정도를 파악하기 어려움
    * 평균 : 전체 관측값이 골고루 반영 -> 대푯값으로 많이 활용. but 극단값의 영향을 많이 받음
- 퍼진 정도의 측도 : 분산(엑셀 'var'), 표준편차(엑셀 'stdev'), 사분위수(엑셀 'quartile'), 상자그림
    * 분산/표준편차 : 관측값이 자료의 중심위치로부터 떨어진 정도를 고려함
    * 분산 : 각 관측값과 평균의 차이
    * 표본분산 : 편차의 제곱합을 n-1로 나눈 값. 표본분산의 값이 클수록 관측값들이 표본평균으로부터 멀리 퍼져 있다는 의미.
    * 표준편차 : 표본분산의 양의 제곱근. 분산의 경우 단위가 제곱이 되기 때문에 단위를 맞춰주기 위해 분산보다는 표준편차를 사용.
    * 사분위수 : 전체 관측값을 작은 순서로 배열했을 때 전체를 사등분하는 값
    * 상자그림 : 자료로부터 얻는 다섯 가지의 요약수치인 최솟값, 사분위수, 최댓값을 가지고 그림을 그린 것. 두 그룹을 비교하는데 유용함.

13. 수치 요약 2
- 변수 : 자연 및 사회 현상의 여러가지 요인
- 영향을 받는 변수 = 반응변수, 종속변수 (y)
- 영향을 주는 변수 = 설명변수, 독립변수 (x)
- 종속변수/설명변수가 모두 연속형인 경우 산점도, 모두 범주형인 경우 모자이크 플랏, 변수형과 연속형이 하나씩인 경우 상자그림 사용.
- 산점도 : x를 수평축에 놓고 y를 수직축에 놓은 후에 각 관측값의 짝을 좌표 위에 표시한 그림. 두 변수 간의 관계를 시각적으로 대략 파악.
    * 한쪽으로 데이터가 쏠린 경우, 중앙으로 모아주기 위해 데이터에 로그 변환 수행(엑셀 'ln'). 로그 변환의 분모는 자연상수 E임.
- 모자이크 플랏 : 범주에 따른 비율을 파악, 면적의 크기는 도수의 양과 비례함.
- 상관계수(엑셀 'correl') : 산점도에서 점들이 얼마나 직선에 가까운가의 정도를 나타내는 데 쓰이는 측도.
    * 표본상관계수의 절대값의 크기는 직선관계에 가까운 정도를 나타내며, 부호는 직선관계의 방향을 나타냄.
    * 단점 : 직선관계가 있어야만 변수 간의 관계가 노출됨. (= 산점도 없이 상관계수만 보면 위험함)
    * 상관계수 값이 항상 두 변수 사이의 인과관계를 의미하지는 않음.

14. 향후 학습 예정 내용
- 이산형 변수의 확률 : 확률분포표, 포아송, 이항분포, 베르누이
- 연속형 변수의 확률 : 정규분포, 지수분포, 감마분포, 중심극한의 정리.
- 구간추정, 신뢰구간, 대립가설/귀무가설 등
- Homework : 오늘 엑셀로 실습한 내용을 python으로 똑같이 구현하기 (Due date : 2018.07.20.금)


### Git & GitHub (참조 : https://backlog.com/git-tutorial/kr/intro/intro1_3.html)

1. 헌법개정안('1987) 실습
![20180629_GitHub_터미널 예시](https://github.com/YoungestSalon/TIL/blob/master/TIL_20180629_GitHub.JPG?raw=true)
- 터미널을 활용한 Git & GitHub 사용 실습 (Init, Add, Push 관련 실습)
- 터미널 명령어 : pwd(현재 경로 확인), cd(Change Directory)
- 터미널 작업 : 작업 대상 파일이 있는 폴더로 이동(cd)해서 작업해야 함.

2. 헌법개정안('2018) 실습 : Branch off
- Branch Off 관련 실습 (개인별 선택사항)
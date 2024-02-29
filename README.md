# Kaggle 이용한 ML 연봉 예측 대회
: 실무 데이터로 우수한 예측 모델 구축<br>

<br>

## 배경
- 세부직종, 경력, 자격증 등의 11개 Feature를 통해 지원자의 연봉 금액을 예측
- 2개의 최종 submission 파일 만든 후 Kaggle 통해 성능 확인
<br>

## 의의
- 실무 raw 데이터 처리 능력 향상
- Bow, PCA 등 다양한 기법 적용하여 Feature Engineering
- Catboost, Xgboost, LM 등 다양한 모델 구성하고, 앙상블
<br>

## Code
### submission1
- 가장 성능이 좋았던 Catboost 기본 모델로 선정
- 모델별 상관계수와 성능을 그래프로 그려보고, 이질적인 모델 추가하여 앙상블
- 성능이 좋았던 lgbm, Xgboost은 앙상블 결과 성능 향상 기대 x
- 부스팅 모델 제외한 선형 모델 Ridge에서 성능 대폭 향상
- Catboost 4개 + Ridge 가중 평균 사용하여 최종 앙상블

### submission2
- 과적합 요인을 막기 위해 public score를 보며 앙상블하는 것이 아닌, Cross Validation Stacking 수행
- Publice score에서 submission1 결과와 비슷한 성능
- 최종 Private에서 성능 향상
### ⚠ 기업에서 제공 받았기 때문에, 데이터는 공유 불가


프로젝트 개요
이 프로젝트는 심박수 데이터를 이용하여 수면 단계를 예측하는 모델을 개발합니다.

데이터 개요
데이터셋: train.csv
컬럼: id, subjectID, pulse, sleep_stage
데이터 처리
정규화: MinMaxScaler를 사용하여 심박수 데이터를 정규화.
시차 특성 생성: 과거 29시간의 심박수 데이터를 기반으로 특성 생성.
이상치 제거: 상위 2개의 이상치 제거.
모델 학습
모델: LightGBM
파라미터:
objective: 'multiclass'
num_class: 5
metric: 'multi_logloss'
boosting_type: 'gbdt'
num_leaves: 31
learning_rate: 0.05
feature_fraction: 0.9
성능 평가
훈련 정확도: 51.36%
검증 정확도: 45.84%
결론
본 모델은 심박수 데이터를 사용하여 수면 단계를 예측할 수 있으며, 약 46%의 정확도를 보입니다.

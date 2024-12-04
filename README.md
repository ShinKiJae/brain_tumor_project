![image](https://github.com/user-attachments/assets/956443e3-efb7-4f1d-8da7-d566c25df566)# brain_tumor_project
## 1. 문제 정의
### MRI 이미지를 활용해 뇌종양 여부를 자동으로 분류하는 모델을 구현
### 입력 데이터 : 128x128 크기의 흑백 MRI 이미지
### 출력 데이터 : 종양의 존재 여부를 나타내는 이진 분류 결과 (Yes/No)


## 2. 사용하는 데이터
### Brain MRI Images for Brain Tumor Detection
### - 두 개의 클래스(뇌종양 여부)에 해당하는 MRI 이미지로 구성
### 출처 : 캐글


## 3. 모델 종류, 구조
### -CNN
### Convolutional Layers
#### 첫 번째 레이어: 입력 채널 1 → 출력 채널 32 (3x3 필터, 패딩 1)
#### 두 번째 레이어: 입력 채널 32 → 출력 채널 64 (3x3 필터, 패딩 1)
#### 각 레이어 뒤에 ReLU 활성화 함수와 MaxPooling(2x2) 적용

### Fully Connected Layers
#### Flatten 후 첫 번째 Fully Connected Layer: 64 x 32 x 32 → 128 뉴런
#### 드롭아웃으로 과적합 방지
#### 출력 레이어: 128 → 2 (출력 클래스 수)
#### 활성화 함수: ReLU
#### 손실 함수: CrossEntropyLoss
#### 최적화 알고리즘: Adam

## 4. 실험 결과. hyper parameter 변경 
### 배치 사이즈, 학습률 등 하이퍼 파라미터 조정하여 성능 개선

## 5. 모델 성능
### 약 86% 정확도

## 6. 결론
### 모델 정확도 86%, 대체로 잘 분류
### 학습 과정에서 배치 크기, 학습률 등 하이퍼 파라미터를 조정함으로써 모델 성능 개선
### 규모가 큰 데이터 셋을 사용하여 진행하면 더 좋은 성능을 보일 것으로 예상



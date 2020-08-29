# Measure_BoneAge
딥러닝(CNN)을 활용하여 손 X-Ray 이미지와 csv 파일을 통해 뼈 나이를 측정합니다.

## 데이터
- Kaagle : https://www.kaggle.com/kmader/rsna-bone-age
- 파일 크기 약 9GB
- 이미지 총 12611장
  - 남자 6833장
  - 여자 5778장
- csv 파일 데이터 : 파일명, 뼈 나이, 성별
- 뼈 나이는 최소 1부터 최대 288까지 존재. (단위 : 개월)
  ![이미지 모음](https://user-images.githubusercontent.com/37574274/91641383-eea77a00-ea5e-11ea-8e4a-15ba9ebb1d88.png)
- ㅇㅇㅇ


## 모델 구현

### 성별 구분 없이 이미지만으로 학습

### 성별을 구분하여 성별 전용 모델 2가지를 만들어서 학습

### CNN 이후 성별 데이터를 입력하여 학습

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
- ㅇㅇㅇㅇㅇ

## 모델 구현
- InceptionV3 사용
- loss='mae', optimizer='adam'

### 성별 구분 없이 이미지만으로 학습
![이미지만사용_1](https://user-images.githubusercontent.com/37574274/91690208-83fe5780-eba0-11ea-9ede-8527704b02a4.png)
![이미지만사용_2](https://user-images.githubusercontent.com/37574274/91690210-852f8480-eba0-11ea-8893-e1de98c37667.png)  
- 최소 loss : 16.5637

### 성별을 구분하여 성별 전용 모델 2가지를 만들어서 학습
- Male 전용  
![male_1](https://user-images.githubusercontent.com/37574274/91690242-91b3dd00-eba0-11ea-97cd-10142247c20c.png)
![male_2](https://user-images.githubusercontent.com/37574274/91690244-924c7380-eba0-11ea-82c5-8b5e98576533.png)  
  - 최소 loss : 13.3120
  
- Female 전용  
![female_1](https://user-images.githubusercontent.com/37574274/91690289-a7290700-eba0-11ea-8cdf-9cab483bcbdc.png)
![female_2](https://user-images.githubusercontent.com/37574274/91690290-a7c19d80-eba0-11ea-9879-f6bf60ac885b.png)  
  - 최소 loss : 16.5866
  
### CNN 이후 성별 데이터를 입력하여 학습 (레이어 )
![layer_1](https://user-images.githubusercontent.com/37574274/91690645-46e69500-eba1-11ea-8315-52fabec4d2e8.png)
![layer_2](https://user-images.githubusercontent.com/37574274/91690651-48b05880-eba1-11ea-86bf-3f826e0b2d48.png)  
- 어딘가 잘못된 것 같다

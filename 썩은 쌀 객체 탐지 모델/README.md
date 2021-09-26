# Rice-Images-for-Object-Detection

## 1. Dataset

### 1-1 Image Labeling

![image](https://user-images.githubusercontent.com/61724682/134811861-8b03e8b0-55eb-4833-a577-e71fab2f0df2.png)

#### - labelImg 툴을 사용하여 지도학습을 위한 학습 데이터 라벨링

![image](https://user-images.githubusercontent.com/61724682/134811937-213a63b4-e3c4-4c93-a5ee-a104d8bce432.png) ![image](https://user-images.githubusercontent.com/61724682/134811941-92ce1fc3-6f50-44c4-b4ed-c2a2d2a391ab.png)

#### - 라벨링 정보를 xml 형태로 저장 : Pascal VOC 형식

### 1-2 Data Sample

![image](https://user-images.githubusercontent.com/61724682/134812002-8a56dfec-0d84-4e65-b2a7-b8ea8e1d0e75.png) ![image](https://user-images.githubusercontent.com/61724682/134812010-3fcebcde-5ca6-482f-9e2f-ac81cd8953d6.png)

#### - Train dataset : 32
#### - Validation dataset : 8
#### - Test data set : 10

## 2. Faster R-CNN Model Architecture

#### - Faster R-CNN은 CNN 특징 추출 및 Classification, Bounding Box Regression을 모두 하나의 모델에서 학습시키고자 한 모델

![image](https://user-images.githubusercontent.com/61724682/134812044-a7db1b8f-2aac-46de-a674-5370f50ae5ec.png)

### 2-1 Network Architecture

![image](https://user-images.githubusercontent.com/61724682/134812069-dd3c9585-4234-4320-885e-51776d7b053a.png)

1. 이미지 입력
2. pre-train CNN 모델의 Feature map 추출
3. 전체 이미지의 feature map을 통해 Region Proposal Network를 실행시켜 후보군 BoundingBox좌표를 예측
4. RPN에서 나온 BB의 좌표에 따라, feature map의 ROI를 잘라내어 ROI pooling
5. 이를 Image classification과 BoundingBox regression에 각각 넣어주어 최종 판단

### 2-1-1 RPN(Region Proposal Network)

#### - object 경계와 각 위치에서의 사물성의 스코어를 동시에 예측하는 fully conv 네트웍 
#### -> 질 좋은 region proposal을 생성하기 위해 end-to-end로 학습

![image](https://user-images.githubusercontent.com/61724682/134812089-23a7d032-c255-429b-b458-efea639d8340.png)

### 2-1-2 RoI Pooling

#### - RoI 영역에 해당하는 부분만 max-pooling을 통해 feature map으로부터 고정된 길이의 저차원 벡터로 축소하는 단계를 의미

![image](https://user-images.githubusercontent.com/61724682/134812104-dc7cb35c-17f2-416d-9c32-c5c2ed0ee656.png)


## 3. Model Training

![image](https://user-images.githubusercontent.com/61724682/134812162-d318984f-5f86-4804-a7e1-e6577810e14d.png)

## 4. Model Validation

![image](https://user-images.githubusercontent.com/61724682/134812170-44400aa7-ddb6-4150-a441-e080e9a28d26.png)


## 5. Model Evaluation

![image](https://user-images.githubusercontent.com/61724682/134812184-00629319-ab3e-4989-a615-f4f745b3f481.png)

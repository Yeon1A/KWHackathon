# KWHackathon
Hackathon
## 대회 기간
> 2023.07.29~2023.09.11

## AI를 통한 반려묘 안구질환 진단 
### 선정 배경
 요즘 반려동물에 대한 관심이 증가하고, 많은 사람들이 반려동물을 키우는 현 상황에서 자신이 키우는 동물의 건강 상태를 스스로 진단하기는 쉽지 않다. 
이 때, 동물병원에 가지 않고도 집에서 간단하게 반려동물의 안구질환을 파악하고 더 쉽고 빠르게 대처하기 위함이다. 

### 데이터 셋
#### 반려동물 안구 질환 데이터
AI-Hub에 있는 반려동물의 안구 질환에 대한 데이터셋을 선정하였다.
저희는 해당 데이터셋에서 반려묘에 관한 데이터를 활용하여 고양이의 안구질환을 진단하기 위한 AI를 개발할 예정이다.
하단의 사진은 활용할 데이터셋 사진이다.
![](https://velog.velcdn.com/images/stilltravel/post/de6235f2-5e21-4d37-ab2e-4046b39a8415/image.png)
![](https://velog.velcdn.com/images/stilltravel/post/1de945ef-bbc5-4e53-881d-22981109b2dd/image.png) 
>그 중 (400,400) 크기의 라벨링 데이터를 사용하여 학습을 진행할 예정.  
>출처:  https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=realm&dataSetSn=562

### 판단 질병의 종류
>
#### A. 각막궤양
![](https://velog.velcdn.com/images/stilltravel/post/be70e872-7870-4a68-962f-e1382c91d038/image.png)
눈의 제일 바깥 부분에 해당하는 각막에 염증이 생겨 각막상피와 기질이 손상된 것
- 데이터 수는 6250개 (유,무 포함)
#### 특징
보호자가 보기에 눈이 불투명하고 탁하게 보이며, 눈곱과 눈물이 많이 생김
각막 중앙부에 원형으로 초록색 염색부위가 관찰가능하지만 진행정도나 병변 범위에 따라 다양하게 나타날 수 있습니다.
#### B. 각막 부골편
![](https://velog.velcdn.com/images/stilltravel/post/f16e429f-c870-4e44-9f9f-2ee00b7c8c9b/image.png)
- 데이터의 개수는 6234개 (유,무 포함)
#### 특징
각막 부골편은 갈색에서 검은색을 띄고 있으며 검붉은 농성 분비물, 동공이 축소, 일반적으로 만성적인 궤양후 발생하게 됩니다. 즉, 만성 각막궤양을 통해 발병할 가능성이 있고 안검염을 유발하는 질병 (동시 관찰도 가능)
#### C. 결막염
![](https://velog.velcdn.com/images/stilltravel/post/070d7de5-5cb8-4923-8d4f-37d99b11dcd9/image.png)
- 데이터의 개수는 6239개
#### 특징
결막염은 주로 눈이 붓거나 눈 주변(흰자위)이 붉게 충혈되는 증상을 가짐
#### D. 비궤양성 각막염
![](https://velog.velcdn.com/images/stilltravel/post/a9c7ba65-1e86-45af-831b-1dad168c7a08/image.png)
- 데이터의 개수는 2391개
#### 특징
비궤양성 각막염은 곰팡이나 세균등의 이물질이 각막을 자극함
각막이 팽창하고, 눈동자가 탁해지는 현상을 가지고있고, 각막염증이기 때문에 각막궤양을 유발
#### E. 안검염
![](https://velog.velcdn.com/images/stilltravel/post/ab18b78c-8d4a-4101-be51-5b49a9a36609/image.png)
- 데이터의 개수는 1910개
#### 특징
안구 외부에서, 눈꺼풀 피부 혹은 속눈썹 주변부위에 염증이 생기는 질병
눈주위나 눈꺼풀이 붓고, 붉게 변함.
주로 각막궤양과 함께 나타나는 경우가 많음

### 환경
>
Google Colaboratory 환경에서 시행
- Python
- OpenCV
- Numpy
- Tensorflow ,Keras

### Network
> 
- ResNet-18Layer (Input_image size: (224,224))
>>
GitHub:
https://github.com/Yeon1A/KWHackathon/blob/main/ResNet18_disease_a.ipynb  
Velog:
https://velog.io/@stilltravel/AI-ResNet-18-Layer
- ResNet-50Layer (Input_image size: (224,224))
>>
GitHub:
https://github.com/Yeon1A/KWHackathon/blob/main/ResNet50_disease_a.ipynb  
Velog:
https://velog.io/@stilltravel/AI-ResNet-50Layer
- EfficientNet B0 (Input_image size: (224,224))
>>
GitHub:
Velog:
https://velog.io/@stilltravel/AI-EfficientNet
- EfficientNet B5 (Input_image size: (456,456))
>>
GitHub:
Velog:
https://velog.io/@stilltravel/AI-EfficientNet

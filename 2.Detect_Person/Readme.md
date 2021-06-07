### 본 프로젝트는 CNN과 Object Detect 분야를 조금씩 알게 되는 과정으로 작성되었습니다.

## 1. yolov4 model 무작정 학습시켜보기
회사에서 yolov4로 진행을 하고 있어서 yolov4 모델을 사용하여 학습을 진행<br/>
yolov4는 darknet이라는 자기만의 개성있는 프레임워크 툴을 사용하고 있다.<br/>

Darknet은 개성이 있는 만큼 간편하게 학습이 가능하지만,<br/>
일단,darknet tool을 처음 본 나로서는 어떻게 작동되는지 잘 모르지만 학습을 진행할 수 있었다.<br/>
장기적으로 모델의 세부적인 부분을 접근할 때는 tensorflow나 keras가 좋지 않을까 생각한다.

object detection
1. one-stage-detection
2. two-stage-detection


### 진행 과정
1. yolov4 model 및 사람 데이터 
- yolov4의 pre-train 된 모델과 weight를 사용하면 어느 정도 사람을 인지 가능
- coco dataset을 기반으로 학습했는데 coco dataset에서는 사람의 손도 person으로 잡는 등 사람의 일부분을 사람으로 잡고 있다.
- 엄청 작은 부분까지 person으로 학습된 모델이기 때문에 다른 영상으로 테스트할 경우, 멀리 있는 새를 사람으로 잡고 있다.
- 서비스를 제공하는 입장에서 안정적인 정확도(90% 이상에서 일정하게 유지)와 최대한 오인률?(사람이 아닌 것을 사람으로 인식)을 낮춰야한다.

2. yolov4x-mish model 사용


3. yolov4-csp model 사용



## 3. 어떻게 특정 행동(action)을 잡을 수 있을까?(쓰러짐과 서 있는 사람 구별)
person과 down person 이렇게 나눠서 학습을 진행해야될까???

![image](https://user-images.githubusercontent.com/57121112/120961845-8c239d00-c799-11eb-9b89-6b163cea922a.png)


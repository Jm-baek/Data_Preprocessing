### 본 프로젝트는 CNN과 Object Detect 분야를 조금씩 알게 되는 과정으로 작성되었습니다.

## 1. yolov4 model 무작정 학습시켜보기
회사에서 yolov4로 진행을 하고 있어서 yolov4 모델을 사용하여 학습을 진행<br/>
yolov4는 darknet이라는 자기만의 개성있는 프레임워크 툴을 사용하고 있다.

object detection
1. one-stage-detection
2. 
3. two-stage-detection


### 진행 과정
1. yolov4 model 및 사람 데이터 
- yolov4의 pre-train 된 모델과 weight를 사용하면 어느 정도 사람을 인지 가능
- but, coco dataset을 기반으로 학습했는데 coco dataset에서 사람의 손도 person으로 잡는 등 다른 부분을 사람으로 잡고 있다.
- 서비스를 제공하는 입장에서 안정적인 정확도(90% 이상에서 일정하게 유지)와 최대한 오인률?(사람이 아닌 것을 사람으로 인식)을 낮춰야한다.


2. yolov4x-mish model 사용


3. yolov4-csp model 사용

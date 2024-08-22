# 목차

1. [06/19 데이터 어노테이션 및 라벨링](#06/19-데이터-어노테이션-및-라벨링)
2. [06/20 OTX 모델 학습](#06/20-otx-모델-학습)
3. [06/23 신호등 신호 판단 알고리즘 개발](#06/23-신호등-신호-판단-알고리즘-개발)
4. [06/24 모델 통합 및 최적화](#06/24-모델-통합-및-최적화)
5. [06/26 코드 클래스화 및 통신 추가](#06/26-코드-클래스화-및-통신-추가)
6. [06/27 UI 개발](#06/27-UI-개발)

   
---

# 06/19 데이터 어노테이션 및 라벨링
- AI Hub에서 추출한 데이터에서 비보호 좌회전 표지판과 신호등 어노테이션 작업 수행
![image](https://github.com/user-attachments/assets/b32c6ce6-f5fa-430d-b2cf-53ca9259fce7)

---

# 06/20 YOLO 모델 학습
- Ultralytics의 Yolov8n  모델 활용 학습

## Yolov8n 학습 코드
- *sign_light_yolo.py*

![image](https://github.com/user-attachments/assets/8bba31e8-898e-4568-b952-687096993ced)



### 최적화

- Optimize with OpenVINO POT
- Precision Compress to FP16

## 테스트 추론
- *inference.py*

![performance_metrics](https://github.com/suhwanjo/Intel-Edge-AI-Project/assets/112834460/149c796d-6e35-4bc7-97a6-e50096e9f91c)

---

# 06/23 신호등 신호 판단 알고리즘 개발
- *inference_sign_light.py*
- 신호등 객체를 4개의 segment로 분리한 후 평균 밝기를 계산합니다.

---

# 06/24 모델 통합 및 최적화
- *model_integration.py*
-데스크탑에서 최적화 시행

---

# 06/26 코드 클래스화 및 통신 추가
- *main.py*

- *traffic_sign_detection.py*
- 신호등 및 비보호 좌회전 표지판 인식 및 처리 스레드입니다.

- *vehicle_detection.py*
- 차량 인식 및 거리 예측 스레드입니다.

- *video_processor.py*
- 실시간 영상의 프레임 처리 스레드입니다.
---

# 06/27 UI 개발
- *qt.py*
- PyQT를 사용한 GUI입니다.


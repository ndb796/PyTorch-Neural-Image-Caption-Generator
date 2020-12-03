### PyTorch Neural Image Caption Generator

* 작성자: 나동빈(Dongbin Na / dongbinna@postech.ac.kr)
* 본 코드는 POSTECH의 **CSED703G 수업** 과제로 작성한 코드입니다.

### Show and Tell: A Neural Image Caption Generator (CVPR 2015)

* 흔히 NIC라고 알려진 네트워크를 제안한 논문입니다.
* NIC 학습/평가 전체 소스코드는 Google Colab을 이용해 실행할 수 있도록 작성했습니다.
* 성능 비교를 위하여 광범위한 실험을 진행했습니다.

#### [NIC using ResNet-101](Neural_Image_Captioning_(NIC)_using_ResNet_101.ipynb)

* ResNet-101을 이용할 때 가장 학습 효율이 좋았습니다.
* <b>5번의 Epoch을 반복</b>하여 다음과 같은 성능을 낼 수 있었습니다.

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|60.54|38.94|25.50|16.99|

* **[학습된 인코더 모델 다운로드 (NIC using ResNet-101 165MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERnDZFI8KD9OrX8rZGB4zucBLL1C2OQl5zdEIj9M23VH8A)**
* **[학습된 디코더 모델 다운로드 (NIC using ResNet-101 16MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfpMfIRuTy1NndX8U7C70XMBmu6wd3JofEo5T-uyIP8YOA)**

* 캡션 생성 예시

![image](https://user-images.githubusercontent.com/16822641/100955005-1116cb00-3559-11eb-9662-7ab78c84b5d2.png)

> &lt;start&gt; a man is climbing a rock wall . &lt;end&gt;

#### [NIC using ResNet-152](Neural_Image_Captioning_(NIC)_using_ResNet_152.ipynb)

* 동일한 하이퍼 파라미터에서 ResNet-152로 바꾸면 다음과 같이 성능이 오히려 떨어질 수 있습니다.

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|53.45|34.20|21.79|14.17|

* **[학습된 인코더 모델 다운로드 (NIC using ResNet-152 225MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYnv1WJvdBFHlavWFfP9t4IBO_etYTh6bRpu1LmKgz1g-A)**
* **[학습된 디코더 모델 다운로드 (NIC using ResNet-152 16MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfNwJM0ZzUZMpYyS8MQUDkABwfxQQg5kILMlrzBJoGcpIA)**

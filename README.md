### PyTorch Neural Image Caption Generator

* 작성자: 나동빈(Dongbin Na / dongbinna@postech.ac.kr)
* 본 코드는 POSTECH의 **CSED703G 수업** 과제로 작성한 코드입니다.

### Show and Tell: A Neural Image Caption Generator (CVPR 2015)

* 흔히 NIC라고 알려진 네트워크를 제안한 논문입니다.
* NIC 학습/평가 전체 소스코드는 Google Colab을 이용해 실행할 수 있도록 작성했습니다.
* 성능 비교를 위하여 광범위한 실험을 진행했습니다.

#### [NIC using ResNet-101](Neural_Image_Captioning_(NIC)_using_ResNet_101.ipynb)

* ResNet-101을 이용할 때 상대적으로 학습 효율이 좋았습니다.
* <b>5번의 Epoch을 반복</b>하여 다음과 같은 성능을 낼 수 있었습니다.

|Cumulative BLEU Scores (표준)|BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|60.54|38.94|25.50|16.99|

|Individual BLEU Scores|BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|60.54|25.05|10.93|5.02|

* **[학습된 인코더 모델 다운로드 (NIC using ResNet-101 165MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERnDZFI8KD9OrX8rZGB4zucBLL1C2OQl5zdEIj9M23VH8A)**
* **[학습된 디코더 모델 다운로드 (NIC using ResNet-101 16MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfpMfIRuTy1NndX8U7C70XMBmu6wd3JofEo5T-uyIP8YOA)**

* <b>캡션(caption) 생성</b> 예시

![image](https://user-images.githubusercontent.com/16822641/100955005-1116cb00-3559-11eb-9662-7ab78c84b5d2.png)

> &lt;start&gt; a man is climbing a rock wall . &lt;end&gt;

#### [NIC using ResNet-152](Neural_Image_Captioning_(NIC)_using_ResNet_152.ipynb)

* 동일한 하이퍼 파라미터에서 ResNet-152로 바꾸면 다음과 같이 성능이 오히려 떨어질 수 있습니다.

|Cumulative BLEU Scores (표준)|BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|53.45|34.20|21.79|14.17|

|Individual BLEU Scores|BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC|53.45|21.89|8.84|3.89|

* **[학습된 인코더 모델 다운로드 (NIC using ResNet-152 225MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYnv1WJvdBFHlavWFfP9t4IBO_etYTh6bRpu1LmKgz1g-A)**
* **[학습된 디코더 모델 다운로드 (NIC using ResNet-152 16MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfNwJM0ZzUZMpYyS8MQUDkABwfxQQg5kILMlrzBJoGcpIA)**

### Show, Attend and Tell: Neural Image Caption Generation with Visual Attention (ICML 2015)

* 흔히 NIC with Attention이라고 알려진 네트워크를 제안한 논문입니다.
* NIC with Attention 학습/평가 전체 소스코드는 Google Colab을 이용해 실행할 수 있도록 작성했습니다.
* 성능 비교를 위하여 광범위한 실험을 진행했습니다.

#### [NIC using ResNet-101 with Soft Attention](Neural_Image_Captioning_(NIC)_using_ResNet_101_with_Soft_Attention.ipynb)

* ResNet-101을 이용할 때 상대적으로 학습 효율이 좋았습니다.
* <b>10번의 Epoch을 반복</b>하여 다음과 같은 성능을 낼 수 있었습니다
* Validation BLEU scores

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|65.52|42.73|26.38|16.02|

* Testing BLEU scores (beam size = 3)

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|63.83|46.05|32.28|22.24|

* Testing BLEU scores (beam size = 5)

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|64.07|46.49|32.82|22.90|

* **[학습된 모델 다운로드 (NIC using ResNet-101 with Soft Attention 317MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EX5AfxJbBstNmFWEvjBepqwB9wt5nwxYwwhJzwKIPyRSrQ)**

#### [NIC using VGGNet-19 with Soft Attention](Neural_Image_Captioning_(NIC)_using_VGGNet_19_with_Soft_Attention.ipynb)

* VGGNet-19을 사용하여 어텐션(attention) 정보를 시각적으로 잘 표현할 수 있습니다.
* ResNet-101과 비교했을 때 성능은 조금 떨어지지만 용량이 적어 효율적

![image](https://user-images.githubusercontent.com/16822641/100955415-d82b2600-3559-11eb-95c5-35c1e687029e.png)

* <b>10번의 Epoch을 반복</b>하여 다음과 같은 성능을 낼 수 있었습니다
* Validation BLEU scores

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|64.40|41.41|25.19|15.24|

* Testing BLEU scores (beam size = 3)

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|62.84|44.73|31.08|21.49|

* Testing BLEU scores (beam size = 5)

||BLEU-1|BLEU-2|BLEU-3|BLEU-4|
|---|---|---|---|---|
|NIC with Attention|62.87|45.03|31.25|21.44|

* **[학습된 모델 다운로드 (NIC using VGGNet-19 with Soft Attention 158MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EaS9knMWuv5Nr6-eeWwoTG8BvZNuR5YtJiJ8vRhe4vFvsw)**

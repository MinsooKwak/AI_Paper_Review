# Multimodal Machine Learning: A Survey and Taxonomy

- Paper : [Multimodal Machine Learning: A Survey and Taxonomy](https://arxiv.org/pdf/1705.09406.pdf) (2017)
</br>

**0. 기존 연구와 한계**
- 단일 모달에 대해서는 DL에서의 비지도학습이 성공적으로 적용
- Multimodal에 대한 연구가 부족했음 </br> </br>

**1. Contribution**
- multimodal에 대한 task들을 제안 (cross modal ect.)
- Modality 사이의 representation 처리 방식과 특정한 task에 대한 평가 </br> </br>

**2. Dataset**

오디오 뿐 아니라 영상에 대한 평가, 교차 평가 수행
- Audio Speech Classification
  - CUAVE
  - AVLetters </br> </br>

**3. Multi-Modal**
- 멀티모달은 multiple source로부터 연관된 정보들이 결합되어 있는 형태
- 결합 형태가 다양 (밀접하게 관련, 중간 수준 등)
- 모달 간의 우월성도 존재 (MacGurk effect)
- 해당 논문에서는 데이터의 관계가 mid-level 수준인 case에 주목 </br></br>

4. 추가 설명
- **MacGurk effect**
  - speech Recognition task에는 오디오, 시각 정보가 결합되어 있음
  - /ga/와 /da/ 발음을 영상과 배치해 실험 수행된 첫 케이스 </br></br>

- **데이터 간의 관계성**
  - "1차 상관관계(correlated at first order)" : image / 3-d depth scan
  - "중간 수준 (mid-level)" : audio /visual data </br></br>
  
----

### 실험
- supervised training / test phase 고정
- 모델만 변경하며 수행
- 3가지 세팅
  - multimodal fusion
  - cross modality learning
  - shared representation learning
- self-taught learning의 한 case
- 미세조정에 RBM(Restricted Boltzmann Machine) + greedy layer-wise training

  ![image](https://github.com/MinsooKwak/AI_Paper_Review/assets/89770691/3bfb0bdb-a3a8-41af-8270-7a0085fa904a)

</br></br>

**0. Sparse restricted Boltzmann machines (RBM)**



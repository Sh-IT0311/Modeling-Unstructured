# Modeling-Unstructured
## Deep Learning Process
0. Process
* 복잡한 문제를 ML/DL 문제로 치환 잘하기 
    * 단일 모델로 해결 할 수 있는지, 복수의 모델을 사용할지 설계를 잘 할 것
* SOTA + Awesome Paper 검색 잘하기 
    * ChatGPT의 견해도 도움이 많이 되었음
* Input → Output 을 명확히 할 것 
    * NLP의 경우 스페셜 토큰을 잘 정의해야할 수 있음
* 비즈니스 목적에 부합하는 평가지표 설계
* 일반화를 기대할 수 있는 Validation / Test Set 구성
* Baseline Model 을 통해 빠른 프로토타이핑 
    * Versioning과 성능 측정을 잘 할 것
    * 재현을 위해 Seed 설정을 잘 할 것
1. Input
* Data Analysis 
    * Data Distribution
    * (Relational) Inductive bias
* Pre-processing, Transform
    * 결과를 보고 틀린 케이스에 대해 개선 방향을 반영함
* Data Augmentation
2. Model( = Feature Extraction + Downstream Task)
* Normalization(Batch, Layer..)
* Activation Function
* Weight Initialization 
    * Gaussian Initialization 
        * Xavier, He Initialization
    * Transfer Learning 
        * Freeze 구간 설정에 대해 고민이 필요함
    * Self-Supervised Learning 
        * Pre-train Task를 구성해 직접 Pre-train을 구현해 볼 수 있음
        * Data Dependency, Tokenizing(NLP)
        * Contrastive Learning
 * Customize Model Layers
     * Inductive Bias
     * Feature Extraction 단계에서 Representation Power를 높이는 관점으로 연구함
     * 결과를 보고 틀린 케이스에 대해 개선 방향을 반영함
 * Ensemble 
     * 모델 간의 Correlation 낮아야 효과를 볼 수 있음
     * Ranker
3. Loss
* Input → Output의 의도를 모델에 잘 반영할 수 있도록 올바른 Loss 설계가 필요함
    * Task마다 사용하는 Loss Function마다 Loss의 Scale은 다를 수 있다. 즉, 절대적으로 작다고 해서 해당 Task에서 정말 작은지는 판단이 필요함
* Optimizer
* (Learning Rate) Scheduling
* Regularization(Overfitting : Noise에 예민하게 반응해서 발생하는 문제)
    * Early Stopping
    * Drop Out
    * L1, L2 Regularization
    * Weight Decay
    * R-DROP
    * R3F
* Gradient Accumulation / Clipping
* Cost-Sensitive Learning 
    * Policy Learning : (특히, 생성형 AI에 대해) Loss와 Performance 간에 불일치를 직접적으로 Align 시킬 수 있음
* Joint Learning
4. Output
* Post-processing
* Feedback 
    * Output Distribution VS Label Distribution
    * Gradient Distribution
    * Weight Distribution
    * Layer Distribution
    
## 토이프로젝트
* [FMCW 레이더를 활용한 Breathing Rate 추출](https://colab.research.google.com/drive/1d84s_-P4nSTnnM4FE9Jc6PFtbnDsE2Ga?usp=sharing)
* [안구 질병을 판별 하기 위한 CNN 기반 광간섭 단층촬영 이미지 분류](https://colab.research.google.com/drive/1fNuloWRSR9iws_Gh2OUWIB3BuShYwOse?usp=sharing)

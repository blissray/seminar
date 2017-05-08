### Multi-Label Learning Algorithms
- Problem Transformation Methods : Multi Label 알고리즘을 다른 형태의 문제로 변환하여 해결함, Fit data to algorithm
    - Binary Relevance - first-order approaches
    - Calibrated Label Ranking - second-order approach
    - Random k-Labelsets - Multi-label Learning을 Mullti Class Classification 으로 변환
- Algorithm adaption methods:  기존 알고리즘을 직접 Multi-Label 문제에 적용하여 해결함, Fit data to algorithm
    - ML-kNN - First-order approach, Adopting lazy learning techniques
    - ML-DT - decision tree techqnies
    - Rank-SVM - second order technqiues
    - CML - Adapting information-theoretic technqiues

- First-order approach
    - 라벨별로 Classifier를 구축하여 병렬 구현이 용이, 1개의 Training Set에 대해 q개의 Classifier를 병렬적으로 구현.
- High-order approach
    - Reandom 하게 Label 간의 상간관계를 고려하는 방식임

- Binary Relevance
   - 예는 일단 모든 Label에 대한 Classifier를 만들어서 각 데이터 별로 다 돌려 보는 것
   - Label에서 데이터가 모두 0일경우 즉 포함되지 않을 경우, 가장 확률이 높은 놈을 포함시키다.\
   - 일반적으로 직관적으로 나눈다는 장점이 있고, 많은 Multi-Label 문제에 사용된다는 점이 있음
   - 그러나 Label 간의 상관관계가 존재하는 걸 무시하고, q가 크고 Label Density(많은 정도가) 낮을때, Class 분균일 문제가 발생할 수 있음

- Classifier Chains
    - 기존 y 값에 대한 순엽 function을 만들어서
    - 학습을 할때 Training Set에 학습할 데이터를 연결해서 붙임
    - 그걸로 학습을 해서 결과 값을 예상함
    - BR에 비해 변수간의 상관관계가 학습할 때 포함되지만, 병렬적 학습이 어렵다는 단점이 있음
    - 나이브 베이지안 같은 것을 사용하여 사후 확률을 예측할 수 있는 장점이 있음

- Calibrated Label Ranking



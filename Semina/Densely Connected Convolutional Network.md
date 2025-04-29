# Densely Connected Convolutional Networks (CVPR 2017)

- **학회/년도**: CVPR 2017
- **원문 링크**: [https://arxiv.org/abs/1608.06993](https://arxiv.org/abs/1608.06993)

## 1. 요약
DenseNet은 CNN 아키텍처에서 각 레이어가 모든 이전 레이어의 출력을 입력으로 받아 feature reuse를 극대화하는 방법을 제안합니다. 이 구조는 그래디언트 흐름을 개선하고, feature를 재활용하며, 파라미터 수를 효율적으로 줄이는 데 기여합니다. DenseNet은 다양한 이미지 분류 벤치마크 (CIFAR, ImageNet)에서 뛰어난 성능을 기록했습니다.

## 2. 핵심 아이디어
- **Dense Connectivity**: 레이어 \(l\)의 입력이 0부터 \(l-1\)까지의 모든 이전 레이어의 feature map을 연결(concatenate)한 것.
- **Feature reuse**: 이전 layer의 출력을 재사용하여 redundancy를 줄이고 효율을 높임.
- **Improved gradient flow**: 깊은 네트워크에서도 그래디언트 소실(vanishing gradient) 문제를 줄임.

## 3. 기여도
- CNN 구조 설계에 대한 혁신적 접근 제안
- 적은 파라미터로도 높은 성능 달성
- Feature propagation, Feature reuse, Feature preservation을 모두 달성
- 후속 연구들(e.g., EfficientNet, DenseASPP 등)에 영향을 끼침

## 4. 한계점
- 메모리 사용량이 많아짐 (모든 레이어의 feature map을 저장해야 함)
- 일부 경우에서 inference 속도가 느려질 수 있음
- Dense connection으로 인한 구조 복잡성 증가

## 5. 개인적인 생각
DenseNet은 ResNet 이후의 CNN 아키텍처 진화에 있어 중요한 이정표라고 생각합니다. 특히 feature reuse 개념은 이후 다양한 네트워크 최적화 전략에도 영감을 주었습니다. 다만 실제 산업 적용 시 메모리 최적화가 필요한 경우가 많아, DenseNet의 구조를 변형하거나 pruning 기법과 함께 사용하는 것이 필요할 것 같습니다.


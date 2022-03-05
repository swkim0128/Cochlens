# 👂 Cochlens
| 청각 장애인을 위한 비대면 취미 학습 플랫폼

## 👨‍👩‍👦 팀원 소개

- **강태훈**
    - Github: [@xktmxkem](https://github.com/xktmxkem)
- **김성우**
    - Github: [@swkim0128](https://github.com/swkim0128)
- **박지유**
    - Github: [@icehoney0208](https://github.com/icehoneypark)
- **이수환**
    - Github: [@essk13](https://github.com/essk13)
- **이재희**
    - Github: [@Hui-Story](https://github.com/Hui-Story)

## ****📆**** 프로젝트 개요

- **진행 기간** :  2022/01/10 ~ 2022/02/18
- **목표**
    - 청각 장애인 분들이 온라인으로 취미를 학습 할 수 있는 플랫폼을 개발 합니다.
    - 소리가 들리시지 않더라도 학습을 위한 보조 기능을 설계해 청각 장애인 사용자 분들의 학습을 돕습니다.
    - 원활한 학습 진행을 위한 UI/UX를 설계하여 사용자 분들이 쾌적한 플랫폼 서비스를 누릴 수 있도록 유도합니다.
- **기대 효과**
    - 코로나 사태로 인해 감소한 장애인 분들의 삶의 만족도 증진
    - 장애인 분들의 학습권이 지켜지지 않던 기존의 비대면 화상 강의 시스템에 대한 재고
- **🖼와이어프레임**
    - [와이어프레임 보러 가기](https://www.figma.com/file/GpG25exfNrOLTNtQpBWVNo?embed_host=notion&kind=&node-id=0%3A1&viewer=1)

## ****✍**** 프로젝트 소개

**Cochlens**는 청각 장애인을 위한 온라인 화상 취미 클래스 학습 플랫폼 입니다.

코로나 19 바이러스의 대유행 이후 우리의 생활은 완전히 뒤바뀌게 되었습니다.  특히 대면으로 진행하던 많은 서비스들이 비대면으로 전환이 이루어지게 되었습니다. 실제로 학교 수업의 비대면 전환율은 크게 올라갔고 많은 학생들이 이에 익숙해져 가고 있습니다. 하지만 여전히 비대면 학습에 익숙해지기 어려운 분들이 있습니다. 비대면 학습의 특성상 모니터와 스피커에 의존해야 하는 만큼 청각장애인 분들에게 비대면 학습이란 여전히 넘기 어려운 벽으로 존재하고 있습니다. 따라서 이번 프로젝트에서 청각 장애인 분들의 학습권을 보장하기 위한 취미 학습 플랫폼 **Cochlens**를 개발하게 되었습니다. 

**Cochlens**는 비대면 취미 학습 플랫폼입니다. 코로나로 인해 모두의 삶의 만족도가 감소하였지만, 그 중에서도 장애인 분들의 삶의 만족도는 더욱 크게 감소하였습니다. 저희는 삶의 만족도를 올리는 요소 중 취미 개발을 생각하여, 청각 장애인 분들이 비대면으로 취미를 배우고 이를 통해 삶의 만족도를 올리는 서비스를 목표로 하였습니다. 따라서 원할한 취미 학습을 위해 청각 장애인 분들의 소통 방식을 공부하고 연구하였습니다. 우선, 실시간 자막 기능으로 강사가 말하는 음성을 텍스트로 변환하여 학생들이 쉽게 수업 흐릅을 따라갈 수 있도록 구성하였습니다. 또한 자막으로 미처 변환하지 못한 텍스트를 대비하여 강사의 입모양을 클로즈업하여 청각 장애인 분들의 구어 소통을 돕도록 구현하였습니다. 마지막으로 취미 클래스인 만큼 손을 사용하기 힘든 상황을 대비하여 간단한 모션만으로 강사에게 의미가 전달되는 모션 커멘드를 추가하였습니다. 이 외에도 원할한 학습을 위해 개인 수강 목록과 학습 진행도를 파악할 수 있도록 하였으며, 청각 장애인 분들의 시각에서 서비스를 바라 볼 수 있도록 노력하였습니다.

**Cochlens**를 통해 베리어 프리 문화를 알리며, 모두가 함께 나아가는 사회를 만들어 나갑니다.

## 🛠️ 서비스 아키텍쳐

- Vue3 (Web Server)
- MySQL (DB)
- Springboot (API Server)
- Kurento (Docker)
- Jenkins

## ****⭐️**** 주요 기능

### 라이브 취미 클래스 (WebRTC)

- 강사는 취미 클래스를 개설하고 강좌를 등록할 수 있습니다.
- 사용자는 원하는 취미 클래스를 등록하고 라이브 클래스를 수강할 수 있습니다.

### 실시간 라이브 자막 (STT)

- Microsoft Azure의 STT API를 사용합니다.
- 강사가 말하는 음성을 인식하여 텍스트로 변환한 뒤 수업을 듣는 학생들에게 자막을 보여주게 하는 기능입니다.

### 강사의 입모양 클로즈업 (face-api)

- 청각 장애인의 구어 인식을 편하게 하기위한 기능입니다.
- 강사의 얼굴을 인식 후 확대하여 강사 강의 화면 오른쪽 상단에 보여줍니다.
- 사용자는 확대된 강사의 얼굴을 보고 구어를 조금 더 쉽게 인식할 수 있습니다.

### 모션 커멘드 (Teachble Machine)

- 사용자가 특정 말을 하고 싶을 때 모션인식을 통하여 클래스 강의를 듣는 사람들에게 전달하는 기능입니다.
- 청각 장애인이 말을 할 수가 없고, 채팅 기능을 통한 대화가 힘들 때, 간단하게 모션인식으로 통하여 원하는 말을 사람들에게 전달해주는 기능입니다.
- 기능 구현은 완료하였지만 강사의 입모양 클로즈업(face-api) 기능과의 충돌로 최종 프로젝트에서는 임의로 막아놓은 상태입니다.

## ****😋**** Installation

### [Frontend]

```bash
cd frontend
npm i
npm run serve
```

### [Backend]

```bash
# java build
$ gradlew clean build 
# docker-compose
$ docker-compose up -d --build
```

## ****⚙**** 개발 환경 및 IDE

- Java (1.8.0_312-1)
- MySQL (5.7.35)
- Intellij IDEA (2021.3.2)
- VSCode (1.59)
- Docker (Desktop 4.3.2)
- node.js (17.3.0)
- Vue3 (3.2.26)
- kurento (6.16.0)
- gradle (v7.3.3)

## ****🎞**** 최종산출물

- 중간발표
    
    [Cochlens 중간발표.pdf](documentation/Cochlens_중간발표.pdf)
    
- 최종발표
    
    [Cochlens 최종발표.pdf](documentation/Cochlens_최종발표.pdf)

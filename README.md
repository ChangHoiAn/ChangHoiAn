<div align="center">

# 👋 안녕하세요! 임베디드 시스템 & IoT 개발자 **안창회**입니다.

임베디드 펌웨어부터 **Linux 디바이스/드라이버**, Edge/Robot 시스템까지
임베디드와 Linux 기반 시스템을 연결하는 프로젝트를 진행해왔습니다.

</div>

---

## 🧑‍💻 About Me

- **임베디드 시스템 & IoT 개발자**
- **관심 키워드:** MCU Firmware · USB/Serial · Linux Driver · ROS2 · Edge AI · System Integration

---

## 🧩 Embedded Strength

- **Firmware**: 인터럽트 기반 이벤트 처리, 센서/모터 제어, 프로토콜 프레이밍(고정 프레임/검증)
- **Linux Interface**: `/dev/*` 기반 I/O 흐름 이해, 커널 드라이버 구조 학습 및 연동
- **Field-ready 통합**: 네트워크 불안정/현장 환경 고려한 자동 실행 + 복구(Recovery) 설계

---

## 🧰 기술 스택

<p align="center">
  <img src="https://img.shields.io/badge/-STM32-03234B?style=flat&logo=stmicroelectronics&logoColor=white" />
  <img src="https://img.shields.io/badge/-Linux-FCC624?style=flat&logo=linux&logoColor=black" />
  <img src="https://img.shields.io/badge/-RaspberryPi-A22846?style=flat&logo=raspberrypi&logoColor=white" />
  <img src="https://img.shields.io/badge/-ROS2-22314E?style=flat&logo=ros&logoColor=white" />
  <img src="https://img.shields.io/badge/-Qt-41CD52?style=flat&logo=qt&logoColor=white" />
  <img src="https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/-MySQL-4479A1?style=flat&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/-Bluetooth-0082FC?style=flat&logo=bluetooth&logoColor=white" />
  <img src="https://img.shields.io/badge/-WiFi-000000?style=flat&logo=wifi&logoColor=white" />
  <img src="https://img.shields.io/badge/-HailoAI-FF6F00?style=flat" />
</p>

---

## 🚀 Featured Project

### ☕ USB-MACRO — 원클릭 로봇 실행 Smart USB Bridge (Store & Forward + Recovery)
- **Repo:** [USB-Macro](https://github.com/won-jong-wan/USB-Macro)
- **한 줄:** PC에서 명령 패킷 “적재(Store)” → 로봇 연결 시 “자동 실행(Run)” + 네트워크 장애 시 “시리얼 복구(Recovery)”
- **Embedded Point**
  - **256Byte 고정 프레임** 프로토콜로 패킷 경계/검증/디버깅 용이
  - **USB Vendor + SD 저장** 기반 Store-and-Forward로 테스트 재현성 강화
  - **CDC↔UART Serial Console**로 SSH/네트워크 장애 상황에서도 현장 복구 가능
  - PC(Qt) / Linux 커널 드라이버(/dev) / RPi daemon까지 연결

```mermaid
flowchart LR
  PC["PC<br/>Qt Client + /dev/custom_usb_pc"] -->|"Vendor 256B STORE"| MCU["STM32 Black Pill<br/>TinyUSB Vendor + SD Store"]
  MCU -->|"Vendor 256B SEND"| RPI["Raspberry Pi<br/>/dev/custom_usb_rpi + daemon"]
  RPI --> RUN["Execute<br/>ROS2 / System Command"]
```

---

## 🚀 주요 프로젝트

### 🧷 Linux Device Driver — 모듈 기반 시계 디바이스 드라이버
- **Repo:** [Project-DeviceDriver](https://github.com/ChangHoiAn/Project-DeviceDriver)
- **Embedded Point**
  - 커널/유저 영역 경계에서 디바이스 제어 흐름 설계 및 구현
  - 기능을 모듈로 분리해 드라이버 구조와 유지보수성 중심으로 정리

---

### 🤖 Raspberry Pi5 + Hailo 기반 AI 면접 시스템 (Edge AI)
- **Repo:** [Project-AI-Interview-system](https://github.com/ChangHoiAn/Project-AI-Interview-system)
- **내용**
  - Raspberry Pi5 + Hailo 가속기로 정량적 AI 면접 구현
  - 웹캠으로 자세·표정 XML 저장
  - PC 클라이언트가 XML을 받아 LLM(Gemini) 분석 → 면접 점수 제공
  - 면접 시작/종료 명령 전송, 녹화 및 데이터 처리 자동화

---

### 🔐 IoT 기반 실시간 침입 감지 시스템 (MCU ↔ SBC ↔ DB ↔ Arduino)
- **Repo:** [Project-Instruction-Detection-system](https://github.com/ChangHoiAn/Project-Instruction-Detection-system)
- **내용**
  - STM32 GPIO 인터럽트로 이벤트 감지
  - Wi-Fi로 Raspberry Pi → MySQL 저장
  - 침입 시 Bluetooth로 Arduino 제어 → 부저/LED/LCD

---

### ☀️ 태양광 추적 시스템 (센서 + 액추에이터 제어)
- **Repo:** [Project-Solar-Tracking-system](https://github.com/ChangHoiAn/Project-Solar-Tracking-system)
- **내용**
  - STM32 기반 태양 위치 추적 → 효율적 에너지 수집
  - 서보 모터 제어 및 센서 데이터 처리

---

### ⚙️ 모터 제어 및 MATLAB Simulink 시뮬레이션 (센서리스 모터 제어)
- **Repo:** [Project-Motor-Control](https://github.com/ChangHoiAn/Project-Motor-Control)
- **내용**
  - PMSM 모터 속도 제어 Simulink 구성 및 실행
  - C2000(TMS) MCU 기반 속도 제어 구현

---

### 🎹 RTOS 기반 신디사이저 (STM32 Black Pill + FreeRTOS)
- **Repo:** [Project-신디사이저](https://github.com/won-jong-wan/SYNTH_RTOS_BLACKPILL)
- **내용**
  - STM32 F4(Black Pill)와 FreeRTOS를 활용해 실시간 오디오 합성 및 파형 제어를 구현한 임베디드 전자 악기
  - 오디오 처리, 입력 감지, 디스플레이 갱신을 멀티태스킹 환경에서 안정적으로 구동
- **Embedded Point**
  - RTOS Task 설계: Audio 생성, Input(로터리, 스위치), UI 태스크를 분리하고 우선순위 스케줄링으로 Audio Latency 최소화
  - IPC: Queue와 Semaphore를 활용해 사용자 입력(ISR/Task)과 오디오 엔진 간 Thread-Safe 데이터 동기화
  - Resource 최적화: 제한된 MCU 자원 내에서 DMA 및 버퍼링을 활용한 끊김 없는 파형 출력 구현


---

## 💡 관심 분야

**Embedded System | RTOS | Device Driver | USB/Serial | Motor Control | ROS2 | Linux Kernel | Edge AI**

---

## 📫 연락처
- **Email:** changhoian99@gmail.com

---

<div align="center">

## ⭐ GitHub Stats
[![Metrics](./github-metrics.svg)](https://github.com/lowlighter/metrics)

</div>

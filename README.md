<div align="center">

# 🚨 삐용 BBIYONG

**CCTV 와 순찰 로봇으로 화재를 먼저 찾는 통합 관제 시스템**

CCTV 영상에서 AI 가 불꽃·연기를 감지하면, 순찰 로봇이 현장으로 가서 확인하고 관제 화면에 바로 알린다.

삼성 청년 SW·AI 아카데미(SSAFY) 15기 공통 프로젝트 · 2026.07 – 2026.08 · 6인 팀

</div>

---

## 구성

| 부분 | 폴더 | 내용 | 기술 |
|---|---|---|---|
| 관제 화면 | [`FE/bbiyong-react`](FE/bbiyong-react) | CCTV·로봇 상태와 화재 알림을 보는 통합 관제 대시보드, 3D 지도 | React · TypeScript · Vite · three.js · HLS · STOMP |
| 관제 서버 | [`BE_system`](BE_system) | 알림·영상·로봇 상태를 실시간으로 중계하는 API · WebSocket 서버 | Spring Boot · WebSocket |
| 순찰 로봇 | [`BE_robot`](BE_robot) | 로봇 주행·지도 작성(SLAM)·센서 펌웨어·온보드 대시보드 | ROS 2 · Jetson Orin · Python |
| 화재 감지 AI | [`AI`](AI) | 불꽃·연기 객체 탐지 모델 학습·평가·Jetson 배포 | YOLO(Ultralytics) · D-Fire · FASDD · ONNX/TensorRT |
| 설계 문서 | [`docs`](docs) | 기획서·기능명세서·API 명세·아키텍처·시뮬레이션 | — |

## 맡은 일 (이예승)

- **기획** — 서비스 기획서·기능명세서, 관제 시나리오
- **프론트엔드** — 관제 대시보드 화면

## 팀

모진성 · 이예승 · 장효준 · 박재현 · 이승현 · 고지혁

> 이 저장소는 SSAFY GitLab 에서 진행한 원본을 포트폴리오용으로 옮긴 것입니다.
> 팀원 개인 메일은 가렸고, 용량이 큰 학습 결과 모델(`*.pt`)과 시험 영상은 뺐습니다 — 모델은 [`AI/README.md`](AI/README.md) 의 방법으로 다시 학습할 수 있습니다.

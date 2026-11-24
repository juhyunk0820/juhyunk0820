# Juhyun Kang (강주현)

> **React Native · Python · OpenAI API** | 모바일 앱을 출시하고, 서버와 AI 기능을 연결해 제품을 만드는 개발자

📍 Seoul, Korea · 🎓 세종대학교 컴퓨터공학과 (2019.03–2026.02, 졸업) · 📱 iOS / Android

---

## 👋 About Me

React Native를 기반으로 고객의 요구를 앱 기능으로 구현하고 출시까지 연결한 개발자입니다. **대모산개발단 프리랜서 프론트엔드 개발자**로 **AI 펫닥터**와 **Healing Sound**를 개발했습니다. AI 펫닥터는 8인 팀에서 앱 프론트엔드를 단독 담당해 양대 스토어 출시와 후속 개선까지 진행했습니다.

PM 공백기에 고객·백엔드·디자이너와 결제 기능의 개발 범위와 일정을 조율했습니다. PASS 본인인증, Toss Payments 결제, Firebase 알림을 연동하고, 실기기에서 채팅방을 나가면 AI 답변이 끊기는 문제를 재현해 SSE 응답을 끝까지 수신하도록 고쳤습니다.

개인 프로젝트 **Artiv**에서는 Spring Boot로 작품별 접근 권한을 검사하는 API를 구현하고 계정을 바꿔 로컬에서 검증했습니다. **주식 자동매매 프로그램**에서는 OpenAI API가 종목 후보를 선정하고, 별도 세션의 거래 평가를 다음 후보 선정 요청에 반영하는 흐름을 구현했습니다.

### 🏆 Awards
- 🥈 **세종대학교 컴퓨터공학과 캡스톤 디자인 우수상 (2등)** — AI 기반 실시간 교통안내 시스템
- 🥉 **교내 창업시연대회 3등** — AI 페어링 앱 (데이팅 매칭 서비스)

### 💼 Key Experiences
- 📱 React Native 앱 **App Store / Play Store 정식 출시** 경험
- 🛠 **Expo / React Native CLI / EAS** 세 가지 환경 모두 실전 경험
- 🧩 BLE, 소셜 로그인(Apple/Kakao/Google), 결제(Toss Payments), 본인인증(PASS) 연동 경험
- 🔁 **GitHub Actions + Fastlane** 및 **EAS Build/Submit** 기반 CI/CD 구축 경험
- 🧮 A* 알고리즘 구현, 공공데이터포털 VDS 수집·정제·DB 인덱싱 경험

---

## 🚀 Featured Projects

### AI 펫닥터 — 반려동물 건강상담 앱

> **대모산개발단 프리랜서 프로젝트 (2025.11–2026.04)** — 반려동물 건강상담·커머스·멤버십 앱. **8인 팀 중 앱 프론트엔드 단독 담당, 2026.03 양대 스토어 v2.0 출시 및 v2.0.6 개선.** 백엔드·AI 모델은 별도 담당자가 개발했습니다.

**Key Contributions**
- `결제 구조 개선` — AI 펫닥터에서 Apple 인앱결제 대신 **Toss Payments PG 결제**를 연동해 결제 구조를 변경하고, 수수료 **30% → 3%** 구조 확보
- `커머스·정기결제` — 구매·장바구니·결제 내역·취소와 멤버십 정기결제의 앱 흐름 구현, 카드 등록 절차·상태 표시 추가
- `PASS 본인인증` — 인증 여부·CI와 PetPass 등록 상태를 가입·로그인·정보 입력 흐름에 연동
- `상태 관리` — TanStack Query로 서버 데이터를, Zustand로 로그인·화면 상태를 관리
- `AI 보조 개발·검증` — Figma MCP와 화면별 테스트 프롬프트를 활용하고, 버튼 연타와 결제 완료 후 뒤로가기 오류를 직접 재현해 수정·재검증

**Tech Stack** `React Native` `TypeScript` `Expo` `React Query` `Zustand` `Toss Payments`

<a href="https://apps.apple.com/kr/app/id6484592134"><img src="https://img.shields.io/badge/App_Store-0D96F6?style=for-the-badge&logo=app-store&logoColor=white" /></a>
<a href="https://play.google.com/store/apps/details?id=com.anlicy.petdoctor"><img src="https://img.shields.io/badge/Google_Play-414141?style=for-the-badge&logo=google-play&logoColor=white" /></a>
<a href="https://juhyunkang-portfolio.notion.site/"><img src="https://img.shields.io/badge/📖_Portfolio-FF5722?style=for-the-badge" /></a>

> 📝 **코드는 클라이언트 소유 private 레포로 관리되므로 공개되지 않습니다. 포트폴리오 링크에서 상세 내용을 확인하실 수 있습니다.**

---

### 주식 자동매매 프로그램 — 주문 기록과 LLM 피드백

> **개인 프로젝트 · 2026.11 – 현재 · 개발 중** | Electron·React 화면과 독립 Python 엔진을 나눠 설계한 Windows 앱입니다.

- **주문 상태 확인** — KIS WebSocket 시세를 화면에 반영하고, 주문별 접수·부분 체결·잔량을 SQLite에 기록해 모의 주문 내역과 대조했습니다.
- **LLM 오케스트레이션** — OpenAI API로 후보를 선정합니다. 별도 세션에서 보유 기간의 시세 변화와 시장 참여자 매매 데이터를 바탕으로 거래별 판단을 평가하고, 그 결과를 다음 후보 선정 요청에 반영합니다.
- **예외 처리** — 주문 응답이 유실되면 중복 전송을 차단하도록 구현하고 가상 응답으로 검증했습니다.

---

## 🛠 Tech Stack

**Mobile / Frontend**
<br/>
<img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
<img src="https://img.shields.io/badge/Expo-1B1F23?style=for-the-badge&logo=expo&logoColor=white" />
<img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" />
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />

**State Management & Data**
<br/>
<img src="https://img.shields.io/badge/React_Query-FF4154?style=for-the-badge&logo=reactquery&logoColor=white" />
<img src="https://img.shields.io/badge/Zustand-2D3748?style=for-the-badge" />
<img src="https://img.shields.io/badge/Redux-764ABC?style=for-the-badge&logo=redux&logoColor=white" />

**DevOps & Tools**
<br/>
<img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white" />
<img src="https://img.shields.io/badge/Fastlane-00F200?style=for-the-badge&logo=fastlane&logoColor=white" />
<img src="https://img.shields.io/badge/EAS-000020?style=for-the-badge&logo=expo&logoColor=white" />
<img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
<img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />

**Collaboration**
<br/>
<img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" />
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white" />

---

## 📂 Projects

| Project | Description | Tech | Link |
|---------|-------------|------|------|
| **AI 펫닥터** | 대모산개발단 프리랜서 · AI 기반 반려동물 건강상담 앱 · **스토어 정식 출시** | RN, TS, Toss Payments | [App Store](https://apps.apple.com/kr/app/id6484592134) · [Play Store](https://play.google.com/store/apps/details?id=com.anlicy.petdoctor) |
| **AI 기반 실시간 교통안내 시스템** | VDS 수집·정제·결측 보완·A* 구현 · **캡스톤 우수상(2등)** | React, Flask REST 연계, LightGBM, A* | [FE](https://github.com/AI-based-ETA/Capstone_Kakaomap) · [Org](https://github.com/AI-based-ETA) |
| **Healing Sound** | 대모산개발단 프리랜서 · Android 웰니스 디바이스 BLE 연동 앱 · 고객 시연 후 BLE PoC 납품 | RN, BLE, 로컬 DB | *private* |
| **Wit** | 여행 동행찾기 앱 · GitHub Actions + Fastlane CI/CD | RN, Expo, Zustand, React Query | [Repo](https://github.com/withtravel/FE-WitCli) |
| **AI 페어링 앱** | AI 궁합 분석 데이팅 앱 · **창업시연대회 3등** | RN CLI, Redux, 네이티브 코드 | *private* |
| **항공 사고 조회 앱** | 기종·항공사·날짜 검색·필터링 앱 (별도 외주) | RN, React Query, Zustand | [Repo](https://github.com/InquiryingAccident/IA-FE) |
| **Malsami** | 세종대 자료 게시판 앱 확장 · 모바일 API 협업 · EAS Build/Submit | RN, Expo | *private* |
| **Match** | 테니스 대회 신청 앱 | RN, Expo | [Repo](https://github.com/Team-ServeItUp/FE-MatchExpo) |

---

## 📈 GitHub Stats

![juhyunk0820's GitHub stats](https://github-readme-stats.vercel.app/api?username=juhyunk0820&show_icons=true&theme=tokyonight&count_private=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=juhyunk0820&layout=compact&theme=tokyonight)

---

## 📫 Contact

- 📧 **Email** — kjh002899@gmail.com
- 📱 **Phone** — 010-9642-4868
- 📖 **Portfolio** — [포트폴리오](https://juhyunkang-portfolio.notion.site/)

---

<p align="center"><i>"동작하는 코드를 넘어, 사용자에게 도달하는 제품을 만듭니다."</i></p>

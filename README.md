<div align="center">

# 🐿️ 다람쥐택시 — 예약·운영 관리 서비스

**🇰🇷 한국어** &nbsp;·&nbsp; [🇬🇧 English](./README.en.md)

> ### "교통이 끊기면, 생활도 끊긴다."
>
> 충북 옥천군 청산면의 **이동권**을 위한 다람쥐택시 예약·운영 디지털 서비스

![Award](https://img.shields.io/badge/🥇_1등_·_Social_Value_Award-Tech_for_Impact_Campus_2026-FFE500?style=for-the-badge&labelColor=1A1A1A)
&nbsp;
![Team](https://img.shields.io/badge/팀_연송이-Yonsei_University-F2994A?style=for-the-badge&labelColor=1A1A1A)

[![Live Demo](https://img.shields.io/badge/🔗_프로토타입_바로가기-daramjwi--taxi--client.vercel.app-F2994A?style=for-the-badge&labelColor=1A1A1A)](https://daramjwi-taxi-client.vercel.app/)

</div>

---

## 🥇 Tech for Impact Campus 2026 · 1등 (사회가치상) 수상

연세대학교 × kakao!mpact가 함께한 **Tech for Impact Campus** 성과 공유회에서
**옥천신문 — 팀 연송이**가 **1등(사회가치상)** 을 수상했습니다.

<div align="center">

<!-- 📸 시상식 사진 자리 -->
<img width="600" height="450" alt="KakaoTalk_20260619_173317412" src="https://github.com/user-attachments/assets/eea28383-d806-4fb0-a891-4f5999a9037b" />


</div>

---

## 🔗 프로토타입 체험하기

👉 **[다람쥐택시 앱 바로가기](https://daramjwi-taxi-client.vercel.app/)** &nbsp;— 휴대폰으로 열면 가장 자연스럽습니다.

휴대폰 카메라로 아래 QR을 찍으면 바로 열립니다.

<div align="center">
<img width="216" height="216" alt="daramjwi_qr" src="https://github.com/user-attachments/assets/6309a344-3212-42b0-baca-d4fd46fffdfd" />
</div>

---

## 🚐 우리가 푼 문제
<img width="520" height="360" alt="image" src="https://github.com/user-attachments/assets/4b8164b8-81ad-403a-9376-cd475ea4fa3a" />
<img width="512" height="326" alt="image" src="https://github.com/user-attachments/assets/9b755f95-9fdc-4453-b651-455d48e7b7cc" />
<img width="512" height="326" alt="image" src="https://github.com/user-attachments/assets/27031478-85e0-4430-b48b-079b93991ec1" />


청산면 주민은 병원·시장·관공서를 가려면 옥천 읍내로 나가야 합니다.
하지만 버스는 배차 간격이 길어 한 번 놓치면 **1시간 이상** 기다려야 하고,
일반 택시는 읍내까지 **약 6만 원**으로 일상적인 대안이 되기 어렵습니다.

옥천군에는 이를 위한 좋은 제도, **다람쥐택시**가 이미 있습니다.
버스 요금 수준(**1,700원**)으로 택시를 이용할 수 있고, 차액은 군 예산으로 보전됩니다.
다만 마을 단위로 **하루 4회 · 월 112회**라는 한도가 있어, 제한된 운행을 마을 안에서 고르게 조율하는 일이 핵심입니다.

문제는 그 좋은 제도가 여전히 **전화·기억·수기 메모**에 의존한다는 점이었습니다.
주민은 이장님께 전화로 가능 여부를 확인하고, 기사님은 운행 중 전화를 받아 예약을 기억해야 했습니다.

> **그래서 우리는 문제를 다시 정의했습니다.**
> 진짜 문제는 *이동수단의 부재*가 아니라,
> **제한된 공공 이동 자원을 함께 조율하는 시스템의 부재**였습니다.

---

## 💡 해결 방식

도시형 호출 앱(개인 호출·결제 등록·실시간 배차)을 그대로 옮기지 않았습니다.
고령 주민에게는 앱 설치 자체가 장벽이 되고, 농촌에서는 *개인 즉시 호출*보다 *마을 단위 자원 조율*이 더 중요하기 때문입니다.

설계 원칙은 **Culture in Action** — *현장을 바꾸지 않고, 현장에 맞게 연결*하는 것이었습니다.
앱이 편한 주민에게는 직접 신청 경로를, 앱이 어려운 주민에게는 기존 전화 방식을 그대로 남겼습니다.

| 구분 | 역할 |
| --- | --- |
| 👵 **주민용 앱** | 탑승 신청 · 오늘 운행 · 마을 현황 · 내 예약 · 잔여 횟수 확인 |
| 🚕 **기사용 앱** | 앱·전화 예약 통합 입력 · 운행 현황 · 확정/취소 · 월별 현황 관리 |

주민이 앱을 쓰든 전화로 신청하든, 예약 정보는 결국 **기사님 앱 한 곳으로** 안정적으로 모입니다.
제한된 운행 횟수를 효율적으로 쓰기 위한 **동승 묶기 기능**도 함께 설계했습니다.

> 1·2차 유저테스트를 거치며 *이장님용 앱 → 기사님용 앱*으로 핵심 사용자를 피벗했고,
> 72세 택시회사 상무님이 5개 과제를 모두 수행하며 사용성을 검증했습니다.
> 옥천군청 도시교통과로부터 **47개 마을 전체 상용화** 제안을 받아, 수요응답형 교통(DRT) 운영 플랫폼으로 확장을 준비하고 있습니다.

---

## 🗺️ 서비스 구조도

<div align="center">
<img width="2001" height="1125" alt="daramjwi_architecture" src="https://github.com/user-attachments/assets/44096a12-1eaf-4472-b123-ada2aedd6b8d" />
</div>

주민용·기사용은 하나의 **Next.js PWA**(역할 선택 후 분기)로 동작하며, 백엔드 **REST API 서버**(Next.js · Vercel)와 **Supabase**(PostgreSQL · Auth · Realtime)를 함께 사용합니다. 클라이언트는 OTP 인증과 실시간 동기화를 위해 Supabase에 **직접** 연결되기도 합니다. 인증은 **카카오 로그인(OAuth 2.0)**, 알림은 **Web Push(VAPID)** — SMS·알림톡은 사업자 연동 후 추가될 예정입니다.

---

## 🛠️ 기술 스택

![Next.js](https://img.shields.io/badge/Next.js_15-000000?logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?logo=pwa&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
![Kakao](https://img.shields.io/badge/Kakao_Login-FFCD00?logo=kakao&logoColor=000000)

- **Frontend** — Next.js 15, TypeScript, PWA (서비스워커 · 웹 푸시 알림)
- **Backend** — Supabase (PostgreSQL · Auth · Realtime), Vercel 배포
- **Auth** — Kakao OAuth, Supabase 휴대폰 OTP
- **고령 사용자 설계** — 큰 터치 영역, 직접 입력 최소화(최초 1회 등록 후 버튼 중심), 랜드마크 기반 안내

---

## 📦 레포지토리

| Repository | 설명 |
| --- | --- |
| [`daramjwi-taxi-client`](../../daramjwi-taxi-client) | 주민용·기사용 통합 PWA 프론트엔드 |
| [`daramjwi-taxi-server`](../../daramjwi-taxi-server) | 예약·운행·정산 API 서버 (Supabase + Next.js) |

🔗 **Live** — https://daramjwi-taxi-client.vercel.app/

---

## 👥 팀 연송이

| 이름 | 역할 |
| --- | --- |
| 유지희(팀장) | Backend · Server |
| 김설 · 공윤아 | UI/UX Design |
| 연석인 | Frontend · Product Direction |
| 윤예진 | Planning · Presentor | 
| 정호영 | Planning |

---

## 🙏 With

프로젝트의 방향을 잡아주신 **강연아 교수님 · 송진영 교수님**,
현장을 열어주신 옥천신문 **황민호 대표님**,
기획부터 기술 구현까지 함께 고민해주신 kakao **제이(Jay) 멘토님 · 에릭(Eric) 멘토님**께 감사드립니다.

> *"기술이 개입해야 할 영역과, 현장의 자율성을 존중해야 할 영역을 구분하는 법을 배웠습니다."*

<div align="center">

<!-- 📸 발표/행사 사진 자리 -->
<img width="400" height="300" alt="KakaoTalk_20260619_151113079_01" src="https://github.com/user-attachments/assets/8f59130a-6462-48cd-8e07-a139dd080590" />
<img width="300" height="400" alt="KakaoTalk_20260619_151113079_04" src="https://github.com/user-attachments/assets/25590e55-2ff3-448d-bb61-47688252cb33" />
<img width="300" height="400" alt="KakaoTalk_20260619_151113079_02" src="https://github.com/user-attachments/assets/004adc28-51ce-421a-a3b9-8a44893ba652" />
<img width="403" height="302" alt="KakaoTalk_20260619_205236519_03" src="https://github.com/user-attachments/assets/580653e5-0a21-4670-bf33-38071a3f0c43" />

**팀 연송이 · Tech for Impact Campus · Yonsei University**

</div>

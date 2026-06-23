<div align="center">

# 🐿️ Daramjwi (Squirrel) Taxi — Reservation & Operations Service
[🇰🇷 한국어](./README.md) &nbsp;·&nbsp; **🇬🇧 English**

> ## "When transit stops, daily life stops."
> A digital reservation & operations layer for **Daramjwi Taxi**, a rural mobility service in Cheongsan-myeon, Okcheon County, South Korea.

![Award](https://img.shields.io/badge/🥇_1st_Place_·_Social_Value_Award-Tech_for_Impact_Campus_2026-FFE500?style=for-the-badge&labelColor=1A1A1A)
&nbsp;
![Team](https://img.shields.io/badge/Team_Yeonsongi-Yonsei_University-F2994A?style=for-the-badge&labelColor=1A1A1A)

[![Live Demo](https://img.shields.io/badge/🔗_Live_Demo-daramjwi--taxi--client.vercel.app-F2994A?style=for-the-badge&labelColor=1A1A1A)](https://daramjwi-taxi-client.vercel.app/)

</div>

---

## 🥇 Social Value Award · Tech for Impact Campus 2026

At the Tech for Impact Campus showcase (Yonsei University × kakao!mpact),
**Okcheon News — Team Yeonsongi** won **Social Value Award**.

<div align="center">
<!-- 📸 Award photo -->
<img width="600" height="450" alt="KakaoTalk_20260619_173317412" src="https://github.com/user-attachments/assets/eea28383-d806-4fb0-a891-4f5999a9037b" />
</div>

---

## 🔗 Try the Prototype

👉 **[Open the Daramjwi Taxi app](https://daramjwi-taxi-client.vercel.app/)** — best viewed on a phone.

Or scan the QR code below with your phone camera.

<div align="center">
<img width="216" height="216" alt="daramjwi_qr" src="https://github.com/user-attachments/assets/6309a344-3212-42b0-baca-d4fd46fffdfd" />
</div>

---

## 🚐 The Problem

<img width="440" height="260" alt="KakaoTalk_20260619_211651236" src="https://github.com/user-attachments/assets/219a5cf8-5dcb-43ec-8a95-5a36d1e919e0" />
<img width="440" height="260" alt="image" src="https://github.com/user-attachments/assets/9b755f95-9fdc-4453-b651-455d48e7b7cc" />
<img width="440" height="260" alt="image" src="https://github.com/user-attachments/assets/4b8164b8-81ad-403a-9376-cd475ea4fa3a" />
<img width="440" height="260" alt="image" src="https://github.com/user-attachments/assets/27031478-85e0-4430-b48b-079b93991ec1" />

· In a depopulating rural Korea, mobility is the **gateway to economic and social access** — work, healthcare, markets, public offices. Miss the infrequent bus in Cheongsan-myeon and you wait an hour or more; a regular taxi to town costs **~₩60,000**, far beyond a daily option.

· Okcheon County already runs a strong welfare program, **Daramjwi Taxi**, letting residents ride for a bus-level fare (**₩1,700**), with the county subsidizing the difference. But it is capped per village (**4 rides/day, 112/month**), so the real work is *coordinating limited public rides fairly within each village*.

· The catch: this good policy still ran on **phone calls, memory, and handwritten notes**. Residents called the village chief to check availability; drivers took calls mid-route and had to remember each booking.

> [!NOTE]
> **So we reframed the problem.**
> The real gap was not a *shortage of rides*, but the
> **absence of a system to coordinate limited public mobility resources** — a coordination failure, not a supply failure.

This reframing advanced the existing welfare subsidy toward a **Demand-Responsive Transit (DRT)** model.

---

## 💡 The Approach

· We deliberately avoided porting a city-style ride-hailing app (personal hailing, payment registration, real-time dispatch). For elderly residents, app installation itself is a barrier; in rural areas, *coordinating village-level resources* matters more than *instant individual hailing*.

· Our design principle was **Culture in Action** — *connect to the field as it is, rather than forcing new behavior*. Residents comfortable with apps get a direct booking path; those who aren't keep the familiar phone route.

| | Role |
| --- | --- |
| 👵 **Resident app** | Book a ride · today's service · village status · my reservations · remaining quota |
| 🚕 **Driver app** | Unified entry for app + phone bookings · live status · confirm/cancel · monthly overview |

· Whether a resident books in-app or by phone, every reservation lands reliably in **one place — the driver's app**. A **ride-pooling feature** helps use the capped rides efficiently.

> [!NOTE]
> Through two rounds of user testing we pivoted the operator app from *village chief → driver*. A 72-year-old taxi-company director completed all five tasks, validating usability. The Okcheon County transport division proposed **scaling across all 47 villages**, and we are preparing the service as a DRT operations platform. **Beta launch upcoming.**

---

## 🗺️ Service Architecture

<div align="center">
<img width="800" height="400" alt="daramjwi_architecture" src="https://github.com/user-attachments/assets/44096a12-1eaf-4472-b123-ada2aedd6b8d" />
</div>

· The resident and driver apps run as a single **Next.js PWA** (branching after a role-select step), backed by a **REST API server** (Next.js · Vercel) and **Supabase** (PostgreSQL · Auth · Realtime). The client also connects to Supabase **directly** for phone-OTP auth and real-time sync. Authentication uses **Kakao Login (OAuth 2.0)**, and notifications use **Web Push (VAPID)** — SMS / KakaoTalk alerts are planned once business integration is complete.

---

## 🛠️ Tech Stack

![Next.js](https://img.shields.io/badge/Next.js_15-000000?logo=next.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3FCF8E?logo=supabase&logoColor=white)
![PWA](https://img.shields.io/badge/PWA-5A0FC8?logo=pwa&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?logo=vercel&logoColor=white)
![Kakao](https://img.shields.io/badge/Kakao_Login-FFCD00?logo=kakao&logoColor=000000)

- **Frontend** — Next.js 15, TypeScript, PWA (service worker · web push)
- **Backend** — Supabase (PostgreSQL · Auth · Realtime), deployed on Vercel
- **Auth** — Kakao OAuth, Supabase phone OTP
- **Elderly-first UX** — large touch targets, minimized typing (one-time registration, then button-driven), landmark-based guidance

---

## 📦 Repositories

| Repository | Description |
| --- | --- |
| [`daramjwi-taxi-client`](../../../../daramjwi-taxi-client) | Unified resident + driver PWA frontend |
| [`daramjwi-taxi-server`](../../../../daramjwi-taxi-server) | Reservation / operations / settlement API (Supabase + Next.js) |

🔗 **Live** — https://daramjwi-taxi-client.vercel.app/

---

## 👥 Team Yeonsongi

| Name | Role |
| --- | --- |
| Ji-hee Yu(TL) | Backend · Server |
| Yun-a Gong · Seol Kim| UI/UX Design |
| Seok-in Yeon | Frontend · Product Direction |
| Ye-jin Yun | Planning · Presentor |
| Ho-yeong Jeong | Planning |


---

## 🙏 With

· Heartfelt thanks to **Prof. Kang Yeon-a · Prof. Song Jin-yeong** for guiding our direction, to **CEO Hwang Min-ho** of Okcheon News for opening the field, and to kakao mentors **Jay · Eric** for thinking through everything from planning to implementation.

<div align="center">

<!-- 📸 Presentation / event photo (optional): drop an image below this line. -->
<img width="400" height="510" alt="KakaoTalk_20260619_151113079_04" src="https://github.com/user-attachments/assets/25590e55-2ff3-448d-bb61-47688252cb33" />
<img width="400" height="510" alt="KakaoTalk_20260619_151113079_02" src="https://github.com/user-attachments/assets/004adc28-51ce-421a-a3b9-8a44893ba652" />
<img width="800" height="600" alt="KakaoTalk_20260619_151113079_01" src="https://github.com/user-attachments/assets/8f59130a-6462-48cd-8e07-a139dd080590" />
<img width="800" height="600" alt="KakaoTalk_20260619_205236519_03" src="https://github.com/user-attachments/assets/580653e5-0a21-4670-bf33-38071a3f0c43" />
**Team Yeonsongi · Tech for Impact Campus · Yonsei University**

</div>

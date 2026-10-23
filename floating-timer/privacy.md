---
title: Floating Timer 개인정보처리방침 · Privacy Policy
permalink: /floating-timer/privacy/
---

<!--
  초안 (release.md R5-1). 게시 위치: https://lcemjr.github.io/floating-timer/privacy/
  앱 동작 · 권한 · SDK가 바뀌면 이 문서와 Play 데이터 보안 양식(R3-4)을 함께 고친다.
  크래시 수집(Crashlytics 등)을 넣기로 하면 2절 · 4절 · 영어 2 · 4에 항목을 추가한다.
-->

[한국어](#ko) · [English](#en)

<a id="ko"></a>

# Floating Timer 개인정보처리방침

LCEMJR(이하 "개발자")는 Floating Timer 앱(이하 "앱")을 이용하는 분의 개인정보를 「개인정보 보호법」에 따라 처리하며, 다음과 같이 처리방침을 공개합니다.

**요약**
- 앱은 회원가입이 없고, 타이머 설정은 **기기 안에만** 저장됩니다.
- 어떤 앱이 화면 앞에 있는지 · 설치된 앱 목록은 **기기 안에서만 쓰고 밖으로 보내지 않습니다.**
- 개발자가 받는 개인정보는 **사용자가 직접 보낸 "의견 보내기" 내용**뿐입니다.
- 앱 화면 하단의 광고는 Google AdMob이 표시하며, 광고 ID 등은 Google이 처리합니다.

## 1. 처리 목적

| 목적 | 내용 |
|---|---|
| 의견 · 문의 응대 | 기능 요청 · 버그 신고 확인, 답변 받을 이메일을 적은 경우 답변 |
| 앱 개선 | 받은 의견과 (선택한 경우) 앱 버전 · 기기 정보로 문제 재현 · 수정 |
| 광고 표시 | 앱 화면(S1) 하단 배너 광고 표시 (Google AdMob) |
| 후원 처리 | 인앱 후원 결제 확인 및 후원자 광고 제거 (Google Play 결제) |

## 2. 처리하는 개인정보 항목

### 2-1. 개발자가 받는 정보 — "의견 보내기"를 사용한 경우만
| 항목 | 필수 · 선택 |
|---|---|
| 의견 종류(기능 요청 · 버그 · 기타), 의견 내용 | 필수 (보내기를 누른 경우) |
| 답변 받을 이메일 주소 | 선택 |
| 앱 버전, Android 버전, 기기 모델명 | 선택 ("앱 버전 · 기기 정보 함께 보내기"를 체크한 경우, 보내기 전 화면에 그대로 표시) |

의견은 Google 폼으로 전송되어 개발자의 Google 스프레드시트에 저장됩니다.

### 2-2. 기기 안에서만 처리하고 밖으로 보내지 않는 정보
| 항목 | 쓰는 곳 |
|---|---|
| 화면 앞에 있는 앱의 패키지 이름 (사용 정보 접근 권한) | 지정한 게임이 켜질 때 타이머 자동 표시, 다른 앱으로 나갔을 때 아이콘 반투명 · 숨김, 타이머별 "보이는 앱" |
| 설치된 앱 목록 (런처에 보이는 앱) | 자동 실행 앱 · 보이는 앱 선택 화면 |
| 타이머 · 그룹 · 닉네임 · 앱 설정, 실행 중 타이머 | 앱 동작 |

### 2-3. 제3자 서비스가 처리하는 정보
| 서비스 | 처리하는 정보 | 개발자가 받는 것 |
|---|---|---|
| Google AdMob (광고) | 광고 ID, IP 주소, 기기 · 앱 정보, 광고 상호작용 등 | 없음 (집계 수익 보고서만) |
| Google Play 결제 (후원) | 결제 수단, 구매 기록 | 구매한 후원 상품 종류 · 구매 확인 정보 (이름 · 결제 수단은 받지 않음) |
| Google 폼 · 스프레드시트 (의견 보내기) | 2-1 항목, 전송 시 Google이 수집하는 접속 정보 | 2-1 항목 |

각 서비스의 처리 방식은 [Google 개인정보처리방침](https://policies.google.com/privacy)을 따릅니다.

## 3. 보유 기간 및 파기

- 의견 보내기 정보: 받은 날부터 **1년** 보관 후 파기합니다. 답변 · 수정이 끝난 의견은 그 전에도 파기할 수 있습니다. 삭제를 요청하시면 바로 파기합니다.
- 기기 안의 정보: 앱을 삭제하거나 앱 데이터를 지우면 함께 삭제됩니다.
- 파기 방법: 스프레드시트의 해당 행을 복구할 수 없게 삭제합니다.

## 4. 처리 위탁 및 국외 이전

개발자는 개인정보를 제3자에게 제공하지 않습니다. 앱 운영을 위해 아래와 같이 처리를 맡기며, 이 과정에서 개인정보가 국외로 이전됩니다.

| 받는 자 | 이전 국가 | 이전 항목 | 목적 | 이전 일시 · 방법 | 보유 기간 |
|---|---|---|---|---|---|
| Google LLC (Google 폼 · 스프레드시트) | 미국 등 Google 데이터센터 소재국 | 2-1 항목 | 의견 저장 | 의견을 보낼 때 네트워크(HTTPS)로 전송 | 3절과 같음 |
| Google LLC (AdMob) | 미국 등 | 2-3 광고 항목 | 광고 표시 · 측정 | 광고를 불러올 때 네트워크로 전송 | Google 정책에 따름 |
| Google LLC (Google Play 결제) | 미국 등 | 2-3 결제 항목 | 결제 처리 | 결제할 때 | Google 정책에 따름 |

이전을 원하지 않으시면: 의견 보내기를 사용하지 않거나 이메일 · 기기 정보를 빼고 보낼 수 있고, 광고 개인정보는 아래 5절 방법으로 제한할 수 있습니다. 결제는 Google Play를 통해서만 가능합니다.

## 5. 광고 ID 등 자동 수집 장치와 거부 방법

- 앱은 쿠키를 쓰지 않습니다. 광고 SDK가 Android 광고 ID를 사용합니다.
- 거부 · 제한 방법
  - Android 설정 > 개인정보 보호(또는 Google) > 광고 > **광고 ID 삭제**
  - 유럽경제지역(EEA) · 영국 등: 앱 첫 실행 시 동의 창, 이후 앱의 **설정 > 앱 정보 > 광고 개인정보 설정**에서 변경
- 후원을 한 번이라도 하면 광고가 표시되지 않습니다.

## 6. 앱이 사용하는 권한

| 권한 | 이유 | 거부하면 |
|---|---|---|
| 다른 앱 위에 표시 | 게임 위에 타이머 아이콘을 띄우기 위해 | 앱의 핵심 기능을 쓸 수 없음 |
| 알림 | 타이머 종료 알림, 실행 중 표시 | 종료 알림이 오지 않음 |
| 사용 정보 접근 | 앞 화면 앱 확인 (2-2) — 기기 밖으로 보내지 않음 | 자동 실행 · 앱별 표시 기능만 꺼지고 나머지는 동작 |
| 정확한 알람 | 화면이 꺼져 있어도 정확한 시각에 타이머 종료 | — |
| 인터넷 | 의견 보내기, 광고, 결제 | — |

## 7. 이용자의 권리와 행사 방법

의견 보내기로 보낸 정보의 열람 · 정정 · 삭제 · 처리정지를 아래 이메일로 요청할 수 있습니다. 보낸 날짜와 내용 일부를 알려 주시면 찾기 쉽습니다. 요청을 받으면 지체 없이 처리하고 결과를 알려 드립니다.

## 8. 안전성 확보 조치

- 의견은 암호화된 연결(HTTPS)로 전송합니다.
- 의견이 저장되는 스프레드시트는 개발자 계정만 접근할 수 있고, 계정에는 2단계 인증을 사용합니다.

## 9. 아동의 개인정보

앱은 만 14세 미만 아동을 대상으로 하지 않습니다. 만 14세 미만이라면 의견 보내기에 이메일을 적지 말아 주세요. 만 14세 미만 아동의 개인정보를 받은 것을 알게 되면 바로 삭제합니다.

## 10. 개인정보 보호책임자

| 구분 | 내용 |
|---|---|
| 개인정보 보호책임자 | 천마로 (개발자) |
| 연락처 | lcemjr.apps@gmail.com |

## 11. 권익침해 구제 방법

개인정보 침해에 대한 신고 · 상담은 아래 기관에 문의할 수 있습니다.
- 개인정보침해신고센터: privacy.kisa.or.kr / 국번 없이 118
- 개인정보분쟁조정위원회: www.kopico.go.kr / 1833-6972
- 대검찰청: www.spo.go.kr / 국번 없이 1301
- 경찰청: ecrm.police.go.kr / 국번 없이 182

## 12. 처리방침의 변경

이 처리방침은 **2026년 10월 23일**부터 적용됩니다. 내용이 바뀌면 이 페이지에 시행일과 함께 알립니다.

- 2026-10-23 최초 시행

---

<a id="en"></a>

# Floating Timer Privacy Policy

This policy explains how LCEMJR ("the developer") handles information in the Floating Timer app ("the app").

**Summary**
- There is no sign-up. Your timer settings are stored **only on your device**.
- Which app is in the foreground and the list of installed apps are used **on your device only and never sent anywhere**.
- The only personal information the developer receives is **what you send through "Send feedback"**.
- The banner ad at the bottom of the app screen is served by Google AdMob, which processes data such as the advertising ID.

## 1. Purposes

| Purpose | Details |
|---|---|
| Responding to feedback | Reviewing feature requests and bug reports; replying if you provide an email address |
| Improving the app | Reproducing and fixing issues using your feedback and (if you choose) app version and device information |
| Showing ads | Showing a banner ad at the bottom of the app screen (Google AdMob) |
| Processing tips | Verifying in-app tip purchases and removing ads for supporters (Google Play Billing) |

## 2. Information we process

### 2-1. Information the developer receives — only when you use "Send feedback"
| Item | Required / optional |
|---|---|
| Feedback type (feature request, bug, other) and message | Required (when you tap Send) |
| Email address for a reply | Optional |
| App version, Android version, device model | Optional (only if you check "Include app version and device info"; shown on screen before sending) |

Feedback is submitted through Google Forms and stored in the developer's Google Sheets.

### 2-2. Information processed on your device only
| Item | Used for |
|---|---|
| Package name of the foreground app (Usage access permission) | Showing the timer automatically when a chosen game starts, dimming or hiding the icon in other apps, per-timer "visible apps" |
| List of installed apps (apps shown in the launcher) | Choosing auto-start apps and visible apps |
| Timers, groups, nicknames, settings, running timers | Running the app |

### 2-3. Information processed by third-party services
| Service | Information | What the developer receives |
|---|---|---|
| Google AdMob (ads) | Advertising ID, IP address, device and app information, ad interactions | Nothing (aggregated revenue reports only) |
| Google Play Billing (tips) | Payment method, purchase history | Which tip product was purchased and purchase verification data (no name or payment details) |
| Google Forms / Sheets (feedback) | Items in 2-1 and connection data collected by Google | Items in 2-1 |

See the [Google Privacy Policy](https://policies.google.com/privacy) for how these services handle data.

## 3. Retention and deletion

- Feedback: kept for **1 year** from receipt, then deleted. It may be deleted earlier once handled, and immediately on request.
- On-device data: deleted when you uninstall the app or clear its data.

## 4. Processors and international transfers

The developer does not sell or share your personal information with third parties. Google LLC processes data on the developer's behalf (Forms/Sheets for feedback, AdMob for ads, Play Billing for payments), which may involve transfer to the United States and other countries where Google operates data centers.

## 5. Advertising ID and your choices

- The app does not use cookies. The ads SDK uses the Android advertising ID.
- You can delete or reset it in Android Settings > Privacy (or Google) > Ads.
- In the EEA, UK and other applicable regions, you will see a consent form on first launch and can change your choice later in **Settings > App info > Ad privacy settings**.
- Legal bases (EEA/UK): consent for personalized ads; legitimate interest for responding to feedback you send.
- Ads are removed once you make any tip purchase.

## 6. Permissions

| Permission | Why | If denied |
|---|---|---|
| Display over other apps | To show the timer icon over games | Core features unavailable |
| Notifications | Timer finished alerts and ongoing status | No finish alerts |
| Usage access | To know the foreground app (2-2) — never leaves your device | Only auto-start and per-app visibility are disabled |
| Exact alarms | To finish timers on time even when the screen is off | — |
| Internet | Feedback, ads, payments | — |

## 7. Your rights

You can ask to access, correct, or delete the feedback you sent, or object to its processing, by emailing the address below. Including the date and part of the message helps us find it.

## 8. Children

The app is not directed to children under 14 (under 13 in the United States). If you are a child, please do not include an email address in feedback. If we learn we have received a child's personal information, we will delete it.

## 9. Contact

LCEMJR (Privacy officer: Maro Cheon) — lcemjr.apps@gmail.com

## 10. Changes

This policy is effective from **October 23, 2026**. Changes will be posted on this page with a new effective date.

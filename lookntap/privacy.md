---
title: Look n Tap 개인정보처리방침 · Privacy Policy
permalink: /lookntap/privacy/
---

<!--
  초안 (2026-11-03, 관리 세션). 게시 위치: https://lcemjr.github.io/lookntap/privacy/
  틀: floating-timer release/site/floating-timer/privacy.md. 게시는 lcemjr.github.io 저장소에 복사 · push (사용자 확인 후).
  근거 (2026-11-03 코드 기준): 매니페스트 권한 POST_NOTIFICATIONS · VIBRATE + 접근성 서비스(LookService), INTERNET 없음.
  외부 SDK는 Play 인앱 업데이트(app-update-ktx)뿐. 자동 백업은 설정(sharedpref lookntap.xml)만 — 레시피 · 사진 · 기록은 백업 안 됨.
  이 문서 · 앱 안 공개 문구(ui-flow S2, Q27) · Play 접근성 신고(release/play-console/accessibility.md) · 데이터 보안 양식은 항상 같은 내용이어야 한다.
  함께 고칠 때: 인터넷 권한 · 광고 · 결제 · 의견 보내기 · 크래시 수집 · OCR(ML Kit) 출시 포함 · 공유(SH, 서버 업로드)가 들어오면
  2절 · 4절 · 6절과 영어 같은 절에 항목 추가. 공유를 넣으면 '사용자가 미리 보고 확인한 레시피만 올림'(SH1 · SH2)을 명시.
  시행일 2026-11-03 게시. 바꿀 때는 12절 · 영어 10절에 변경 이력 추가.
-->

[한국어](#ko) · [English](#en)

<a id="ko"></a>

# 룩앤탭(Look n Tap) 개인정보처리방침

LCEMJR(이하 "개발자")는 룩앤탭 앱(이하 "앱")을 이용하는 분의 개인정보를 「개인정보 보호법」에 따라 처리하며, 다음과 같이 처리방침을 공개합니다.

**요약**
- 앱은 회원가입이 없고, **인터넷 권한이 없습니다.** 앱이 보거나 만든 정보는 기기 밖으로 나가지 않습니다.
- 앱은 접근성 서비스로 화면의 글자 · 버튼 정보와 화면 사진을 봅니다. 이것은 **사용자가 화면 위 조작 패널을 띄워 둔 동안에만**(녹화 · 보정 · 실행 · 시작할 레시피 고르기), 사용자가 녹화한 탭을 다시 누르기 위해서만 씁니다. 패널을 닫으면 화면을 읽지 않습니다.
- 레시피 · 버튼 사진 · 실행 기록은 **기기 안에만** 저장됩니다. 비밀번호 칸의 내용은 저장하지 않습니다.
- 개발자는 사용자에 관한 어떤 정보도 받지 않습니다.

## 1. 처리 목적

| 목적 | 내용 |
|---|---|
| 녹화 | 사용자가 누른 버튼이 무엇인지 기억 (글자 · ID · 위치 · 버튼 사진 · 주변 요소) |
| 보정 · 실행 | 녹화한 버튼이 화면에 보이는지 찾아 대신 누르기, 찾지 못하면 멈추고 사용자에게 묻기 |
| 실행 기록 | 실패한 단계를 사용자가 확인하고 고칠 수 있게 그 순간의 화면 정보를 남기기 |

## 2. 처리하는 개인정보 항목

### 2-1. 개발자가 받는 정보

**없습니다.** 앱에는 회원가입 · 의견 전송 · 광고 · 분석 · 크래시 수집 기능이 없고, 인터넷 권한도 없습니다.

### 2-2. 기기 안에서만 처리하고 밖으로 보내지 않는 정보

| 항목 | 언제 | 쓰는 곳 · 보관 |
|---|---|---|
| 화면의 UI 정보 (보이는 글자, 버튼 ID · 종류 · 위치) — 접근성 서비스 | 패널을 띄워 둔 동안에만 | 지금 화면에서 시작할 레시피 고르기, 누른 버튼을 알아보고 다시 찾기. 레시피에는 누른 버튼과 그 주변 요소만 저장 |
| 화면 사진 (접근성 `takeScreenshot`) | 패널을 띄워 둔 동안에만 | 글자가 없는 버튼을 그림으로 찾기. 레시피에는 버튼 부분만 잘라 저장, 화면 전체는 찾은 뒤 버림 |
| 레시피 (단계 · 버튼 정보 · 버튼 사진 · 대기 시간) | 사용자가 저장할 때 | 실행. 사용자가 지울 때까지 |
| 실행 기록 (실패한 단계의 화면 사진 · UI 정보 · 후보) | 실행이 실패했을 때 | 실패 화면에서 고치기. 고치면 지우고 최근 몇 개만 남김 |
| 앱 설정 · 동의 기록 | — | 앱 동작 |

- **비밀번호 칸**(Android가 비밀번호로 표시한 입력 칸)의 내용은 녹화 · 저장하지 않습니다.
- 실행할 때마다 바뀌는 입력 값은 실행 · 보정 때 화면에서 물어보고 저장하지 않습니다.
- Android가 보안 화면으로 막은 화면(은행 앱 등)은 사진을 찍을 수 없습니다.

### 2-3. 제3자 서비스

| 서비스 | 처리하는 정보 | 개발자가 받는 것 |
|---|---|---|
| Google Play 인앱 업데이트 | 새 버전 확인 · 내려받기 (기기의 Play 스토어 앱이 처리) | 없음 |
| Android 백업 (Google 계정, 사용자가 켠 경우) | **앱 설정만** — 레시피 · 사진 · 실행 기록은 백업하지 않음 | 없음 |

각 서비스의 처리 방식은 [Google 개인정보처리방침](https://policies.google.com/privacy)을 따릅니다.

## 3. 보유 기간 및 파기

- 기기 안의 정보: 사용자가 레시피 · 기록을 지우거나, 앱을 삭제하거나, 앱 데이터를 지우면 삭제됩니다.
- 실행 기록은 고치면 지우고 최근 몇 개만 남깁니다.
- 개발자가 보관하는 정보는 없습니다.

## 4. 제3자 제공 · 처리 위탁 · 국외 이전

개발자는 개인정보를 받지 않으므로 제3자에게 제공하거나 처리를 맡기거나 국외로 이전하지 않습니다. (Android 백업은 사용자 본인의 Google 계정에 저장되며 2-3의 앱 설정만 포함합니다.)

## 5. 자동 수집 장치

앱은 쿠키 · 광고 ID · 분석 도구를 쓰지 않습니다.

## 6. 앱이 사용하는 권한

| 권한 | 이유 | 거부하면 |
|---|---|---|
| 접근성 서비스 | 화면의 버튼을 알아보고(2-2) 녹화한 탭 · 스와이프 · 입력을 대신 하기, 볼륨 키 길게 눌러 멈추기, 화면 위 조작 패널 표시. 켜기 전에 앱 안에서 무엇을 보고 어떻게 쓰는지 안내하고 동의를 받습니다 | 앱의 핵심 기능을 쓸 수 없음 |
| 알림 | 실행 중 표시, 끝 · 실패 알림 | 알림이 오지 않음 (실행은 됨) |
| 진동 | 실행 끝 · 질문 알림 진동 | — |

앱은 **인터넷 권한을 요청하지 않습니다.** 접근성 서비스는 언제든 Android 설정 > 접근성에서 끌 수 있습니다.

## 7. 이용자의 권리와 행사 방법

개발자는 이용자의 개인정보를 갖고 있지 않습니다. 기기 안의 정보는 앱에서 레시피 · 기록을 지우거나 앱 데이터를 지워 직접 삭제할 수 있습니다. 궁금한 점은 아래 이메일로 문의해 주세요.

## 8. 안전성 확보 조치

- 모든 정보는 다른 앱이 읽을 수 없는 앱 전용 저장소에 저장됩니다.
- 앱은 인터넷 권한이 없어 정보를 기기 밖으로 보낼 수 없습니다.
- 접근성 서비스가 켜져 있어도 사용자가 패널을 띄우지 않으면 화면을 읽지 않고, 앱 안 공개 · 동의 전에는 아무것도 읽지 않습니다.

## 9. 아동의 개인정보

앱은 만 14세 미만 아동을 대상으로 하지 않으며, 아동의 개인정보를 받지 않습니다.

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

이 처리방침은 **2026년 11월 3일**부터 적용됩니다. 내용이 바뀌면 이 페이지에 시행일과 함께 알립니다. 레시피 공유처럼 정보를 기기 밖으로 보내는 기능이 생기면, 그 기능을 넣기 전에 이 처리방침을 먼저 고칩니다.

- 2026-11-03 최초 시행

---

<a id="en"></a>

# Look n Tap Privacy Policy

This policy explains how LCEMJR ("the developer") handles information in the Look n Tap app ("the app").

**Summary**
- There is no sign-up, and the app **does not have the Internet permission**. Nothing the app sees or creates leaves your device.
- The app uses an accessibility service to read on-screen text, button information and screenshots — **only while you keep the floating control panel open** (recording, calibrating, running, or choosing a recipe to start), and only to tap again the buttons you recorded. When the panel is closed, the app does not read the screen.
- Recipes, button images and run history are stored **only on your device**. Password fields are never stored.
- The developer receives no information about you.

## 1. Purposes

| Purpose | Details |
|---|---|
| Recording | Remembering which button you tapped (text, ID, position, button image, nearby elements) |
| Calibrating and running | Waiting until a recorded button is visible and tapping it for you; stopping and asking you when it cannot be found |
| Run history | Keeping the screen information of a failed step so you can review and fix it |

## 2. Information we process

### 2-1. Information the developer receives

**None.** The app has no sign-up, feedback upload, ads, analytics or crash reporting, and no Internet permission.

### 2-2. Information processed on your device only

| Item | When | Used for / kept |
|---|---|---|
| On-screen UI information (visible text, view IDs, types, positions) — accessibility service | Only while the panel is open | Choosing a recipe to start on the current screen; identifying and finding the tapped button. A recipe stores only the tapped button and its nearby elements |
| Screenshots (accessibility `takeScreenshot`) | Only while the panel is open | Finding buttons that have no text. A recipe stores only the cropped button; full screenshots are discarded after matching |
| Recipes (steps, button information, button images, waits) | When you save | Running. Until you delete them |
| Run history (screenshot, UI information and candidates of a failed step) | When a run fails | Fixing the step. Removed once fixed; only the most recent few are kept |
| App settings and consent record | — | Running the app |

- Contents of **password fields** (input fields Android marks as passwords) are never recorded or stored.
- Values that change on every run are asked on screen during the run and are not stored.
- Screens protected by Android as secure (e.g. banking apps) cannot be captured.

### 2-3. Third-party services

| Service | Information | What the developer receives |
|---|---|---|
| Google Play in-app updates | Checking for and downloading new versions (handled by the Play Store app on your device) | Nothing |
| Android backup (your Google account, if enabled) | **App settings only** — recipes, images and run history are not backed up | Nothing |

See the [Google Privacy Policy](https://policies.google.com/privacy) for how these services handle data.

## 3. Retention and deletion

- On-device data is deleted when you delete recipes or history, uninstall the app, or clear its data.
- Run history is removed once fixed, and only the most recent few entries are kept.
- The developer keeps no data.

## 4. Sharing and international transfers

Because the developer receives no personal information, none is shared with third parties, processed on the developer's behalf, or transferred abroad. (Android backup is stored in your own Google account and contains only the app settings in 2-3.)

## 5. Cookies and identifiers

The app does not use cookies, the advertising ID, or analytics tools.

## 6. Permissions

| Permission | Why | If denied |
|---|---|---|
| Accessibility service | To identify buttons on screen (2-2) and perform the recorded taps, swipes and text input for you, to stop on a long press of the volume key, and to show the floating control panel. Before you turn it on, the app explains in the app what it reads and how it is used and asks for your consent | Core features unavailable |
| Notifications | Ongoing run status, finish and failure alerts | No alerts (runs still work) |
| Vibration | Vibration for finish and question alerts | — |

The app **does not request the Internet permission.** You can turn off the accessibility service at any time in Android Settings > Accessibility.

## 7. Your rights

The developer holds no personal information about you. You can delete on-device data yourself by deleting recipes or history in the app, or by clearing the app's data. For questions, email the address below.

## 8. Children

The app is not directed to children under 14 (under 13 in the United States) and does not collect children's personal information.

## 9. Contact

LCEMJR (Privacy officer: Maro Cheon) — lcemjr.apps@gmail.com

## 10. Changes

This policy is effective from **November 3, 2026**. Changes will be posted on this page with a new effective date. If a feature that sends information off the device (such as recipe sharing) is added, this policy will be updated before that feature is released.

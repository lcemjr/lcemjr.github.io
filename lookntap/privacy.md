---
title: Look n Tap 개인정보처리방침 · Privacy Policy
permalink: /lookntap/privacy/
---

<!--
  초안 (2026-11-03, 관리 세션). 게시 위치: https://lcemjr.github.io/lookntap/privacy/
  틀: floating-timer release/site/floating-timer/privacy.md. 게시는 lcemjr.github.io 저장소에 복사 · push (사용자 확인 후).
  근거 (2026-11-03 출시 합친 매니페스트, 개발 세션 60b7e54): 우리 권한 POST_NOTIFICATIONS · VIBRATE + 접근성 서비스(LookService).
  광고 SDK(play-services-ads 25.4.0 · UMP 4.0.0)가 INTERNET · ACCESS_NETWORK_STATE · AD_ID · ACCESS_ADSERVICES_* · WAKE_LOCK · FOREGROUND_SERVICE(WorkManager)를 넣음.
  광고는 S1 아래 배너만, 빈 AdRequest(화면 내용 · 레시피 안 넘김), 후원(adFree)이면 UMP · 배너 없음 (SA10 · Q30). 결제(커피 후원 D9)는 b3bd2f4에서 들어옴 — billing 9.0.0이 com.android.vending.BILLING 추가.
  녹화 중 터치 받기(b38cbbb · Q35) · 뒤로 · 홈 · 앱 열기(4e3a41f · Q34, queries LAUNCHER · HOME — 패키지 이름은 레시피에만, 밖으로 안 보냄) 2026-11-04 반영.
  실행이 막혔을 때(c87254f · Q36): 팝업 규칙 · 견본은 레시피에, 배터리 온도는 읽기만 (2026-11-04 사후 점검).
  진입 설계(1699db3 · Q42 · Q43): 알림창 · 빠른 설정 단계, 홈 위젯 찾기, 처음부터 다시 열기(CLEAR_TASK) 2026-11-04 반영.
  확인 중 입력 막기(ae821b0 · Q44): 보정 중 터치는 막기만 하고 기록 · 전달 안 함 — 2026-11-05 반영.
  그 밖 SDK: Play 인앱 업데이트(app-update-ktx). 자동 백업은 설정(sharedpref lookntap.xml)만 — 레시피 · 사진 · 기록은 백업 안 됨.
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
- 앱은 회원가입이 없습니다. 앱이 화면에서 본 내용과 레시피 · 실행 기록은 **기기 밖으로 나가지 않고, 광고 · 분석에 쓰지 않습니다.**
- 앱은 접근성 서비스로 화면의 글자 · 버튼 정보와 화면 사진을 봅니다. 이것은 **사용자가 화면 위 조작 패널을 띄워 둔 동안에만**(녹화 · 보정 · 실행 · 시작할 레시피 고르기), 사용자가 녹화한 탭을 다시 누르기 위해서만 씁니다. 패널을 닫으면 화면을 읽지 않습니다. 녹화 중에는 화면 터치를 받아 누른 자리를 기억한 뒤 앱에 그대로 전달합니다. 녹화 뒤 확인(천천히 실행) 중에는 잘못 눌리지 않게 화면 터치를 잠시 막으며, 이 터치는 기록하지 않습니다.
- 레시피 · 버튼 사진 · 실행 기록은 **기기 안에만** 저장됩니다. 녹화한 화면 사진은 고칠 때 쓰려고 레시피를 저장하기 전까지만 두고 지웁니다. 비밀번호 칸의 내용은 저장하지 않습니다.
- 앱 홈 화면 아래의 배너 광고는 Google AdMob이 표시하며, 광고 ID 등은 Google이 처리합니다. 광고는 앱 화면에만 있고, 다른 앱 위에 뜨는 패널에는 없습니다.
- 개발자는 사용자를 알아볼 수 있는 정보를 받지 않습니다.

## 1. 처리 목적

| 목적 | 내용 |
|---|---|
| 녹화 | 사용자가 누른 버튼이 무엇인지 기억 (글자 · ID · 위치 · 버튼 사진 · 주변 요소), 녹화 중 화면 터치를 받아 누른 자리를 기억한 뒤 앱에 그대로 전달, 뒤로 · 홈 · 연 앱 기억, 저장 전 편집에서 목표 · 조건 영역을 다시 고를 수 있게 단계마다 화면을 잠시 남기기 |
| 보정 · 실행 | 녹화한 버튼이 화면에 보이는지 찾아 대신 누르기, 찾지 못하면 멈추고 사용자에게 묻기 |
| 실행 기록 | 실패한 단계를 사용자가 확인하고 고칠 수 있게 그 순간의 화면 정보를 남기기 |
| 광고 표시 | 앱 홈 화면 하단 배너 광고 표시 (Google AdMob) |
| 후원 처리 | 인앱 후원 결제 확인 및 후원자 광고 제거 (Google Play 결제, 후원 기능을 제공하는 경우) |

## 2. 처리하는 개인정보 항목

### 2-1. 개발자가 받는 정보

**없습니다.** 앱에는 회원가입 · 의견 전송 · 분석 · 크래시 수집 기능이 없습니다. 광고 · 결제 · 글자 인식 서비스에서는 집계 보고서와 구매 확인 정보만 받습니다(2-3).

### 2-2. 기기 안에서만 처리하고 밖으로 보내지 않는 정보

| 항목 | 언제 | 쓰는 곳 · 보관 |
|---|---|---|
| 화면의 UI 정보 (보이는 글자, 버튼 ID · 종류 · 위치) — 접근성 서비스 | 패널을 띄워 둔 동안에만 | 지금 화면에서 시작할 레시피 고르기, 누른 버튼을 알아보고 다시 찾기. 레시피에는 누른 버튼과 그 주변 요소만 저장 |
| 화면 사진 (접근성 `takeScreenshot`) | 패널을 띄워 둔 동안에만 | 글자가 없는 버튼을 그림으로 찾기. 레시피에는 버튼 부분만 잘라 저장, 화면 전체는 찾은 뒤 버림 |
| 녹화 중 화면 터치 (누른 자리 · 길게 누르기 · 밀기) — 접근성 오버레이 | 녹화할 때만 (상태 표시줄 · 내비게이션 바는 덮지 않음) | 클릭 신호를 보내지 않는 앱에서도 누른 자리를 단계로 기억하고, 같은 터치를 그 앱에 그대로 전달. 레시피에는 누른 자리 · 그 자리 버튼 정보 · 버튼 사진만 저장 |
| 실행할 앱 (설치된 앱 중 녹화 중 연 앱의 패키지 이름, 기본 홈 앱) | 녹화할 때 | 녹화 중 홈으로 가거나 다른 앱을 열면 그 단계를 기억하고, 실행 때 그 앱을 엶(녹화 때와 다른 화면이면 묻고 그 앱을 첫 화면부터 다시 엶). 레시피에만 저장 |
| 알림창 · 빠른 설정 (녹화 중 누른 알림의 앱 · 제목, 누른 타일 글자) | 녹화 중 알림창을 열어 누를 때 | 실행 때 알림창을 열어 같은 앱 · 제목의 알림을 찾아 누름. 레시피에는 누른 알림 줄의 글자(앱 이름 · 제목 · 그 알림의 내용 · 버튼 글자)만 저장, 다른 알림 내용은 저장하지 않음 |
| 녹화 화면 (단계마다 화면 전체 사진 · 그 화면 UI 정보) | 녹화할 때 | 저장 전 편집에서 목표 다시 고르기 · 숫자 조건 영역 고르기. **레시피를 저장하면 지움**, 녹화를 버리거나 레시피를 지우거나 저장하지 않고 7일이 지나도 지움 |
| 레시피 (단계 · 버튼 정보 · 버튼 사진 · 대기 시간 · 사용자가 가르친 팝업 닫기 버튼 · 견본) | 사용자가 저장할 때 | 실행. 사용자가 지울 때까지 |
| 실행 기록 (실패한 단계의 화면 사진 · UI 정보 · 후보) | 실행이 실패했을 때 | 실패 화면에서 고치기. 고치면 지우고 최근 몇 개만 남김 |
| 앱 설정 · 동의 기록 | — | 앱 동작 |

- **비밀번호 칸**(Android가 비밀번호로 표시한 입력 칸)의 내용은 녹화 · 저장하지 않습니다.
- 실행할 때마다 바뀌는 입력 값은 실행 · 보정 때 화면에서 물어보고 저장하지 않습니다.
- Android가 보안 화면으로 막은 화면(은행 앱 등)은 사진을 찍을 수 없습니다.
- 위 정보는 광고 요청에 넣지 않습니다. 광고 SDK는 앱이 화면에서 읽은 내용 · 레시피를 받지 않습니다.

### 2-3. 제3자 서비스

| 서비스 | 처리하는 정보 | 개발자가 받는 것 |
|---|---|---|
| Google AdMob (광고 · 광고 동의) | 광고 ID, IP 주소, 기기 · 앱 정보, 광고 상호작용, 광고 동의 선택 | 없음 (집계 수익 보고서만) |
| Google ML Kit 글자 인식 (Google Play 서비스) | 기기 정보(제조사 · 모델 · OS 버전), 앱 패키지 이름 · 버전, 설치별 식별자, 성능 지표(처리 시간) — Google이 진단 · 사용 통계에 씀. **화면 사진과 읽은 글자는 보내지 않음** (기기 안에서 인식), 글자 인식 모델은 Play 서비스가 내려받음 | 없음 |
| Google Play 결제 (후원) | 결제 수단, 구매 기록 | 구매한 후원 상품 종류 · 구매 확인 정보 (이름 · 결제 수단은 받지 않음) |
| Google Play 인앱 업데이트 | 새 버전 확인 · 내려받기 (기기의 Play 스토어 앱이 처리) | 없음 |
| Android 백업 (Google 계정, 사용자가 켠 경우) | **앱 설정만** — 레시피 · 사진 · 실행 기록은 백업하지 않음 | 없음 |

각 서비스의 처리 방식은 [Google 개인정보처리방침](https://policies.google.com/privacy)을 따릅니다.

## 3. 보유 기간 및 파기

- 기기 안의 정보: 사용자가 레시피 · 기록을 지우거나, 앱을 삭제하거나, 앱 데이터를 지우면 삭제됩니다.
- 녹화 화면 사진은 레시피를 저장하면 지우고, 저장하지 않은 녹화는 7일 뒤 지웁니다.
- 실행 기록은 고치면 지우고 최근 몇 개만 남깁니다.
- 개발자가 보관하는 개인정보는 없습니다. 광고 · 결제 정보는 Google 정책에 따라 Google이 보관합니다.

## 4. 제3자 제공 · 처리 위탁 및 국외 이전

개발자는 개인정보를 제3자에게 제공하지 않습니다. 광고 · 결제 · 글자 인식을 위해 아래와 같이 Google이 처리하며, 이 과정에서 정보가 국외로 이전됩니다.

| 받는 자 | 이전 국가 | 이전 항목 | 목적 | 이전 일시 · 방법 | 보유 기간 |
|---|---|---|---|---|---|
| Google LLC (AdMob) | 미국 등 Google 데이터센터 소재국 | 2-3 광고 항목 | 광고 표시 · 측정 · 광고 동의 | 앱 홈 화면에서 광고를 불러올 때 네트워크(HTTPS)로 전송 | Google 정책에 따름 |
| Google LLC (Google Play 결제) | 미국 등 | 2-3 결제 항목 | 결제 처리 | 결제할 때 | Google 정책에 따름 |
| Google LLC (ML Kit) | 미국 등 | 2-3 글자 인식 항목 (화면 사진 · 글자 제외) | 진단 · 사용 통계 | 글자 인식을 쓸 때 네트워크(HTTPS)로 전송 | Google 정책에 따름 |

화면 내용 · 레시피 · 실행 기록은 이전하지 않습니다. 광고 개인정보는 5절 방법으로 제한할 수 있습니다. Android 백업은 사용자 본인의 Google 계정에 저장되며 2-3의 앱 설정만 포함합니다.

## 5. 광고 ID 등 자동 수집 장치와 거부 방법

- 앱은 쿠키 · 분석 도구를 쓰지 않습니다. 광고 SDK가 Android 광고 ID를 사용합니다. 글자 인식(ML Kit)은 광고 ID가 아닌 설치별 식별자를 진단용으로 씁니다.
- 거부 · 제한 방법
  - Android 설정 > 개인정보 보호(또는 Google) > 광고 > **광고 ID 삭제**
  - 유럽경제지역(EEA) · 영국 등: 앱 첫 실행 시 동의 창, 이후 앱의 **설정 > 광고 개인정보 설정**에서 변경
- 후원을 한 번이라도 하면 광고와 광고 동의 창이 표시되지 않습니다.

## 6. 앱이 사용하는 권한

| 권한 | 이유 | 거부하면 |
|---|---|---|
| 접근성 서비스 | 화면의 버튼을 알아보고(2-2) 녹화한 탭 · 스와이프 · 입력 · 뒤로 · 홈 · 앱 열기를 대신 하기, 녹화 중에만 화면 터치를 받아 기억하고 앱에 전달, 볼륨 키 길게 눌러 멈추기, 화면 위 조작 패널 표시. 켜기 전에 앱 안에서 무엇을 보고 어떻게 쓰는지 안내하고 동의를 받습니다 | 앱의 핵심 기능을 쓸 수 없음 |
| 알림 | 실행 중 표시, 끝 · 실패 알림 | 알림이 오지 않음 (실행은 됨) |
| 진동 | 실행 끝 · 질문 알림 진동 | — |
| 인터넷 · 네트워크 상태 · 광고 ID (광고 SDK가 추가) | 배너 광고 · 광고 동의 · 결제 · 글자 인식 모델 | — |
| Google Play 결제 (결제 라이브러리가 추가) | 후원 상품 구매 · 구매 확인 | 후원만 할 수 없음 (나머지 기능은 됨) |

인터넷은 광고 · 결제 · 글자 인식 모델 내려받기와 그 진단 정보에만 쓰며, 화면 내용 · 레시피를 보내는 데 쓰지 않습니다. 접근성 서비스는 언제든 Android 설정 > 접근성에서 끌 수 있습니다. 설정에서 '흔들어 멈추기'를 켜면 녹화 · 보정 · 실행 중에만 움직임 센서 값을 기기 안에서 읽고 저장하지 않습니다(따로 권한 없음). 실행 중에는 기기가 뜨거워지지 않게 배터리 온도 · 잔량 · 충전 여부를 기기 안에서 읽어 찾는 간격을 늘리거나 멈추며, 저장하거나 보내지 않습니다.

## 7. 이용자의 권리와 행사 방법

개발자는 이용자를 알아볼 수 있는 개인정보를 갖고 있지 않습니다. 광고 개인정보는 5절 방법으로 바꿀 수 있습니다. 기기 안의 정보는 앱에서 레시피 · 기록을 지우거나 앱 데이터를 지워 직접 삭제할 수 있습니다. 궁금한 점은 아래 이메일로 문의해 주세요.

## 8. 안전성 확보 조치

- 모든 정보는 다른 앱이 읽을 수 없는 앱 전용 저장소에 저장됩니다.
- 화면 내용 · 레시피 · 실행 기록을 네트워크로 보내는 기능이 없고, 광고 요청에도 넣지 않습니다.
- 접근성 서비스가 켜져 있어도 사용자가 패널을 띄우지 않으면 화면을 읽지 않고, 앱 안 공개 · 동의 전에는 아무것도 읽지 않습니다.

## 9. 아동의 개인정보

앱은 만 14세 미만 아동을 대상으로 하지 않습니다. 만 14세 미만 아동의 개인정보를 받은 것을 알게 되면 바로 삭제합니다.

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
- There is no sign-up. What the app reads on screen, your recipes and run history **never leave your device and are not used for ads or analytics.**
- The app uses an accessibility service to read on-screen text, button information and screenshots — **only while you keep the floating control panel open** (recording, calibrating, running, or choosing a recipe to start), and only to tap again the buttons you recorded. When the panel is closed, the app does not read the screen. While recording, it receives your touches to remember where you tapped and passes them on to the app. While checking a new recipe (slow replay), it briefly blocks touches so nothing is tapped by accident; these touches are not recorded.
- Recipes, button images and run history are stored **only on your device**. Recorded screenshots are kept only until you save the recipe, for fixing steps, then deleted. Password fields are never stored.
- The banner ad at the bottom of the app's home screen is served by Google AdMob, which processes data such as the advertising ID. Ads appear only in the app's own screens, never in the floating panel over other apps.
- The developer receives no information that identifies you.

## 1. Purposes

| Purpose | Details |
|---|---|
| Recording | Remembering which button you tapped (text, ID, position, button image, nearby elements), receiving your touches while recording to remember where you tapped and passing them on to the app, remembering Back, Home and apps you opened, and briefly keeping each step's screen so you can re-choose targets or condition areas before saving |
| Calibrating and running | Waiting until a recorded button is visible and tapping it for you; stopping and asking you when it cannot be found |
| Run history | Keeping the screen information of a failed step so you can review and fix it |
| Showing ads | Showing a banner ad at the bottom of the app's home screen (Google AdMob) |
| Processing tips | Verifying in-app tip purchases and removing ads for supporters (Google Play Billing, where tips are offered) |

## 2. Information we process

### 2-1. Information the developer receives

**None.** The app has no sign-up, feedback upload, analytics or crash reporting. From the ad, billing and text recognition services the developer receives only aggregated reports and purchase verification data (2-3).

### 2-2. Information processed on your device only

| Item | When | Used for / kept |
|---|---|---|
| On-screen UI information (visible text, view IDs, types, positions) — accessibility service | Only while the panel is open | Choosing a recipe to start on the current screen; identifying and finding the tapped button. A recipe stores only the tapped button and its nearby elements |
| Screenshots (accessibility `takeScreenshot`) | Only while the panel is open | Finding buttons that have no text. A recipe stores only the cropped button; full screenshots are discarded after matching |
| Touches while recording (where you tap, long-press or swipe) — accessibility overlay | Only while recording (the status bar and navigation bar are not covered) | Remembering where you tapped even in apps that send no click signal, and passing the same touch on to that app. A recipe stores only the tapped position, the button information there and the button image |
| Apps to open (package names of installed apps you open while recording, the default home app) | While recording | Remembering a step when you go home or open another app while recording, and opening that app when running (if it opens on a different screen, the app asks and reopens it from its first screen). Stored only in the recipe |
| Notification shade and quick settings (the app and title of a notification you tap while recording, the tile text) | When you open the shade and tap while recording | Opening the shade when running and tapping a notification from the same app with the same title. A recipe stores only the text of the notification you tapped (app name, title, its content and button text), not other notifications |
| Recorded screens (a full screenshot and its UI information for each step) | While recording | Re-choosing a target or a number-condition area while editing before you save. **Deleted when you save the recipe**, and also when you discard the recording, delete the recipe, or after 7 days unsaved |
| Recipes (steps, button information, button images, waits, popup close buttons and samples you taught) | When you save | Running. Until you delete them |
| Run history (screenshot, UI information and candidates of a failed step) | When a run fails | Fixing the step. Removed once fixed; only the most recent few are kept |
| App settings and consent record | — | Running the app |

- Contents of **password fields** (input fields Android marks as passwords) are never recorded or stored.
- Values that change on every run are asked on screen during the run and are not stored.
- Screens protected by Android as secure (e.g. banking apps) cannot be captured.
- None of the above is included in ad requests. The ads SDK does not receive what the app reads on screen or your recipes.

### 2-3. Third-party services

| Service | Information | What the developer receives |
|---|---|---|
| Google AdMob (ads and ad consent) | Advertising ID, IP address, device and app information, ad interactions, consent choices | Nothing (aggregated revenue reports only) |
| Google ML Kit text recognition (Google Play services) | Device information (manufacturer, model, OS version), app package name and version, a per-installation identifier, performance metrics (latency) — used by Google for diagnostics and usage analytics. **Screenshots and recognized text are not sent** (recognition runs on the device); the model is downloaded by Play services | Nothing |
| Google Play Billing (tips) | Payment method, purchase history | Which tip product was purchased and purchase verification data (no name or payment details) |
| Google Play in-app updates | Checking for and downloading new versions (handled by the Play Store app on your device) | Nothing |
| Android backup (your Google account, if enabled) | **App settings only** — recipes, images and run history are not backed up | Nothing |

See the [Google Privacy Policy](https://policies.google.com/privacy) for how these services handle data.

## 3. Retention and deletion

- On-device data is deleted when you delete recipes or history, uninstall the app, or clear its data.
- Recorded screenshots are deleted when you save the recipe; unsaved recordings are deleted after 7 days.
- Run history is removed once fixed, and only the most recent few entries are kept.
- The developer keeps no personal data. Ad and billing data are kept by Google under Google's policies.

## 4. Processors and international transfers

The developer does not sell or share your personal information with third parties. Google LLC processes data for ads (AdMob), payments (Play Billing) and text recognition diagnostics (ML Kit), which may involve transfer to the United States and other countries where Google operates data centers. On-screen content, recipes and run history are never transferred. Android backup is stored in your own Google account and contains only the app settings in 2-3.

## 5. Advertising ID and your choices

- The app does not use cookies or analytics tools. The ads SDK uses the Android advertising ID. Text recognition (ML Kit) uses a per-installation identifier for diagnostics, not the advertising ID.
- You can delete or reset it in Android Settings > Privacy (or Google) > Ads.
- In the EEA, UK and other applicable regions, you will see a consent form on first launch and can change your choice later in **Settings > Ad privacy settings**.
- Legal basis (EEA/UK): consent for personalized ads.
- Ads and the consent form are not shown once you make any tip purchase.

## 6. Permissions

| Permission | Why | If denied |
|---|---|---|
| Accessibility service | To identify buttons on screen (2-2) and perform the recorded taps, swipes, text input, back, home and app launches for you, to receive your touches only while recording and pass them on to the app, to stop on a long press of the volume key, and to show the floating control panel. Before you turn it on, the app explains in the app what it reads and how it is used and asks for your consent | Core features unavailable |
| Notifications | Ongoing run status, finish and failure alerts | No alerts (runs still work) |
| Vibration | Vibration for finish and question alerts | — |
| Internet, network state, advertising ID (added by the ads SDK) | Banner ads, ad consent, payments, text recognition model | — |
| Google Play Billing (added by the billing library) | Buying tip products and verifying purchases | Tips unavailable (everything else works) |

The Internet is used only for ads, payments, downloading the text recognition model and its diagnostics, never to send on-screen content or recipes. You can turn off the accessibility service at any time in Android Settings > Accessibility. If you turn on "shake to stop" in Settings, the app reads the motion sensor on the device only while recording, calibrating or running, and does not store it (no permission required). While running, the app reads the battery temperature, level and charging state on the device to slow down or stop before the device overheats; this is not stored or sent.

## 7. Your rights

The developer holds no personal information that identifies you. You can change ad privacy choices as described in section 5. You can delete on-device data yourself by deleting recipes or history in the app, or by clearing the app's data. For questions, email the address below.

## 8. Children

The app is not directed to children under 14 (under 13 in the United States) If we learn we have received a child's personal information, we will delete it.

## 9. Contact

LCEMJR (Privacy officer: Maro Cheon) — lcemjr.apps@gmail.com

## 10. Changes

This policy is effective from **November 3, 2026**. Changes will be posted on this page with a new effective date. If a feature that sends information off the device (such as recipe sharing) is added, this policy will be updated before that feature is released.

# 주중계획표 공개 화면

교직원 공유용 주소는 아래 하나만 사용합니다.

<https://school-training-sign.github.io/weekly-plan/>

이 저장소는 주중계획표 화면만 제공하며 일정·운영현황·방송 요청 데이터는
저장하지 않습니다. 실제 데이터는 학교 계정 소유 Google Sheet에 남고,
학교 계정 소유 Apps Script는 익명 JSON API로만 호출됩니다.

## 운영 원칙

- `script.google.com` 주소를 교직원에게 직접 공유하지 않습니다.
- 다른 주소로 자동 이동시키는 리디렉션을 추가하지 않습니다.
- `index.html`은 `weekly-plan-apps-script/frontend` 빌드 결과로 교체합니다.
- 화면 변경 후에는 API 호환성 검사와 비로그인 접속 검사를 통과한 결과만 게시합니다.

이 구조는 여러 Google 계정이 로그인된 브라우저가 Apps Script 주소에
`/u/숫자`를 삽입해 접속을 실패시키는 문제를 피하기 위한 것입니다.

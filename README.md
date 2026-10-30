# 위촉·임명장 발급소 스킬 (appointment-certificate-office)

위촉장·임명장을 기안 → 검토·결재 → 발급번호 → 발급·전달 → 대장·수령·진위확인·취소까지 다루는 AI 스킬입니다.
Claude 아티팩트 「위촉·임명장 발급소」(https://claude.ai/artifact/8jdR8WSzYTSXCeXddPxFtf)를 쓰고, 고치고, 다른 위원회(예: 중랑 AI파트너즈)에 맞춰 다시 만들 때 씁니다.

## 구성

- `SKILL.md` — 원칙 5개, 작업 흐름, 일괄 발급, 앱 수정 지침, 완료 보고 형식
- `references/app-spec.md` — 화면·입력 칸·번호와 코드·저장 구조
- `references/gpt-review-2026-10-29.md` — GPT 개선 의견(공공 실무/UX/보안/확장) 원문, 코드 대조, v2 반영 현황표
- `assets/index.html` — 앱 v2 소스 (GPT 검토 반영: 예시값·미연결 발급 차단, 결재문서 번호 필수, 생년월일 최소수집, 직인 원본 비공개, 12자리 진위코드, 상태 변경 사유·이력, 수령 확인)
- `assets/index_v1.html` — 10/29 이전 원본(비교용)

## 주의

- 이 스킬은 결재·관인 사용 권한을 만들지 않습니다. 공식 결재 근거를 확인한 뒤에만 발급합니다.
- 실제 개인정보, 관인 이미지, 인증정보를 이 저장소에 올리지 마세요. 예시값(홍길동·한빛구·김한빛)은 견본입니다.
- 진위확인은 "발급 기록 대조"이며 이미지 위변조 판별이나 전자서명이 아닙니다. 서버 권한검사·조회 횟수 제한·전자서명은 아티팩트 구조상 v2에도 없습니다. 공식 운영 전 서버 조회·권한 분리가 필요합니다.
- 법·규정(사무전결, 관인, 개인정보, 기록물 보존) 관련 내용은 담당 부서 확인이 필요합니다.

## 연계 (밸류체인)

이 저장소는 [policy-media-desk](https://github.com/goodmorninghope-khs/policy-media-desk) 밸류체인의 **⑥ 기록** 고리다. 상태: 제안 (발행인 확인 후 실제로 이으면 '연계'로 바꾼다).

- 받음: 독자 패널·외부 필진·AI파트너즈 위촉이 생기면 위촉장 발급
- 넘김: 위촉된 사람 → PEOPLE 지면 소개 후보
- 넘길 때는 출처 지면(지면명·호수·날짜·링크)과 '닿는 공약'을 붙이고, 침은 의견으로 남긴다. 결정은 받는 고리의 책임자가 한다.

전체 사슬: [references/value-chain.md](https://github.com/goodmorninghope-khs/policy-media-desk/blob/main/references/value-chain.md)

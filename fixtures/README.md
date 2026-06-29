# 테스트 픽스처

> **이 디렉터리의 `hwp5/*.hwp`·`hwpx/*.hwpx` 문서는 저장소에 동봉하지 않는다**
> (`.gitignore`로 제외 — 로컬 전용). 아래 출처에서 받아 같은 경로에 두면 렌더/PDF 테스트가
> 동작하고, 없으면 해당 테스트는 자동으로 **skip**된다. 이 README와 `golden/README.md`만 커밋한다.

## hwp5/

[hahnlee/hwp-rs](https://github.com/hahnlee/hwp-rs) (Apache-2.0)의 통합 테스트
픽스처에서 가져옴:

- `hello_world.hwp`, `bookmark.hwp`, `color_fill.hwp`, `outline.hwp` — 기능별 최소 파일
  (hwp-rs `integration/project/files`)
- `annual_report.hwp`, `work_report.hwp` — 실문서에 가까운 샘플
  (hwp-rs `integration/naver_documents/files`, 원출처 Naver 무료 문서 템플릿)

`annual_report.hwp`에는 템플릿에 포함된 장식용 이미지(BinData JPG/PNG), `work_report.hwp`에는
작은 비트맵(117×17 BMP)이 임베드되어 있다. 본문은 자리표시자("OOOOO", "상세 내용을 입력하세요")
뿐인 빈 템플릿으로 실제 개인정보·조직 식별 정보는 없다. 모든 픽스처는 위 Apache-2.0 저장소에서
재배포된 것을 가져왔다(루트 `NOTICE` 참고).

## hwpx/

- `minimal.hwpx` — hwpx MCP 서버로 생성한 최소 문서 (한/영/숫자 혼합 3문단)

## 대형 corpus

수백 개 이상의 야생 문서 소크 테스트는 커밋하지 않고
`HWP_CORPUS_DIR` 환경변수로 외부 디렉터리를 가리켜 실행한다.

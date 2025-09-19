# 물리치료 환자 스케줄 매트릭스

환자별 치료 스케줄을 매트릭스 형태로 시각화하는 웹 애플리케이션입니다.

## 주요 기능

- 📋 환자별 치료 스케줄 매트릭스 뷰
- 📅 월별 필터링
- 🔍 환자 검색
- 🎨 코스별 색상 구분
- 📱 반응형 디자인

## 파일 구조

- `pt_data.js` - 환자 데이터 (JavaScript 형식)
- `pt_data.json` - 환자 데이터 (JSON 형식)
- `real_pt_data.json` - 가명처리된 실제 환자 데이터
- `excel_format_data.json` - Excel 형식 데이터
- `*.html` - 다양한 매트릭스 뷰 페이지

## 개인정보 보호

모든 환자 정보는 가명처리되었습니다:
- 실제 환자 이름 → 환자A, 환자B, 환자C...
- 실제 치료사 이름 → 치료사A, 치료사B, 치료사C...

## 사용법

HTML 파일을 브라우저에서 열어서 사용하세요:
- `patient-schedule-matrix.html` - 메인 스케줄 매트릭스
- `real-patient-matrix.html` - 실시간 환자 매트릭스
- `excel-style-matrix.html` - Excel 스타일 매트릭스
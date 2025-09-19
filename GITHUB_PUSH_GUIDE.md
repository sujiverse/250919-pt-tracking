# 🚀 GitHub 푸시 가이드

## 방법 1: GitHub 웹사이트 사용 (가장 쉬움)

### 1단계: GitHub에서 새 리포지토리 생성
1. [GitHub.com](https://github.com)에 로그인
2. 우상단 `+` 버튼 클릭 → `New repository`
3. Repository name: `pt-schedule-matrix` (또는 원하는 이름)
4. Description: `물리치료 환자 스케줄 매트릭스 시스템 (가명처리 완료)`
5. **Public** 또는 **Private** 선택 (Private 권장)
6. ❌ `Add a README file` 체크 해제 (이미 있음)
7. `Create repository` 클릭

### 2단계: 로컬에서 원격 리포지토리 연결
GitHub에서 생성한 리포지토리 페이지에서 표시되는 HTTPS 주소를 복사한 후:

```bash
# 원격 리포지토리 추가
git remote add origin https://github.com/YOUR_USERNAME/pt-schedule-matrix.git

# 브랜치 이름 확인
git branch -M main

# 푸시
git push -u origin main
```

## 방법 2: GitHub CLI 사용 (설치 필요)

### GitHub CLI 설치 후:
```bash
# 리포지토리 생성 및 푸시를 한 번에
gh repo create pt-schedule-matrix --private --source=. --remote=origin --push
```

## 중요 사항

### ✅ 개인정보 보호 완료
- 모든 실제 환자 이름 → 환자A, 환자B, 환자101, 환자201 등으로 가명처리
- 모든 실제 치료사 이름 → 치료사1, 치료사2 등으로 가명처리
- Excel 파일 등 개인정보 포함 파일 제거
- 총 100+ 개 실제 이름 가명처리 완료

### 📁 포함된 파일들
- `README.md` - 프로젝트 설명
- `patient-schedule-matrix.html` - 메인 스케줄 매트릭스
- `real-patient-matrix.html` - 실시간 환자 매트릭스
- `pt_data.json` - 가명처리된 환자 데이터
- `real_pt_data.json` - 가명처리된 실제 환자 데이터
- 기타 HTML 매트릭스 뷰들

### 🔒 안전성
- GitHub에 업로드해도 개인정보 노출 위험 없음
- Public 리포지토리로 설정해도 안전
- 모든 실제 이름이 가명으로 처리됨

## 문제 해결

### 인증 오류 시:
```bash
# GitHub Personal Access Token 사용
# Settings → Developer settings → Personal access tokens → Generate new token
# Username 대신 토큰 사용
```

### 푸시 실패 시:
```bash
# 강제 푸시 (주의: 처음에만 사용)
git push -f origin main
```

## 푸시 후 확인사항
- [ ] GitHub에서 파일들이 정상적으로 업로드됨
- [ ] README.md가 제대로 표시됨
- [ ] HTML 파일들이 GitHub Pages로 호스팅 가능
- [ ] 모든 개인정보가 가명처리된 상태
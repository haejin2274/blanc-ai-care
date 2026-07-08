# 블랑 AI Care

블랑여성의원 환자용 AI 상담 웹앱 프로토타입입니다.

## 현재 포함 기능
- 환자 회원가입 / 로그인 / 자동 로그인 유지
- 관리자 로그인
- AI 상담 카테고리와 FAQ 키워드 답변
- 질염·방광염 증상 태그
- 피부과 시술 목록
- 피부과 시술 네이버예약 / 전화문의 연결 구조
- 병원 위치, 주차, 진료시간 안내
- 휴무일 및 공지사항 관리
- 관리자 시술 추가
- 관리자 FAQ 답변 등록

## GitHub 업로드
1. GitHub에서 새 저장소를 만듭니다.
2. 이 폴더 안의 파일 전체를 업로드합니다.
3. `index.html`, `render.yaml`, `README.md`가 저장소 최상단에 있어야 합니다.

## Render 배포
### Blueprint 방식
1. Render에서 GitHub 계정을 연결합니다.
2. `New` → `Blueprint`를 선택합니다.
3. 방금 만든 GitHub 저장소를 선택합니다.
4. Render가 저장소 최상단의 `render.yaml`을 찾으면 배포합니다.

### 직접 Static Site 방식
Blueprint 대신 직접 만들 경우:
- 서비스 유형: Static Site
- Build Command: `echo "Static site - no build required"`
- Publish Directory: `.`
- 브랜치: `main`

## 현재 버전의 중요한 제한
이 버전은 정적 웹앱입니다.
공지, 휴무일, FAQ, 관리자 계정 등은 각 브라우저의 Local Storage에 저장됩니다.
따라서 Render에 배포해도 다른 휴대폰이나 다른 직원 PC와 데이터가 자동 공유되지는 않습니다.

다음 단계에서 Node.js 서버와 DB를 연결하면:
- 직원 여러 명이 같은 공지·FAQ·휴무일을 관리
- 환자 문의와 상담기록 저장
- 관리자 계정 보안 강화
- 실제 AI API 연결

이 가능해집니다.

# 제품 요구사항 문서 (PRD)

## 📋 개요

**claude-nextjs-starters**는 다양한 Next.js 프로젝트의 출발점이 되는 **모던 웹 애플리케이션 스타터 템플릿**입니다.

이 프로젝트는 반복적인 초기 설정 작업을 최소화하고, 즉시 사용 가능한 일관된 폼 패턴, 디자인 시스템, 문서화된 개발 컨벤션을 제공하는 것을 목표로 합니다.

## 🎯 목표 (Goals)

1. **개발 속도 향상**: 새 프로젝트를 빠르게 시작할 수 있는 견고한 기반 제공
2. **코드 일관성**: React Hook Form + Zod를 표준 폼 패턴으로 통일하여 프로젝트 전체에서 일관된 개발 경험 제공
3. **설계 시스템**: shadcn/ui를 통한 일관된 UI 컴포넌트 사용
4. **문서화**: 모든 개발 관례를 명확하게 문서화하여 팀 협업 효율성 증대
5. **모범 사례**: Next.js 15, React 19의 최신 기능을 반영한 현대적 아키텍처

## 👥 타깃 사용자

- **개발자/팀**: 새로운 Next.js 프로젝트를 빠르게 시작하려는 개발자
- **스타트업**: MVP를 빠르게 구축해야 하는 초기 스타트업
- **엔터프라이즈 팀**: 회사 표준 스택을 바탕으로 한 일관된 프로젝트 구조가 필요한 조직

## ✅ 범위 (In Scope)

이 스타터 템플릿에 포함되는 기능과 특징:

### 기술 스택

- Next.js 15.5.3 (App Router + Turbopack)
- React 19.1.0
- TypeScript 5 (strict mode)
- TailwindCSS v4
- shadcn/ui (new-york style, Radix UI 기반)

### 아키텍처 & 구조

- App Router 기반 라우팅 체계
- 계층화된 디렉토리 구조 (app, components, lib, styles)
- 환경 변수 검증 (Zod)
- 유틸리티 함수 모음

### UI & 디자인

- 16개의 shadcn/ui 컴포넌트 (Button, Input, Card, Dialog 등)
- 반응형 레이아웃 (Header, Footer, Navigation)
- 다크모드 지원 (next-themes)
- 현대적인 아이콘 라이브러리 (Lucide Icons)

### 폼 처리 (표준 패턴)

- **React Hook Form + Zod** 조합으로 폼 검증
- 로그인 폼 (이메일, 비밀번호, 기억하기)
- 회원가입 폼 (이름, 이메일, 비밀번호, 약관 동의)
- 실시간 검증 (mode: 'onChange')
- 일관된 에러 메시지 출력

### 페이지

- **홈 페이지**: 랜딩 페이지 (Hero, Features, CTA 섹션)
- **로그인 페이지**: 기본 로그인 폼 UI
- **회원가입 페이지**: 기본 회원가입 폼 UI

### 개발 도구 & 자동화

- ESLint 9 (next/core-web-vitals, prettier 통합)
- Prettier 3.6 (tailwindcss 클래스 정렬)
- Husky 9 (Git hooks 자동화)
- lint-staged (변경된 파일만 검사)
- TypeScript strict mode

### 문서

- [프로젝트 구조 가이드](guides/project-structure.md)
- [Next.js 15 상세 가이드](guides/nextjs-15.md)
- [컴포넌트 패턴 가이드](guides/component-patterns.md)
- [스타일링 가이드](guides/styling-guide.md)
- [React Hook Form 완전 가이드](guides/forms-react-hook-form.md)

## ❌ 비범위 (Out of Scope)

다음 항목들은 이 스타터 템플릿의 범위를 벗어나며, 추후 확장 또는 프로젝트별 요구에 따라 추가됩니다:

### 인증 & 세션 관리

- 실제 인증 백엔드 (NextAuth.js, Clerk, Auth0 등)
- 세션 토큰 관리
- 보호된 라우트 미들웨어

**사유**: 프로젝트마다 인증 요구사항이 다르므로, 폼 UI와 검증만 제공하고 백엔드 연동은 프로젝트에서 구현

### 데이터베이스 연동

- ORM/쿼리 빌더 (Prisma, Drizzle 등)
- 데이터베이스 마이그레이션
- API 라우트 구현

**사유**: DB 선택이 프로젝트마다 다르며, 스타터에 종속성을 추가하면 유지보수 부담 증가

### 테스트 인프라

- 단위 테스트 (Vitest 등)
- 통합 테스트
- E2E 테스트 (Playwright 등)

**사유**: 테스트는 프로젝트 요구사항에 따라 다르며, 스타터에는 최소한의 설정만 포함

### CI/CD 파이프라인

- GitHub Actions 워크플로우
- 배포 자동화

**사유**: 배포 인프라는 조직/프로젝트마다 상이하므로, 템플릿 레벨에서는 제공하지 않음

### 상태 관리

- Zustand, Redux 등의 전역 상태 관리

**사유**: 폼 상태는 로컬로 충분하며, 필요한 경우 프로젝트에서 추가

## 📊 성공 기준

이 스타터 템플릿이 성공했다고 판단하는 기준:

1. **코드 품질**
   - ✅ `npm run check-all` (typecheck + lint + format:check) 항상 통과
   - ✅ `npm run build` 성공 (Turbopack 빌드)
   - ✅ 모든 파일이 TypeScript strict mode 준수

2. **폼 표준 준수**
   - ✅ 모든 폼 컴포넌트가 React Hook Form + Zod 패턴 사용
   - ✅ 일관된 에러 메시지 및 검증 로직

3. **문서 완성도**
   - ✅ 모든 개발 가이드 문서가 최신 상태 유지
   - ✅ 새로운 기능/변경사항이 문서에 반영

4. **개발 경험**
   - ✅ 신규 페이지/컴포넌트 추가 시 기존 가이드 패턴 준수 가능
   - ✅ 개발자가 쉽게 프로젝트를 포크하여 시작할 수 있음

5. **유지보수**
   - ✅ 의존성 업데이트 시 호환성 유지
   - ✅ 보안 취약점 해결

## 🔄 향후 확장 계획

다음 항목들은 "Out of Scope"이지만 추후 별도 문서 또는 가이드로 제공될 예정입니다:

- [ROADMAP.md](ROADMAP.md)에서 "진행 중/예정" 섹션 참고
  - 인증 백엔드 연동 가이드
  - 데이터베이스 셋업 가이드
  - API 라우트 구현 패턴
  - 테스트 슈트 구축 방법
  - CI/CD 구성 예제

## 📌 참고

- 자세한 기술 스택 정보는 [CLAUDE.md](../CLAUDE.md) 참고
- 개발 중 질문이나 개선 사항은 ROADMAP 또는 이슈로 등록

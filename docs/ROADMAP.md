# 개발 로드맵 (ROADMAP)

## 개요

이 문서는 **claude-nextjs-starters** 프로젝트의 완료 상황과 향후 계획을 추적합니다.

더 자세한 프로젝트 목표와 범위는 [PRD.md](PRD.md)를 참고하세요.

---

## ✅ 완료된 항목 (Phase 1 - Foundation)

### 기본 환경 설정

- [x] Next.js 15.5.3 + Turbopack 초기 셋업
- [x] React 19.1.0 + TypeScript 5 (strict mode)
- [x] 파일 기반 라우팅 (App Router)
- [x] @/\* 경로 alias 설정

### 스타일링 & UI 시스템

- [x] TailwindCSS v4 통합
- [x] shadcn/ui (new-york style) 설정
- [x] 16개 shadcn 컴포넌트 설치 (Button, Input, Card, Dialog, Badge, Alert, Avatar, Checkbox, Label, Separator, Navigation Menu, Progress, Select, Sheet, Skeleton, Sonner)
- [x] Lucide Icons 통합
- [x] 다크모드 지원 (next-themes)

### 레이아웃 & 네비게이션

- [x] 루트 레이아웃 (fonts, metadata, providers)
- [x] Header 컴포넌트 (네비게이션, 모바일 메뉴, 테마 토글)
- [x] Footer 컴포넌트
- [x] 반응형 디자인 (mobile-first)

### 페이지 구조

- [x] 홈 페이지 (Hero, Features, CTA 섹션)
- [x] 로그인 페이지
- [x] 회원가입 페이지

### 폼 처리 표준 통일

- [x] React Hook Form 7.x 통합
- [x] Zod 4.x 스키마 검증
- [x] 로그인 폼 (RHF + Zod 패턴으로 표준화)
  - 이메일 검증
  - 비밀번호 (8자 이상)
  - 기억하기 체크박스
- [x] 회원가입 폼 (RHF + Zod 패턴으로 표준화)
  - 이름 (2-50자)
  - 이메일 검증
  - 비밀번호 (8자 이상)
  - 비밀번호 확인 (일치 검증)
  - 약관 동의 필수

### 개발 도구 & 자동화

- [x] ESLint 9 (flat config, next/core-web-vitals, prettier)
- [x] Prettier 3.6 (tailwindcss 클래스 정렬)
- [x] Husky 9 (pre-commit hook)
- [x] lint-staged (변경된 파일만 검사)
- [x] npm 스크립트 통합:
  - dev (Turbopack)
  - build (production)
  - start (production server)
  - lint, lint:fix
  - format, format:check
  - typecheck
  - check-all (integrated)

### 환경 & 설정

- [x] Environment variable validation (src/lib/env.ts)
- [x] Next.js config 최적화
- [x] TypeScript strict mode

### 문서화

- [x] [프로젝트 구조 가이드](guides/project-structure.md) (9.1KB)
- [x] [Next.js 15 상세 가이드](guides/nextjs-15.md) (11.7KB)
- [x] [컴포넌트 패턴 가이드](guides/component-patterns.md) (16.5KB)
- [x] [React Hook Form 완전 가이드](guides/forms-react-hook-form.md) (41.7KB)
- [x] [스타일링 가이드](guides/styling-guide.md) (11.4KB)
- [x] README.md (프로젝트 소개 및 시작 가이드)
- [x] PRD.md (제품 요구사항 및 범위)
- [x] ROADMAP.md (이 파일)
- [x] CLAUDE.md (개발 지침)

---

## 🚧 진행 중 / 예정 항목 (Phase 2+ - Extensions)

### 인증 & 세션 관리

- [ ] NextAuth.js 또는 Clerk 통합 가이드 작성
- [ ] Server Action 기반 인증 예제
- [ ] 보호된 라우트 미들웨어 (middleware.ts)
- [ ] JWT 토큰 관리 패턴
- [ ] 로그아웃, 프로필 페이지

**예상 시간**: 2-3주  
**의존성**: 폼 표준화 완료 (✅)

### 데이터베이스 & API 라우트

- [ ] Prisma 또는 Drizzle 통합 가이드
- [ ] 기본 API 라우트 구조 예제
- [ ] Server Actions vs API Routes 비교 가이드
- [ ] 데이터베이스 마이그레이션 전략

**예상 시간**: 3-4주  
**의존성**: 인증 구현 (진행 중)

### 테스트 인프라

- [ ] Vitest 또는 Jest 셋업 가이드
- [ ] 단위 테스트 예제 (컴포넌트, 유틸리티)
- [ ] 통합 테스트 예제 (폼 검증 등)
- [ ] Playwright E2E 테스트 가이드

**예상 시간**: 2-3주

### CI/CD 파이프라인

- [ ] GitHub Actions 워크플로우 예제
- [ ] 린트, 빌드, 테스트 자동화
- [ ] 배포 자동화 (Vercel)
- [ ] 환경 변수 관리 가이드

**예상 시간**: 1-2주  
**의존성**: 테스트 인프라 (예정)

### 성능 최적화

- [ ] Image 최적화 (next/image)
- [ ] Font 로딩 최적화
- [ ] 번들 사이즈 분석 및 최적화
- [ ] Core Web Vitals 개선 가이드

**예상 시간**: 1-2주

### 상태 관리

- [ ] Zustand 통합 가이드 (선택사항)
- [ ] Context API 패턴 (내장)
- [ ] 복잡한 폼 상태 관리 예제

**예상 시간**: 1주

### 추가 페이지 & 기능

- [ ] 대시보드 페이지 예제
- [ ] 설정 페이지 예제
- [ ] 404, 500 에러 페이지
- [ ] 로딩 및 스켈레톤 UI 패턴

**예상 시간**: 1-2주

---

## 🎯 마일스톤 계획

### Milestone 1: Foundation (완료 ✅)

- 기본 프로젝트 구조
- 폼 표준 통일
- 문서 기반 제공
- **상태**: ✅ 완료

### Milestone 2: Auth & API (예상 6월 말)

- 인증 백엔드 통합
- API 라우트 구축
- 보호된 라우트

### Milestone 3: Testing & CI (예상 7월 말)

- 테스트 인프라
- CI/CD 파이프라인
- 자동화 검증

### Milestone 4: Production Ready (예상 8월 중)

- 성능 최적화
- 완전한 배포 가이드
- 모니터링 및 로깅

---

## 📊 진행 상황

| 카테고리       | 완료도  | 상태        |
| -------------- | ------- | ----------- |
| 기본 환경 설정 | 100%    | ✅          |
| UI & 스타일링  | 100%    | ✅          |
| 폼 처리        | 100%    | ✅          |
| 개발 도구      | 100%    | ✅          |
| 문서화         | 100%    | ✅          |
| 인증 백엔드    | 0%      | 📋          |
| 데이터베이스   | 0%      | 📋          |
| 테스트         | 0%      | 📋          |
| CI/CD          | 0%      | 📋          |
| **전체**       | **25%** | **Phase 1** |

---

## 🔗 관련 문서

- [PRD.md](PRD.md) - 프로젝트 목표 및 범위
- [CLAUDE.md](../CLAUDE.md) - 개발 지침
- [README.md](../README.md) - 프로젝트 소개

---

## 💬 피드백 및 기여

개선 사항이나 새로운 기능에 대한 제안은 이슈 또는 PR로 제출해주세요.

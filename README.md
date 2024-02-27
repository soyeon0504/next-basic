# Next.js

## 1. Next.js 기본 상식

### 1.1. App Router 채용

    : 파일 시스템 라우터
    : /src/app/test 폴더생성 / page.tsx 파일생성
    ```ts
    // app/basic/page.tsx
    import React from "react";

    const page = () => {
    return <div>베이직 페이지</div>;
    };

    export default page;

    ```

    : /src/app/basic 폴더생성 / page.tsx 파일생성
    ```ts
    // app/test/page.tsx
    import React from "react";

    const page = () => {
    return <div>테스트 페이지</div>;
    };

    export default page;
    ```

### 1.2. RSC 가 Next.js 기본 컴포넌트

- React Server Component
- React 18 버전
- 서버에서 만드므로 보안
- 서버에서 만드므로 속도 (API 연동)
- 서버에서 만드므로 캐싱이 기본
- yarn buil 시 압축을 하므로 용량 감소
- use 즉, Hook 사용못함, 이벤트 핸들러 사용 못함.

### 1.3. Client Component 가 Next.js 기본 컴포넌트

- 'use client' 작성하면 Hook 사용, 이벤트 핸들러도 가능

### 1.4. 라우팅 자동 지원

- App Router 방식이므로 보여줄 페이지들은 반드시 app/ 폴더에 생성
- 웹 브라우저 URL형식에 맞게 /app/폴더생성
- 정적경로(Static Router)
- 사용하는 파일 명이 미리 약속이 되어있다.
  : [파일명참조](https://nextjs.org/docs/getting-started/project-structure)
  : http://localhost:3000/board/
  : /app/board/page.tsx 실행

- 동적 경로(Dynamic Router)
  : http://localhost:3000/board/[aaa] 폴더명 / page.tsx
  : http://localhost:3000/board/1
  : http://localhost:3000/board/100

### 1.5. 페이지이동

- Link 라이브러리 내장.
- useRouter : 버튼/실행결과로 페이지 이동('use client')

### 1.6. CSS

- css
- CSS-IN-JS : styled, emotion
- 파일명.module.css
- scss

### 1.7. API 백엔드 데이터 패칭

- React Query 와 비슷하게 처리 (revalitdate : 재검증)
- Next.js 내부적으로 Fetch API 제공

### 1.8. Metadata 제공

- SEO 지원 (미리 html 만들기 때문에 검색엔진 html 노출)
- 정적 Metadata 객체 생성 및 적용
- 동적 Metadata 객체 생성 및 적용

### 1.9. 배포
- Server 가 있어야 합니다.
- Nofde.js 버전을 맞추어야 함.
- 환경설정 파일을 셋팅

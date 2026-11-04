# Prompt Archive — 배포용

## 기능
- 페소 프롬 / 행동 프롬프트 분리
- 검색, 복사, 이미지 미리보기
- 관리자 이메일 로그인 후 프롬프트 추가·수정·삭제 및 이미지 업로드
- 공개 방문자는 조회·복사만 가능

## 설정 및 배포
1. Supabase 프로젝트를 생성합니다.
2. SQL Editor에서 `supabase-setup.sql`을 실행합니다. `YOUR_ADMIN_EMAIL`을 관리자 이메일로 치환한 후 실행하세요.
3. Authentication > Users에서 관리자 이메일/비밀번호 사용자를 만듭니다.
4. Project Settings > API에서 Project URL 및 anon/public key를 가져옵니다.
5. `index.html` 내 `SUPABASE_URL`, `SUPABASE_ANON_KEY` 값을 교체합니다. **service_role 키는 절대 브라우저에 넣지 마세요.**
6. `index.html`을 Netlify 또는 GitHub Pages에 배포하고 링크를 공유합니다.

이미지는 Supabase Storage의 공개 `prompt-images` bucket에 저장되며 8MB 이하로 업로드하도록 제한했습니다.
GitHub Pages guide: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
Netlify: https://docs.netlify.com/

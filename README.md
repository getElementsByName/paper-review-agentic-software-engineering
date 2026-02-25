# Slidev Presentation Project

This repository is configured for building and presenting slides with [Slidev](https://sli.dev/).

## Getting Started

1. Install dependencies:
   ```bash
   npm install
   ```

2. Run local dev server:
   ```bash
   npm run dev
   ```

3. Build static presentation:
   ```bash
   npm run build
   ```

4. Export PDF (requires Playwright/Chromium):
   ```bash
   npm run export
   ```

## Deploy to GitHub Pages

`main` branch push 시 GitHub Actions가 자동으로 정적 빌드 후 Pages에 배포합니다.

1. GitHub 저장소에서 `Settings > Pages`로 이동합니다.
2. `Build and deployment`의 `Source`를 `GitHub Actions`로 선택합니다.
3. `main`에 푸시하면 `.github/workflows/deploy-pages.yml`이 실행됩니다.

배포 URL:

- 사용자/조직 사이트(`{user}.github.io`) 저장소: `https://{user}.github.io/`
- 프로젝트 저장소: `https://{user}.github.io/{repo}/`

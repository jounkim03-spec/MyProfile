# MyProfile-KJU

전북대학교 컴퓨터인공지능학부 김조운의 개인 소개 웹사이트입니다. 2026학년도 초급프로젝트 과제로 제작하게 됐습니다.

- 사이트: https://jounkim03-spec.github.io/MyProfile/
- 저장소: https://github.com/jounkim03-spec/MyProfile

## 사이트 구성
- 홈: 글 목록(대회 활동 글)
- 자기소개: 관심 분야, 학습 목표, 역량과 적용 사례
- 대표 활동: 2026 프로그래밍 경진대회 도전상
- 보관함, 검색: 테마 기본 기능

## 사용한 도구와 버전
GitHub Actions 빌드 환경 기준입니다. (`.github/workflows/`의 워크플로 파일)

| 도구 | 버전 |
|---|---|
| Hugo (extended) | 0.167.0 |
| Dart Sass | 1.105.0 |
| Go | 1.27.1 |
| Python | 3.12 |
| Node.js | 24 |

테마: Hugo Theme Stack v3 (Hugo 모듈로 가져옴)

## 빌드와 배포
`main` 브랜치에 push하면 GitHub Actions가 자동으로 빌드하고 GitHub Pages에 배포합니다.

워크플로에서 실행하는 빌드 명령:
```bash
python .github/pages_build.py --dependencies
SITE_BASE_URL="https://jounkim03-spec.github.io/MyProfile/" python .github/pages_build.py --build
```
결과물은 `public/` 폴더에 생성됩니다. (`.gitignore`로 제외)

로컬 실행: 제 컴퓨터에는 Hugo를 설치하지 않았습니다. 파일을 수정한 뒤 push하면 GitHub Actions가 빌드하고, 배포된 사이트에서 결과를 확인합니다.

## 수정과 재배포
| 수정할 것 | 위치 |
|---|---|
| 글 | `site/content/post/` |
| 자기소개 등 고정 페이지 | `site/content/page/` |
| 사이트 제목, 언어, 메뉴, 사이드바 | `site/config/_default/` |
| 아바타 이미지 | `site/assets/img/avatar.png` |

1. 파일을 수정합니다.
2. `git add`, `git commit`, `git push origin main`을 합니다.
3. GitHub 저장소의 **Actions** 탭에서 실행이 초록(성공)인지 확인합니다.
4. 사이트를 새로고침(Ctrl+F5)해서 변경이 반영됐는지 확인합니다.

## 출처와 라이선스
| 자료 | 구분 | 출처 | 이용 조건 |
|---|---|---|---|
| Hugo Theme Stack | 외부 자료 | https://github.com/CaiJimmy/hugo-theme-stack | GNU GPL v3 |
| 소개 글, 대회 활동 글 | 직접 작성(구성은 AI 제안 참고) | - | - |
| 아바타 이미지 |  AI 도구(Claude)를 활용한 아바타 이미지 생성 | Claude | - |
| 빌드 설정·스크립트 | 수업 제공 | `prepare_github_pages.py` (수업 제공) | 수업 자료 |

테마는 **GNU General Public License v3.0**으로 배포됩니다. 테마 하단의 "Theme Stack designed by Jimmy" 문구와 링크를 유지합니다.

테마 ZIP 다운로드 날짜: 2026-11-04

AI 도구를 일부 작업에 활용했고, 자세한 내용은 제출 보고서에 있습니다.
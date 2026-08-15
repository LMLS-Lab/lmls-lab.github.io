# Large-scale Machine Learning Systems Lab. — 연구실 홈페이지

Jekyll로 만든 정적 연구실 홈페이지입니다. GitHub Pages에 무료로 배포할 수 있도록 구성되어 있습니다.

## 폴더 구조

```
_config.yml          사이트 전역 설정 (연구실 이름, 이메일, 네비게이션 메뉴 등)
Gemfile               로컬 빌드용 Ruby 의존성 (github-pages 공식 gem)
index.md              홈 (소개)
research.md           연구 분야 소개
people.md             People 목록 페이지 (교수/학생/졸업생 자동 그룹핑)
publications.md       논문 목록 페이지 (연도별 자동 그룹핑)
news.md               뉴스 목록 페이지
contact.md            연락처
_people/              구성원 1인당 파일 1개 (마크다운 + front matter)
_publications/        논문 1편당 파일 1개
_news/                뉴스/공지 1건당 파일 1개
_layouts/              페이지 템플릿
_includes/             헤더/푸터 등 공통 조각
assets/                CSS, JS, 이미지
.github/workflows/pages.yml   GitHub Actions 자동 배포 워크플로
```

## 1. 내용 채우기 (가장 먼저 할 일)

### `_config.yml`
`TODO` 주석이 달린 항목을 실제 정보로 바꿔주세요.
- `department`, `address` — 정확한 학과명/주소
- `url`, `baseurl` — 배포 방식에 따라 다름 (아래 "배포하기" 참고)
- `github_username`, `google_scholar_url` 등 — 있으면 채우고, 없으면 빈 문자열로 두세요

### 구성원 추가 — `_people/`
- `_people/example-member.md`를 복사해서 `_people/이름.md`로 새로 만드세요.
- `group` 필드로 Faculty / Ph.D. / M.S. / Undergraduate / Alumni 중 하나를 지정하면 People 페이지에서 자동으로 그룹핑됩니다.
- 사진은 `assets/images/people/` 폴더에 넣고 `photo: /assets/images/people/파일명.jpg`로 지정하세요. 사진이 없으면 이니셜 아이콘이 자동으로 표시됩니다.
- 예시 템플릿 파일(`example-member.md`)은 `published: false`로 되어 있어 실제 사이트에는 노출되지 않습니다. 필요 없으면 지워도 됩니다.

### 논문 추가 — `_publications/`
- `_publications/example-publication.md`를 복사해서 새 파일을 만드세요.
- `year`, `venue`, `pdf`, `code`, `arxiv`, `bibtex` 등을 채우면 자동으로 연도별로 정렬/그룹핑되어 표시됩니다.

### 뉴스 추가 — `_news/`
- `_news/example-news-item.md`를 복사해서 새 파일을 만드세요. 파일명에 날짜를 넣을 필요는 없고, front matter의 `date` 필드만 정확히 채우면 됩니다.

## 2. 로컬에서 미리보기 (선택 사항)

Ruby가 설치되어 있다면:

```bash
bundle install
bundle exec jekyll serve
```

그다음 `http://localhost:4000` 에서 확인할 수 있습니다. (참고: 이번 세션의 클라우드 환경은 rubygems.org 접근이 막혀 있어 여기서는 직접 빌드 테스트를 하지 못했습니다. 대신 모든 YAML front matter와 Liquid 템플릿 문법을 스크립트로 검증했습니다. 실제 빌드는 로컬 또는 GitHub Actions에서 처음 시도하시게 되니, 혹시 에러가 나면 에러 메시지를 알려주시면 바로 고쳐드릴게요.)

## 3. 배포하기 (GitHub Pages)

### 방법 A — GitHub Actions로 배포 (추천, 워크플로 파일 포함되어 있음)

1. GitHub에 새 저장소를 만들고 이 폴더의 내용을 push 합니다.
2. 저장소 **Settings → Pages** 에서 **Source**를 **GitHub Actions**로 선택합니다.
3. `main` 브랜치에 push하면 `.github/workflows/pages.yml`이 자동으로 빌드/배포합니다.
4. 이 방식은 `baseurl`을 빌드 시점에 자동으로 계산하므로 `_config.yml`의 `baseurl` 값을 신경 쓰지 않아도 됩니다.

### 방법 B — 브랜치에서 바로 배포 (더 단순하지만 baseurl을 직접 맞춰야 함)

1. 저장소 **Settings → Pages** 에서 **Source**를 **Deploy from a branch**로, 브랜치는 `main` (루트 `/`)로 선택합니다.
2. `_config.yml`의 `baseurl`을 저장소 이름에 맞게 수정합니다.
   - 저장소 이름이 `사용자명.github.io` (개인/조직 대표 페이지)라면 `baseurl: ""`
   - 저장소 이름이 그 외(`lab-site` 등)라면 `baseurl: "/저장소이름"`
3. `url`도 `https://사용자명.github.io`로 수정합니다.

배포 후 사이트 주소는 `https://사용자명.github.io/저장소이름/` (또는 개인 대표 페이지라면 `https://사용자명.github.io/`) 형태가 됩니다.

## 4. 디자인/색상 바꾸기

`assets/css/style.scss` 상단의 `:root` 변수(`--color-brand` 등)만 바꾸면 사이트 전체 색상 테마가 바뀝니다.

## 5. 언어

현재 모든 페이지 텍스트는 영어로 작성되어 있습니다(국제적인 연구실 홈페이지의 일반적인 관례). 한국어 버전이 필요하시면 말씀해 주세요 — 각 페이지를 한국어로 다시 쓰거나, `/ko/` 하위에 한국어 버전을 별도로 구성해 드릴 수 있습니다.

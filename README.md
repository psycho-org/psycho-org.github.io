# Psycho Tech Blog

Psycho 팀의 기술 블로그 레포지토리입니다.  
팀원들이 개발 과정에서 얻은 경험과 인사이트를 아티클 형태로 공유합니다.

원본 테마는 [`texture`](https://github.com/samarsault/texture)를 기반으로 커스터마이징했습니다.

---

## Tech Stack

- **Static Site Generator**: [Jekyll](https://jekyllrb.com/)
- **Theme**: [texture](https://github.com/samarsault/texture) (커스터마이징 버전)
- **Hosting**: GitHub Pages
- **Language**: Markdown, HTML, SCSS

---

## Getting Started (로컬 실행)

1. 의존성 설치

```bash
bundle install
```

2. 로컬 서버 실행

```bash
bundle exec jekyll serve
```

3. 브라우저에서 접속

```
http://localhost:4000
```


## Writing Posts (글 작성 가이드)

새 글은 _posts 디렉터리에 Markdown 파일로 추가합니다.

파일명 규칙:

```
_posts/YYYY-MM-DD-slug.md
예) _posts/2026-03-14-introducing-psycho-tech-blog.md
```

```md
---
layout: post
title: "Psycho Tech Blog 소개"
date: 2026-03-14
author: ahn
categories: [intro, culture]
---

본문 내용은 여기서부터 작성합니다.

```

### Author 관리

- author 필드는 글 작성자 ID를 의미합니다.
- (선택) _data/authors.yml을 사용해 작성자 정보를 관리할 수 있습니다.

## Configuration

주요 설정은 _config.yml에서 관리합니다.

- 사이트 메타 정보
    - title: 블로그 이름
    - author: 대표 조직명 (예: Psycho Engineering)
    - email: 연락용 이메일
    - description: 블로그 한 줄 소개
- 테마 설정 (texture 블록)
    - style: 색상 테마 (black, blue, green 등)
    - showNav: 상단 네비게이션 표시 여부
    - social_links: 푸터에 노출할 소셜 링크 (GitHub, RSS 등)

자세한 테마 옵션은 [HELP.md](./HELP.md) 또는 help 문서를 참고하세요.


## Deployment


이 레포는 GitHub Pages를 통해 배포됩니다.

- 브랜치: main
- (예시) Pages 설정:
    - Settings → Pages → Deploy from a branch
    - Branch: main / Folder: / (root)

실제 배포 URL은 GitHub Pages 설정을 참고하세요.

## Project Structure

간단한 디렉터리 구조는 다음과 같습니다.

```
.
├── _config.yml      # Jekyll & theme 설정
├── _posts/          # 블로그 글
├── _layouts/        # 레이아웃 템플릿
├── _includes/       # 재사용 가능한 HTML 조각들
├── _data/           # authors 등 YAML 기반 설정/메타데이터
├── assets/          # CSS, 이미지 등 정적 리소스
└── _sass/           # SCSS partials
```

## Contributing

팀원 누구나 PR을 통해 글 추가 및 개선을 제안할 수 있습니다.

- 새로운 글 작성 시:
    - `_posts`에 Markdown 파일 추가
    - 로컬에서 bundle exec jekyll serve로 확인
    - PR 생성 시 간단한 설명과 스크린샷(선택)을 함께 남겨주세요.
- 코드/스타일 수정 시:
    - 가능하면 작은 단위로 PR을 나누어 주세요.
    - 커밋 메시지는 Conventional Commits 규칙을 가급적 따릅니다.  
        - 예: feat: add favicon and refine Psycho tech blog base configuration

## License & Credits


- Theme: [texture](https://github.com/samarsault/texture) (MIT License)
- 이 레포의 커스텀 코드와 글 내용은 Psycho 팀에 귀속됩니다.


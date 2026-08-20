# 계리사 데이터 포트폴리오 - 사용 설명서

돈 한 푼 안 들이고 운영하는 개인 포트폴리오 사이트입니다.
GitHub Pages(무료 호스팅 + 무료 도메인)에 올려서 씁니다.

---

## 1. GitHub 계정 만들기
https://github.com 에서 무료 가입. (되도록 실명 또는 취업용으로 쓸 아이디로)

## 2. 저장소(repository) 만들고 파일 올리기
1. GitHub 우측 상단 `+` → `New repository`
2. 저장소 이름을 `아이디.github.io` 형식으로 만들면 → 무료 도메인이 `https://아이디.github.io` 가 됩니다.
3. Public으로 설정 → Create
4. 이 폴더 안의 모든 파일을 그 저장소에 업로드 (`Add file → Upload files`)
   * **주의**: 압축 파일(zip)을 그대로 올리지 말고, 압축을 푼 뒤 안의 파일들을 올리세요.

## 3. GitHub Pages 켜기
1. 저장소 → `Settings` → `Pages`
2. `Source`를 `Deploy from a branch`, Branch는 `main` / `(root)` → Save
3. 몇 분 후 `https://아이디.github.io` 접속하면 사이트가 뜹니다.

## 4. 내 정보로 바꾸기
- `_config.yml`: `title`, `description`, `url`, `author`
- `about.md`: 경력, 자격증, 핵심 역량 요약
- `skills.md`: Python/Excel/Prophet/AI 각 항목의 실제 경험
- `contact.md`: 이메일, LinkedIn, GitHub 링크

## 5. 이력서 PDF 첨부하기 (선택, 추천)
1. 이력서를 PDF로 저장 → 파일명을 `resume.pdf`로 변경
2. 저장소 최상위(root)에 업로드
3. `about.md`의 `[다운로드](/resume.pdf)` 링크가 자동으로 연결됩니다.

## 6. 새 프로젝트 글 쓰는 법
`_posts` 폴더에 `2026-08-21-프로젝트이름.md` 형식으로 파일을 만들고 아래처럼 씁니다.

```
---
title: "글 제목"
tags: [Python, Prophet]
description: "검색 결과에 노출될 한두 문장 요약"
github: https://github.com/아이디/저장소     # 없으면 삭제
demo: https://your-demo-link.com             # 없으면 삭제
---

문제 정의 → 접근 방법(코드 포함) → 결과 순서로 작성 추천.
```

예시 글(`_posts/2026-08-20-example-project-template.md`)에 작성 가이드가 자세히 있습니다.

## 7. 검색 노출(SEO) 마무리
1. https://search.google.com/search-console 접속 → 사이트 등록
2. `Sitemaps`에 `sitemap.xml` 제출 (자동 생성되어 있음: `https://아이디.github.io/sitemap.xml`)
3. 본인 이름 + "계리사" + "포트폴리오" 등으로 검색했을 때 노출되길 원한다면,
   `about.md`와 `_config.yml`의 description에 이 키워드들을 자연스럽게 포함시키세요.

## 8. 자소서/이력서에 첨부할 때 체크리스트
- [ ] `about.md`에 실제 경력·자격증 정보를 채웠는가
- [ ] 최소 3~5개 이상의 프로젝트 글이 올라와 있는가 (개수보다 깊이가 중요)
- [ ] 각 프로젝트가 "문제 → 접근 → 결과" 구조로 정량적 성과를 담고 있는가
- [ ] 코드가 있다면 GitHub 링크가 걸려 있는가 (심사자가 코드를 직접 볼 수 있어야 신뢰도가 올라감)
- [ ] `resume.pdf`가 연결되어 있는가
- [ ] 오탈자, 깨진 링크 없는지 최종 확인

## 참고: 커스텀 도메인
채용 포트폴리오는 `아이디.github.io`만으로도 충분하지만,
`이름.dev`, `이름.me` 같은 짧은 커스텀 도메인(연 1만원대~)을 쓰면 명함이나
자소서에 적었을 때 조금 더 전문적으로 보이는 효과는 있습니다. 필수는 아닙니다.
저장소 `Settings → Pages → Custom domain`에서 연결할 수 있습니다.

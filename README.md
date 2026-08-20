# 리뷰 블로그 - 사용 설명서

돈 한 푼 안 들이고 운영할 수 있는 개인 리뷰 블로그입니다.
GitHub Pages(무료 호스팅 + 무료 도메인)에 올려서 씁니다.

---

## 1. GitHub 계정 만들기
https://github.com 에서 무료 가입.

## 2. 저장소(repository) 만들고 파일 올리기
1. GitHub 우측 상단 `+` → `New repository` 클릭
2. 저장소 이름을 `아이디.github.io` 형식으로 만들면 → 무료 도메인이 `https://아이디.github.io` 가 됩니다.
   (예: 아이디가 hong123이면 저장소 이름은 `hong123.github.io`)
   * 이 이름이 아닌 다른 이름으로 만들면 주소가 `https://아이디.github.io/저장소이름` 이 됩니다. 이 경우 `_config.yml`의 `baseurl` 값에 `/저장소이름`을 적어주세요.
3. Public으로 설정 → Create
4. 이 폴더(review-blog) 안의 모든 파일을 그 저장소에 업로드
   (웹 브라우저에서 `Add file → Upload files`로 통째로 드래그해서 올리면 됩니다)

## 3. GitHub Pages 켜기
1. 저장소 → `Settings` → 왼쪽 메뉴 `Pages`
2. `Source`를 `Deploy from a branch`, Branch는 `main` / `(root)` 선택 → Save
3. 몇 분 후 `https://아이디.github.io` 로 접속하면 사이트가 뜹니다.
   (Jekyll이라 별도 빌드 명령 없이 GitHub이 자동으로 빌드해줍니다)

## 4. 내 정보로 바꾸기
- `_config.yml` 파일에서 `title`, `description`, `url`, `author` 수정
- `about.md`, `contact.md`, `privacy.md` 안의 예시 문구를 실제 내용으로 교체
  (특히 `privacy.md`, `about.md`, `contact.md`는 애드센스 심사 때 꼭 확인하는 페이지들입니다)

## 5. 새 리뷰 글 쓰는 법
`_posts` 폴더 안에 `2026-08-21-제품이름.md` 형식으로 파일을 새로 만들고
아래 형식으로 시작하면 됩니다.

```
---
title: "글 제목"
category: 전자제품
rating: 4
description: "검색 결과에 노출될 한두 문장 요약"
---

본문은 여기부터 마크다운으로 자유롭게 씁니다.
```

- `rating`은 1~5 사이 숫자로, 별점 대신 원형 도장 형태로 표시됩니다. 없어도 됩니다.
- `_posts/2026-08-20-how-to-write-here.md` 파일이 예시이자 작성 가이드이니, 참고 후 지워도 됩니다.

파일을 저장소에 업로드(커밋)하면 자동으로 사이트에 반영됩니다. 별도 프로그램 설치 없이
GitHub 웹사이트에서 `Add file → Create new file`로 바로 글을 쓸 수도 있습니다.

## 6. 검색 노출(SEO) 마무리 - 꼭 하세요
1. https://search.google.com/search-console 접속 → 내 사이트 주소 등록
2. 소유권 확인 후, 왼쪽 메뉴 `Sitemaps`에 `sitemap.xml` 을 제출
   (사이트가 만들어지면 `https://아이디.github.io/sitemap.xml` 이 자동 생성되어 있습니다)
3. 이렇게 하면 구글이 내 글들을 훨씬 빨리 찾아서 검색결과에 노출시킵니다.

## 7. 애드센스 신청 전 체크리스트
- [ ] `about`, `contact`, `privacy` 페이지 내용을 실제 정보로 채웠는가
- [ ] 글이 최소 15~20편 이상 쌓였는가
- [ ] 각 글이 최소 1,000~1,500자 이상이고, 직접 경험한 구체적인 내용을 담고 있는가
- [ ] 다른 사이트 내용을 복사/짜깁기한 글이 없는가
- [ ] 커스텀 도메인(예: myblog.com)을 쓸 경우 무료 서브도메인보다 승인이 조금 더 잘 되는 경향이 있음 (필수는 아님)
- [ ] Google Search Console에 사이트/sitemap을 등록했는가

## 참고: 나중에 커스텀 도메인을 쓰고 싶다면
가비아·후이즈 등에서 도메인을 구매(연 1만원대~)한 뒤, 저장소 `Settings → Pages → Custom domain`에
입력하면 됩니다. 지금은 무료로 시작하는 것이 목표이므로 필수는 아닙니다.

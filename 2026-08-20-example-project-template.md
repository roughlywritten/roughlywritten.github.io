---
title: "예시: 프로젝트 글은 이렇게 씁니다 (작성 가이드)"
tags: [안내]
description: "새 프로젝트 글을 추가하는 방법과, 채용 담당자에게 설득력 있는 구조를 안내합니다."
github: https://github.com/your-id/example-repo
---

이 글은 실제 프로젝트가 아니라 작성 가이드입니다. 첫 프로젝트를 쓸 준비가 되면
이 파일은 지우거나 `_posts` 폴더 밖으로 옮기세요.

## 새 프로젝트 글을 추가하는 방법

1. `_posts` 폴더에 `2026-08-21-프로젝트이름.md` 형식으로 새 파일을 만듭니다.
2. 맨 위에 아래처럼 정보를 적습니다.

   ```
   ---
   title: "글 제목"
   tags: [Python, Prophet]
   description: "검색 결과와 목록에 보일 한두 문장 요약"
   github: https://github.com/아이디/저장소     # 없으면 이 줄 삭제
   demo: https://your-demo-link.com             # 없으면 이 줄 삭제
   ---
   ```

3. 본문은 아래 구조를 권장합니다.

## 문제 정의
어떤 업무 상의 불편함, 비효율, 과제가 있었는지 구체적으로 씁니다.
(예: "매월 준비금 산출 후 검증에 반나절이 걸렸다")

## 접근 방법
어떤 기술로 어떻게 해결했는지 씁니다. 코드 일부를 보여주면 신뢰도가 올라갑니다.

```python
import pandas as pd

def check_reserve(df: pd.DataFrame) -> pd.DataFrame:
    """준비금 산출 결과의 이상치를 자동으로 탐지한다."""
    threshold = df["reserve"].mean() + 3 * df["reserve"].std()
    return df[df["reserve"] > threshold]
```

## 결과
정량적으로 표현하세요. "빨라졌다"보다 "반나절 걸리던 검증을 10분으로 단축했다"처럼
구체적인 숫자가 훨씬 설득력 있습니다.

## 배운 점 (선택)
기술적으로든 업무적으로든 얻은 인사이트를 짧게 남기면 좋습니다.

---

이 구조(문제-접근-결과)를 지키면 채용 담당자가 실무 역량을 빠르게 파악할 수 있습니다.

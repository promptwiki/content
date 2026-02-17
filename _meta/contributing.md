---
title: "처음으로 PR을 올리는 방법"
slug: "how-to-contribute"
purpose: guide
level: beginner
persona:
  - general
  - power-user
  - developer
status: stable
lang: ko
translationKey: "how-to-contribute"
summary: "GitHub을 잘 몰라도 PromptWiki에 문서를 기여할 수 있다. 처음부터 끝까지 단계별로 안내한다."
tags:
  - contributing
  - github
  - beginner-essential
requiredKnowledge: []
createdAt: 2026-02-18
lastReviewed: 2026-02-18
contributors:
  - Raunplaymore
---

## 기여하기 전에

PromptWiki의 모든 문서는 GitHub를 통해 기여한다.
GitHub 계정이 없다면 먼저 [github.com](https://github.com)에서 무료 계정을 만든다.

---

## 기여 방식 선택

### 방법 A — 작은 수정 (오탈자, 링크 등)
GitHub 웹에서 직접 편집할 수 있다. 코드를 몰라도 된다.

### 방법 B — 새 문서 작성 또는 큰 수정
Fork → 작성 → PR 순서로 진행한다.

---

## 방법 A: 웹에서 바로 수정하기

1. 수정하고 싶은 문서를 [github.com/promptwiki/content](https://github.com/promptwiki/content)에서 찾는다.
2. 파일을 클릭하면 오른쪽 상단에 연필 아이콘(✏️)이 있다.
3. 클릭하면 자동으로 Fork가 만들어지고 편집 모드가 열린다.
4. 수정 후 하단에서 **"Propose changes"** 클릭.
5. PR 설명을 작성하고 **"Create pull request"** 클릭.
6. 완료! 리뷰 후 머지된다.

---

## 방법 B: 새 문서 작성하기

### 1단계: Fork 만들기

[github.com/promptwiki/content](https://github.com/promptwiki/content)에서 우측 상단 **Fork** 버튼 클릭.
내 계정에 복사본이 만들어진다.

### 2단계: 파일 만들기

Fork된 내 레포에서 적절한 경로로 이동한다.

```
경로 규칙: {lang}/{purpose}/{level}/{slug}.md

예시:
ko/guide/beginner/my-new-guide.md
ko/template/general/meeting-summary.md
```

**Add file → Create new file** 클릭 후 파일명을 경로와 함께 입력한다.

### 3단계: Frontmatter 작성하기

파일 내용의 맨 위에 아래 템플릿을 붙여넣고 내용을 채운다.

```yaml
---
title: "문서 제목"
slug: "파일명과-동일하게"
purpose: guide
level: beginner
persona:
  - general
status: draft
lang: ko
translationKey: "파일명과-동일하게"
summary: "한 줄 설명"
tags:
  - 태그1
requiredKnowledge: []
createdAt: 2026-02-18
lastReviewed: 2026-02-18
contributors:
  - 내-GitHub-아이디
---
```

**필수 값 목록**

| 필드 | 허용 값 |
|---|---|
| `purpose` | guide, rule, template, example, reference |
| `level` | beginner, intermediate, advanced |
| `persona` | general, power-user, developer, organization |
| `status` | draft (새 문서는 항상 draft로 시작) |
| `lang` | ko, en |

### 4단계: 본문 작성하기

Frontmatter 아래에 Markdown으로 내용을 작성한다.

목적(purpose)별 권장 본문 구조는 [content-structure.md](https://github.com/promptwiki/.github) 를 참고한다.

### 5단계: PR 제출하기

1. **Commit changes** 클릭 → 변경사항 저장.
2. 내 Fork 페이지로 이동하면 **"Contribute → Open pull request"** 버튼이 보인다.
3. 클릭 후 PR 템플릿의 체크리스트를 확인하고 설명을 작성한다.
4. **Create pull request** 클릭.

---

## PR 이후 과정

1. 자동으로 **Frontmatter 유효성 검사**가 실행된다. 필수 항목이 누락되면 실패한다.
2. Reviewer가 내용을 검토하고 피드백을 남긴다.
3. 수정이 필요하면 같은 파일을 편집하면 자동으로 PR에 반영된다.
4. 승인되면 Maintainer가 머지한다.
5. 2~3분 후 웹사이트에 반영된다.

---

## 자주 묻는 질문

**Q: 영어를 못해도 기여할 수 있나요?**
한국어 문서라면 한국어로 작성하면 된다. 영어 번역은 별도로 기여받는다.

**Q: 내가 쓴 내용이 수정되면 어떻게 하나요?**
리뷰 과정에서 내용이 수정될 수 있다. 이것은 문서의 품질을 위한 과정이며, 기여 내역은 Git 히스토리에 영구 기록된다.

**Q: 거절당하면요?**
거절 사유와 함께 개선 방향을 안내받는다. 수정 후 재제출할 수 있다.

---

## 도움이 필요하다면

[GitHub Issues](https://github.com/promptwiki/content/issues)에서 `doc-request` 또는 `improvement` 템플릿으로 먼저 제안을 올려도 된다. 직접 작성하지 않아도 아이디어 제안만으로도 기여다.

# jinokim94 개인 홈페이지

GitHub Pages용 정적 페이지입니다. 빌드나 외부 라이브러리가 필요하지 않습니다.

- 홈페이지: https://jinokim94.github.io/
- 게시 원본: `main` 브랜치의 루트
- 기존 홈페이지 저장소는 별도로 유지합니다.

## 기본 파일

| 파일 | 용도 |
| --- | --- |
| `index.html` | 홈페이지 |
| `style.css` | 홈페이지와 독립 문서의 공통 스타일 |
| `projects/` | 프로젝트별 공개 문서 |
| `templates/privacy.html.template` | 개인정보처리방침의 빈 HTML 틀 |
| `templates/document.html.template` | 소개·매뉴얼의 빈 HTML 틀 |

## 개인정보처리방침만 게시하기

예를 들어 `my-app`의 방침만 공개하려면:

1. `projects/my-app/` 폴더를 만듭니다.
2. `templates/privacy.html.template`을 그 폴더의 `privacy.html`로 복사합니다.
3. 프로젝트 이름, 시행일, 수정일과 본문을 직접 작성하고 작성용 안내를 삭제합니다.
4. 검색 노출이 필요하면 `<meta name="robots" content="noindex">`를 삭제합니다. `noindex`는 접근 제한 기능이 아닙니다.
5. `main`에 커밋하고 push하면 GitHub Pages에 자동 배포됩니다.

공개 주소: **https://jinokim94.github.io/projects/my-app/privacy.html**

소개 페이지나 매뉴얼, 공개 소스 저장소가 없어도 이 주소로 방침만 독립 게시할 수 있습니다. 홈페이지에 링크를 추가하는 것도 선택입니다. 홈페이지 링크가 없어도 URL로 직접 접근할 수 있습니다.

## 소개·매뉴얼 추가하기 (선택)

`templates/document.html.template`을 같은 폴더의 `index.html` 또는 `guide.html`로 복사해 내용을 작성하세요. 문서끼리 연결할 때는 `href="privacy.html"`, `href="guide.html"`처럼 상대 경로를 사용하면 됩니다.

## 홈페이지에 문서 링크 추가하기 (선택)

`index.html`의 프로젝트 영역에서 아래처럼 실제 게시된 문서로 연결합니다. 첫 항목을 추가할 때는 기존 준비 중 안내를 지우면 됩니다.

```html
<article>
  <h3>프로젝트 이름</h3>
  <a href="projects/my-app/privacy.html">개인정보처리방침</a>
</article>
```

## 작성 시 참고

문서 틀에는 실제 개인정보 처리에 대한 주장을 넣지 않았습니다. 프로젝트마다 직접 확정한 내용을 작성하세요. 필요 없는 소개·매뉴얼은 만들지 않아도 됩니다. 프로젝트 폴더 이름은 공개 URL의 일부이므로 게시 후에는 유지하는 편이 좋습니다.

백업 파일과 비공개 소스는 이 저장소에 포함하지 않습니다.

## 게시된 독립 문서

- TIPA HR Contact Finder: https://jinokim94.github.io/userapi_extension/PrivacyPolicy/
- 원본: `jinokim94/userapi_extension`, `browser_extensions/userapi_extension/PRIVACY_POLICY.md`
- 원본 blob SHA: `8cd75d0f49ded86c699db5cb0dd5b5414f86aae0`
- 최신 원본 내용을 그대로 게시한 문서입니다. 원본 변경 시 게시본도 별도로 검토·갱신해야 합니다.
- 메인페이지에 링크를 추가하지 않고 직접 URL로 접근하도록 게시했습니다.

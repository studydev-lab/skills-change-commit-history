<header>

# 커밋 히스토리 변경

Git에서 실수로 커밋된 내용을 제거하는 것은 까다로울 수 있습니다. 이 GitHub Skills 실습에서는 BFG Repo-Cleaner를 사용하여 Git 저장소의 히스토리를 변경합니다. 이 실습에서 배운 내용을 적용하여 자신의 저장소에서 민감한 자료를 완전히 제거할 수 있습니다.

</header>

## 환영합니다

신뢰할 수 있는 커밋 히스토리는 Git 버전 관리의 기본입니다. 그 결과, 커밋 히스토리를 변경하는 것은 설계상 어렵습니다. 때로는 실수로 체크인된 자격 증명이나 기타 민감한 데이터를 제거하기 위해 히스토리를 변경해야 합니다. 이 실습에서는 저장소의 전체 히스토리에서 콘텐츠를 제거하고 향후 실수로 커밋하는 것을 방지하기 위한 모범 사례를 적용하는 방법을 배웁니다.

- **대상**: Git 중급 사용자, 조직
- **배울 내용**: Git의 전체 히스토리에서 파일을 제거하는 방법
- **만들 것**: Git 저장소의 히스토리를 조작합니다
- **사전 요구사항**: 이 저장소를 로컬에 클론하고 커맨드라인을 사용하여 따라하는 것을 권장합니다. BFG Repo-Cleaner도 설치해야 하지만, 단계에서 안내됩니다.
- **소요 시간**: 이 실습은 1시간 이내에 완료할 수 있습니다.

이 실습에서 다음을 수행합니다:

1. 저장소의 루트 디렉토리에서 콘텐츠 제거
2. BFG Repo-Cleaner를 사용하여 저장소 히스토리에서 콘텐츠 제거
3. `.gitignore`에 패턴을 추가하여 향후 실수로 커밋하는 것 방지

### 이 실습을 시작하는 방법

실습을 내 계정으로 복사한 뒤, Octocat(Mona)이 첫 번째 레슨을 준비할 때까지 **약 20초** 기다린 후 **페이지를 새로고침**하세요.

[![](https://img.shields.io/badge/실습%20복사-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/new?template_owner=skills-kr&template_name=change-commit-history&owner=%40me&name=skills-change-commit-history&description=실습:+커밋+히스토리+변경&visibility=public)

<details>
<summary>문제가 있나요? 🤷</summary><br/>

실습을 복사할 때 다음 설정을 권장합니다:

- 소유자(owner)는 개인 계정 또는 조직(organization)을 선택하세요.
- 비공개 저장소는 Actions 사용 시간이 소모되므로 공개 저장소를 만드는 것을 권장합니다.

20초 후에도 실습이 준비되지 않으면:

1. 새 저장소가 생성된 후 약 20초 기다린 다음 페이지를 새로고침하세요.
2. 저장소에 생성된 이슈의 단계별 지침을 따르세요.
3. 페이지가 자동으로 새로고침되지 않으면 [Actions](../../actions) 탭을 확인하세요.
   - 작업이 실행 중인지 확인하세요. 때로는 조금 더 오래 걸릴 수 있습니다.
   - 실패한 작업이 표시되면 이슈를 제출해 주세요. 버그를 발견하셨네요! 🐛

</details>

---

> **참고**: 이 실습은 [skills/change-commit-history](https://github.com/skills/change-commit-history)를 기반으로 한글화하고, [🏆 GitHub Skills Workshop Dashboard](https://github-skills.studydev.com)와 연계되어 있습니다.

&copy; 2024 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

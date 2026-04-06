## 2단계: BFG Repo-Cleaner를 사용하여 Git 히스토리에서 파일 제거하기

_저장소의 루트 디렉토리에서 `.env`를 제거했습니다! :tada:_

파일을 삭제했으므로 GitHub.com에서 저장소를 탐색하거나 최신 커밋만 보는 사람은 파일을 볼 수 없습니다. 하지만 Git의 특성상 파일은 여전히 히스토리에 남아있습니다. 이 단계에서는 저장소 히스토리에서 파일을 제거하는 작업을 하겠습니다.

**_head 커밋_이란?** Git에서 HEAD는 브랜치나 커밋을 가리킵니다. [head 커밋](https://docs.github.com/en/get-started/quickstart/github-glossary#head)이라고 하면 보통 저장소 히스토리의 가장 최신 커밋을 의미합니다.

Git 히스토리를 제거하는 여러 도구가 있으며, 이 단계에서는 BFG Repo-Cleaner를 사용합니다. [GitHub Docs의 BFG 사용하기](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#using-the-bfg)에서 추가 문서를 찾을 수 있습니다.

**_BFG Repo-Cleaner_란?** BFG Repo-Cleaner는 저장소 히스토리를 검색하고 변경하는 데 도움이 되는 소프트웨어입니다. Git은 기본적으로 [`git filter-repo`](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#using-git-filter-repo)를 사용하여 이 작업을 할 수 있지만, 더 복잡할 수 있습니다.

### :keyboard: 활동: BFG Repo-Cleaner를 사용하여 `.env` 파일 제거하기

1. 로컬 저장소의 복사본을 업데이트하여 최신 버전의 실습 파일을 가져오세요.
   ```shell
   git pull
   ```
2. BFG Repo-Cleaner를 컴퓨터에 설치하세요. [웹사이트의 지침](https://rtyley.github.io/bfg-repo-cleaner/)을 따르거나 운영체제의 패키지 관리자를 사용할 수 있습니다.
3. `.env` 파일이 루트 디렉토리에서 제거되었는지 확인하세요. 명령어가 비어있어야 합니다.
   ```shell
   find . -name ".env"
   ```
4. 저장소의 히스토리에서 .env를 검색하세요. 명령어가 최소 2개의 커밋을 반환해야 합니다: 템플릿 저장소를 복사할 때 `.env`가 추가된 것과 `.env`가 제거된 것.
   ```shell
   git log --stat --all -- .env
   ```
5. BFG Repo-Cleaner를 사용하여 저장소에 존재하는 `.env`에 대한 모든 참조를 삭제하세요.
   ```shell
   bfg --delete-files .env
   ```
6. 도구가 실행되며 후속 명령에 대한 제안을 합니다. 로컬 저장소를 정리하기 위해 해당 명령을 실행하세요.
7. 저장소의 히스토리에서 `.env` 검색을 반복하세요. 이번에는 명령어가 비어있어야 합니다.
   ```shell
   git log --stat --all -- .env
   ```
8. 변경사항을 GitHub에 푸시하세요. Git 히스토리를 변경하므로 이 단계에서는 `--force` 인자를 사용합니다.
   ```shell
   git push --force
   ```
9. 약 20초 후 이 페이지(지침을 따르고 있는 페이지)를 새로고침하세요. [GitHub Actions](https://docs.github.com/en/actions)가 자동으로 다음 단계로 업데이트합니다.

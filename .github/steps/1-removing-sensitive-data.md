## 1단계: 민감한 데이터 제거하기

_"커밋 히스토리 변경"에 오신 것을 환영합니다! :wave:_

먼저 `.env` 파일을 다루는 것부터 시작하겠습니다. 이 파일에는 보통 민감한 내용이 포함되어 있습니다. 이 실습에서는 해당 파일을 제거하고 Git 히스토리의 모든 흔적을 지우는 작업을 합니다. 첫 번째 단계는 저장소에서 파일을 제거하는 것입니다. 히스토리는 나중에 변경하겠습니다.

커맨드라인을 사용한다고 가정하지만, 원하는 도구를 사용하여 실습을 완료할 수 있습니다.

**_민감한 콘텐츠_란?** 민감한 콘텐츠는 저장소 히스토리에 체크인되어 사용자나 조직을 위험에 빠뜨릴 수 있는 모든 것입니다. 이 콘텐츠는 보통 자격 증명(예: 비밀번호, 액세스 키) 형태로 나타납니다. 실수로 노출된 민감한 콘텐츠에 대한 모범 사례는 해당 콘텐츠를 무효화(예: 개인 액세스 토큰 취소)하고, 모든 저장소 사본에서 완전히 제거하며, 향후 노출을 방지하는 조치를 취하는 것입니다.

파일 제거에 대한 추가 도움이 필요하면 [GitHub Docs의 파일 삭제](https://docs.github.com/en/repositories/working-with-files/managing-files/deleting-files-in-a-repository#deleting-a-file)를 참조하세요.

### :keyboard: 활동: 프로젝트 루트 디렉토리에서 `.env` 제거하기
1. 터미널을 열고 이 저장소를 클론한 뒤 저장소 디렉토리로 이동하세요.
   ![Git clone example](https://raw.githubusercontent.com/skills-kr/change-commit-history/main/.github/images/git_clone.png)
   ```shell
   git clone <your-repository-url>
   cd <your-repository-name>
   ```
   > **팁:** 저장소 페이지의 **Code** 버튼에서 `git clone` 명령어를 복사할 수 있습니다.

2. 루트 디렉토리에서 `.env`를 삭제하세요.
   ```shell
   git rm .env
   ```
3. `.env` 제거를 커밋하세요.
   ```shell
   git commit -m "remove .env file"
   ```
4. GitHub에 푸시하세요:
   ```shell
   git push
   ```
5. 약 20초 후 이 페이지(지침을 따르고 있는 페이지)를 새로고침하세요. [GitHub Actions](https://docs.github.com/en/actions)가 자동으로 다음 단계로 업데이트합니다.

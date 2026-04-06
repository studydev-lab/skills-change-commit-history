## 3단계: `.env`를 사용한 향후 커밋 방지하기

_저장소의 전체 히스토리에서 파일을 제거하는 훌륭한 작업을 해냈습니다! :sparkles:_

지금까지 수행한 단계는 저장소의 모든 _새로운_ 클론에 민감한 데이터가 포함되지 않도록 합니다. 하지만 이미 저장소 사본을 가지고 있는 협업자는 어떨까요? 저장소 사본을 가진 모든 사람에게 삭제하고 저장소를 새로 클론하도록 요청해야 합니다. 실제 상황에서는 GitHub.com에 캐시된 민감한 데이터가 없는지 확인하기 위한 [추가 단계](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository#fully-removing-the-data-from-github)도 수행해야 합니다.

민감한 콘텐츠 노출 위험을 완화했으므로, 이제 사전 예방적으로 추가를 방지하겠습니다.

`.gitignore`에 `.env`를 추가하여 향후 민감한 콘텐츠 추가를 무시하도록 Git을 구성하겠습니다. 누군가 로컬 저장소 사본에 해당 파일을 추가하더라도 기여자의 컴퓨터에만 남아있고 GitHub에 푸시되지 않습니다.

**`.gitignore`란?** 이 특수 파일을 사용하면 Git에게 무시할 파일 이름 패턴을 알려줄 수 있습니다. [GitHub Docs의 파일 무시하기](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files)에서 자세히 알아볼 수 있습니다.

### :keyboard: 활동: `.gitignore`에 `.env` 추가하기

1. 로컬 저장소의 복사본을 업데이트하여 최신 버전의 실습 파일을 가져오세요.
   ```shell
   git pull
   ```
2. 저장소에 추가된 `.gitignore` 파일을 찾으세요.
3. 파일에 `.env`를 추가하세요.
4. 스테이징하고 파일을 커밋하세요:
   ```shell
   git add .gitignore
   git commit -m "ignore .env files"
   ```
5. GitHub.com에 푸시하세요.
   ```shell
   git push
   ```
6. 약 20초 후 이 페이지(지침을 따르고 있는 페이지)를 새로고침하세요. [GitHub Actions](https://docs.github.com/en/actions)가 자동으로 다음 단계로 업데이트합니다.

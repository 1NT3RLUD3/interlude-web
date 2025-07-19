앞으로는 다음과 같은 워크플로우를 따르면 됩니다:

main 브랜치로 이동 및 최신 상태 동기화:
새로운 작업을 시작하기 전에 항상 로컬 main 브랜치를 GitHub의 최신 상태로 업데이트합니다.

Bash

git checkout main
git pull
이 과정은 다른 팀원들이 main 브랜치에 병합한 내용이 있다면 당신의 로컬 main에도 반영되도록 합니다.

새로운 기능 브랜치 생성 및 이동:
어떤 새로운 기능 개발, 버그 수정, 또는 개선 작업이든 간에, 항상 main 브랜치에서 새로운 브랜치를 생성하고 그 브랜치로 이동하여 작업합니다.

Bash

git checkout -b feature/새로운-기능-이름
# 예시: git checkout -b feature/sticky-header
# 예시: git checkout -b bugfix/login-page-error
브랜치 이름은 feature/, bugfix/, chore/ 등으로 시작하여 작업의 종류를 명확히 하는 것이 좋습니다.

새로운 브랜치에서 작업 및 커밋:
새로운 브랜치에서 코드를 수정하고, 의미 있는 단위로 변경사항을 커밋합니다.

Bash

# 파일 수정...
git add .
git commit -m "feat: [간결한 설명]" # 또는 "fix: [간결한 설명]"
자신의 브랜치 푸시:
작업이 완료되면 (또는 중간에 백업이나 공유를 위해) 자신의 기능 브랜치를 GitHub 원격 저장소에 푸시합니다.

Bash

git push -u origin feature/새로운-기능-이름
(-u 옵션은 해당 브랜치를 처음 푸시할 때만 사용합니다. 다음부터는 git push만으로 됩니다.)

Pull Request (PR) 생성 및 병합:

GitHub 웹사이트로 이동하여 방금 푸시한 기능 브랜치에서 main 브랜치로 Pull Request를 생성합니다.

팀원들과 코드 리뷰를 진행하고, 승인되면 main 브랜치로 병합(Merge)합니다.

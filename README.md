# CI-CD
간단한 CI/CD 파이프라인을 구축해보는 개인프로젝트


1. 소스 관리는 github로 한다.
2. github에 코드가 push되면 webhook으로 소스가 변경되었음을 감지한다.
3. Jenkins로 이미지를 build한다.
4. (추후)이 과정에서 생긴 issue는 slack bot을 통해 알린다.
5. build된 image를 dockerhub에 이미지를 push한다.
6. ansible을 통해 이미지를 cloud환경이나 local에 배포한다.

---

CI

1. git commit -> git hub repo에 merge
2. github webhook으로 jenkins build 실행
3. docker image build후 docker hub에 image push

CD

1. ansible로 image pull해서 docker instance group에 배포

---

**VCS(Version Control System)** - Git 기반의 repository

**Container image registry** -  Docker hub

**CI** - 우선 python programming 지원

**CD** - amazon의 ec2 환경으로 제공

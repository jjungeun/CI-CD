# CI-CD
간단한 CI/CD 파이프라인을 구축해보는 개인프로젝트


1. 소스 관리는 github로 한다.
2. github에 코드가 push되면 webhook으로 소스가 변경되었음을 감지한다.
3. Jenkins로 이미지를 build하고 ansible을 통해 이미지를 테스트한다.
4. (추후)이 과정에서 생긴 issue는 slack bot을 통해 알린다.
5. 테스트가 통과되면 dockerhub에 이미지를 push한다.
6. 새로운 이미지를 local이나 cloud환경의 kubernetes에 배포한다.

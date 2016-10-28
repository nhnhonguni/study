# Git & GitHub 사용기
## 사용 프로그램
* Eclipse(STS)
* SourceTree - [www.sourcetreeapp.com](www.sourcetreeapp.com)
  * 자체 Git Flow 지원

## Git Flow?
* WorkFlow 형태를 정립하기위한 브랜칭 전략
* Develop과 Master 브랜치를 중심으로 Feature, Release, Hotfix 브랜치 존재
  * master
    * 배포 완료 상태의 소스코드가 존재하는 브랜치      
  * develop
    * 다음 릴리즈로 배포가 가능한 상태의 소스코드가 존재하는 브랜치  
    ![main](http://nvie.com/img/main-branches@2x.png)    
  * feature
    * 개별 기능을 개발하는 브랜치
    * 개발이 완료되면 develop 브랜치에 merge하고 feature브랜치는 삭제  
    ![feature](http://nvie.com/img/fb@2x.png) 
    * feature 이력관리를 위해 FastFoward를 none으로 설정(git merge --no-ff [branch])  
    ![noff](http://nvie.com/img/merge-without-ff@2x.png)
  * release
    * 배포 준비를 위한 브랜치(버그를 찾고 수정하는 목적으로 사용)
    * 수정되는 버그는 지속적으로 develop 브랜치에 merge
    * 검수 완료되면 master에 merge하고 release는 삭제
  * hotfix
    * 배포가 완료된 버전에 문제가 있는 경우 master 브랜치로부터 hotfix 브랜치를 따온다.
    * 수정이 완료되면 master브랜치와 develop브랜치로 동시에 merge하고 hotfitx브랜치는 삭제  
    ![hotfix](http://nvie.com/img/hotfix-branches@2x.png)


출처 - blog.naver.com/hthasdrubal/220622642022

# Git & Github  

* Git이란?   
    프로그램등의 소스 코드 관리를 위한 분산 버전 관리 시스템 (Distributed Version Control System)이다.
    * Git 다운로드  
        https://git-scm.com/downloads

* Git을 사용하는 이유
    1. 버전관리 : 파일 변화를 시간에 따라 기록했다가 후에 특정 시점의 버전을 꺼내올 수 있다.  
    2. 백업 : 여러 컴퓨터에 정보를 복제,저장 하며 안전하게 보호 할 수 있다.  
    3. 협업 : 장소에 상관없이 소스 코드를 여러 사람이 주고받을 수 있다.  

* Git 관련 주요 용어  
    * Repository  
     프로젝트가 거주할 수 있는 디렉토리나 저장 공간을 의미한다.  

    * Branches  
     가지 또는 분기점. 저장소에서 작업에 필요한 상태를 복사하여 생성한다.  

    * Working tree (Working directory)  
     실제 파일이 존재하는 작업공간을 의미한다.

    * Staging area (index)  
     작업공간에서 변경 또는 추가된 파일들이 등록되는 공간을 의미한다. 곧 commit 할 파일들의 정보를 저장한다.  

    * Commit  
     작업을 확정하고 저장소에 반영하는 작업이다.  

    * Push  
     commit을 원격 저장소에 올리는 작업이다.  

    * Pull  
    다른 사람이 개발한 코드(커밋)를 내 컴퓨터에 받아오는 작업이다. 

    * Merge  
    브랜치와 브랜치를 병합하는 작업이다.  

    * Pull request  
     Merge 전 다른 개발자들에게 리뷰 & 컨펌을 받는 '병합 요청 편지'를 보내는 작업이다.  

* Github이란?  
    Git repository를 업로드 하고 공유할 수 있는 웹사이트이다. 다른 개발자들이 올린 데이터를 함께 공유하고 보완할 수 있으며 동시에 같은 파일을 작업 할 수도 있다.

* Github 사용법  
 
     [Github 사이트](https://github.com)에 들어가서 회원가입을 한다.  

    * Repository 생성  
     1. 'New repository'버튼을 클릭한다.  
     2. 'Repository name'에 새로운 저장소 이름을 적고, 'Initialize this repository with a README' 박스에 체크한다.  
    ![1](https://user-images.githubusercontent.com/49367190/60703075-c2b46580-9f3b-11e9-8e63-1fef53871145.JPG)
     3. 'Create repository' 버튼을 클릭한다.  
     4. 새 저장소(Repository)가 생겼다.  
     ![2](https://user-images.githubusercontent.com/49367190/60703331-7fa6c200-9f3c-11e9-88ba-9e965a13d780.JPG)  

    * Branch 생성  
     1. 새로 만든 repository로 가서 'branch: master'라고 적힌 드롭다운 버튼을 클릭한다.  
     ![3](https://user-images.githubusercontent.com/49367190/60704779-5daf3e80-9f40-11e9-86f7-448fb9802250.JPG)  
     2. branch 이름을 적고 'Create branch'버튼 또는 엔터키를 누른다.  
      ![4](https://user-images.githubusercontent.com/49367190/60704873-9cdd8f80-9f40-11e9-8592-a06853f3c715.JPG)  
      새로운 branch가 생긴 것을 확인할 수 있다. 새 branch는 master branch의 파일들을 똑같이 복사해온다.

    * Commit change
     1. README.md파일을 클릭한다.
     2. 오른쪽 상단 연필 아이콘을 클릭해서 파일을 수정한다.
      ![5](https://user-images.githubusercontent.com/49367190/60705068-1f664f00-9f41-11e9-8e2e-23a5830ce0ac.JPG)  
      ![6](https://user-images.githubusercontent.com/49367190/60705210-79671480-9f41-11e9-8780-ad1661919ed4.JPG)    
     3. Commit message를 간략하게 적고 'Commit changes'버튼을 클릭한다.  
     ![7](https://user-images.githubusercontent.com/49367190/60705219-7ec45f00-9f41-11e9-9116-4b6401c97183.JPG)

    * Pull request 보내기  
     1. 'Pull request' 탭에 들어간다.  
     2. 'New pull request' 버튼을 클릭한다.  
      ![8](https://user-images.githubusercontent.com/49367190/60705683-b089f580-9f42-11e9-9642-3b088fe52e33.JPG)  
     3. 'Example Comparisons' 박스에서 작업한 branch를 선택해 변경사항을 master와 비교해본다.  
     ![9](https://user-images.githubusercontent.com/49367190/60705689-b41d7c80-9f42-11e9-9d44-1d242044cce7.JPG)  
     ![10](https://user-images.githubusercontent.com/49367190/60705705-bb448a80-9f42-11e9-8da6-46daf52d0842.JPG)  
     4. 확인이 끝났다면 'Create pull request' 버튼을 클릭한다.
     5. 제목과 간략한 설명을 적고 한번 더 'Create pull request' 버튼을 클릭한다.  
      ![11](https://user-images.githubusercontent.com/49367190/60705708-be3f7b00-9f42-11e9-8ca2-0740554594a7.JPG)

    * Pull request를 Merge 하기  
     1. 'Merge pull request' 버튼을 눌러 작업했던 branch와 원래 master branch를 병합해준다.  
     ![12](https://user-images.githubusercontent.com/49367190/60705710-bf70a800-9f42-11e9-8b7d-a5829eadb0a1.JPG)
     2. 'Confirm merge' 버튼을 누른다.  
     3. 'Delete branch' 버튼을 눌러 작업했던 branch는 삭제해준다.  
     ![13](https://user-images.githubusercontent.com/49367190/60705713-c13a6b80-9f42-11e9-8f36-f230b4514e61.JPG)





      











    


### [InteliJ][Git] Untracked Files Prevent Merge 오류
> 현상 : 프로젝트 소스 업데이트 받다가 취소되면서 아래 오류 발생    
> 내용 : "Untracked Files Prevent Merge Move or commit them before merge"   
> 해결 : 해당 프로젝트 > gitbash >  ``` $ git clean -d -f -f```   

### [InteliJ][Lombook] import 오류
> 현상 : lombook @어노테이션 컴파일 에러
> 해결 : InteliJ -> Plugins 메뉴 -> ⚙버튼→'Install Plugin from disk' -> 클릭하여 import (Local저장된 lombook Plugins)

 
### [IntelliJ][Settings] 소스 에러 표시 안나올 때   
> 현상 : 프로젝트 자동 빌드 안될 때   
> 해결 : 설정 -> 컴파일러 -> 프로젝트 자동 빌드... -> 항목 체크 -> 적용 -> 확인   

### [IntelliJ][Tomcat] Tomcat Console Log utf-8 깨지는 현상      
> 현상 : Tomcat Console Log 한글깨짐  
> 해결 : Tomcat 설정시 [Server] > [Vm Options] > -Duser.language=en -Duser.region=us or -Dfile.encoding=UTF-8 입력  

### [IntelliJ][Tomcat] 설정시 com.fasterxml.jackson.core.JsonParseException: Unexpected character ('<' (code 60)):      
> 현상 : 웹페이지 404   
> 해결 : Tomcat 설정시 [Deployment] > [+] 클릭 > Artifact > 위에서 추가한 프로젝트명:war exploded를 선택   
> 컴파일안된 소스를 Tomcat 올려서 I/F통신시 웹페이지 HTML 값들을 가져옴. 컴파일된 아카이브 파일 선택해야함.  

### [InteliJ] Untracked Files Prevent Merge 오류
> 현상 : 프로젝트 소스 업데이트 받다가 취소되면서 아래 오류 발생    
> 내용 : "Untracked Files Prevent Merge Move or commit them before merge"   
> 해결 : 해당 프로젝트 > gitbash >  ``` $ git clean -d -f -f```   

### [InteliJ] lombook import 오류
> 현상 : lombook @어노테이션 컴파일 에러
> 해결 : InteliJ -> Plugins 메뉴 -> ⚙버튼→'Install Plugin from disk' -> 클릭하여 import (Local저장된 lombook Plugins)

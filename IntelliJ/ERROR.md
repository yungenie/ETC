### [InteliJ] Untracked Files Prevent Merge 오류
> 현상 : 프로젝트 소스 업데이트 받다가 취소되면서 아래 오류 발생    
> 내용 : "Untracked Files Prevent Merge Move or commit them before merge"    
> 해결방법 : 해당 프로젝트 > gitbash >  $ git clean -d -f -f   

[파일 로그 보기]   
tail -f [파일명] | grep [일정 단어 포함]   
grep -r -A10 -B10 '14:24:2*' [파일명] 

[용량확인]   
top   

[파일 복사 및 삭제]   
cp -r 폴더명   
rm -rf 폴더명   

[task kill]    
ps -ef l grep mariner
kill -9 PID   

[vi 편집모드]  
vi -R file : 지정한 파일의 내용을 읽기 전용으로 열어 볼 때   
esc shift : q! -> 강제종료   
esc shift : wq -> 저장하고 종료   

- 입력모드   
i > 커서 위치부터 입력   
a > 커서 위치의 다음칸부터 입력  
o > 커서 바로 아래 줄부터 입력(enter)처럼  

- 검색   
shift + g : 파일의 맨 끝 줄   
? : 검색방향 위   
/ : 검색방향 아래   
n : 다음 문자열 탐색   
N(shift + n) : 역방향으로 문자열 탐색  

[cat 보기용]   
tail -500f  log 파일 -> 실시간 로그 확인   
ps -ef | grep java -> java 프로세스 확인  

[ls 현재디렉토리리스트]  
ls -ltr -> 최종수정시간 역순으로 자세하게 출력  
ls -al > ls -al/home/ 과 같이 출력하고 싶은 디렉토리를 지정할 수 있음.  
ls -alSrh : 숨겨진 파일까지 포함해서 파일크기(S) 역순(r)으로 보기 좋게(h) 자세히 (l) 보여주세요.  

in -s 폴더명 sd -> 링크걸기   
chmod 777 파일명, 등등 -> 권한부여    
USER   GROUP  OTHER  
rw- r-- r--  
6 4 4  
110  

r w x 권한없음
4 2 1  0

tar -cvf  생성이름.tar 대상이름  
jar xvf 파일이름.war

**터미널 bash prompt 색상 변경**  
> - .bash_profile에 아래 문구 추가  
> - export PS1 = "\[\e[36;1m\]\u@\[\e[32;1m\]\h:\[\e[31;1m\]\w:> \[\e[0m\]"      
> - 설명 : PS1 변수를 통해 프롬프트 모양을 바꿀 수 있음. 호스트명, 파일명 보기 좋게 색깔로 구분됨.  
> - 참고 : https://www.lesstif.com/system-admin/bash-prompt-profile-12943439.html  

[mount]
remount 작업 - mount -o rw,remount /system

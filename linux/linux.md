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
shift + g : 파일 맨 마지막
? : 검색방향 위
/ : 검색방향 아래
n/shift + n : 해당 검색어 

cat 보기용   
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

tar -cvf  생성이름.tar 대상이름  
jar xvf 파일이름.war

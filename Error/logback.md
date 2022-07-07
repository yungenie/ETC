### [logback][masking] 개인정보 항목 마스킹 처리
> 현상 : 서버로그 개인정보 항목 logback.xml 정규식패턴을 활용한 마스킹 처리시 다양한 json형태 처리안됨.  
> 내용 : https://oingdaddy.tistory.com/383 [SI Supply Depot:티스토리] 블로그와 동일하게 구현. 단, json형태가 다양하여 여러경우의 수 처리 ("key":"" 처리 포함)  
> 해결 : [`<maskPattern>\"key\"\s*:\s*\"(.*?)\"</maskPattern> ---> <maskPattern>\"key\\{0,1}\"\s*:\s*\\{0,1}\"(.*?)\"</maskPattern>`]()  
> json 형태 예시 : 1. "key":"value", 2. "key":"", 3. \"key\":\"value\", 4. \"key\":\"\"  


### [logback][masking] 개인정보 항목 마스킹 처리시 서버 로그파일에 적용 안됨
> 현상 : 서버로그 개인정보 항목 logback.xml 정규식패턴을 활용한 마스킹 처리시 console 적용됨. 서버 로그파일에는 적용 안됨.
> 내용 : https://oingdaddy.tistory.com/383 [SI Supply Depot:티스토리] 블로그와 동일하게 구현.   
> 해결 : <appener name="file">에도 <maskPattern>정규식 패턴</maskPattern> 넣어줘야 함.

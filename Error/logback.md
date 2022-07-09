### [logback][log masking] 개인정보 항목 마스킹 처리
> 현상 : 서버로그파일 개인정보 항목 logback.xml 정규식패턴을 활용한 마스킹 처리시, json 표준 규격에 맞지 않는 특정 데이터 처리안됨.  
> 내용 : https://oingdaddy.tistory.com/383 블로그와 동일하게 구현했으며, 추가적으로 정규식 패턴 표준화 처리 (json형태 "key":"" 처리 포함)   
> 해결 : [`<maskPattern>\"key\"\s*:\s*\"(.*?)\"</maskPattern> -> <maskPattern>\"key\\{0,1}\"\s*:\s*\\{0,1}\"(.*?)\"</maskPattern>`]()   
> 데이터 예시 : 1. "key":"value", 2. "key":"", 3. \\"key\\":\\"value\\", 4. \\"key\\":\\"\\"   
> 정규식패턴 참조 : https://gh402.tistory.com/54?category=890133  


### [logback][log masking] 개인정보 항목 마스킹 처리시 서버 로그파일에 적용 안됨
> 현상 : 서버로그 개인정보 항목 logback.xml 정규식패턴을 활용한 마스킹 처리시 console 적용됨. 서버 로그파일에는 적용 안됨.  
> 내용 : https://oingdaddy.tistory.com/383 블로그와 동일하게 구현.     
> 해결 : \<appener name="file">에도 \<maskPattern>정규식 패턴\</maskPattern> 넣어줘야 함.

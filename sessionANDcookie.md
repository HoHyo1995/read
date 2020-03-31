# Session(세션)과 Cookie(쿠키)
## 1. session(세션)이란?
일정시간동안 클라이언트(사용자)가 보내는 요구를 하나의 상태로 보고, 그 상태를 유지시켜 클라이언트와 서버의  
연결을 유지시키는 기술로 http 프로토콜 요청은 한번의 요청(클라이언트 -> 서버)와 한번의 응답(서버 -> 클라이언트)  
로 이루어진 후 연결이 해제 된다.  

그래서 서버는 요청을 한 클라이언트에게 set-cookie 값으로 클라이언트 식별자인 session id를 통해 사용자를  
식별한다. 즉 기존정보를 계속 유지해야 하므로 session을 사용해 정보를 저장한다.

## 2. cookie(쿠키)란?
서버가 만들어 클라이언트에서 관리되는 작은 데이터 파일을 말하며 사용자 인증이 유효한 시간을 명시하며 한 번 유효시간이 정해지면 브라우저를 끄더라도 인증이 유지된다.

클라이언트가 페이지를 요청하면 서버에서 쿠키를 생성해서 HTTP헤더에 쿠키를 포함시켜 응답을 한 후 클라이언트에서  
보관을 합니다. 그 후 요청을 하면 쿠키가 포함되어 요청이 되고 변경할 쿠키 정보가 있으면 업데이트 후 응답된다.




<hr>  

## 참고  
<https://velog.io/@max9106/JSP-Session%EC%84%B8%EC%85%98-j0k5ccyiub>  
<https://hahahoho5915.tistory.com/32>  
<https://mohwaproject.tistory.com/entry/HTTP-Session-%EC%9D%B4%EB%9E%80>  
<https://victorydntmd.tistory.com/34>  
<https://cjh5414.github.io/cookie-and-session/>

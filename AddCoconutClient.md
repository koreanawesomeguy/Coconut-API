# Coconut 회원 가입


- API : https://7hob5mtfll.execute-api.us-east-2.amazonaws.com/AddCoconutClient (POST)


- Request

  * Sample
  {
      "FIT" : "ReUTaYQeUDcpq2YMxZE3mKfaX6C3",
      "CoconutPIN" : "123456",
      "MobileNumber" : "123456",
      "Email" : "aaaaa@google.com"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  CoconutPIN | 회원가입 시 입력한 비밀번호 | String/필수
  MobileNumber | 회원가입 시 입력한 휴대폰번호 | String/필수
  Email | 회원가입 시 입력한 이메일 | String/옵션

- Response Success

  * Sample 
  {
      "status": "3000",
      "response": "OK"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 그 외 에러 코드 참조) | String/필수
  response | 요청 결과 | String/필수
  
- Response Error
  
  * Sample
  {
      "status": "3200",
      "response": ""
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  3100 | "" | Firebase Id Token 오류
  3200 | "Member Exist" | 이미 코코넛 회원가입 상태
  

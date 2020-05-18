# Coconut 회원 가입


- API : https://7hob5mtfll.execute-api.us-east-2.amazonaws.com/AddCoconutClient (POST)


- Request

  * Sample
  {
      "FIT" : "eyJhbGciOiJSUzI1NiIsImtpZCI6ImY1YzlhZWJlMjM0ZGE2MDE2YmQ3Yjk0OTE2OGI4Y2Q1YjRlYzllZWIiLCJ0eXAiOiJKV1QifQ.eyJpc3MiOiJodHRwczovL3NlY3VyZXRva2VuLmdvb2dsZS5jb20vY29jb251dC04MzAwOCIsImF1ZCI6ImNvY29udXQtODMwMDgiLCJhdXRoX3RpbWUiOjE1ODk3MjQ3ODEsInVzZXJfaWQiOiJrTTdMaG1TZlN6TXBZU1RsZXN5ZldzUWQzZjgzIiwic3ViIjoia003TGhtU2ZTek1wWVNUbGVzeWZXc1FkM2Y4MyIsImlhdCI6MTU4OTgwMzk2MiwiZXhwIjoxNTg5ODA3NTYyLCJlbWFpbCI6ImFiY2RAbmF0ZS5jb20iLCJlbWFpbF92ZXJpZmllZCI6ZmFsc2UsImZpcmViYXNlIjp7ImlkZW50aXRpZXMiOnsiZW1haWwiOlsiYWJjZEBuYXRlLmNvbSJdfSwic2lnbl9pbl9wcm92aWRlciI6InBhc3N3b3JkIn19.P1AyZEdUjEoL1wmF-Yk0ojD6UzhqisYdfmOVSr0nKf5L_U6l-WLfTTDxDxIVFUCKsAfq4BKYN7uVcgt1B97a8085M97Hw-r8bY3sGhJz9SrXCq3itsx1UPyzFaFsgAxiQxcO1WYyXXp0AT1H2dOyTBd78WEFdmufGSU9-B4nlr9LKkueFyBueJszNUI3PUo9Z1jIzzewC1wVsAKUWZCcv58VlHydiSzr8rYb3_6cJzIEWimOMDgpFw1IPzaIMasp82nqTT8TU1xdJsmzTl69PyxVNxn2_qGkZhN73G7E5nQrqyom23QnZnc5-2UbiidBI4bioSOAew0uL2B7PXiKLg",
      "CoconutPIN" : "123456",
      "PhoneNumber" : "123456",
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
  status | 결과 상태 코드 (정상: 3000, FIT 에러 : 3100, 이미 회원 : 3300, 회원가입 실패 : 3400) | String/필수
  response | 요청 결과 | String/필수

# 회원 조회


- API : https://wx9did7o26.execute-api.us-east-2.amazonaws.com/CheckMemberForThirdParty (POST)


- Request

  * Sample : 
{ 
    "Email": "koreanawesomeguy@gmail.com", 
    "PhoneNumber" : "821041139274", 
    "Caller" : "Vroomgo" 
}
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  PhoneNumber | Vroomgo 회원 휴대폰번호 | String/필수
  Email | Vroomgo 회원 이메일 | String/필수
  Caller | Caller Service | String/필수
  
- Response Success

  * Sample : 
  {
      "status": 3000,
      "response": "OK"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/coinville/Coconut/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 

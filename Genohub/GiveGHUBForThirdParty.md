# GHUB 지급. 회원가입 시, 회원추천 시


- API : https://89q8lkgok1.execute-api.us-east-2.amazonaws.com/GiveGHUBForThirdParty (POST)


- Request

  * Phone, Email 전부 사용하는 경우 : 
  { 
     "Email": "rlackstjdsla@naver.com", 
     "PhoneNumber" : "821041139274",
     "Type" : "SignUp",
     "Caller" : "Genohub"
  }
  
  * Phone만 사용하는 경우 : 
  { 
     "PhoneNumber" : "821041139274", 
     "Caller" : "Genohub",
     "Type" : "SignUp"
  }
  
  * Email만 사용하는 경우 : 
  { 
      "Email": "rlackstjdsla@naver.com", 
      "Caller" : "Genohub", 
      "Type" : "Recommend" 
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  MobileNumber | Genohub 회원 휴대폰번호 | String/필수
  Email | Genohub 회원 이메일 | String/필수
  Caller | Caller Service | String/필수
  Type | SignUp : 회원가입 시 코인 지급, Recommend : 친구 추천 시 코인 지급 | String/필수
  
- Response Success

  * Sample : 
{
    "status": "3000",
    "response": "200"
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 

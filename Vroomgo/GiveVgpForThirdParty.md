
# VGP 적립하기  


- API : https://9k3w2hs99a.execute-api.us-east-2.amazonaws.com/GiveVgpForThirdParty (POST)


- Request

  * Phone, Email 전부 사용하는 경우 : 
  { 
     "Email": "test@coinville.ph", 
     "PhoneNumber" : "821041139274", 
     "Caller" : "Vroomgo",
     "VGPDeposit" : "10",
     PID : "123456",
     Timestamp: "1590934309"
  }
  
  * Email만 사용하는 경우 : 
  { 
     "Email": "rlackstjdsla@naver.com", 
     "Caller" : "Vroomgo",
     "VGPDeposit" : "10",
     PID : "123456",
     Timestamp: "1590934309"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  PhoneNumber | Genohub 회원 휴대폰번호 | String
  Email | Genohub 회원 이메일 | String/필수
  Caller | Caller Service | String/필수
  VGPDeposit | VGP 적립량 | String/필수
  PID | 거래 번호 | String/필수
  Timestamp | transaction time | String/필수
  
- Response Success

  * Sample : 
{
    "status": "3000",
    "response": "OK"
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
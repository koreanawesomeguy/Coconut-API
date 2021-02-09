# VRGX - VGP 환율 정보 

- API : https://zdtac1fie3.execute-api.us-east-2.amazonaws.com/GetExchangeRateForThirdParty (POST)


- Request

  * Phone, Email 전부 사용하는 경우 : 
  { 
     "Email": "rlackstjdsla@naver.com", 
     "PhoneNumber" : "821041139274", 
     "Caller" : "Vroomgo"
  }
  
  * Phone만 사용하는 경우 : 
  { 
     "PhoneNumber" : "821041139274", 
     "Caller" : "Vroomgo"
  }
  
  * Email만 사용하는 경우 : 
  { 
     "Email": "rlackstjdsla@naver.com", 
     "Caller" : "Vroomgo"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  PhoneNumber | Vroomgo 회원 휴대폰번호 | String/옵션
  Email | Vroomgo 회원 이메일 | String/옵션
  Caller | Caller Service | String/필수
    
- Response Success

  * Sample : 
{
    "status": "3000",
    "response": {
        "VRGXPrice": "4.90",
        "TransferCommission": "3",
        "PHP": "0.0430422884"
    }
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/coinville/Coconut/blob/master/Vroomgo/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 

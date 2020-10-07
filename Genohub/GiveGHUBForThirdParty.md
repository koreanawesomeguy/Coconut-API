# GHUB 지급. 회원가입 시, 회원추천 시


- API : https://89q8lkgok1.execute-api.us-east-2.amazonaws.com/GiveGHUBForThirdParty (POST)

- Request

  * 제노허브 가입한 회원이면서 코코넛 가입한 회원인 경우 : 
  { 
     "Email": "rlackstjdsla@naver.com", 
     "Type" : "SignUp",
     "Caller" : "Genohub"
  }
  
  * 코코넛 + 제노허브 가입자 B가 코코넛 + 제노허브 가입자 A를 추천인 코드로 등록 후 첫 결제 시 A에게 GHUB 지급
  { 
      "Caller" : "Genohub", 
      "Type" : "Recommend", 
      "Recommender" :"sapphire1009@nate.com", 
      "Recommendee" :"rlackstjdsla@naver.com"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  MobileNumber | Genohub 회원 휴대폰번호 | String/필수
  Email | Genohub 회원 이메일 | String/필수
  Caller | Caller Service | String/필수
  Type | SignUp : 회원가입 시 코인 지급, Recommend : 친구 추천 시 코인 지급 | String/필수
  Recommendee | 추천받는 회원 Email | String/필수
  Recommender | 추천하는 회원 Email | String/필수
  
- Response Success

  * Request body 에서 Type이 SignUp 인 경우, response에 제노허브 + 코코넛 회원가입 시 지급받는 GHUB 갯수가 return. 마찬가지로 Type이 Recommend인 경우 추천 시 지급할 GHUB 갯수를 return.
  
{
    "status": "3000",
    "response": "200"
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 

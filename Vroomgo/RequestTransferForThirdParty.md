
# VRGX -> VGP 환전 요청

- API : https://rc1y2sfa08.execute-api.us-east-2.amazonaws.com/RequestTransferForThirdParty (POST)

- Request

  * 제노허브 가입한 회원이면서 코코넛 가입한 회원인 경우 : 
    { 
        "Caller" : "Vroomgo", 
        "Type" : "ThirdParty", 
        "AssetCode" :"VRGX", 
        "Point" :"VGP", 
        "Amount" :"51", 
        "Email" :"sapphire1009@nate.com", 
        "PhoneNumber" :"821041139274" 
    }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  Caller | Vroomgo 하드 코딩 | String/필수
  Type | ThirdParty 하드 코딩 | String/필수
  AssetCode | VRGX 하드 코딩 | String/필수
  Point | VGP 하드 코딩 | String/필수
  Amount | 환전하고자 하는 VRGX Amount | String/필수
  Email | 회원 Email | String/필수
  PhoneNumber | 회원 전화번호 | String/필수
  
- Response Success  
{
    "status": "3000",
    "response": "200"
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Vroomgo/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | String/필수
 

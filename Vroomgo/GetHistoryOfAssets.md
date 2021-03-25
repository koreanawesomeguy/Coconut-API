
# Target 코인의 변동 내역 조회  


- API : https://4jfmusl72i.execute-api.us-east-2.amazonaws.com/GetHistoryOfAssets (POST)


- Request

  * Phone, Email 전부 사용하는 경우 : 
  { 
     "Email": "test@coinville.ph", 
     "AssetCode" : "VGP"
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
  PhoneNumber | Genohub 회원 휴대폰번호 | String
  Email | Genohub 회원 이메일 | String/필수
  AssetCode | 코인의 종류 (ex. VRGX, VGP, GHUB, ...) | String/필수
  Caller | Caller Service | String/필수
  
- Response Success

  * Sample : 
{
    "status": "3000",
    "response": [
        {
            "Timestamp": "1590934309",
            "AssetCode": "VGP",
            "PhoneNumber": "+821089268034",
            "Usage": "-10",
            "Caller": "Vroomgo",
            "Balance": 20,
            "PID": "12345678990900",
            "Type": "Payment",
            "StoreInfo": "Familymart",
            "Email": "test@coinville.ph"
        },
        {
            "Timestamp": "1616304235",
            "AssetCode": "VGP",
            "PhoneNumber": "+821089268034",
            "Usage": "10",
            "Caller": "Vroomgo",
            "Balance": 30,
            "PID": "12345678990900",
            "Type": "Cancel",
            "StoreInfo": "Familymart",
            "Email": "test@coinville.ph"
        }
    ]
}
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 에러의 경우 https://github.com/koreanawesomeguy/Coconut-API/blob/master/Genohub/Error%20Code.md 참고) | String/필수
  response | 요청 결과 | Array,String/필수
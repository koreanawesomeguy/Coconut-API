# Coconut 로그인 관리


- API : https://r97dhhawq4.execute-api.us-east-2.amazonaws.com/GetCoconutLoginHistory (POST)

- Request

  * Sample
  {
      "FIT" : "ReUTaYQeUDcpq2YMxZE3mKfaX6C3",
      "Timestamp" : "1590888063",
      "IP" : "127.0.0.1",
      "Location" : "대한민국"
      "Device" : "Android"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  Timestamp | 현재 시간 정보(Timestamp) | String/필수
  IP | IP 주소 | String/필수
  Location | 위치 | String/옵션
  Device | Device 종류 | String/옵션
  
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

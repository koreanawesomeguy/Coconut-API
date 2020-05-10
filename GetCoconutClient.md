# Coconut 회원 조회


- API : https://8aa4963gcd.execute-api.us-east-2.amazonaws.com/GetCoconutClient (POST)


- Request

  * Sample
  {
      "FIT": "ReUTaYQeUDcpq2YMxZE3mKfaX6C3"
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수

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
 

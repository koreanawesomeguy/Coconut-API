# Coconut 회원 조회


- API : https://8aa4963gcd.execute-api.us-east-2.amazonaws.com/GetCoconutClient (POST)


- Request
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  * Sample
  {
      "FIT": "ReUTaYQeUDcpq2YMxZE3mKfaX6C3"
  }

- Response Success
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 그 외 에러 코드 참조) | String/필수
  * Sample 
  {
      "status": "3000",
      "response": "OK"
  }

- Response Error
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  5100 | "" | Firebase Id Token 오류
  5200 | 'Not Member' | 회원가입이 되어있지 않음
  * Sample
  {
      "status": "3100",
      "response": ""
  }

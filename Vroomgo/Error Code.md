# Error Code

- Response Error
  
  * Sample
  {
      "status": "3100",
      "response": "Wrong Caller"
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  "3100" | "Wrong Caller" | Caller Service 오류
  "3200" | "Not Member" | 회원가입이 되어있지 않음
  "3300" | "No Asset Information" | VRGX, VGP 자산 정보 없음

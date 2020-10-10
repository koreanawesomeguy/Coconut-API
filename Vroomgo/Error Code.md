# Error Code

- Response Error
  
  * Sample : 
  {
      "status": "3100",
      "response": "Wrong Caller"
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  "3100" | "Wrong Caller" | Caller Service 오류
  "3200" | "Not Member" | 회원가입이 되어있지 않음
  "3300" | "No Asset Information" | 자산 정보 없음
  "3301" | "Balance Insufficient" | 자산 부족
  "3302" | "Type is empty" | Recommend/SignUp 파라미터 없음
  "3303" | "Recommender or Recommendee is empty" | Sender/Receiver 파라미터 없음
  "3400" | "Unhandled Error" | 비정상 

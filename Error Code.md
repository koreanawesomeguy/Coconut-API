# Error Code

- Response Error
  
  * Sample
  {
      "status": "3300",
      "response": "Member Exist"
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  3001 | "None" | 등록된 정보가 없는 경우 
  3100 | "" | Firebase Id Token 오류
  3200 | "Not Member" | 회원가입이 되어있지 않음
  3300 | "Member Exist" | 이미 코코넛 회원가입 상태
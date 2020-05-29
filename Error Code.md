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
  3400 | "SignUp Failed" | 회원가입 실패
  3500 | "Create Address Failed" | 자산 주소 생성 실패
  3600 | "Request Eth Address Again" | 자산 주소 생성 실패
  3700 | "Invalid Parameter" | 잘못된 인자 값으로 호출
  4000 | "Unknown Error" | 알 수 없는 에러

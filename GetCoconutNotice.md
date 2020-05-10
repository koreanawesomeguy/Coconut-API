# Coconut 회원 가입


- API : https://tiphzvavs0.execute-api.us-east-2.amazonaws.com/GetCoconutNotice (POST)


- Request

  * Sample
  {
      "FIT" : "ReUTaYQeUDcpq2YMxZE3mKfaX6C3",
      "Caller" : "Coconut",
      "ACTION" : "Select",
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  Caller | 요청 Service | String/필수
  ACTION | 게시판 정보 선택 | String/필수

- Response Success

  * Sample 
  {
      "status": "3000",
      "response": 
      "{
          "Content":"1121","ReportingDate":"2020.4.13 3:15:8","Title":"121111", "Timestamp":"1586715308", "Type":"Notice", "Writer":"awesomeguy@coinville.ph"
       },
       {
           "Content":"2222","ReportingDate":"2020.4.13 3:15:13", "Title":"2222", "Timestamp":"1586715313", "Type":"Notice", "Writer":"awesomeguy@coinville.ph"
       },
       {
           "Content":"3333", "ReportingDate":"2020.4.13 3:15:17", "Title":"33333", "Timestamp":"1586715317", "Type":"Notice", "Writer":"awesomeguy@coinville.ph"
       },
       {
           "Content":"444444444444", "ReportingDate":"2020.4.13 3:15:20", "Title":"4444444444444", "Timestamp":"1586715320", "Type":"Notice", "Writer":"awesomeguy@coinville.ph"
       },
       {
           "Content":"5555555555555555555555555555555555","ReportingDate":"2020.4.13 3:15:25", "Title":"555555555555555555555555555555", "Timestamp":"1586715325", "Type":"Notice", "Writer":"awesomeguy@coinville.ph"
       }"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 그 외 에러 코드 참조) | String/필수
  response | Title : 제목, Content : 내용, ReportingDate : 작성일시 | String/필수
  
- Response Error
  
  * Sample
  {
      "status": "3300",
      "response": ""
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  3100 | "" | Firebase Id Token 오류
  3200 | "Member Exist" | 이미 코코넛 회원가입 상태
  

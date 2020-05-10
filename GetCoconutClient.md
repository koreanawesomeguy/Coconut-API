# Coconut 회원 조회


- API : https://8aa4963gcd.execute-api.us-east-2.amazonaws.com/GetCoconutClient (POST)


- Request Sample
  * Content type : application/json
  * Request Parameters

요청 변수 | 설명 | 타입
------------ | ------------- | -------------
FIT | Firebase Id Token | String/필수


- Response Sample
{
    "status": "3000",
    "response": "OK"
}

- Response
필드, 설명, 타임으로 구성된 표
필드	설명	타입
status	결과 상태 코드 (정상: 0000, 그 외 에러 코드 참조)	String

- Error Sample
{
    "status": "3100",
    "response": ""
}

- Error
에러 코드 | 에러 메시지 | 설명
------------ | ------------- | -------------
5100 | '' | Firebase Id Token 오류
5200 | 'Not Member' | 회원가입이 되어있지 않음

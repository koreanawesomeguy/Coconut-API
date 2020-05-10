# Coconut 회원 조회


- API : https://8aa4963gcd.execute-api.us-east-2.amazonaws.com/GetCoconutClient (POST)


- Request Sample
  . Content type : application/json
  . Request Parameters

요청 변수 | 설명 | 타입
------------ | ------------- | -------------
FIT | Firebase Id Token | String/필수


- Response Sample

에러 코드 | 에러 메시지 | 설명
------------ | ------------- | -------------
5100 | '' | Firebase Id Token 오류
5200 | 'Not Member' | 회원가입이 되어있지 않음

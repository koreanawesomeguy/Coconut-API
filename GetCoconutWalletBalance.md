# Coconut Balance 정보


- API : https://f6fp9lrs33.execute-api.us-east-2.amazonaws.com/GetCoconutWalletBalance (POST)


- Request

  * Sample
  {
      "FIT" : "ReUTaYQeUDcpq2YMxZE3mKfaX6C3",
      "AssetCode" : "all"                    
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  AssetCode | 얻고자 하는 Balance 이름(all : 모든 자산의 Balance, BTC/ETH/XRP/LTC/GHUB/GHD/VRGX/VGP/CSMT) | String/필수

- Response Success

  * Sample 
  {
      "status": "3000",
      "response": "{'GHUB': '0', 'BTC': '0', 'GHD': '0', 'XRP': '0', 'CSMT': '0', 'VRGX': '0', 'ETH': '0', 'LTC': '0', 'VGP': '0'}"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 그 외 에러 코드 참조) | String/필수
  GHUB | GHUB 자산 내역 | String/필수
  GHD | GHD 자산 내역 | String/필수
  VRGX | VRGX 자산 내역 | String/필수
  VGP | VGP 자산 내역 | String/필수
  CSMT | CSMT 자산 내역 | String/필수
  BTC | BTC 자산 내역 | String/필수
  ETH | ETH 자산 내역 | String/필수
  LTC | LTC 자산 내역 | String/필수
  XRP | XRP 자산 내역 | String/필수
              
- Response Error
  
  * Sample
  {
      "status": "3001",
      "response": "None"
  }
  
  * Response Schema (application/json)

  에러 코드 | 에러 메시지 | 설명
  ------------ | ------------- | -------------
  3001 | "None" | 해당 회원의 자산정보 없음
  3100 | "" | Firebase Id Token 오류
  

# Coconut 자산 주소 정보


- API : https://0onl0boee8.execute-api.us-east-2.amazonaws.com/GetCoconutWalletAddress (POST)


- Request

  * Sample
  {
      "FIT" : "ReUTaYQeUDcpq2YMxZE3mKfaX6C3",
      "AssetCode" : "ALL"                         //BTC, ETH, LTC, XRP
  }
  
  * Request body schema (application/json)
  
  요청 변수 | 설명 | 타입
  ------------ | ------------- | -------------
  FIT | Firebase Id Token | String/필수
  AssetCode | 생성하고자 하는 자산 이름(all : 모든 자산의 주소, BTC/ETH/XRP/LTC/GHUB/GHD/VRGX/VGP/CSMT) | String/필수

- Response Success

  * Sample 
  {
      "status": "3000",
      "response": "{'GHUB': 'dgjajkejiofasfd', 'BTC': '30dsfmklaeiof129skd', 'GHD': 'dsgdsfasdf', 'XRP': 'dsfg12lkal1ksdf', 'CSMT': 'fgdaeffgadfs', 'VRGX': '1idkjdkljslkadf', 'ETH': '0x123xafsdsafdsf', 'LTC': 'dslkfiaejfasdgsdag', 'VGP': 'dkdajklflkjasdf'}"
  }
  
  * Response Schema (application/json)

  필드 | 설명 | 타입
  ------------ | ------------- | -------------
  status | 결과 상태 코드 (정상: 3000, 그 외 에러 코드 참조) | String/필수
  GHUB | GHUB 주소 정보 | String/필수
  GHD | GHD 주소 정보 | String/필수
  VRGX | VRGX 주소 정보 | String/필수
  VGP | VGP 주소 정보 | String/필수
  CSMT | CSMT 주소 정보 | String/필수
  BTC | BTC 주소 정보 | String/필수
  ETH | ETH 주소 정보 | String/필수
  LTC | LTC 주소 정보 | String/필수
  XRP | XRP 주소 정보 | String/필수
              
  * ETH의 경우 최초 한번은 ETH ID 값, 다음 번 요청시에 실제 ETH 주소값을 받을 수 있다.
  ex) 최초 회원가입 완료 후 Main페이지에서 AssetCode:ALL로 모든 지갑 주소 생성 -> ETH는 ID값을 가지고 있기 때문에 ETH 카드로 들어가는 경우, AssetCode:ETH로 다시 한번 요청해야 함. 

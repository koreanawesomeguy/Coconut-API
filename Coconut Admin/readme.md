- AWS Light Sail 서버 사용 : coconutadmin.coinville.ph (52.79.221.240)

- admin 페이지 접속 정보
  . 접속 방법
    2. Coconut Admin 접속 시 아래 순서로 진행 부탁드립니다.
      1). Chrome browser 비밀창 띄우기 : ctrl + Shift + n
      2). http://work.coinville.ph/ 접속
      3). coinville.ph 계정 id, pwd 입력
      4). Coconut admin 클릭
  . 현재 Master 계정 및 비밀번호 : awesomeguy@coinville.ph / Ckstjd927$ 
    -> 해당 계정으로 다른 admin user의 권한 변경 가능
  . Coconut Admin 진입 후 1 시간 마다 Access token이 만료. 하여 token이 만료 될 때마다 http://work.coinville.ph/ 로 진입하여 새로운 token을 받아서 진행 필요.
  
- 소스코드 다운로드 방법
  . Visual Studio Code 에서 아래 sftp 설정을 통한 코드 다운로드 (pem 파일을 privateKeyPath path 저장해야 다운로드 가능)
  
    {
      "name": "coconutadmin.coinville.ph",
      "host": "coconutadmin.coinville.ph",
      "protocol": "sftp",
      "port": 22,
      "username": "bitnami",
      "privateKeyPath": "C:\\Users\\korea\\Desktop\\Coconut\\Coconut_Admin\\pem\\key-coconutadmin.coinville.ph.pem",
      "remotePath": "/opt/bitnami/nginx/html/",
      "watcher": {"files": "**", "autoUpload": true, "autoDelete": true},
      "uploadOnSave": true
    }

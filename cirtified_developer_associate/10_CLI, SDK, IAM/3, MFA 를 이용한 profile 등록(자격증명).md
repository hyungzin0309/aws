Multi-Factor Authentication

> aws CLI 를 이용하기 위해선, aws 권한을 가진 사용자의 profile 을 등록해야 한다. 영구적으로 사용되는 사용자 정보 입력 시, 정보 노출로 인한 보안 위험이 있기 떄문에 임시로 자격증명을 발급하여 profile 등록에 사용할 수 있다.


### 사용방법

1. AWS 인터페이스에서 특정 사용자에 대한 MFA 등록
2. AWS CLI 에서 해당 사용자에 대한 자격증명 요청
   1. `aws sts get-session-token --serial-number={value} --token-code=${value}`
   2. return 받은 자격증명(accessKeyId, secretAccessKey)을 통해 profile 을 등록
   3. credentials 파일 -> 방금 등록한 profile 에 대해 access token 필드 추가
      - `aws_access_token=${value}`
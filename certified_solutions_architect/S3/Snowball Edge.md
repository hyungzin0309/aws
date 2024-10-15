> AWS Snowball Edge는 AWS의 데이터 전송 및 엣지 컴퓨팅 디바이스로, 대규모 데이터를 안전하고 효율적으로 AWS로 전송하거나, 로컬 환경에서 데이터를 처리할 수 있는 서비스다. Snowball Edge는 스토리지 기능뿐만 아니라 엣지 컴퓨팅 기능도 제공하여, 클라우드에 연결되지 않은 환경에서도 데이터 수집 및 분석 작업을 수행할 수 있다.

### 1. AWS Snowball Edge

- **물리 디바이스 사용** : 스노우볼 엣지를 사용하기 위해 AWS 에 서비스를 요청하면, 오프라인으로 물리 장치 디바이스가 배송이 되며, 소비자는 해당 디바이스에 데이터를 저장하고 다시 AWS 에 요청하여 해당 디바이스를 AWS 측에 전달
- **대규모 데이터 전송**: Snowball Edge를 사용하면 네트워크 대역폭에 의존하지 않고 **TB~PB 단위**의 데이터를 물리적으로 AWS로 전송할 수 있다.
- **엣지 컴퓨팅**: Snowball Edge는 로컬에서 데이터를 **처리**하고 **분석**할 수 있는 **컴퓨팅 리소스**(EC2 인스턴스, Lambda 함수 등)를 제공하여, 네트워크 연결 없이도 AWS 환경에서 애플리케이션을 실행할 수 있다.
- **보안**: Snowball Edge는 **256비트 AES 암호화**와 **내장된 보안 모듈**을 사용하여 데이터를 안전하게 보호하며, 디바이스가 AWS로 반환될 때 데이터를 자동으로 삭제한다.
- **내구성**: Snowball Edge는 **내구성이 뛰어나고 방수** 및 **충격 방지** 기능을 갖춘 하드웨어로, **극한 환경**에서도 안정적으로 사용할 수 있다.
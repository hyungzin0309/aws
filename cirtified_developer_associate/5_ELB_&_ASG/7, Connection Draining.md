

> Connection Draining 기능은 ELB 의 중요한 기능 중 하나로, 특정 인스턴스가 유지 보수, 업데이트, 스케일 인/아웃 등의 이유로 로드 밸런싱 풀에서 제거될 때 이미 활성 연결을 보호하는 역할을 한다. 이 기능은 로드 밸런서가 인스턴스를 로드 밸런싱 풀에서 안전하게 분리할 수 있도록 하여, 진행 중인 요청이나 세션이 중단되지 않고 정상적으로 완료될 수 있도록 한다.

### 작동 방식
1. **비활성화 요청**: 인스턴스가 유지 보수 등의 이유로 로드 밸런서 풀에서 제거되거나 비활성화 될 때, Connection Draining 이 활성화되어 있다면, 이 기능이 작동을 시작한다.


2. **연결 유지**: Connection Draining 이 활성화된 상태에서 인스턴스가 비활성화 명령을 받으면, 로드 밸런서는 해당 인스턴스로 새로운 트래픽을 보내지 않으며, 이미 진행 중인 요청은 완료될 때까지 유지한다.


3. **타임아웃 설정**: 관리자는 Connection Draining 에 대한 타임아웃을 설정할 수 있다. 이 시간 동안에는 기존의 연결이 유지되고, 설정된 시간이 지나면, 아직 완료되지 않은 연결이 있더라도 인스턴스는 로드 밸런싱 풀에서 제거된다.

### 설정
타임아웃 기간은 일반적으로 몇 초에서 몇 분 사이로 설정되며, 어플리케이션의 요구 사항과 트래픽 패턴에 따라 조정될 수 있다.

### 장점
- **서비스 중단 최소화**: 진행 중인 세션과 트랜잭션이 갑작스럽게 끊기지 않고 정상적으로 처리될 수 있어, 사용자 경험과 서비스의 안정성이 향상된다.
- **유연한 인스턴스 관리**: 유지 보수, 인스턴스 업그레이드, 스케일 조정 등이 필요할 때, 연결 드레이닝은 서비스의 가용성을 유지하면서 이러한 작업을 용이하게 한다.
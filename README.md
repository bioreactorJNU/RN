+----------------+      +----------------+      +----------------+
|     User       |  1   |    Device      |  N   |  SensorData    |
|----------------|------|----------------|------|----------------|
| UserID (PK)    |      | DeviceID (PK)  |      | DataID (PK)    |
| Name           |      | UserID (FK)    |      | DeviceID (FK)  |
| Email          |      | DeviceName     |      | Temperature     |
| Password       |      |                |      | Humidity       |
+----------------+      +----------------+      +----------------+
                                                       |
                                                       |
                                                       |
                                                +----------------+
                                                |   ImageData    |
                                                |----------------|
                                                | ImageID (PK)   |
                                                | DeviceID (FK)  |
                                                | ImageURL       |
                                                | Timestamp      |
                                                +----------------+

### 기능 구현 부분 추가 내용 (Raspberry Pi 하드웨어 서버 통신 포함)

1. **기술 스택**
   - **프론트엔드**: React native
   - **백엔드**: Firebase Database
   - **하드웨어**: Raspberry Pi
   - **기타 라이브러리 및 프레임워크**: 필요한 경우 추가 명시

2. **아키텍처**
   - **애플리케이션 구조**: MVC 또는 MVVM 등
   - **하드웨어 통신 구조**: Raspberry Pi와 서버 간의 통신 패턴 및 프로토콜 (MQTT, HTTPS)

3. **데이터베이스 구조**
   - 주요 데이터 모델 및 스키마
   - 데이터 관계도 (ER 다이어그램)

4. **서버 통신**
   - **API 설계 및 명세**: Raspberry Pi에서 서버로, 서버에서 Raspberry Pi로의 데이터 전송 방법
   - **통신 프로토콜**: MQTT (실시간 데이터), HTTPS (비실시간 데이터)
   - **데이터 동기화 및 오프라인 지원 전략**: Raspberry Pi의 데이터 동기화 방식

5. **하드웨어 통신**
   - **Raspberry Pi 사양**
     - 모델명: Raspberry Pi 4
     - 사용되는 센서 및 부속품: DHT22 온습도 센서, Raspberry Pi Camera Module 등
   - **데이터 수집 방식**
     - 센서로부터 데이터 수집 방법 및 주기
     - Raspberry Pi에서 데이터 필터링 및 처리 방식
   - **데이터 전송 방식**
     - 서버로의 데이터 전송 방법: WiFi를 통해 MQTT 및 HTTPS 사용
   - **통신 보안**
     - 데이터 전송 시 보안 방식: TLS/SSL 암호화

6. **사용자 인증 및 보안**
   - Firebase Authentication 인증

7. **테스트 전략**
  - JUNIT

8. **배포 및 운영**
   - AWS Amplify

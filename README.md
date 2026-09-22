# Game Spring Expert Assignment

Spring Boot 기반의 실시간 멀티플레이어 게임 서버 과제입니다. REST API로 플레이어/월드를 관리하고,
WebSocket으로 이동·채팅·접속자 목록 등 실시간 기능을 제공합니다.

- API 명세: [WebCraft API 문서](https://f-api.github.io/game-spring-api-docs/expert/api-docs.html)

## 기술 스택

- **Java 21**, **Spring Boot**
- **MySQL** — 플레이어, 월드, 채팅 내역 등 영구 데이터 저장
- **Redis** — 월드별 접속(presence) 상태 관리
- **WebSocket** — 이동, 채팅, 접속자 목록 등 실시간 통신
- **JPA(Hibernate)**, **Gradle**



## 구현 단계 (Lv 1 ~ Lv 15)

과제는 단계별(Lv 1~15)로 진행되며, 각 단계마다 대응하는 테스트 클래스의 주석을 해제해 검증합니다.

1. Docker로 MySQL/Redis 설정
2. `ChatMessage`에 인덱스(`idx_chat_world_created_at`) 선언
3. 플레이어 등록 API (요청 검증, DTO, 닉네임 중복 처리)
4. 월드 생성 API
5. 채팅 저장 및 최근 채팅 조회 로직
6. 최근 채팅 조회 API
7. WebSocket 핸드셰이크에서 사용자 식별
8. `HandshakeInterceptor` 등록
9. 월드별 WebSocket 세션 관리
10. Redis 접속 상태 관리
11. 메시지 라우팅과 Ping/Pong
12. 플레이어 이동 요청 처리
13. 채팅 요청 처리와 응답 구성
14. 같은 월드 참여자에게 채팅 브로드캐스트
15. 접속자 목록 조회

각 단계의 상세 요구사항은 과제 안내 문서를 참고하세요.


# 유병규 (Byeong-gyu Yoo)
> **Backend Developer** | 성능 최적화와 안정적인 시스템 구축에 관심이 많은 개발자입니다.

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=ybg6539)](https://solved.ac/ybg6539/) 
[![Gmail](https://img.shields.io/badge/-ybg653924@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:ybg653924@gmail.com)
<br> [코테 연습](https://github.com/Gyulguma/Coding-Drawer)

---

## 🚀 Featured Projects

### **Meethub** - 멀티 영상 소스 기반 회의 요약 B2B 솔루션 (SSAFY 자율 프로젝트 우수상)
`Spring Boot` `Spring Security` `MySQL` `Redis` `Docker` `Jenkins` `Prometheus` `Grafana` `2025.10-11`

기업 연계 프로젝트로, 계층적 폴더 권한 시스템과 모니터링 환경 구축을 담당
- **문제**: 상위 폴더를 한 단계씩 거슬러 오르며 권한을 조회해, 폴더 깊이만큼 쿼리가 반복되는 N+1 문제 (`@PreAuthorize`로 대부분의 API 요청마다 수행)
- **해결**: 재귀 CTE(`WITH RECURSIVE`) 단일 쿼리로 통합하고, Redis Look-Aside 캐싱 도입. 권한 변경·삭제 시 하위 폴더 캐시까지 일괄 무효화하여 정합성 유지
- **협업**: 명세에 없던 "회의 미참석자를 위한 자료 공유" 기능을 선제적으로 기획·구현

### **틔움** - 주말 농장 관리 서비스 (SSAFY 특화 프로젝트 우수상)
`Spring Boot` `Redis` `MySQL` `Docker` `Prometheus` `Grafana` `Loki` `2025.08-09`

주말 농장 이용자를 위한 실시간 기상 정보 제공 서비스에서 백엔드와 모니터링 환경 구축을 담당
- **문제**: 접속할 때마다 외부 날씨 API를 직접 호출하면 호출 제한 초과 및 과금 위험
- **해결**: 위경도를 구역(Grid) 단위로 분할해 Redis 캐싱 키를 설계, 동일 구역 요청은 외부 API 호출 없이 캐시 반환
- **운영**: Prometheus, Grafana, Loki, Promtail 기반 로깅·모니터링 환경 구축

### **메아리** - MSA 기반 실시간 교육 플랫폼
`Spring Boot` `WebSocket` `Kafka` `Redis` `Docker` `Jenkins` `2025.07-08`

SSAFY에서 5주간 진행한 교육 기부 플랫폼으로, 실시간 채팅 시스템과 마이크로서비스·CI/CD 인프라를 담당
- **성과**: REST 폴링을 WebSocket으로 전환하고 Fetch Join을 적용하여 응답시간 70% 단축, 불필요한 요청 90% 감소
- **성과**: WAS와 WebSocket 서버를 분리하고 Kafka 비동기 메시지 구조를 도입해 장애 전파를 차단 (메시지 유실 방지를 위해 Redis Pub/Sub 대신 Kafka 채택)
- **성과**: Jenkins 기반 자동 배포·롤백 파이프라인으로 배포 시간 30분 → 5분

### **귀위비** - AWS 경진대회 1위 수상작
`Spring Boot` `AWS RDS` `AWS Lambda` `AWS Bedrock` `2024.06`

생활용품 교체주기 알림 서비스로 2일 해커톤에서 완성도 높은 MVP 개발
- **성과**: Spring 서버에서 Lambda 호출을 비동기 처리로 최적화하여 물품 등록 시간 50% 단축 (6초→3초)

### **메타버스 플랫폼 쇼핑몰** - 기업 연계 프로젝트
`Spring Boot` `AWS` `JPA` `2024.09-12`

3D 가상공간 내 패션 커머스 키오스크 시스템
- **협업**: 심스리얼리티와 애자일 방식으로 매주 피드백을 받으며 실제 운용 가능한 시스템 구축

### **INFO.M** - SW 경진대회 본선진출
`AWS RDS` `AWS Lambda` `2024.07-08`

대학교 공지사항 등 정보 알림 서비스로 백엔드 파트의 데이터 수집과 서버리스 인프라 구축 담당
- **성과**: 비용 효율적인 Lambda 스케줄링으로 대용량 등록 처리

<br>

<details>
<summary><b>전체 프로젝트 목록 보기</b></summary>

| 프로젝트 | 설명 | 기간 | 역할 | 기술스택 | 링크 |
|---------|------|------|------|----------|------|
| **Meethub** | 멀티 영상 회의 요약 B2B 솔루션 | 2025.10-11 | BE, Infra | Spring Boot, MySQL, Redis, Docker, Jenkins, Prometheus, Grafana | Private |
| **틔움** | 주말 농장 관리 서비스 | 2025.08-09 | BE, Infra | Spring Boot, MySQL, Redis, Docker, Prometheus, Grafana, Loki | Private |
| **메아리** | 교육 기부 플랫폼 | 2025.07-08 | BE, Infra | Spring Boot, AWS EC2, AWS S3, MySQL, Redis, Kafka, Docker, Jenkins | Private |
| **Trippy** | 여행 플래너 서비스 | 2025.05 | Full Stack | Spring Boot, MySQL, Vue.js | Private |
| **메타버스 쇼핑몰** | 3D 가상 패션 서비스 | 2024.09-12 | BE, QA | Spring Boot, AWS | Private |
| **Busan.zip** | 부산 관광/정착 서비스 | 2024.10 | BE, Infra | Spring Boot, AWS, MySQL, Python | [GitHub](https://github.com/orgs/dive-2024-busanzip/repositories) |
| **INFO.M** | 학교 정보 알리미 | 2024.07-08 | BE, Infra | AWS Lambda | Private |
| **귀위비** | 생활용품 알림 서비스 | 2024.06 | BE, Infra | Spring Boot, AWS Bedrock, AWS Lambda | Private |
| **리뷰캔버스** | 서드파티 리뷰 시스템 | 2024.03-06 | BE | Spring Boot, MySQL | Private |
| **AMS** | 학원 성적 관리 시스템 | 2023.03-07 | Full Stack | Spring Boot, React, Tailwind | [GitHub](https://github.com/Gyulguma/AMS) |
| **GetIT** | 전자기기 추천 서비스 | 2022.03-08 | BE | Spring Boot, AWS, Redis | [GitHub](https://github.com/UMC-GetIT/GetIT-server) |

</details>

---

## 🛠 Tech Stack
**Backend**       : `Java` `Spring Boot` `Spring Security` `JPA` `MSA` <br>
**Infra & Cloud** : `AWS` `Docker` `Kafka` `Jenkins` `Nginx` <br>
**Database**      : `MySQL` `Redis` <br>
**Monitoring**    : `Prometheus` `Grafana` `Loki` <br>
**Collaboration** : `Git` `Jira` `Slack` <br>

---

## 🏆 Awards

- SSAFY 자율 프로젝트(기업연계) 우수상 - Meethub (2025.11)
- SSAFY 특화 프로젝트(빅데이터 추천) 우수상 - 틔움 (2025)
- AWS 역량강화캠프 해커톤 1위 (2024.06)
- ZEPETO World Jam Fall 2023 'Best Technical Implementation' 수상 (2023.11)

---

## 📚 Education & Certificates

**삼성 청년 SW AI 아카데미(SSAFY) 13기 수료 (상위 30%)** `2025.01 ~ 2025.12`  
**2024 벤처 스타트업 아카데미 (SW/컨텐츠분야) 수료** `2024.03 ~ 2025.02`  
**UMC 2기 백엔드 트랙 수료** `2022.03 ~ 2022.08`  
**정보처리기사** `2024.06` · **OPIc IM1** `2026.03`

---

<div align="center">

*"기술로 문제를 해결하고, 사용자에게 가치를 전달하는 개발자가 되겠습니다."*

</div>

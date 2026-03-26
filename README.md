# 🛠 IaC 기반 온프레미스 인프라 자동화 구축

## 📌 프로젝트 개요
Ansible을 활용하여 DNS, WEB, DB, Load Balancer, Monitoring 환경을 자동화한  
온프레미스 인프라 구축 프로젝트입니다.

Role 기반 구조를 통해 인프라를 모듈화하고,  
Playbook을 활용하여 전체 서버를 일괄적으로 구성할 수 있도록 설계했습니다.

---

## 🏗 아키텍처
- DNS / WEB / DB / LB / Monitoring 구조
- Ansible Inventory 기반 서버 그룹 관리
- Role 기반 자동화 구성
- 서비스 간 연동을 고려한 3-Tier 구조

---

## 🛠 Tech Stack
- **OS**: Linux (CentOS / Rocky Linux)
- **IaC**: Ansible (Role, Playbook, Inventory)
- **Web/WAS**: Apache, Tomcat, mod_ssl, mod_proxy
- **Infra**: HAProxy, NFS, MariaDB
- **Monitoring**: Prometheus, Grafana, Loki
- **Network/Security**: firewalld, HTTP/HTTPS

---

## 👥 역할 분담

| 파트 | 담당 | 주요 역할 |
|------|------|-----------|
| Monitoring | 이지영 | Prometheus, Grafana 기반 모니터링 구축 |
| FTP & MAIL | 정구현 | FTP / Mail 서버 구축 및 서비스 설정 |
| WEB | 노영주 | Apache + Tomcat 기반 WEB/WAS 자동화 구축 |
| DB | 남소현 | MariaDB 설치 및 DB 환경 구성 |
| NTP | 김자윤 | NTP 서버 구축 및 시간 동기화 설정 |
| WEB 이중화 | 이승화 | HAProxy 기반 WEB 이중화 및 로드밸런싱 |
| DNS | 김영성 | 내부 DNS 서버 구축 및 도메인 관리 |

---

## 👨‍💻 담당 역할 (WEB)

- Apache + Tomcat 기반 WEB/WAS 환경 자동화 구축
- Reverse Proxy 및 AJP Connector를 활용한 Apache–Tomcat 연동 구성
- VirtualHost 기반 도메인 설정
- firewalld를 통한 포트(80, 443, 8080) 제어
- Tomcat systemd 서비스 등록 및 자동 실행 구성

---

## ⚙️ 주요 구현 내용

- Ansible Role 기반 구조 설계
- DNS / WEB / DB / LB / Monitoring 서버 자동화
- Playbook을 통한 일괄 배포 및 서버 구성
- 서비스 간 연동 구조 설계 (WEB ↔ DB ↔ LB)

---

## 🚀 실행 방법

```bash
ansible-playbook playbook.yml

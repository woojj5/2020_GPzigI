# GP지기

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![PyTorch](https://img.shields.io/badge/pytorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
---

**2020.06 작품 - 전진우, 신찬엽**

한 번의 로그인을 통한 잔여학점 분석기

![image](https://user-images.githubusercontent.com/54899906/121851316-ecca5100-cd28-11eb-89a1-9d062eae09d5.png)

---

## 구성 파일 설명

- **app.py** : Flask 기반 웹 서비스 구현
- **saves.ipynb** : 웹 크롤링, 잔여학점 계산 작업 후 결과값을 리턴
- **counter.py** : 접속자 수 카운터

---
## 역할 분담

| 이름 | 주요 역할 |
| :-- | :-- |
| 신찬엽 | 웹 스크래핑 구현, 웹 구현 보조 |
| 전진우 | 프로젝트 기획, 설계, - 기본적인 프로젝트 구조 기획, selenium을 이용한 웹 스크래핑 구현 보조,  웹 구현, 클라우드를 이용한 프로젝트 배포|
---


## 사용한 Tools & Library

- **웹 크롤링** : Selenium
- **잔여학점 계산** : Python
- **웹사이트 구현** : Flask
- **배포**  
  - **서버 환경** : Ubuntu(Linux)
  - **웹 서버** : Nginx (역방향 프록시 및 정적 파일 제공)
  - **클라우드 플랫폼** : AWS EC2 (가상 서버 인스턴스)
  - **배포 방식**  
    - Nginx와 Flask(Gunicorn/WSGI)를 연동해 웹 서비스를 배포
    - AWS EC2 인스턴스에 Ubuntu 운영체제를 설치하여 서버 구축
    - 외부 접속을 위해 적절한 포트(예: 80, 443)와 보안 그룹 설정 적용

---

## 참고 이미지

![ㅋㅌㅊㅋㅌㅊㅋㅌㅊㅋㅌㅊ](https://github.com/user-attachments/assets/e8972f53-7bc8-4bf0-af3c-0cded6e08249)

## 배포 방식 상세

1. **AWS EC2 인스턴스 생성**
   - Ubuntu 운영체제 선택
   - 필요한 포트(80, 443 등) 개방 및 보안 그룹 설정

2. **프로젝트 코드 업로드**
   - Git 또는 SCP를 통해 서버에 코드 배포

3. **Python 및 라이브러리 설치**
   - `python3`, `pip`, `virtualenv` 등 설치
   - 프로젝트 의존성 패키지 설치

4. **Nginx 설치 및 설정**
   - Nginx 설치: `sudo apt-get install nginx`
   - `/etc/nginx/sites-available` 및 `/etc/nginx/sites-enabled`에 서버 블록 설정
   - 예시:
     ```
     server {
         listen 80;
         server_name your-domain.com;

         location / {
             proxy_pass http://127.0.0.1:8000;
             proxy_set_header Host $host;
             proxy_set_header X-Real-IP $remote_addr;
         }
     }
     ```

5. **Flask 앱 실행**
   - Gunicorn 또는 uWSGI를 사용해 Flask 앱 실행
   - 예시: `gunicorn -w 4 -b 127.0.0.1:8000 app:app`

6. **서비스 자동화**
   - systemd 또는 supervisor로 서비스 등록 및 자동 실행 설정

# GP지기

**2020.06 작품 - 전진우, 신찬엽**

한 번의 로그인을 통한 잔여학점 분석기

![image](https://user-images.githubusercontent.com/54899906/121851316-ecca5100-cd28-11eb-89a1-9d062eae09d5.png)

---

## 구성 파일 설명

- **app.py** : Flask 기반 웹 서비스 구현
- **saves.ipynb** : 웹 크롤링, 잔여학점 계산 작업 후 결과값을 리턴
- **counter.py** : 접속자 수 카운터

---

## 나의 역할

- 기본적인 프로젝트 구조 기획
- selenium을 이용한 크롤링 구현 보조
- 웹 구현
- 클라우드를 이용한 프로젝트 배포

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

※ 두 번째 이미지는 정상적으로 불러와지지 않을 수 있습니다.

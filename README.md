# GP지기

2020.06 작품 - 신찬엽 외 1명

한번의 로그인을 통한 잔여학점 분석기

![image](https://user-images.githubusercontent.com/54899906/121851316-ecca5100-cd28-11eb-89a1-9d062eae09d5.png)

![image](https://user-images.githubusercontent.com/54899906/121851368-f9e74000-cd28-11eb-8a12-222e484a16e9.png)

## 구성파일 설명

app.py : flask 웹 구현

saves.ipynb : 웹 크롤링, 잔여학점 계산 작업 후 결과값을 리턴

counter.py : 접속자 수 카운터

## 나의 역할
- selenium을 이용한 크롤링 & 계산 알고리즘 작성
- 웹 구현 보조
- 접속자 수 카운터 추가

## 사용한 tools & library

웹 크롤링 : Selenium

잔여학점 계산 : Python

웹사이트 구현 : Flask

배포 : Nginx, AWS(ubuntu)

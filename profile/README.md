## RUUniv (대학생 인증 Third Party API)

---

![re1](https://github.com/user-attachments/assets/55364e4f-f50d-4756-8171-b54b9e25bb1b)

### 링크

- 🔥[Site](http://ruuniv.xyz)

### 개발기간

- (2024 / 06 / 22 ~ 배포중)

### 기여도 (개인 프로젝트)

- BE : 100%
- FE : 100%

### 주요 기능

- 이메일을 통한 대학생 인증
- Api Key 관리 기능

---

## 기술 스택

- Java , Spring Boot
- JavaScript , Nest Js
- Spring Cloud
- AWS , Docker , Kafka

---

## 마이크로 서비스 설명

### Account Server

- 사용자 계정을 관리한다

### Statistics Server

- Verification Server에서 로그를 수집하고 , 통계를 제공한다

### Verification Server

- 대학생 인증을 담당한다

---

## ERD

<img width="705" alt="re2" src="https://github.com/user-attachments/assets/9d6ae2b0-7544-4371-b4ca-1462a3c32863">


## 로그 데이터 형식

```jsx
{
	"method" : "POST",
	"api" : "GET_VERIFIED_STUDENT",
	"apiKey" : "1111-4afs-zxvd-zzzz"
	"status" : 200
}
```

## 아키텍쳐

<img width="994" alt="re3" src="https://github.com/user-attachments/assets/8181596c-2a3c-4627-a6c4-cb256cb816e0">


## Version

- 1.0 - 배포 (07/01)
- 1.1 - API 키 관리자 기능 추가 (인증 유저 조회 , 생성 , 삭제) (07/05)
- 1.2 - 학생 인증 도메인은 Internal Server Error를 제외 항상 200을 반환 및 BaseResponse를 도입하고 , isSuccess Flag를 통해 성공여부를 판단하게 변경 (8/5)
- 1.3 - Monolithic → MSA 전환 및 Statistics 서비스 구현 (8/18)

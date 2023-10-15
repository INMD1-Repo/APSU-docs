---
layout: default
title: Auth Api
parent: Dev Api
nav_order: 1
---

# Auth Api
사용자 인증과 사용자 생성 API입니다.

## Login

### Get: /api/auth/local
#### Header
```json
    {
        "headers": {
            "Content-Type": "application/json",
        },
    }
```
#### Data
```json
    {
        "identifier": "this.id", //String
        "password": "this.pw", //String
    }
```
### Return 200 OK
```json
{
    "jwt": "example token", //인증토큰 String
    "user": {
        "id": 9, // 생성순서(라고함) int
        "username": "test",// ID String
        "email": "test@test.com", // 이메일 String
        "provider": "local", 
        "createdAt": "2023-07-28T17:30:34.946Z", // 생성시각 String
        "updatedAt": "2023-09-23T14:51:20.887Z",// 업데이트 시각 String
        "belong": "N포대", //포(중대) String
        "specialty": "전포",// 주특기 String
        "Classes": "상등병",// 계급 String
        "korea_name": "아무개",// 이름 String
        "showcode": "Veterans", // 타입 String
        "face_image_url": "/uploads/???.png", // 프로필 사진 주소 String
        "birthday": "1942-01-03" // 생일(YYYY-MM-DD) String
    }
}
```


## Sing up

### POST: /api/auth/local/register
#### Header
```json
    {
        "headers": {
        "Content-Type": "application/json",
        },
    }
```

#### Data
```json
{
    "class": "this.Class", // 계급 String
    "username": "this.sing_id", // 아이디 String
    "belong": "this.belong", //포(중대) String
    "specialty": "this.specialty", // 주특기 String
    "birthday": "this.birthday",// 생일(YYYY-MM-DD) String
    "korea_name": "this.si_name",// 이름 String
    "password": "this.sing_pw", // 비밀번호 String
    "email": "this.si_email", // 이메일 String
    "showcode": "Veterans", // 타입 String 
}
```

### Return 200 OK
```json
{
    "jwt": "example token", //발급된 String
    "user": {
        "id": 9, // 생성순서(라고함) int
        "username": "test",// ID String
        "email": "test@test.com", // 이메일 String
        "provider": "local", 
        "createdAt": "2023-07-28T17:30:34.946Z", // 생성시각 String
        "updatedAt": "2023-09-23T14:51:20.887Z",// 업데이트 시각 String
        "belong": "N포대", //포(중대) String
        "specialty": "전포",// 주특기 String
        "Classes": "상등병",// 계급 String
        "korea_name": "아무개",// 이름 String
        "showcode": "Veterans", // 타입 String
        "face_image_url": "/uploads/???.png", // 프로필 사진 주소 String
        "birthday": "1942-01-03" // 생일(YYYY-MM-DD) String
    }
}
```

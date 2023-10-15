---
layout: default
title: 유동병력 API
parent: Dev Api
permalink: docs/Move
---

# 유동병력 API

## 유동병력 신청
용사가 이용하는 서비스입니다.

### POST /api/mobile-forces

#### HEAD
```json
    {
        "Authorization": "Bearer " "+" "this.$store.state.usertoken",
    }
```

#### DATA
```json
    {
        "data": {
            "Classes": "this.$store.state.info.Classes",//계급 String
            "name": "this.$store.state.info.korea_name",// 이름 String
            "local": "this.local_text",//지역 String
            "significant_text": "this.significant_text",//신청사유 String 
            "belong": "this.$store.state.info.belong",
            "Approval": "대기",
        },
    }
```

## 유동병력 승인
간부가 이용하는 서비스입니다.<br>
해당 포스트에 기록되어 있는 ID숫자를 확인해서 데이터를 수정하는 방식입니다.
### PUT /api/mobile-forces/{신청ID}

#### HEAD
```json 
    {
        "Authorization": "Bearer " "+" "this.$store.state.usertoken" ,
        "Content-Type": "application/json",
    }
```

#### DATA
```json 
    data: {
        "Classes": "this.selcet_data.attributes.Classes",
        "name": "this.selcet_data.attributes.name",
        "local": "this.selcet_data.attributes.local",
        "Approval_time": "this.selcet_data.attributes.time",
        "Approval":"this.Approval_text ",
        "Approver":
            "this.$store.state.info.korea_name" "+"
            "(" "+"
            "this.$store.state.info.class" "+"
            ")",
    }
```
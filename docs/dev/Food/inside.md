---
layout: default
title: 내부(inside)
grand_parent: Dev Api
parent: Food Api
---
# 내부(inside)
국방부 오픈소스에서 가지고와서 정제를 거치고 데이터베이스에 저장하기 위해서 사용되는 API입니다.

{: .note }
처음에는 Strapi 관리자 페이지 내부에서 아무데이터를 만들어야 합니다. (값을 수정해서 업데이트 하는 방식)

### PUT /api/food-infos/1

#### Header
```json
    {
        "Content-Type": "application/json"
    }
```

#### DATA
```json
    {
       "food_info": "Object" //정제된 데이터들 
    }
```
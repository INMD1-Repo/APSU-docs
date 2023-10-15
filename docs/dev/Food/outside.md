---
layout: default
title: 외부(outside)
grand_parent: Dev Api
parent: Food Api
---
# 외부(outside)
데이터베이스에서 있는 데이터를 보여주는 Api입니다.

### GET /api/food-infos/

#### Return
```json
{
    "data":[
    {
        "id": 1,
        "attributes":{
            "food_info":[{"meal":[{"cal": null, "info": "조식", "menu":[], //식단표 데이터
            "createdAt": "2023-07-29T15:14:12.046Z",
            "updatedAt": "2023-10-13T15:23:19.603Z",
            "publishedAt": "2023-09-14T11:59:46.137Z"}
            }],
        "meta":{
        "pagination":{"page": 1, "pageSize": 25, "pageCount": 1, "total": 1}
    }
}
```

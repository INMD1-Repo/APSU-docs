---
layout: default
title: Backend Api setup
nav_order: 2
parent: installation
---

# Backend
Api나 데이터를 저장하는 백엔드를 구축을 해봅시다.

## API 기본정보 입력
strapi를 처음 설치하면 아무것도 설정이 안되어 있일래 레포에 있는 파일&폴더를 가지고 와서 적용시킴니다.

1. 클론 받은 프로젝트에서 Backend로 이동 해줌니다.
```
cd Backend
```
2. 아래 커맨드를 입력해서 해당 폴더로 이동합니다.
```
cd src/api
```
3. src/api의 폴더에 있는 폴더&파일을 위에서 만든 프로젝트에서 똑같은 폴더에 복사를 합니다.

# JWT 설정
로그인 보안을 좀더 높이기 JWT를 채택을 했고 적용법은 아래와 같습니다.

1. config 파일로 이동을 해서 새로운 파일`plugins.js`을 생성합니다.
``` js
module.exports = ({ env }) => ({
  'users-permissions': {
    config: {
      jwt: {
        expiresIn: '7d',
      },
    },
  },
});
```

2. 루트 디렉토리에 있는 .env에 이 문장을 추가합니다.
```
JWT_SECRET= `최대한 많은 글자`
```

#### 자료출처
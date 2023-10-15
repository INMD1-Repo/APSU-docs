---
layout: default
title: Frontend installation
parent: installation
nav_order: 4
---

# Frontend installation

1. 터미널에 아래와 같은 커맨드를 입력해서 `Frontend` 폴더로 이동합니다.

```
cd Frontend
```

2. npm 모듈을 설치를 해줌니다.

```
npm install
```

3. .env에서 백엔드 서버에서 설정한 IP나 Url을 작성하고 저장합니다.

```
.env
--------------------------------------------

VUE_APP_ALL=http://localhost:1337 -> 주소 변경

--------------------------------------------
```

4. 서버를 실행합니다

```
npm run serve
```
---
---
layout: default
nav_order: 1
title: Backend installation
parent: installation
---

# Backend installation
Api나 데이터를 저장하는 백엔드를 구축을 해봅시다.

##  strapi설치
저희는 strapi 프레임기반으로 백엔드가 구동됨니다.<br>
그래서 strapi를 기본적으로 설치를 하고 다음 단계로 진행합니다.
 > [strapi](https://docs.strapi.io/) 공식문서에서 보고 설치해도 됨니다.

### NPM 프로젝트 생성

1. 터미널에 아래 커맨드를 입력을 합니다.

```
npx create-strapi-app@latest my-project
# 'npx' runs a command from an npm package
# 'create-strapi-app' is the Strapi package
# '@latest' indicates that the latest version of Strapi is used
# 'my-project'는 프로젝트폴더 이길래 이름 변경 가능합니다.
```

2. 설치타입을 `Custom (manual settings)`로 설정합니다
> 빠르게 설치를 하고 싶으면 Quickstart (recommended) 하시고 다음 단계로 넘어가십시오.<br>
> *Quickstart (recommended)시 따로 데이터베이스 설정 불가

3. 계속 진행을 하면 데이터베이스를 선택 해라고 하는데 `mysql로` 설정합니다

```
? Choose your default database client (Use arrow keys)
  sqlite
  postgres
❯ mysql
```

그다음 데이터베이스의 기본적 정보를 입력합니다.

```
? Database name:
? Host:
? Port: 
? Username: 
? Password:
? Enable SSL connection: No
```

4. 그리고 생성된 프로젝트 폴더로 이동해서 터미널에 아래 커맨드를 입력합니다
```
npm run devlop
```
터미널에 뜬 URl로 들어가서 마무리 해주시면 됨니다.
> [strapi user Guide](https://docs.strapi.io/user-docs/intro) 참고하면 이해하기 쉽습니다


---

#### 자료출처

strapi dev docs: https://docs.strapi.io/dev-docs/intro <br>
strapi user docs: https://docs.strapi.io/user-docs/intro
---
layout: default
title: Backend_food Get api
parent: installation
nav_order: 3
---
# Backend_food Get api
공공테이터포털에서 가져온 정보를 이용해서 식단표 데이터로 다시 작성해주는 프로그램 설정입니다.

1. 공공데이터포털에서 해당 부대의 식단정보를 검색합니다.
2. 있을 경우 들어가시면 바로가기 버튼이 있는데 눌려서 새 페이지로 진입합니다.<br>

<center>
<img style="object-fit:fill; height:30vh; width:auto" src="../../../assets/images/vas2fc.jpg"/>
</center>

3. 페이지에 뜬 주소를 `diet_script`파일에 있는 foodget.js에 있는 코드를 아래와 같이 수정해주십시오

```js
    # 위내용생락
    const page = await browser.newPage();
    const client = await page.target().createCDPSession();

    await page.goto("새로운 주소");
    await client.send('Page.setDownloadBehavior', {
        behavior: 'allow',
        downloadPath: downloadPath,})

    # 아래내용 생락
```

4. 서버를 다시 작동시키면 끝입니다.

---

#### 자료출처


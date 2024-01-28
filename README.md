# WMLAlive-QNA

## WMLAlive-QNA Website

- [WMLAlive-QNA](#wmlalive-qna)
  - [WMLAlive-QNA Website](#wmlalive-qna-website)
    - [현재](#현재)
    - [설계](#설계)
    - [동작](#동작)
    - [구현](#구현)

### 현재
- socket.io 적용되어 있는 상태
- 하위 폴더(notion-app-database-query)는 Input기능만 있고, local로 올려주면, Vercel 배포 가능
  
### 설계 
- 간단한 데이터를 기록하기 위해 Notion Table을 DB로 사용하기 ✅
  - 초기로딩시 DB에서 값 불러오기 Query a database in Notion API
  - 값 입력시, DB업로드 Create a page in Notion API 
- 여러대의 아이패드 이용을 위해 데이터 동기화 ✅ 
- Notion Table에서 값(열) 삭제시 웹사이트에서 값 삭제(예정)🚧 🚧
- 배포하기(예정) 🚧🚧
- `github-secret` 또는 `.env` 숨김포함 배포방법 찾아보기(예정)🚧 🚧

### 동작 
  `$ npm start`
  - .env
  
### 구현

- NOTION API **[Create a page](https://developers.notion.com/reference/create-a-database)**
  - Put input values in website to Notion DB(table) 
  - Reference Video **[Using Notion API With React to Create a Notion Database](https://www.youtube.com/watch?v=WbekTHVISh0&feature=emb_title)**

<br />

- NOTION API **[Query a database](https://developers.notion.com/reference/post-database-query)**
  - Take values from Notion DB(table)
  - Reference-1. **[Node express query Notion database](https://daily-dev-tips.com/posts/node-express-query-notion-database/)**
  - Reference-2. **[rebelchris/notion-app](https://github.com/rebelchris/notion-app/tree/database-query)**

<br />

- Socket.io **[Get Started](https://socket.io/get-started/chat)**
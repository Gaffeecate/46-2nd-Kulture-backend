# Project Kulture

![waving](https://capsule-render.vercel.app/api?type=waving&height=200&fontAlignY=40&text=kulture&color=gradient)

#### \*[KREAM](https://kream.co.kr/) 웹사이트를 모델링한 프로젝트입니다.

## 1. 개발 기간 및 인원

- 개발 기간 : 2023/06/16 ~ 2023/06/29
- 개발 인원 : 프론트엔드 3명 , 백엔드 2명
  - Product Manager: 조혜진(F)
  - Project Manager: 김혜중(B)
  - Teammates: 김민정(F), 김지연(F), 하진희(B)
- 깃헙 레포지토리
  - [Frontend](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend)
  - [Backend](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-backend)


## 2.서비스 소개
- 서비스명 : kulture
- 판매상품 : 공연 예술 티켓
- 고객 : 문화생활 및 기부를 통한 사회적 가치 창출에 관심있는 2030
- 기획의도
	- 경매/즉시 구매 두 가지 형태로 공연예술 티켓을 구매할 수 있는 플랫폼
	- 티켓 구매 금액의 10%는 저소득층의 문화생활 지원사업에 자동으로 기부


## 3. 구현 기능
|기능|
|---|
|회원가입/로그인/로그아웃 (카카오 API)
|회원정보, 입찰내역, 주문내역 조회
|회원정보 수정| 
|상품 리스트 - 필터링&정렬 (Calendar 라이브러리)
|상품 카드 컴포넌트|
|상품 상세 페이지(Google Maps API, Chart 라이브러리)
|경매 입찰 모달, 즉시 구매 모달
|위시리스트 추가/삭제/조회|
|입찰 마감 타이머, 잔여 티켓 수량 조회|
|포인트 충전 (카카오페이 API)|
|포인트로 상품 결제|
|결제 완료 티켓 QR코드 조회|
|리뷰 업로드 & 조회|
|리뷰 삭제|
|스크롤 최상단 이동 버튼 컴포넌트|

## 4. 핵심기능 상세
1. 콘서트 티켓이나 이벤트 참가권을 경매 방식으로 판매하는 기획의도를 가지고 있음
2. 입찰 과정에서 사용자는 특정 이벤트에 대해서, 특정 가격을 제시한다. 
그 거래는 실제 화폐단위가 아닌, 해당 사이트에서 사용 가능한 이벤트 토큰으로 거래된다.
3. 다중입찰: 한 사용자는 한 이벤트, 즉 하나의 경매물품에 대하여 여러번 가격제시를 할 수도 있고, 여러 이벤트에도 입찰을 할 수가 있다. 

## 4. Database
- 1:N 관계: (users, bid), (events, bid), (users, orders), (users, event_token_history), (categories, events), (countries, events), (age_ranges, events) - 한 사용자가 여러 입찰, 주문을 할수 있고 여러 토큰 거래내역을 가질 수 있다. 또한 카테고리, 국가, 연령범위에 여러 이벤트가 속할 수 있다.
- N:N 관계: 
1. (users - wishlists - events) : 한 이벤트는 여러 사용자의 위시리스트에 들어가 있을수 있고, 한 유저는 여러 이벤트를 위시리스트에 담을 수 있다.
2. (users - reviews - events) : 한 이벤트는 여러 사용자의 리뷰에 들어가 있을수 있고, 한 사용자는 여러 이벤트에 대한 리뷰를 작성할 수 있다.
3. (users - bid - events) : 한 이벤트는 여러 사용자의 입찰 리스트에 들어가 있을 수 있고, 한 사용자는 여러 이벤트에 대한 입찰을 할 수 있다.
4. (order - order_events - events): 한번의 주문에 여러 이벤트가 포함될 수 있고, 한 이벤트는 여러 주문에 포함 될 수 있다.

<p align="left">
  <img src="https://raw.githubusercontent.com/wecode-bootcamp-korea/46-2nd-Kulture-backend/b964bbe5b5c64017a357c8983b372aa3da6163d8/Kulture%20ERD.png" alt="ERD Diagram" width="800"/>
</p>

## 5. 기술스택
### Frontend
|JavaScript|React|Styled-Components|esLint|Prettier|
|:---:|:---:|:---:|:---:|:---:|
| <img src="https://techstack-generator.vercel.app/js-icon.svg" alt="icon" width="65" height="65" /> | <img src="https://techstack-generator.vercel.app/react-icon.svg" alt="icon" width="65" height="65" /> | <img src="https://www.styled-components.com/atom.png" width="65" height="65" /></div> | <img src="https://techstack-generator.vercel.app/eslint-icon.svg" alt="icon" width="65" height="65" /> | <img src="https://techstack-generator.vercel.app/prettier-icon.svg" alt="icon" width="65" height="65" /> |

### Backend

|JavaScript|Node.js|MySQL|
|:---:|:---:|:---:|
| <img src="https://techstack-generator.vercel.app/js-icon.svg" alt="icon" width="65" height="65" /> | <img src="https://techstack-generator.vercel.app/nginx-icon.svg" alt="icon" width="65" height="65" /> | <img src="https://techstack-generator.vercel.app/mysql-icon.svg" alt="icon" width="65" height="65" /> </div> |



## ⚙️ 협업툴

<div>
<img src="https://img.shields.io/badge/Git-F05032?style=flat&logo=Git&logoColor=white"/>
<img src="https://img.shields.io/badge/Slack-4A154B?style=flat&logo=Slack&logoColor=white"/>
<img src="https://img.shields.io/badge/Trello-0052CC?style=flat&logo=Trello&logoColor=white"/>
<img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white"/>
<img src="https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=Figma&logoColor=white"/>
</div>


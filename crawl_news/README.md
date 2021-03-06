##news_crawler

감정 분석을 하기 위한 네이버 뉴스를 크롤링합니다.

#### Description
네이버 뉴스를 
* 연예 (entertain)
* 스포츠 (sports)
* 과학 (science)
* IT (IT)
* 세계 (world)
* 사회 (society)
* 경제 (economy)
* 정치 (politics)

의 항목으로 나누어 크롤링합니다.

실행 순서

1. 각 항목마다 페이지를 돌며 각 뉴스의 URL을 가져 옵니다.
2. 가져온 URL을 보고 기사에 접근해 본문을 가져 옵니다.
3. 기사 본문을 감정분석 한 뒤 감정, URL, 제목, 본문 순서대로 파일에 저장합니다.

URL을 통해 가지고 올 때는 Requests 패키지를 사용 하고, HTML에서 정보를 뽑아낼 때는 BeautifulSoup 패키지를 사용합니다.

특이사항은 다음과 같습니다.
* 연예, 스포츠는 다른 뉴스항목과 다른 구조의 웹 형식을 띄고 있기 때문에 별도의 메소드로 구현 하였습니다.
* 네이버의 IP 블럭을 막기 위해 각 실행마다 0.5초의 딜레이를 주었습니다.
* 모든 뉴스를 크롤링하면 데이터가 많아지므로, 각 항목의 일반 항목을 크롤링 하였습니다.
* @ 문자를 기준으로 그 뒤의 문자들은 버립니다. (언론사 정보등이 포함되는 경우가 많음)

#### Requirement
**Python3**를 통해 실행해야 합니다.

---
layout: post
title: 컴퓨터공학 분야 학회 및 논문
tags: [research, conference]
comments: false
---

컴퓨터공학 (CS) 분야에서는 국제학회를 통해 주요한 연구 성과가 공유된다. 변화의 주기가 짧은 CS 분야에서는 매년 (혹은 2년에 한번씩) 학회를 통해 연구자들이 한자리에 모여 최신 연구 성과를 공유하면서 함께 성장하는 문화가 잘 갖춰진 것 같다. 포스터나 데모와 같은 extended abstract 형태의 연구 뿐만 아니라 분야별 전문가들의 peer review를 통해 선별된 full paper (two-column 8 ~ 12장 정도 분량)에 대한 발표 세션이 메인 트랙을 구성한다. 

연구 분야 별로 다양한 학회가 있다. 좋은 연구가 많이 게재되는 학회들이 있고 상대적으로 그렇지 않은 학회들도 있다. 그렇기 때문에 분야 별로 어떤 학회에서 대체로 좋은 (많이 읽히고 영향력 있는) 연구가 나오는지에 대해 알고 있으면 논문을 찾아볼 때 도움이 된다. 이 글을 통해 이러한 정보를 간단하게 정리해 보려고 한다. 

### 1. 평가 기준
학회의 신뢰도를 판단하기 위해 활용할 수 있는 기준들이 몇 가지 있다. 

#### 1.1. Ranking
다양한 기관에서 학회의 다양한 실적을 바탕으로 ranking을 산정하여 제공한다. 이와 같은 ranking은 절대적이라 할 수는 없지만 분야별 top-tier 학회를 구분하기 위한 데이터로는 적합하다고 할 수 있다. 
- [CORE](http://portal.core.edu.au/conf-ranks/): 호주 정부에서 운영하는 Computing Research & Education 그룹에서 관리하는 CS conference ranking 데이터베이스로 A* (7%), A (19%), B (29%), C (26%), others (17%)로 등급 구분한다. CS 학회 평가 공신력이 높다.
- [CSRankings](https://csrankings.org/): CS 세부 분야별 학교 별 랭킹을 확인할 수 있는 사이트인데 분야별 탑티어 학회 논문 publish 개수를 기준으로 통계를 낸다. 매우 선별적으로 각 분야별로 소수의 학회만을 선정해 놓은 것이 특징이다. (리스트 확인 방법: 링크의 페이지에서 분야 별로 왼쪽의 화살표 버튼을 클릭하면 학회 리스트를 확인할 수 있다. 탑티어 학회도 세분화해서 티어를 구분해 놓은 것으로 보인다. 예를 들어, Operating Systems 분야의 경우 OSDI, SOSP가 리스트의 가장 위에 위치해 있고, 그 아래로 EuroSys, FAST, USENIX ATC가 위치하도록 정리해 놓았다.)
- [Google Scholar Top Publications](https://scholar.google.co.uk/citations?view_op=top_venues&hl=en): CS 뿐만 아니라 여러 도메인에 걸쳐 세부 연구 분야별 top publication venue 리스트를 제공. 학회 뿐만 아니라 저널도 포함
- [Research.com (Formerly, Guide2Research)](https://research.com/conference-rankings/computer-science/2021) ([개인적 의견] 일반적으로 받아들여지는 기준과 다소 차이를 보이는 랭킹들도 있는 것 같음)

이와 같은 ranking 정보를 통해 관심 분야의 top-tier 학회 목록을 파악하는 것은 연구를 처음 시작할 때 많은 도움이 된다. 
따라서 분야별 top-tier 학회 (최우수 / 우수) 리스트를 따로 정리해 놓은 자료를 활용하는 것도 좋다. 
- [Top Publication Venues in Computer Science (Cornell)](https://www.cs.cornell.edu/andru/csconf.html)
- [KAIST 전산학부 박사 졸업가능 컨퍼런스 리스트](https://cs.kaist.ac.kr/userfiles/file/kaist_soc_conflist.xlsx)
- [서울대 컴퓨터공학과 Top Conference List](https://cse.snu.ac.kr/node/29041)
- [POSTECH 졸업 인정 학술지 및 학술대회 목록](https://cse.postech.ac.kr/%EB%8C%80%ED%95%99%EC%9B%90-%ED%95%99%EC%9C%84%EC%88%98%EC%97%AC-%EC%A3%BC%EC%9A%94%EC%9D%BC%EC%A0%95-%EB%B0%8F-%EC%A1%B8%EC%97%85%EC%9D%B8%EC%A0%95-%ED%95%99%EC%88%A0%EC%A7%80-%EB%B0%8F-%ED%95%99/)
- [한국정보과학회 우수 학술대회 목록](https://www.kiise.or.kr/academy/main/getContent.fa?content_no=74&MENU_ID=130300)
- [CCF Recommended List of International Conferences](https://www.ccf.org.cn/en/Bulletin/2019-05-13/663884.shtml)

#### 1.2. 인용 수 관련
- 학회에 대한 `H5-index`: 지난 **5년** 동안 해당 학회에서 publish 된 논문 중 **최소 n 편이 n번 이상 인용**된 n의 최대값을 `H5-index` 라고 한다. 예를 들면, 어떤 학회에서 지난 5년간 논문 5편이 publish 되었는데 인용 횟수가 각각 [5, 3, 2, 0, 0]이라면 해당 학회의 `H5-index`는 2이다. 인용이 3번 이상된 것은 2편밖에 안되므로 3이 될 수 없다. 
    > H-index 개념은 researcher 개인의 연구 성과를 표현하는 지표로도 널리 활용되고 있다. 즉, 어떤 연구자가 publish 한 논문 중 최소 n 편이 n번 이상 인용된 n의 최대값을 해당 연구자의 h-index라고 한다. 
- Impact factor (저널): 저널의 실적을 표현하는 지표로 지난 2년 동안 해당 저널에 게재된 논문의 평균 인용 횟수 (전체 인용 횟수 / 전체 논문 갯수)를 의미한다.

#### 1.3. (참고) 몇 해 동안 이어져 온 학회인지
- CS 분야는 역사가 상대적으로 짧은 편이지만 그 가운데에서도 오랜 기간 지속되는 학회들은 어느 정도 신뢰성을 보장한다고 할 수 있다. 
  - 예: SOSP: 1967~ (computer systems) / ISCA: 1973~ (컴퓨터 구조) / VLDB, SIGMOD: 1975~ (DB) / NeurIPS: 1987~ (AI) / INFOCOM: 1979~ (Network) / CHI: 1983~ (HCI) 등은 각자의 분야에서 수십년에 걸쳐 성공적으로 운영되고 영향력 있는 논문이 발표되는 top-tier 학회이다. 
- 전통적인 computing 분야와 차별화되는 새로운 패러다임이 등장하면 이에 맞춰 새로운 학회들이 생겨나는데, 해당 분야가 학계 / 산업에서 많은 관심을 끌고 단기간에 주목할만한 성과가 나타나면 이와 같이 오래 되지 않은 학회들도 높은 명성을 얻게 되는 경우도 있다. 
  - 예 1: [MLSys] Conference on Machine Learning and Systems (MLSys)는 Systems for maching learning / machine learning for systems 등 머신러닝과 시스템의 intersection에 대한 연구가 큰 주목을 받으면서 생긴 학회이다 (2018년에 [SysML](https://mlsys.org/Conferences/2018/) 이름으로 시작되어서 2020년부터 현재 이름으로 불림). 이제 (2023년 기준) 6번째 학회를 개최하는 비교적 신생 학회이지만 세계적으로 주목받는 교수진이 committee로 참여하고 좋은 연구들이 다수 발표되면서 단기간에 주목 받는 학회가 되었다. 
  - 예 2: [SoCC] Cloud computing 분야의 ACM Symposium on Cloud Computing (SoCC)와 같은 학회는 2010년에 시작됐지만 분야의 빠른 성장과 함께 짧은 시간에 주목 받는 학회가 되었다. 

#### 1.4. (참고) Acceptance rate
학회에 submit 된 논문 수 대비 accept 된 논문 비율도 참고해볼 수 있다. 

### 2. 검색 방법
다음과 같은 사이트 (third-party services)에서 다양한 기준으로 (연구 키워드 / conference venue / 저자 / 논문 제목 / 발행 연도 등) 논문을 검색할 수 있다. 
- [Google Scholar](https://scholar.google.com/)
- [DBLP](https://dblp.org/): 개인적으로 많이 사용하는 검색 서비스이다. CS 분야 학회 / 저널에 특화되어 있고 publication provider인 IEEE / ACM 등의 공식적인 논문 업데이트와의 싱크가 정확하고 빠른 편이다. 
- [ResearchGate](https://www.researchgate.net/)
- [Semantic Scholar](https://www.semanticscholar.org/)

논문들이 공식적으로 publish 되는 공간으로는 대표적으로 다음과 같은 웹사이트들이 있다. 
- [ACM Digital Library](https://dl.acm.org/)
- [USENIX](https://www.usenix.org/) -- open access; computer systems (OSDI, ATC, FAST), networking (NSDI), security (Usenix-Security, NDSS) 분야 top-tier 학회 / 워크샵 (HotOS, HotCloud) 위주
- [IEEE Explorer](https://ieeexplore.ieee.org/Xplore/home.jsp)
- [Springer](https://www.springer.com/kr/computer-science)

또한, [arXiv](https://arxiv.org/)와 같은 open-access 서비스도 많이 활용된다. 특정 학회나 저널에 accept 되지 않은 논문도 등록할 수 있고 누구나 무료로 등록된 논문을 읽을 수 있다. 공식적으로 리뷰 과정을 거쳐서 publish 하기 전에 pre-print 형태로 arXiv에 올리는 경우가 많아지고 있다. 

### 3. 논문 제출 일정 확인하기
논문 제출 일정을 확인할 수 있는 사이트
- [WikiCFP](http://www.wikicfp.com/cfp/call?conference=computer%20science)
- [Conference Partner (Myhuiban)](https://www.myhuiban.com/)
- [ACM upcoming submission deadline](https://www.acm.org/conferences/upcoming-submission-deadlines)

특정 분야에 한정하여 리스트 정리한 사이트
- [Systems](https://dants.github.io/index_sysvenues_deadline.html)
- [AI](https://jackietseng.github.io/conference_call_for_paper/conferences.html)

### 4. 정리
CS 분야의 학회를 평가하는 기준이 될 수 있는 몇가지 정보와 논문을 검색하기 위한 방법들을 정리해 보았다. CS 분야의 논문 읽기를 시작해 보고 싶은데 어디서 무엇을 봐야할지 잘 모르는 분들에게 도움이 되었으면 좋겠다. 
# [인공지능기초]텍스트 마이닝을 통한 2024 미국 대선 사후 분석 

<br>

> [!IMPORTANT]
> ## 프로젝트 세부 목표
> 1. 후보자에 대해 각 매체(토론/뉴스/SNS)별로 어떤 단어들이 쓰였는가?
> 2. 각 메체(토론/뉴스/SNS)에서 후보자들과 관련있는 단어들은 무엇일까?
> 3. 후보자의 언급 빈도수로 선거결과를 예측할 수 있을까?
> 4. 후보자들에 대한 감성은 어떻게 나타날까?
> 5. 후보자들에 대한 감성으로 선거 결과를 예측 할 수 있을까? 

<br>

> [!NOTE]
> ## 계획 및 진행상황
> **1.토론 데이터**
> - [X] ~크롤링~
> - [ ] 토론에서 각 후보자의 발언 수 비교
> - [ ] 후보자의 발안 데이터 TF-IDF 기반 워드클라우드
> - [ ] LDA를 통한 토픽 분석
> 
> **2.뉴스 데이터**
> - [ ] 크롤링(FOX✔  CBS✔ POLITICO✖ NPR✖ Reuter✖ AP✖ ABC✖ PBS✖)
> - [ ] 편향지수를 가지고 정규화 및 가중치 반영
> - [ ] 빈도수 기반 워드클라우드(표제어 및 불용어 처리 필요🏃‍♀️)
> - [ ] TF-IDF 키워드 분석
> - [ ] 후보자 언급 빈도 분석(FOX, CBS 외 다른 언론사 아직 안함🏃‍♀️)
> 
> **3.SNS 데이터**
> - [ ] 크롤링(youtube🏃‍♀️ instagram✖ facebook✖ truth_social✖) 
> - [ ] TF-IDF 기반 워드클라우드
> - [ ] VADER 기반 감성분석
> - [ ] LLM 기반 감성분석
> - [ ] LSTM 감성 점수 예측
> 
> **4.통합 데이터 (토론 + 뉴스 + SNS)**
> - [ ] Word2Vec


<br>


## 프로젝트 구조

```
📦 
├─ 0.Datasets
│  ├─ 1.대선토론
│  │  └─ trump_harris_debate.json
│  ├─ 2.뉴스
│  │  ├─ cbs
│  │  │  ├─ cbs_news_content.json
│  │  │  └─ cbs_news_url_title.json
│  │  └─ fox
│  │     ├─ fox_news_content.json
│  │     └─ fox_news_url_title.json
│  └─ 3.SNS
│     └─ youtube
│        ├─ harris_youtube_url_title_date.json
│        └─ trump_youtube_url_title_date.json
│
├─ 1.Data_Collection
│  ├─ 1.대선토론
│  │  └─ trump_harris_debate_crawler.ipynb
│  ├─ 2.뉴스
│  │  ├─ cbs
│  │  │  ├─ cbs_news_content_crawler.ipynb
│  │  │  └─ cbs_news_url_title_crawler.ipynb
│  │  └─ fox
│  │     ├─ fox_news_content_crawler.ipynb
│  │     └─ fox_news_url_title_crawler.ipynb
│  └─ 3.SNS
│     └─ youtube
│        ├─ harris_youtube_url_title_date_crawler.ipynb
│        └─ trump_youtube_url_title_date_crawler.ipynb
│
├─ 2.Data_Analysis
│  └─ 2.뉴스
│     └─ 뉴스_빈도분석.ipynb
│
└─ README.md
```

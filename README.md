# [인공지능기초]텍스트 마이닝을 통한 2024 미국 대선 사후 분석 

<br>

> [!NOTE]
> ## 프로젝트 세부 목표
> 1. 후보자에 대해 각 매체(토론/뉴스/유튜브 댓글)별로 어떤 단어들이 쓰였는가?
> 2. 전체 매체(토론/뉴스/유튜브 댓글)에서 후보자들과 관련있는 단어들은 무엇일까?
> 3. 후보자의 언급 빈도수로 선거결과를 예측할 수 있을까?
> 4. 후보자들에 대한 감성은 어떻게 나타날까?
> 5. 후보자들에 대한 감성으로 선거 결과를 예측 할 수 있을까? 

<br>

> [!IMPORTANT]
> ## 계획 및 진행상황
> **1.토론 데이터**
> - [X] ~크롤링~
> - [X] ~전처리(토큰화, 불용어 제거, 표제어 추출 등)~
> - [X] ~토론에서 각 후보자의 발언 수 비교~
> - [X] ~후보자의 발언 데이터 TF-IDF 기반 워드클라우드~
> - [X] ~LDA를 통한 토픽 분석~
> 
> **2.뉴스 데이터**
> - [X] ~크롤링~
> - [ ] 편향지수를 가지고 정규화 및 가중치 반영
> - [ ] 빈도수 기반 워드클라우드(표제어 및 불용어 처리 필요🏃‍♀️)
> - [ ] TF-IDF 키워드 분석
> - [ ] 후보자 언급 빈도 분석
> 
> **3.유튜브 댓글 데이터**
> - [X] ~크롤링~
> - [ ] 샘플링을 통한 편향 조정
> - [ ] TF-IDF 기반 워드클라우드
> - [ ] VADER 기반 감성분석
> - [ ] LLM 기반 감성분석
> - [ ] LSTM 감성 점수 예측
> 
> **4.통합 데이터 (토론 + 뉴스 + 유튜브 댓글)**
> - [ ] Word2Vec


<br>


## 프로젝트 구조

```
📦 
├─ 🗂️1.Data_Collection
│  ├─ 1.Data_Collector
│  │  ├─ 1.대선토론
│  │  │  └─ 💻trump_harris_debate_crawler.ipynb
│  │  ├─ 2.뉴스
│  │  │  ├─ cbs
│  │  │  │  ├─ 💻cbs_news_content_crawler.ipynb
│  │  │  │  └─ 💻cbs_news_url_title_crawler.ipynb
│  │  │  └─ fox
│  │  │     ├─ 💻fox_news_content_crawler.ipynb
│  │  │     └─ 💻fox_news_url_title_crawler.ipynb
│  │  └─ 3.유튜브 댓글
│  │     ├─ 💻harris_youtube_comment_api_crawler.ipynb
│  │     ├─ 💻harris_youtube_comment_commentdate_likes_crawler.ipynb
│  │     ├─ 💻harris_youtube_url_title_date_crawler.ipynb
│  │     ├─ 💻trump_youtube_comment_api_crawler.ipynb
│  │     ├─ 💻trump_youtube_comment_commentdate_likes_crawler.ipynb
│  │     └─ 💻trump_youtube_url_title_date_crawler.ipynb
│  └─ 2.Collected_Data
│     ├─ 1.대선토론
│     │  └─ 📄trump_harris_debate.json
│     ├─ 2.뉴스
│     │  ├─ cbs
│     │  │  ├─ 📄cbs_news_content.json
│     │  │  └─ 📄cbs_news_url_title.json
│     │  └─ fox
│     │     ├─ 📄fox_news_content.json
│     │     └─ 📄fox_news_url_title.json
│     └─ 3.유튜브 댓글
│        ├─ 📄harris_youtube_comment.jsonl
│        ├─ 📄harris_youtube_comment_commentdate_likes.jsonl
│        ├─ 📄harris_youtube_url_title_date.json
│        ├─ 📄trump_youtube_comment.jsonl
│        ├─ 📄trump_youtube_comment_commentdate_likes.jsonl
│        └─ 📄trump_youtube_url_title_date.json
│
├─ 🗂️2.Data_Preprocessing
│  ├─ 1.Data_Preprocessor
│  │  └─ 1.대선토론
│  │     └─ 💻trump_harris_debate_preprocessor.ipynb
│  └─ 2.Preprocessed_Data
│     └─ 1.대선토론
│        ├─ 📄preprocessed_debate_scripts.csv
│        └─ 📄preprocessed_debate_scripts.json
│
├─ 🗂️3.Data_Analysis
│  └─ 2.뉴스
│     └─ 💻뉴스_빈도분석.ipynb
│
└─ README.md
```

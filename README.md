# [인공지능기초]텍스트 마이닝을 통한 2024 미국 대선 사후 분석 

<br>

> [!NOTE]
> ## 프로젝트 세부 목표
> 1. 후보자에 대해 각 매체(토론/뉴스/유튜브 댓글)별로 어떤 단어들이 쓰였는가?
> 2. 전체 매체(토론/뉴스/유튜브 댓글)에서 후보자들과 관련있는 단어들은 무엇일까?
> 3. 후보자들에 대한 감성은 어떻게 나타날까?
> 4. 후보자들에 대한 감성으로 선거 결과를 예측 할 수 있을까? 

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
> - [X] ~전처리(불용어 제거 등)~
> - [X] 빈도수 기반 워드클라우드
> - [X] TF-IDF 키워드 분석
> - [X] 후보자 언급 빈도 분석
> 
> **3.유튜브 댓글 데이터**
> - [X] ~크롤링~
> - [X] ~다운샘플링을 통한 편향 조정~
> - [X] ~VADER 기반 감성분석~
> - [X] LLM 기반 감성분석
> - [X] ~VADER 기반 감성지수 LSTM 예측~
> - [X] ~LLM 기반 감성지수 LSTM  예측~
> - [X] ~VADER 기반 감성지수 Amazon Chronos 예측~
> - [X] ~LLM 기반 감성지수 Amazon Chronos 예측~
> 
> **4.통합 데이터 (토론 + 뉴스 + 유튜브 댓글)**
> - [X] ~Word2Vec~


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
│  │  ├─ 1.대선토론
│  │  │  └─ 💻trump_harris_debate_preprocessor.ipynb
│  │  └─ 3.유튜브 댓글
│  │     └─ 💻youtube_comment_filter_for_llm.ipynb
│  └─ 2.Preprocessed_Data
│     ├─ 1.대선토론
│     │  ├─ 📄preprocessed_debate_scripts.csv
│     │  └─ 📄preprocessed_debate_scripts.json
│     └─ 3.유튜브 댓글
│        ├─ 📄harris_youtube_comment_filtered_for_llm_10000.jsonl
│        ├─ 📄harris_youtube_comment_filtered_for_llm_18000.jsonl
│        ├─ 📄trump_youtube_comment_filtered_for_llm_10000.jsonl
│        └─ 📄trump_youtube_comment_filtered_for_llm_18000.jsonl
│
├─ 🗂️3.Data_Analysis
│  ├─ 1.Data_Analyzer
│  │  ├─ 1.대선토론
│  │  │  └─ 💻debate_analyzer.ipynb
│  │  ├─ 2.뉴스
│  │  │  └─ 💻news_analyzer.ipynb
│  │  ├─ 3.유튜브 댓글
│  │  │  ├─ llm기반 감성분석
│  │  │  │  ├─ 💻llm_sentiment_analysis_colab무료계정1+결과8500개.ipynb
│  │  │  │  ├─ 💻llm_sentiment_analysis_colab무료계정2+결과9000개.ipynb
│  │  │  │  └─ 💻llm_sentiment_analysis_colab무료계정3+결과2500개.ipynb
│  │  │  └─ vader기반 감성분석
│  │  │     └─ 💻vader_sentiment_analyzer.ipynb
│  │  └─ 4.통합데이터
│  │     └─ 💻word2vec.ipynb
│  └─ 2.Analyzed_Data
│     └─ 3.유튜브 댓글
│        ├─ llm기반 감성분석
│        │  ├─ 📄llm_sentiment_analysis.jsonl
│        │  └─ post-processing
│        │     ├─ 📄llm_sentiment_analysis_harris_time_series.json
│        │     ├─ 💻llm_sentiment_analysis_post_processor.ipynb
│        │     └─ 📄llm_sentiment_analysis_trump_time_series.json
│        └─ vader기반 감성분석
│           ├─ 📄vader_sentiment_analysis_harris.json
│           └─ 📄vader_sentiment_analysis_trump.json
│
├─ 🗂️4.Data_Predition
│  └─ 유튜브 댓글
│     ├─ AWS_Chronos
│     │  ├─ llm 기반 감성 지수
│     │  │  └─ 💻llm_sentiment_chronos_predictor.ipynb
│     │  └─ vader 기반 감성 지수
│     │     └─ 💻vader_sentiment_chronos_predictor.ipynb
│     └─ LSTM
│        ├─ llm 기반 감성 지수
│        │  └─ 💻llm_sentiment_lstm_predictor.ipynb
│        └─ vader 기반 감성 지수
│           └─ 💻vader_sentiment_lstm_predictor.ipynb
│
└─ README.md
```

# [인공지능기초]텍스트 마이닝을 통한 2024 미국 대선 사후 분석 🗽
인공지능기초 수업 팀 프로젝트

### 목차
- [1. 프로젝트 소개](#1-프로젝트-소개)
- [2. 팀원 구성 및 역할](#2-팀원-구성-및-역할)
- [3. 프로젝트 세부 목표](#3-프로젝트-세부-목표)
- [4. WBS(업무 분해 구조)](#4-WBS(업무-분해-구조))
- [4. 진행상황]
- [4. 진행상황]
- [4. 진행상황]
- [4. 진행상황]
- [4. 진행상황]
- [4. 진행상황]
- [4. 개선점]
- [4. 앞으로의 계획]
- [4. 프로젝트 구조]

# 1. 프로젝트 소개

- **주제:** 텍스트 마이닝을 통한 2024 미국 대선 사후분석: VADER & LLM 기반 감성지수 시계열 예측을 중심으로
- **기간:** 2024.09.20~2024.12.17
- **결과보고서(발표자료):** 

 # 2. 팀원 구성 및 역할
 <table style="width: 100%;">
<tr>
    <td align="center">팀장</td>
    <td align="center">팀원</td>
</tr>
<tr>
    <td align="center" style="width: 49%;"><img src="https://github.com/user-attachments/assets/c6147619-792b-4c5c-82e0-992a05e736f6" width="130px;" alt=""></a></td>
    <td align="center" style="width: 49%;"><img src="https://github.com/user-attachments/assets/d8708571-59fa-4d4c-b70a-12ba24b93d4b" width="130px;" alt=""></a></td>
</tr>
<tr>
    <td align="center"><a href="https://github.com/PearlLeeCode"><b>이진주</b></a></td>
    <td align="center"><a href=""><b>이건창</b></a></td>
</tr>
<tr>
    <td align="center">정치외교학과</td>
    <td align="center">금융공학과</td>
</tr>
<tr> 
    <td align="center">데이터 수집, 전처리,<br>분석, 모델링 및 예측</td>
    <td align="center">데이터 전처리, 분석,<br>발표</td>
</tr> 
<tr> 
    <td align="center">대선 토론,<br>뉴스,<br>유튜브 댓글<br>데이터</td>
    <td align="center">뉴스<br>데이터</td>
</tr> 
</table>
<br>

# 3. 프로젝트 배경
| ![인공지능기초_기말발표_10조-3-1](https://github.com/user-attachments/assets/1f38e545-59e2-465c-9898-6c74ab904a0d) | ![인공지능기초_기말발표_10조-4-1](https://github.com/user-attachments/assets/35b463a3-ebe5-481c-8485-f93a6e5878f4) |
|------------------------------|------------------------------|
| ![인공지능기초_기말발표_10조-5-1](https://github.com/user-attachments/assets/a661ba60-0c06-457c-969f-3a949947d664) | ![인공지능기초_기말발표_10조-6-1](https://github.com/user-attachments/assets/5753286e-66e8-4546-9e4b-c0e78b041e78) |

# 3. 프로젝트 목표
|![인공지능기초_기말발표_10조-7-1](https://github.com/user-attachments/assets/1c3f5303-25c1-4348-8c26-63bf65144ff8)|![인공지능기초_기말발표_10조-9-1](https://github.com/user-attachments/assets/5fb3779d-76a1-4d27-927f-ffda88287752)|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-10-1](https://github.com/user-attachments/assets/93178cd0-7328-4b39-a7fd-4e0a0ff5d737)|![인공지능기초_기말발표_10조-11-1](https://github.com/user-attachments/assets/be0d989d-fcee-4158-a89d-ef55472597e2)|


|||
|------------------------------|------------------------------|
|||

 
> [!NOTE]
> # 3. 프로젝트 세부 목표
> 1. 후보자에 대해 각 매체(토론/뉴스/유튜브 댓글)별로 어떤 단어들이 쓰였는가?
> 2. 전체 매체(토론/뉴스/유튜브 댓글)에서 후보자들과 관련있는 단어들은 무엇일까?
> 3. 후보자들에 대한 감성은 Vader기반과 LLM기반으로 분석했을때 결과가 각각 어떻게 나타날까?
> 4. 후보자들에 대한 감성으로 선거 결과를 예측 할 수 있을까? 

<br>

> [!IMPORTANT]
> # 4. WBS(업무 분해 구조)
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
> - [X] ~빈도수 기반 워드클라우드~
> - [X] ~TF-IDF 키워드 분석~
> - [X] ~후보자 언급 빈도 분석~
> 
> **3.유튜브 댓글 데이터**
> - [X] ~크롤링~
> - [X] ~다운샘플링을 통한 편향 조정~
> - [X] ~VADER 기반 감성분석~
> - [X] ~LLM 기반 감성분석~
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

# [인공지능기초]텍스트 마이닝을 통한 2024 미국 대선 사후 분석 🗽
인공지능기초 수업 팀 프로젝트

### 목차
- [1. 프로젝트 소개](#1-프로젝트-소개)
- [2. 팀원 구성 및 역할](#2-팀원-구성-및-역할)
- [3. 프로젝트 배경](#3-프로젝트-배경)
- [4. 서비스 대상 정의 및 시장 규모 조사, 시나리오 설정](#4-서비스-대상-정의-및-시장-규모-조사-시나리오-설정)
- [5. 프로젝트 목표](#5-프로젝트-목표)
- [6. 데이터 수집 및 전처리](#6-데이터-수집-및-전처리)
- [7. 데이터 분석 - 빈도분석, TF-IDF](#7-데이터-분석---빈도분석-tf-idf)
- [8. 유튜브 댓글 데이터 감성분석 및 예측 - VADER 사전 기반](#8-유튜브-댓글-데이터-감성분석-및-예측---vader-사전-기반)
- [9. 유튜브 댓글 데이터 감성분석 및 예측 - LLM 기반](#9-유튜브-댓글-데이터-감성분석-및-예측---llm-기반)
- [10. 고찰](#10-고찰)
- [11. 프로젝트 의의 및 추후 개선사항](#11-프로젝트-의의-및-추후-개선사항)
- [12. 소감 및 앞으로의 계획](#12-소감-및-앞으로의-계획)
- [13. WBS(업무 분해 구조)](#13-wbs업무-분해-구조)
- [14. 프로젝트 구조](#14-프로젝트-구조)


# 1. 프로젝트 소개

- **주제:** 텍스트 마이닝을 통한 2024 미국 대선 사후분석: VADER & LLM 기반 감성지수 시계열 예측을 중심으로
- **기간:** 2024.09.20~2024.12.17
- **결과보고서(발표자료):** [인공지능기초_기말발표_10조.pdf](https://github.com/PearlLeeCode/2024-us-election-analysis/blob/main/%EC%9D%B8%EA%B3%B5%EC%A7%80%EB%8A%A5%EA%B8%B0%EC%B4%88_%EA%B8%B0%EB%A7%90%EB%B0%9C%ED%91%9C_10%EC%A1%B0.pdf)

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
    <td align="center">데이터 수집, 전처리,<br>분석, 모델링 및 예측<br>문서화, ppt 제작</td>
    <td align="center">데이터 전처리, 분석,<br>발표</td>
</tr> 
</table>
<br>

# 3. 프로젝트 배경
| ![인공지능기초_기말발표_10조-3-1](https://github.com/user-attachments/assets/1f38e545-59e2-465c-9898-6c74ab904a0d) | ![인공지능기초_기말발표_10조-4-1](https://github.com/user-attachments/assets/35b463a3-ebe5-481c-8485-f93a6e5878f4) |
|------------------------------|------------------------------|
| ![인공지능기초_기말발표_10조-5-1](https://github.com/user-attachments/assets/a661ba60-0c06-457c-969f-3a949947d664) | ![인공지능기초_기말발표_10조-6-1](https://github.com/user-attachments/assets/5753286e-66e8-4546-9e4b-c0e78b041e78) |

# 4. 서비스 대상 정의 및 시장 규모 조사, 시나리오 설정
본 프로젝트는 직접적인 서비스 출시를 목표로 하지 않으며, 단순히 연구에 가깝지만, 연구 성과의 응용 가능성 및 가치를 제고하고 연구 방향성을 수립하기 위해 서비스 대상을 정의 및 시장 규모를 조사하고 서비스 시나리오를 설정해 보았다.
|서비스 대상|선거 여론 예측 시장 성장 규모|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-39-1](https://github.com/user-attachments/assets/6a86ae80-c6ae-4f38-8967-3cb8d3ef78c7)|![인공지능기초_기말발표_10조-40-1](https://github.com/user-attachments/assets/b4a7b66d-63ec-4bf1-9e88-0c4f5729ecad)|
|가상의 서비스 시나리오 설정|서비스 시나리오|
|![인공지능기초_기말발표_10조-42-1](https://github.com/user-attachments/assets/d59f48d7-a8ea-466c-a4b6-baef15eb1951)|![인공지능기초_기말발표_10조-43-1](https://github.com/user-attachments/assets/d1a5b314-1c00-4f51-b0d1-3d6b18dfbc23)|

# 5. 프로젝트 목표
|![인공지능기초_기말발표_10조-7-1](https://github.com/user-attachments/assets/1c3f5303-25c1-4348-8c26-63bf65144ff8)|![인공지능기초_기말발표_10조-9-1](https://github.com/user-attachments/assets/5fb3779d-76a1-4d27-927f-ffda88287752)|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-10-1](https://github.com/user-attachments/assets/93178cd0-7328-4b39-a7fd-4e0a0ff5d737)|![인공지능기초_기말발표_10조-11-1](https://github.com/user-attachments/assets/be0d989d-fcee-4158-a89d-ef55472597e2)|

# 6. 데이터 수집 및 전처리
|![인공지능기초_기말발표_10조-13-1](https://github.com/user-attachments/assets/9310000b-db01-4356-b195-26c84a8e28b3)||
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-14-1](https://github.com/user-attachments/assets/59a55a27-0c23-4eee-848d-039c2e5daf89)|![인공지능기초_기말발표_10조-15-1](https://github.com/user-attachments/assets/39b42f83-e68b-40f2-a7e3-1b007adee37d)|


# 7. 데이터 분석 - 빈도분석, TF-IDF
|토론 데이터 TF-IDF|뉴스 데이터 언급 빈도수|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-17-1](https://github.com/user-attachments/assets/98b55ab0-eebe-4941-8f13-94a05a2151a0)|![인공지능기초_기말발표_10조-18-1](https://github.com/user-attachments/assets/0016b968-4c4a-48eb-b4c9-19b1d87a7f6e)|
|뉴스 데이터 언론사별 전체 키워드 TOP 10|뉴스 데이터 TF-IDF|
|![인공지능기초_기말발표_10조-19-1](https://github.com/user-attachments/assets/b83176ff-32ce-4717-91d0-5720250ed717)|![인공지능기초_기말발표_10조-20-1](https://github.com/user-attachments/assets/29d60e4b-ae2a-46a0-b1f1-550ff8169264)|
|뉴스 데이터 언론사별 후보자 관련 TOP 20|통합 데이터(토론,뉴스,유튜브) Word2Vec|
|![인공지능기초_기말발표_10조-21-1](https://github.com/user-attachments/assets/8e909cd1-cff7-4f3f-926b-3fec12971c02)|![인공지능기초_기말발표_10조-23-1](https://github.com/user-attachments/assets/419e9278-a74d-46ac-9e03-168f69217a09)|

# 8. 유튜브 댓글 데이터 감성분석 및 예측 - VADER 사전 기반 
|VADER 사전 기반 감성분석|VADER 사전 기반 감성분석 결과|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-25-1](https://github.com/user-attachments/assets/93813127-e83c-448c-87a0-501ba1340887)|![인공지능기초_기말발표_10조-26-1](https://github.com/user-attachments/assets/33aec2d2-51a5-409e-be00-6362ec06bed1)|
|VADER 사전 기반 감성지수 LSTM 예측|VADER 사전 기반 감성지수 [Chronos](https://github.com/amazon-science/chronos-forecasting) 예측|
|![인공지능기초_기말발표_10조-27-1](https://github.com/user-attachments/assets/9ef0fa81-ea1a-4652-8e8a-c2a1700fb395)|![인공지능기초_기말발표_10조-28-1](https://github.com/user-attachments/assets/24649123-eb7a-48b3-a55f-75695ed1cc54)|
|한계 (LLM 기반 감성분석 진행의 동기)||
|![인공지능기초_기말발표_10조-29-1](https://github.com/user-attachments/assets/945d54cd-6c4a-4afe-a4cd-a3de515088e9)||

# 9. 유튜브 댓글 데이터 감성분석 및 예측 - LLM 기반
|LLM 기반 감성분석: 모델 선정|LLM 기반 감성분석: 프롬프트 설계|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-31-1](https://github.com/user-attachments/assets/967f36a1-4920-4572-a028-14611fbac3fc)|![인공지능기초_기말발표_10조-32-1](https://github.com/user-attachments/assets/e1fe9dd6-c443-4c10-a0d1-07ba3614d8d1)|
|LLM 기반 감성분석: 프롬프트 설계|LLM 기반 감성분석: 후처리|
|![인공지능기초_기말발표_10조-33-1](https://github.com/user-attachments/assets/e2f2c659-f399-4035-8d15-981639ceaf54)|![인공지능기초_기말발표_10조-34-1](https://github.com/user-attachments/assets/8503fc15-e099-4429-b8f9-9c3ce9749e33)|
|LLM 기반 감성분석 결과|LLM 기반 감성지수 LSTM 예측|
|![인공지능기초_기말발표_10조-35-1](https://github.com/user-attachments/assets/c75cc032-5e2a-4518-abed-2b5eba68448b)|![인공지능기초_기말발표_10조-36-1](https://github.com/user-attachments/assets/9a618435-4210-4e43-8605-f0f4fc28994a)|
|LLM 기반 감성지수 [Chronos](https://github.com/amazon-science/chronos-forecasting) 예측||
|![인공지능기초_기말발표_10조-37-1](https://github.com/user-attachments/assets/faacb4bd-0342-47b3-af8a-61b5f74ed376)||

> [!NOTE]
> # 10. 고찰
> 이번 연구를 통해 샤이 지지층을 포함한 다양한 정치적 입장과 정서를 소셜 미디어 데이터로 포착하는 데에는 한계가 있음을 확인하였다. 특히 LLM 기반 감성분석 및 VADER 기반 감성분석 모두에서 감성지수를 사용한 예측 모델(LSTM, Chronos)의 성능이 기대만큼 일관적이지 않았고, 감성지수 자체가 정치적 성향을 대변하기에는 부족한 면이 있었다. 또한 데이터 소스, 크기, 분석 모델 모두에 대해 추가적인 보완이 필요함을 느꼈다.


# 11. 프로젝트 의의 및 추후 개선사항
|추후 개선사항|프로젝트 의의|
|------------------------------|------------------------------|
|![인공지능기초_기말발표_10조-44-1](https://github.com/user-attachments/assets/78ea6d80-4dcd-4241-9de1-5a0a00d8cc94)|![인공지능기초_기말발표_10조-46-1](https://github.com/user-attachments/assets/3e74672d-49dc-4e62-ad65-5620ca4ff910)|

개선점을 다시한번 정리해본다.

| 항목                     | 세부 내용                                                                 |
|--------------------------|--------------------------------------------------------------------------|
| **LLM 기반 감성분석** | - 기존 LLaMA 모델에서 더 성능 좋은 LLaMA 모델로 교체하기<br>- 프롬프트 개선하기               |
| **예측 모델**        | - 예측 모델에 파라미터 튜닝하기<br>- 반복해서 실험하고 검증하기<br>- 감성지수 외에 추가적인 feature 활용해서 예측 모델 고도화하기                                        |
| **수집 데이터 종류수 늘리고 편향 제거** | - 뉴스 언론사 추가적으로 크롤링하기 (POLITICO, NPR, Reuter, AP, ABC, PBS)<br>- 유튜브 외 다른 SNS(페이스북, 레딧 , 쓰레드) 데이터를 수집하기<br>- 언론사별 편향지수 활용해서 편향 조정하기<br>- sns 데이터도 편향 더욱 최소화하기|





> [!NOTE]
> # 12. 소감 및 앞으로의 계획
> **소감**: 프로젝트를 진행하면서 신경 써야 할 부분과 개선해야 할 점이 많이 발견되었다. 한 가지 예를 들면, LLM 기반 감성 분석에서 제거해야 하거나 분석에 악영향을 미치는 결과가 다수 생성되었다. 프롬프트 수정을 반복하여 이를 개선하고 싶었으나, 시간 부족으로 시도하지 못한 점이 아쉬움으로 남았다.
그러나 이를 통해 "내가 가설을 세우고, 그 가설을 무조건 맞는 방향으로 끌고 가려고 하는 것은 아닌가?"라는 스스로의 태도에 대해 되돌아보는 계기가 되었고, 연구의 본질과 목적에 대해 깊이 고민해볼 수 있었다.  
> **앞으로의 계획**: 방학 기간에도 프로젝트를 지속할 계획이다. Colab을 결제하여 컴퓨팅 자원을 늘리고, 더 많은 데이터를 수집 및 분석할 것이다. 이를 통해 전문가가 보기에 신뢰할 수 있고, 의미 있는 연구 결과를 도출하는 것을 목표로 하고 있다. 연구 주제와 관련된 방법들이나 논문을 참고하고, 교수님께 피드백을 받아서 가능하다면 논문까지 작성해보고 싶다.


> [!IMPORTANT]
> # 13. WBS(업무 분해 구조)
>
> *2024.12.17기준*  
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

# 14. 프로젝트 구조

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
├─ LICENSE
├─ README.md
└─ 인공지능기초_기말발표_10조.pdf
```
*유튜브 수집 코드 및 데이터는 아래 종류의 파일만 유효하다. 아래 형태는 유튜브 api를 사용하여 간편하게 수집한 형태이며(멘토님 감사합니다.) 이외의 파일은 직접 스크랩핑한 코드와 데이터이다. 시계열 분석에 특성상 주기가 일정하게 수집되어야 하므로 폐기하였다. 하지만 몇일간의 수고가 한순간에 날라가는것이 아쉬워 남겨두었음을 유념한다.*
- *youtube_comment_api_crawler.ipynb (harris, trump)*
- *youtube_comment.jsonl (harris, trump)*

 <a href="https://hits.sh/github.com/PearlLeeCode/2024-us-election-analysis"><img alt="Hits" src="https://hits.sh/github.com/PearlLeeCode/2024-us-election-analysis.svg?view=today-total&style=for-the-badge&color=ffffff&labelColor=ffffff" align="right"/></a>

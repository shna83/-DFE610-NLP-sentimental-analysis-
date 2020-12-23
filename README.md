# -DFE610-NLP sentimental-analysis-
◎ NSMC와 Friends 데이터를 이용한 감성분석

1. 감성분석 모델링 개요
  - NSMC 데이터를 이용하여 CNN, LSTM, Bi-LSTM, Bi-LSTM & Attention, KoELECTRA 모델 중 성능 좋은 모델 선택
  - Bert 모델인 KoELECTRA 모델의 성능이 우수하여, Friends 데이터의 경우 ElECTRA 모델 사용하여 모델 구현
  - 실행 환경
    - 클라우드 서버와 GPU를 제공하는 colab에서 구현
    - GPU의 경우 GOOGLE에서 랜덤으로 제공
   
2. 감성분석 모델 구현
  - NSMC(Naver Sentiment Movie Corpus)
    - 데이터 전처리 방법
      ☞ 중복데이터 제거 → null값 제거 → 특수문자 및 공백 등 제거를 통한 한글 정규화 → 불용어 제거 → 형태소 토큰화(Okt 사용) → 정수 인코딩 → 낮은 등장 빈도수 제거 및 공백 제거
    - CNN 모델
    - LSTM 모델
    - Bi-LSTM 모델
    - Bi-LSTM & Attetion 모델
    - KoELECTRA 모델
  - Friends
    - 데이터 전처리 방법
    - ELECTRA 모델
  
3. 참고 사이트
   - https://wikidocs.net/85337
   - https://wikidocs.net/44249
   - https://wikidocs.net/48920
   - https://github.com/jiwonny/nlp_emotion_classification


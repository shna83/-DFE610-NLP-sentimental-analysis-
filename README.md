# -DFE610-NLP sentimental-analysis-
◎ NSMC와 Friends 데이터를 이용한 감성분석

1. 감성분석 모델링 개요
  - NSMC 데이터를 이용하여 CNN, LSTM, Bi-LSTM, Bi-LSTM & Attention, KoELECTRA 모델 중 성능 좋은 모델 선택
  - Bert 모델인 KoELECTRA 모델의 성능이 우수하여, Friends 데이터의 경우 ELECTRA 모델 사용하여 모델 구현
  - 실행 환경 및 방법
    - 클라우드 서버와 GPU를 제공하는 colab에서 구현(colab 런타임 탭에서 런타임 유형 변경: GPU 선택)
    - GPU의 경우 GOOGLE에서 랜덤으로 제공
    - 구글드라이브와 colab 연동 설정 필요(Friends 데이터 사용 및 최종 결과값 CSV 산출 시 필요)
    - colab에서 GPU 설정 후 순서대로 코드 실행 (구글드라이브 연동 필요)
      - NSMC 다운로드 경로 : https://github.com/e9t/nsmc
      - Friends 다운로드 경로 : http://doraemon.iis.sinica.edu.tw/emotionlines/download.html
        - Friends 데이터의 경우 압축해제 후 사용 필요
      - 순서대로 코드 실행하였음에도 불구하고 error가 발생하는 경우는 !pip install 부분으로 다음 install 셀 실행 후 다시 실행
   
   
2. 감성분석 모델 구현
  - NSMC(Naver Sentiment Movie Corpus)
    - 데이터 전처리 방법
      
      중복 및 null값 데이터 제거 → 특수문자 및 공백 등 제거를 통한 한글 정규화 → 불용어 제거 및 형태소 토큰화(Okt()) → 정수 인코딩 → 빈 샘플 제거 및 패딩
    
    - CNN, LSTM, Bi-LSTM, Bi-LSTM & Attention, KoELECTRA 모델 구축
    - 모델 구축 환경
![model 비교](https://user-images.githubusercontent.com/73410906/103128258-f5c25a00-46d7-11eb-88b7-f41408b5fe82.jpg)

    
    
  - Friends
    - 데이터 전처리 방법
    
      [CLS]와 [SEP]로 구성된 문장으로 전처리하여 Pre-trained ELECTRA 토큰화
    
    - ELECTRA 모델 : test accuracy = 54.97%
  
  
3. 참고 사이트
   - https://wikidocs.net/85337
   - https://wikidocs.net/44249
   - https://wikidocs.net/48920
   - https://github.com/jiwonny/nlp_emotion_classification
   - https://github.com/google-research/electra
   - https://github.com/monologg/KoELECTRA


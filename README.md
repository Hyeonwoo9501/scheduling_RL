# scheduling_RL
 

## 목적
강화 학습을 이용하여, 납기일 준수 및 셋업최소화를 위한 공정 스케줄링 최적화

## reference
 - 논문 : <https://scienceon.kisti.re.kr/srch/selectPORSrchArticle.do?cn=JAKO201925462479137&dbt=NART>
 - 자료 : <https://hwk0702.github.io/projects/2019/11/08/Scheduler/>

## Create dataset for training
  1. dataset/data_create.ipynb open
  2. Hyper parameter setting(number of job types, number of orders, min process_time, max process_time, max due_date)
  3. Implementing data_create.ipynb



## Training
 - environment.ipynb 파일에서 서로다른 방식의 학습을 수행
 - 학습 데이터 전처리, DQN class, DQN 학습 및 모델 저장, 학습과정 시각화(train loss) 로 코드진행
 - 다수의 데이터셋 활용해서 모델학습
 - machine state 전체를 binary 값으로 설정
 - Train loss
 
 ![image](https://user-images.githubusercontent.com/52640089/113390417-a40f2700-93cc-11eb-87fd-0bb678045158.png)


## Model test
 - model.h5 : 이전의 학습을 통해서 생성된 모델 저장파일
 - model_test.ipynb : 이전의 학습된 모델을 불러와서, 해당 모델을 기반으로 test 데이터셋에 대해서 최적배치 예측

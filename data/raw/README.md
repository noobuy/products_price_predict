# raw

## raw data입니다.
- 이 데이터는 변경 불가능합니다.
- raw 데이터의 크기가 커 [Google Drive](https://drive.google.com/drive/folders/1t7bitT1ekuxVPQbqEO6fWch1PDaMf-3p)로 대체합니다. 


## Data Explanation
※ 데이터 출처 : 농넷 | 농산물유통종합정보시스템 (nongnet.or.kr) (대회용 API 제공 예정)


1. public_data : public leaderboard용 데이터

	1-1. train.csv : 베이스라인 코드용으로 가공된 학습 데이터
	[기간] 2016년 1/1 ~ 2020년 9/28

date: 일자<br>
요일: 요일<br>
품목_거래량(kg): 해당 품목의 거래량<br>
품목_가격(원/kg): 해당 품목의 kg당 가격<br>
품목_가격 산출 방식 : 품목 또는 품종의 총 거래금액/총 거래량 (※취소된 거래내역 제외)<br>
	1-2. test_files : 베이스라인 코드용으로 가공된 테스트 데이터(추론일자별 분리, ex.test_2020-08-29.csv => 2020년 8월 29일 추론에 사용 가능 데이터)

	1-3. train_AT_TSALET_ALL : 학습용 전국 도매시장 거래정보 데이터(train.csv 생성에 사용)

SALEDATE: 경락 일자<br>
WHSAL_NM: 도매시장<br>
CMP_NM: 법인<br>
PUM_NM: 품목<br>
KIND_NM: 품종<br>
DAN_NM: 단위<br>
POJ_NM: 포장<br>
SIZE_NM: 크기<br>
LV_NM: 등급<br>
SAN_NM: 산지<br>
DANQ: 단위중량<br>
QTY: 물량<br>
COST: 단가<br>
TOT_QTY: 총물량 (음수로 집계된 값은 거래 취소 내역)<br>
TOT_AMT: 총금액<br>
	1-4. test_AT_TSALET_ALL : 추론용 전국 도매시장 거래정보 데이터(test_files 생성에 사용)


2. private_data : private leaderboard용 데이터, public leaderboard 학습 및 추론 사용 불가

	2-1. private.csv : 베이스라인 코드용으로 가공된 데이터

	2-2. AT_TSALET_ALL : 2021년 8월까지의 전국 도매시장 거래정보 데이터(private.csv 생성에 사용)


3. sample_submission.csv : 제출 양식

예측대상일자: 예측대상일(기준일로부터 1,2,4주 뒤 일자)<br>
품목_가격(원/kg): 해당 품목의 kg당 가격


4. 추천 외부 데이터

농산물 유통 정보: https://www.kamis.or.kr/customer/reference/openapi_list.do <br> 
aT 도매유통 정보시스템: https://at.agromarket.kr/openApi/apiInfoDtl.do?apiSeq=1<br>
농촌진흥청 국립농업과학원 농업기상 데이터: https://www.data.go.kr/data/15078057/openapi.do<br>
관세청_품목별 수출입 실적: https://www.data.go.kr/data/3046122/openapi.do<br>
농식품수출정보: https://www.kati.net/statistics/monthlyPerformanceByProduct.do

# 환경성질환 유전자 바이오마커 데이터베이스

## 목차

[1. 연구 배경 및 목적](#content1)

[2. 환경성질환 유전자 바이오마커 수집 전략 및 과정 모식도](#content2)

[3. 알려진 신경계, 호흡계, 알레르기 질환 유전자 바이오마커 정보 수집 결과](#content3)

[3.1 1단계: 공개된 데이터베이스 내 환경성질환 유전자 바이오마커 수집](#content3.1)

[3.2 2단계: 문헌 검색을 통한 환경성질환 유전자 바이오마커 수집](#content3.2)

[3.3 3단계: 1/2단계 정보 통합 데이터베이스 구축](#content3.3)

## 1. 연구 배경 및 목적 <a name="content1"></a>

1. 급격한 산업화에 의하여 배출되는 오염물질의 종류가 상승중
2. 미세먼지, 유해화학물질 등 다양한 환경유해인자 노출로 인한 환경성질환 발생이 지속적으로 증가
3. 따라서 환경유해인자와 환경성질환 간 상관성을 예측하고 평가하기 위한 기술이 필요
----

* 6대 환경성질환군: 호흡계/순환계/알레르기/신경계/임신출산계/감각계 질환
* 환경부령 환경보건법 상에서 공통적으로 환경성질환으로 제시된 신경계/호흡계/알레르기 질환군 3개를 연구 대상으로 설정
* 알려진 신경계, 호흡계, 알레르기 질환에 대한 유전자 바이오마커 정보 수집

## 2. 환경성질환 유전자 바이오마커 수집 전략 및 과정 모식도 <a name="content2"></a>

![](./figures/flowchart.png)

## 3. 알려진 신경계, 호흡계, 알레르기 질환 유전자 바이오마커 정보 수집 결과 <a name="content3"></a>

### 3.1 1단계: 공개된 데이터베이스 내 환경성질환 유전자 바이오마커 수집 <a name="content3.1"></a>

* 잘 알려진 인간 질병 바이오마커 데이터베이스 6종 중 MarkerDB, KEGG Disease Database, DisGeNET 3종을 선정
* 데이터베이스 3종 선정 기준: 라이센스 필요(GOBIOM), 환경성질환 유전자 바이오마커 정보 미포함(IDBD, ResMarkerDB) 데이터베이스는 제외

데이터베이스 | 주요 대상 질병군 | 업데이트 현황 | 웹 주소
---- | ---- | ---- | ----
MarkerDB | 알려진 임상 분자 바이오마커 | 2021년 1월 | https://markerdb.ca
KEGG Disease Database | 질병 유전자/환경 바이오마커 | 2021년 5월 | https://www.genome.jp/kegg/disease
DisGeNET | 질병 관련 유전자, 변이 바이오마커 | 2021년 10월 | https://www.disgenet.org
GOBIOM | 단백질, 유전자 등 바이오마커 | 2022년 2월 | https://gobiomdbplus.com
IDBD | 감염성 질병 관련 바이오마커 | 2008년 1월 | http://biomarker.cdc.go.kr
ResMarkerDB | 유방/대장암 관련 항체 바이오마커 | 2019년 3월 | http://www.resmarkerdb.org

----
### MarkerDB

* Data retrieved: 2021-11-01, "Genetic markers with associated conditions", released on 2020-10-10
* Data link: [MarkerDB_raw_data.tsv](./data/downloaded_rawdata/MarkerDB_raw_data.tsv)

MarkerDB에서 아래 분류에 포함된 질병의 유전자 바이오마커를 수집함
* Nervous System Disorder
* Respiratory System Disorder
* Immune System Disorder 분류 내 Allergic Disease
* Mental or Behavioural Disorder 분류 내 Alzheimer's Disease, Autism

----
### KEGG Disease Database

* Data retrieved: 2021-11-03, "Human Diseases + Gene", last updated 2021-05-01
* Data link: [KEGG_raw_data.keg](./data/downloaded_rawdata/KEGG_raw_data.keg)

KEGG Disease Database에서 아래 분류에 포함된 질병의 유전자 바이오마커를 수집함
* Immune system diseases 분류 내 Allergies and autoimmune diseases (자가면역 질환 제외)
* Nervous system diseases
* Respiratory diseases
* Other diseases 분류 내 ADHD, Autism

----
### DisGeNET

* Data retrieved: 2021-11-02, Source: curated, "Summary of GDAs", last updated 2021-10
* Data link: [DisGeNET_raw_data.tsv](./data/downloaded_rawdata/DisGeNET_raw_data.tsv)

DisGeNET에서 아래 [MeSH Class 코드](https://en.wikipedia.org/wiki/List_of_MeSH_codes)에 포함된 질병의 유전자 바이오마커를 수집함
* C08 - respiratory tract diseases
* C10 - nervous system diseases
* C20 - immune system diseases 코드 내 알레르기 질환
* F03 - Mental or Behavioral Dysfunction 코드 내 ADHD, Autism

----
Feature | MarkerDB | KEGG Disease Database | DisGeNET
---- | ---- | ---- | ----
전체 질환/유전자 바이오마커 수 | 699 / 26,374 | 2,068 / 6,790 | 11,181 / 84,038
신경계 질환/유전자 바이오마커 수 | 13 / 37 | 251 / 1,170 | 364 / 3,773
호흡계 질환/유전자 바이오마커 수 | 3 / 5 | 15 / 83 | 52 / 875
알레르기 질환/유전자 바이오마커 수 | 1 / 12 | 5 / 37 | 9 / 133
확보한 총 연구 대상 질환/유전자 바이오마커 수 | 17 / 54 | 271 / 1,292 | 425 / 4,781

* 데이터베이스 별로 질환군으로 묶어 유전자 바이오마커 목록을 텍스트 파일로 정리
* MarkerDB: [신경계](./data/processed_biomarker_gene/MarkerDB_nerve.txt) / [호흡계](./data/processed_biomarker_gene/MarkerDB_resp.txt) / [알레르기](./data/processed_biomarker_gene/MarkerDB_allergy.txt)
* KEGG Disease Database: [신경계](./data/processed_biomarker_gene/KEGG_nerve.txt) / [호흡계](./data/processed_biomarker_gene/KEGG_resp.txt) / [알레르기](./data/processed_biomarker_gene/KEGG_allergy.txt)
* DisGeNET: [신경계](./data/processed_biomarker_gene/DisGeNET_nerve.txt) / [호흡계](./data/processed_biomarker_gene/DisGeNET_resp.txt) / [알레르기](./data/processed_biomarker_gene/DisGeNET_allergy.txt)
* 3개 데이터베이스에서 총 635개 신경계/호흡계/알레르기 질환에 대한 유전자 바이오마커 5,472개 수집 (중복 제거)

### 3.2 2단계: 문헌 검색을 통한 환경성질환 유전자 바이오마커 수집 <a name="content3.2"></a>

* 공개된 데이터베이스에서 누락된 유전자 바이오마커를 탐색하기 위해 문헌 검색을 통해 유전자 바이오마커 추가 수집

----
### 국제질병분류(ICD-11) 수록 신경계/호흡계/알레르기 질환 분류 수집

* Data retrieved: 2021-10-28, "ICD-11 for Mortality and Morbidity Statistics", Version: 05/2021 from https://icd.who.int/browse11/l-m/en
* Data link: [ICD11_disease_list.txt](./data/downloaded_rawdata/ICD11_disease_list.txt)

문헌 검색에 사용할 표준화된 신경계/호흡계/알레르기 질환명을 ICD-11을 통해 확보, 아래 분류 하위 질환명 수집
* 04 Diseases of the immune system 분류 내 Allergic or hypersensitivity conditions (4A80 - 4A8Z)
* 08 Diseases of the nervous system
* 12 Diseases of the respiratory system
* 6A02 Autism spectrum disorder
* 6A05 Attention deficit hyperactivity disorder (ADHD)

질환군 | ICD-11 분류 내 질환 수 | 질환 예시
---- | ---- | ----
신경계 질환 | 2,109개 | 파킨슨병 (Parkinson disease)
호흡계 질환 | 655개 | 만성 비염 (Chronic rhinitis)
알레르기 질환 | 201개 | 아나필락시스 (Anaphylaxis)
총계 | 2,965개 | -

----
### PubMed 문헌/서지 검색을 이용한 유전자 바이오마커 수집

* [PubMed](https://pubmed.ncbi.nlm.nih.gov/) search data retrieved: 2021-08-13
* Search keyword: "질환명[Title/Abstract]" AND "biomarker[Title/Abstract]"
* 제목 또는 초록에 질환명과 바이오마커(biomarker) 단어를 포함하는 문헌 수집
* 수집 문헌 초록: [신경계](./data/downloaded_rawdata/PubMed_search_nerve.zip) / [호흡계](./data/downloaded_rawdata/PubMed_search_resp.zip) / [알레르기](./data/downloaded_rawdata/PubMed_search_allergy.zip)

질환군 | 검색 결과 문헌 1개 이상 존재 질환 수 및 비율 | 검색 결과 문헌 수
---- | ---- | ----
신경계 질환 | 257개 (12.2%) | 9,794개
호흡계 질환 | 93개 (14.2%) | 6,810개
알레르기 질환 | 30개 (14.9%) | 2,226개
총계 | 380개 (12.8%) | 18,830개

----
### 문헌 내 환경성질환 관련 유전자 바이오마커 사람 유전자 명칭 탐색

* Data retrieved: 2021-08-15 from [NCBI Human Genome Resources](https://www.ncbi.nlm.nih.gov/genome/guide/human/)
* Data link: [Human_gene_list.txt](./data/downloaded_rawdata/Human_gene_list.txt)
* 수집한 PubMed 문헌 초록에 유전자 바이오마커 정보가 포함되어 있는지 확인 위해 사람 유전자 명칭 수집
* 일부 유전자는 별칭(alias)이 존재, e.g. 지질 분해 효소 A(Lipase A, LIPA): LAL, CESD

Feature | 개수
---- | ----
NCBI 데이터베이스 내 사람 유전자 명칭 수 | 63,742개
NCBI 데이터베이스 내 사람 유전자 별칭 수 | 107,954개
별칭이 있는 사람 유전자 명칭 수 | 27,138개
중복 제거 사람 유전자 명칭+별칭 수 | 127,918개

----
### 확보 문헌 초록 사람 유전자 명칭 포함 여부 확인

* 문헌 초록을 띄어쓰기/괄호 기준으로 단어 단위로 분리해 사람 유전자 명칭 목록과 대조
* 전체 18,830개 문헌 중 14,459개에서 사람 유전자 명칭 확인 (76.8%)

질환군 | 검색 결과 문헌 수 | 사람 유전자 명칭 포함 문헌 수
---- | ---- | ----
신경계 질환 | 9,794개 | 7,819개
호흡계 질환 | 6,810개 | 5,103개
알레르기 질환 | 2,226개 | 1,537개
총계 | 18,830개 | 14,459개

### 3.3 3단계: 1/2단계 정보 통합 데이터베이스 구축 <a name="content3.3"></a>

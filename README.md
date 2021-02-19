# 🎯 [YPolaris] 머신러닝을 이용한 상권분석 서비스
---

## 개요

단기 산학협력 프로젝트 (2020/08/28 - 2020/11/29)
* 머신러닝을 이용하여 소매 및 도매점에 한하여 무인점포를 위한 상권분석 서비스 웹페이지 구축
  * 부산광역시의 읍면동별 분석  

**팀장 : `허정훈`**
> 팀원 : `이가영` `강다미` `권기호`
---
### 개발 환경

**[서버 사양]**
서버 : AWS t2.micro 인스턴스
- CPU 1, 메모리 1GiB, i386, x86_64
- ubuntu 18.04
- IP주소 : 52.78.155.149
Service Domain: http://52.78.155.149:5000

**[개발 환경]**
파이썬 : python3.8.5
파이썬 라이브러리 : flask, pymysql
데이터베이스 : db.t2.micro 
- mysql 8.0.20
- 엔드 포인트 : database-1.c4y1s8zaxihb.ap-northeast-2.rds.amazonaws.com
- 계정 : admin, 비밀번호 : mypassword
- 코드 저장소 [code](https://github.com/Kangdamii/yproject)

**[데이터 출처]**
> * 상가정보 - 공공데이터 포털 [link](https://www.data.go.kr/data/15059997/fileData.do)
> * 읍면동별 세대 및 인구 - 통계청(KOSIS) [link](https://kosis.kr/statHtml/statHtml.do?orgId=202&tblId=DT_B1)
> * 구군별 총 카드이용금액  - 부산시 빅데이터포털 [link](https://bigdata.busan.go.kr/)
> * 부산시 읍면동별 매출액 - 통계청(KOSIS) [link](https://kosis.kr/statHtml/statHtml.do?orgId=101&tblId=DT_1KI1511_10&vw_cd=MT_ZTITLE&list_id=K2_KI_001_001_001&seqNo=&lang_mode=ko&language=kor&obj_var_id=&itm_id=&conn_path=MT_ZTITLE)
> * 읍면동별 요일별 유동인구 - 부산시 빅데이터포털 [link](https://bigdata.busan.go.kr/)
---
### 서비스 설명
<img src = "https://user-images.githubusercontent.com/54921730/108481280-59819180-72db-11eb-9a8f-cf38e06e4a01.png" width = 1000, max_width_size=100% height = auto/>

> * 카카오 API를 이용하여 지도를 띄우고 메인페이지를 표출한다. 
> * 사용자가 구를 검색해 동을 선택하면 인구수를 보여주고 유동인구, 경쟁업체수, 총인구, 구매력, 매출액대비 영업이익 등
5개의 변수로 생성된 방사형그래프를 지도의 오른쪽에 띄움으로써 상권분석의 결과를 보여준다.
> * 상권분석의 척도는 좋음, 양호, 고려, 나쁨으로 구분해 사용자가 시각적으로 판단할 수 있게 해 준다. 

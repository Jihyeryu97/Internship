# POWER BI 사용하기  

## json 파일로 대시보드 만들기  
 1. Power bi desktop을 열고, ‘데이터 가져오기’ 버튼을 클릭한다.  
  ![1](https://user-images.githubusercontent.com/49367190/61266471-f2caf680-a7ce-11e9-9b55-f1bf9227fa10.JPG)  
 2. ‘JSON’파일 유형을 클릭한다.  
  ![2](https://user-images.githubusercontent.com/49367190/61266472-f2caf680-a7ce-11e9-905a-0b0737d44015.JPG)  
 3. 분석하고 싶은 json 파일을 선택하고 ‘열기＇ 버튼을 클릭한다.  
  ![3](https://user-images.githubusercontent.com/49367190/61266473-f3638d00-a7ce-11e9-8aaf-0d1d65cb5806.JPG)  
 4. 모든 열 (또는 분석하고 싶은 열) 선택 후 '확인'버튼을 클릭한다.  
  ![4](https://user-images.githubusercontent.com/49367190/61266475-f3638d00-a7ce-11e9-8d35-427f5ffa2a8f.JPG)  
 5. 확장할 열을 선택한다,  
  ![5](https://user-images.githubusercontent.com/49367190/61266476-f3638d00-a7ce-11e9-90b7-138450984e34.JPG)  
  ![6](https://user-images.githubusercontent.com/49367190/61266477-f3638d00-a7ce-11e9-86d8-a835777908a2.JPG)
  ![7](https://user-images.githubusercontent.com/49367190/61266480-f3fc2380-a7ce-11e9-8630-6f66d3d29277.JPG)
  ![8](https://user-images.githubusercontent.com/49367190/61266481-f3fc2380-a7ce-11e9-9134-6f524934ee31.JPG)  
 6. 첫번째 Column에서 마우스 오른쪽 버튼을 클릭해 ‘형식 변경＇을 클릭, ‘날짜/시간/표준 시간대’ 버튼을 클릭한다.  
  ![9](https://user-images.githubusercontent.com/49367190/61266483-f494ba00-a7ce-11e9-8ea8-504b6ac8ebda.JPG)  
 7. 나머지 열을 클릭한 채로 마우스 오른쪽 버튼을 클릭해서 '형식변경' , '정수'로 바꿔준다.  
  ![10](https://user-images.githubusercontent.com/49367190/61266484-f494ba00-a7ce-11e9-9f94-6fd795cfd898.JPG)  
 8. '닫기 및 적용' 버튼을 클릭해서 창을 빠져나간다.  
![11](https://user-images.githubusercontent.com/49367190/61266463-f199c980-a7ce-11e9-9489-f3fdf8797ec6.JPG)  
 9. '필드'란에서 보고 싶은 데이터를 선택한다.  
![12](https://user-images.githubusercontent.com/49367190/61266464-f199c980-a7ce-11e9-83e8-a2f867fd9d1a.JPG)  
 10. '시각화'란에서 원하는 차트나 그래프 모양을 선택한다.  
![13](https://user-images.githubusercontent.com/49367190/61266465-f2326000-a7ce-11e9-9f00-47bf905f86f7.JPG)  
 11. ‘축’의 화살표를 눌러서 ‘Column 1 : timestamp’를 선택해 시간순으로 그래프를 띄운다.  
![15](https://user-images.githubusercontent.com/49367190/61266468-f2326000-a7ce-11e9-97b0-693469c901f5.JPG)
 12. 원하는 데이터를 추가해서 한꺼번에 띄울 수 있으며,  
![16](https://user-images.githubusercontent.com/49367190/61266469-f2caf680-a7ce-11e9-8679-5eb08dc6453f.JPG)
 13. 여러개의 그래프를 한 화면에 담아서 볼 수도 있다.  
![17](https://user-images.githubusercontent.com/49367190/61266470-f2caf680-a7ce-11e9-9d7e-0ed6b36ec09e.JPG)   

## 실시간 데이터 분석  

    실시간 데이터 세트의 형식  
    * 푸시 데이터 세트  
    Power BI desktop의 데이터가 Power BI 서비스로 푸쉬된다. Power BI 서비스는 데이터를 저장하는 데이터베이스를 자동으로 만들어 내며, 데이터 베이스가 있기 때문에 보고서를 데이터와 함께 만들 수 있다. 보고서를 만들고, 해당 시각적 개체 중 하나를 대시보드에 고정할 수 있다. 대시보드에서 시각적 개체는 데이터가 업데이트 될 때마다 실시간으로 업데이트된다.  

    * 스트리밍 데이터 세트  
    스트리밍 데이터 세트는 데이터를 임시 캐시에 저장하기 때문에 기본 데이터베이스가 없어   보고서 시각적 개체를 만들 수 없다.  스트리밍 데이터 세트를 시각화하는 유일한 방법은 타일을 추가하는 것이다. 스트리밍 시각적 개체는 데이터가 푸시 될 때와 시각화 될 때 사이의 대기 시간을 최소화하는 것에 최적화되어 있다.  

    * PubNub 스트리밍 데이터 세트  
    PubNub 스트리밍 데이터 세트를 사용하면 Power BI 서비스에서 저장하는 데이터가 없으며, 스트리밍 데이터 세트와 마찬가지로 Power BI에 기본 데이터베이스가 없으므로 흐르는 데이터에 대한 보고서 시각적 개체를 만들 수 없고 대시보드에 타일을 추가하여 시각화 할 수 있다.  Power BI는 PubNub 데이터 스트림에 직접 연결되어 있기 때문에 데이터가 Power BI서비스에 푸시될 때와 시각적 개체가 업데이트 될 때 사이의 대기 시간이 매우 짧다.   

    Power BI를 통한 실시간 데이터 분석 방법  
    * 예약된 새로 고침  
        * 로컬 파일에서 새로 고침  
        * 

    * 실시간 스트리밍  
    Power BI서비스에 로그인 한 후, '만들기'버튼을 클릭한다.
![슬라이드1](https://user-images.githubusercontent.com/49367190/61517291-dd113780-aa41-11e9-93c0-51d56226b6de.JPG)
    '스트리밍 데이터 세트' 버튼을 클릭한다.  
![슬라이드2](https://user-images.githubusercontent.com/49367190/61517292-dd113780-aa41-11e9-9355-865b5d06fb02.JPG)  
새 스트리밍 데이터 세트창에서 'API' 클릭
![슬라이드3](https://user-images.githubusercontent.com/49367190/61517293-dd113780-aa41-11e9-95c8-ed4a709a70fb.JPG)
내 데이터 안에 있는 정보로 값을 채운 후, '만들기'를 누른다.  
![슬라이드4](https://user-images.githubusercontent.com/49367190/61517294-dda9ce00-aa41-11e9-982d-9ec7deb66a5f.JPG)
푸쉬 URL이 생성된 것을 확인 할 수 있다.  이 URL을 복사하고, '완료'버튼 클릭
![슬라이드5](https://user-images.githubusercontent.com/49367190/61517295-dda9ce00-aa41-11e9-9884-8eb1dc0f776d.JPG)
내 작업 영역에서 '타일 추가' 버튼을 클릭한다.  
![슬라이드6](https://user-images.githubusercontent.com/49367190/61517296-dda9ce00-aa41-11e9-9a65-04505ac98972.JPG)
사용자 지정 스트리밍 데이터를 선택한 후, 만들었던 데이터 세트 이름을 클릭한다.  
![슬라이드7](https://user-images.githubusercontent.com/49367190/61517297-dda9ce00-aa41-11e9-9713-42fc6fa96198.JPG)
시각화 형식과 보고 싶은 데이터를 선택해준다.  
![슬라이드8](https://user-images.githubusercontent.com/49367190/61517299-de426480-aa41-11e9-8692-6229b35993d3.JPG)
REST API 에 아까 복사했던 URL을 넣은 뒤 실행시킨다.  
![슬라이드9](https://user-images.githubusercontent.com/49367190/61517300-de426480-aa41-11e9-83a8-3ed1f28d2158.JPG)
내 대시보드에 실시간으로 그래프가 그려진다.  
![슬라이드10](https://user-images.githubusercontent.com/49367190/61517290-dc78a100-aa41-11e9-9535-6ff4cb3bf154.JPG)

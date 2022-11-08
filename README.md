# cut-paste_image
<img width="491" alt="스크린샷 2022-11-08 오후 7 04 42" src="https://user-images.githubusercontent.com/90492809/200548864-ccb01711-1bdb-421b-842b-942ff45aaa78.png">


위성 영상을 가지고 짙은 구름, 옅은 구름, 구름의 그림자를 분할을 수행하는 데 있어, 부족한 데이터를 증대시키는 방법이다.

해당 방법은 구름 데이터에서 발생하는 문제점을 분석하고, 그 문제점을 해결하기 위해 고안하였다.
- 명확한 형태가 없는 옅은 구름과 그림자간 Trade-off 발생 가능성이 있다.
- 이미지 전체가 배경이거나 객체인 데이터가 다수 존재한다.

# 설명
<img width="469" alt="스크린샷 2022-11-08 오후 7 31 07" src="https://user-images.githubusercontent.com/90492809/200549053-a52865c2-ca66-4465-b224-0e61c3b0bfb4.png">

상기 방법은 배경만 있는 데이터를 선별한 후, 라벨 기반으로 다른 이미지에 있는 객체를 추출하여 선별한 배경 이미지에 합성하는 데이터 증대 방법이다.

## 1.배경 데이터와 객체 데이터 구분
<img width="421" alt="스크린샷 2022-11-08 오후 7 31 53" src="https://user-images.githubusercontent.com/90492809/200549234-2ad81c0a-c3c0-48a8-b127-70d1fec2b05b.png">

## 2.객체 데이터로부터 짙은 구름 추출
<img width="463" alt="스크린샷 2022-11-08 오후 7 34 13" src="https://user-images.githubusercontent.com/90492809/200549283-9f3f09d0-8d21-4b7c-9043-95cbf0e8f569.png">

## 3.배경 데이터에 짙은 구름 합성
<img width="535" alt="스크린샷 2022-11-08 오후 7 34 51" src="https://user-images.githubusercontent.com/90492809/200549348-d1ed33fe-cb3e-49c6-9d3f-593cad86c23d.png">

## 기타 : 가상 그림자 생성
<img width="460" alt="스크린샷 2022-11-08 오후 7 35 38" src="https://user-images.githubusercontent.com/90492809/200549397-69a10db4-593d-4aff-b028-c96ef569966d.png">

그림자에 대한 성능을 향상시키기 위해, 구름 라벨을 활용하여 가상 그림자를 생성하는 방법을 고안했으나, 실제 성능 향상에 영향을 주지 못하여, 추가 연구가 필요로 한다. 

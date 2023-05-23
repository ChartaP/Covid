# Covid
작품명	Covid


https://github.com/ChartaP/Covid/assets/20767587/83d9c4d3-259d-491c-aaf7-4ef83de8a917


# 장르
시뮬레이션 FPS
# 개요
현시점 유행하고 있는 코로나 바이러스에서 아이디어를 얻어 구상하여 바이러스의 전파 과정과 방역 방법을 게임으로 만들었습니다<br>
#조사	
![image](https://github.com/ChartaP/Covid/assets/20767587/c5d20cda-d6b0-412d-99f4-04d6fab9244c)<br>
![image](https://github.com/ChartaP/Covid/assets/20767587/8196af42-c415-472f-8c7a-dc2f00967e22)<br>
코로나19 자가격리 관련 국민인식조사 - 전문자료 | 정책DB | 대한민국 정책브리핑 (korea.kr)<br>
코로나 확산 상황에 대한 국민인식에 대한 설문조사를 참고하면 84.3%의 국민이 현상황이 심각하다고 생각하고 있으나 본인 감염 가능성에 대한 조사는 반반이 55.8%로 감염될 가능성에 대해서는 회의적으로 보입니다<br>
게임을 통해 코로나 방역을 직접 체험하여 현상황의 심각성과 방역수칙 준수의 중요성에 대해 느낄 수 있을 것으로 봅니다<br>

# 조작법
## 이동
WASD
## 시점
마우스
## 도구
### 선택
키보드 1,2,3
### 사용
마우스 왼쪽
## 시민 격리
F키
#구성요소	 
## 맵
![image](https://github.com/ChartaP/Covid/assets/20767587/de5e6ae9-54a8-4266-8591-b55d9e9e73d0)<br>
건물로 둘러싸인 정사각형 공간<br>

## 플레이어
![image](https://github.com/ChartaP/Covid/assets/20767587/de23b790-2b7e-4f85-aaab-2f0167521aa2)<br>
플레이어가 조종하는 캐릭터입니다<br>
머리 부분에 카메라를 배치시켜 1인칭을 구현하였습니다<br>
게임에 사용되는 세가지 도구를 투명한 상태로 배치하였습니다<br>

## 시민
![image](https://github.com/ChartaP/Covid/assets/20767587/69eeea65-d808-4153-8ebf-7b246c931143)<br>
AI컨트롤러에 의해 조종되는 캐릭터입니다<br>
물리적인 콜라이더 외에 추가로 전염에 사용되는 콜라이더가 추가로 배치되어있습니다<br>
마스크는 착용 여부에 따라 투명화합니다<br>
애니메이션은 걷기, 서있기, 사망 세가지 입니다<br>

## 격리소
![image](https://github.com/ChartaP/Covid/assets/20767587/2cb6278f-6d6b-44b3-9140-9eba1666c2b5)<br>
플레이어에 의해 격리된 시민이 들어가는 공간<br>
처음 들어가면 검사를 시작하고 음성, 양성을 판별합니다<br>
음성일 경우 맵으로 되돌려 보내고 양성일 경우 치료를 시작합니다<br>
치료를 마친 시민은 감염 변수가 false가 된 상태로 맵으로 돌아옵니다<br>
격리소의 수용량에는 한계가 있어 꽉차면 더 이상 격리하지 못합니다<br>

## 도구
플레이어가 특정 목적으로 사용하는 액터입니다<br>

## 체온계
![image](https://github.com/ChartaP/Covid/assets/20767587/46c26db2-01e8-44c8-9bfd-6a6d96a76234)<br>
시민의 체온을 검사하여 UI로 보여줍니다<br>
체온이 정상체온인지 아닌지를 텍스트로 보여줍니다<br>

## 마스크
![image](https://github.com/ChartaP/Covid/assets/20767587/52085bbf-a2a2-420d-b0ce-6895c9ece82a)<br>
시민에게 마스크를 주는 도구입니다<br>
마스크를 쓴 시민은 감염 확률이 크게 줄어듭니다<br>

## 화염방사기
![image](https://github.com/ChartaP/Covid/assets/20767587/8d849aac-5239-4f28-9bf9-41ac9a3aa88c)<br>
시민을 불태웁니다<br>
게임 후반 격리소가 꽉차서 급하게 처리해야하는 감염자를 처리할 수 있습니다<br>

# 규칙	
## 방역 실패
![image](https://github.com/ChartaP/Covid/assets/20767587/35d4f206-690f-408f-8585-2c63abae150a)<br>
모든 시민이 죽을 경우 발생하는 게임오버 이벤트입니다<br>
## 방역 성공
![image](https://github.com/ChartaP/Covid/assets/20767587/669e02f3-7e45-4cd3-a2fe-8a74d09993cf)<br>
살아있는 시민이 모두 건강할 때 발생하는 게임종료 이벤트입니다<br>
생존자 비율로 대처 등급을 부여합니다<br>

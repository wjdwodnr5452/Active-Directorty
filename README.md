# 가상머신과 가상머신 소프트웨어의 개념
- 진짜 컴퓨터에 설치된 운영체제(호스트 OS) 안에 가상ㅇ의 컴퓨터를 만들고, 그 안에 또 다른 운영체제 (게스트 OS)를 설치/운영 할 수 있도록 제작된 소프트웨어
<img width="1331" height="823" alt="image" src="https://github.com/user-attachments/assets/3ef9ee54-8be8-47ae-ac63-a3814cd0cab2" />


# Active-Directorty
- 일반적인 회사의 네트워크 상황을 Windows Server에서 구현하기 위한 기술
- 네트워크 상으로 나눠져 있는 여러 자원을 중앙의 관리자가 통합하여 관리함으로써, 본사 및 지사의 직원들은 자신의 PC에 모든 정보를 보관할 필요가 없어짐
- 타 지사에 출장을 가서도 자신의 아이디로 로그인만 하면 타인의 PC가 자신의 PC 환경과 마찬가지로 변경됨
- PC가 있는 장소와 무관하게 회사의 어디서든지 회사 전체 자원을 편리하게 사용
  <img width="565" height="515" alt="image" src="https://github.com/user-attachments/assets/20110d49-a1f8-41c0-bd0b-91c4a9e33877" />

## Active Directory 용어(1)

### Directory Service
- 분산된 네트워크 관련 자원 정보를 중앙의 저장소에 통합시켜 놓은 환경. 즉, 사용자는 중앙의 저장소를 통해서 원하는 네트워크 자원에 대한 정보를 '자동으로' 취득하여 그 자원에 접근할 수 있게 됨.

### Active Directory (약자로 AD)
- Directory Service를 Windows Server에서 구현한 것

### Active Directory 도메인 서비스 (AD DS)
- 컴퓨터, 사용자, 기타 주변 장치에 대한 정보를 네트워크 상에 저장하고 이러한 정보들을 관리자가 통합하여 관리하도록 해줌

## Active Directory 용어(2)
### 도메인 
- Active Directory의 가장 기본이 되는 단위. 그림에서 서울 본사, 부산 지사 등이 각각 하나의 도메인이라고 보면 됨.

### 트리(Tree)와 포리스트(Forest)
- 트리는 도메인의 집합. 포리스트는 두 개의 트리로 구성
- 도메인 < 트리 <= 포리스트의 관계
<img width="807" height="462" alt="image" src="https://github.com/user-attachments/assets/b0c3d3c5-a6d1-464f-a722-50b6475cf089" />

## Active Directory 용어(3)

### 사이트(Site)
- 도메인이 논리적인 범주라면, 사이트는 물리적인 범주. 사이트는 지리적으로 떨어져 있으며, IP 주소대가 다른 묶음 정도로 보면됨.

### 트러스트 (Trust)
- 도메인 또는 포리스트 사이에 신뢰할지 여부에 대한 관계를 나타내는 의미로 사용

### 조직 구성 단위
- 한 도메인 안에서 세부적인 단위로 나누는 것. (예로 부서 단위)

## Active Directory 용어(4)
### 도메인 컨트롤러 
- 로그인, 이용권한 확인, 새로운 사용자 등록, 암호 변경 그룹 등을 처리하는 기능하는 서버 컴퓨터. 도메인에 하나 이상의 DC를 설치.

### 읽기 전용 도메인 컨트롤러 (REad Only Domain Controller, 약자로 RODC)
- 주 도메인 컨트롤러로 부터 데이터를 전송받아서 저장한 후 사용하지만 스스로 데이터를 추가하거나 변경하지는 않음.
- 소규모로 운영되어서 별도의 서버 관리자를 두기가 어려울 경우 유용

### 글로벌 카탈로그
- 트러스트 내의 도메인들에 포함된

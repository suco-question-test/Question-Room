# Memo-App 배포 가이드

## 준비
![스크린샷 2025-01-10 오후 4 20 44](https://github.com/user-attachments/assets/d7cbdd5f-5b8e-4f7c-8185-17bb04e5685a)
### 메모앱이 로컬에서 구현 완료된 상태라고 가정하고 작성된 가이드입니다.
### venv(가상환경) 관련한 부분은 특정 케이스에서 필요한 요소이고, [install-related-python.md](https://github.com/suco-question-test/Question-Room/blob/main/install-related-python.md)에서 필요하신 분들은 이미 설정되어 있으실 겁니다. python 관련 패키지 설치에서 문제 겪지 않으신 분들은 무시해주셔도 무방합니다!

## 1.Github 저장소 연결
### 먼저 깃허브에 로그인해 빈 레포지토리를 하나 생성합니다.
![스크린샷 2025-01-10 오후 4 29 02](https://github.com/user-attachments/assets/b462dbee-7054-4e0f-9822-aa7bb419b912)
### 레포지토리명 입력해주시고, private으로 체크해주신 다음 생성해주시면 됩니다.
![스크린샷 2025-01-10 오후 4 30 49](https://github.com/user-attachments/assets/dc292c15-6252-4b09-8fee-a6e38f46b0ae)
### 링크 복사해주시고 다시 VSCode로 넘어가겠습니다.
![스크린샷 2025-01-10 오후 4 32 36](https://github.com/user-attachments/assets/18d13b88-828c-4b38-8651-7aefce1be0cd)
### 메모앱 프로젝트를 git 저장소에 초기 등록하기 위해 아래 명령어를 사용해줍니다.
```bash
git init
```
![스크린샷 2025-01-10 오후 4 38 04](https://github.com/user-attachments/assets/f3d2ce94-784b-4c95-9292-f27b4a923bba)
### 이제 방금 등록한 저장소를 아까 만든 레포지토리에 연결해주는데, 이때 아까 복사해둔 링크를 사용합니다.
```bash
git remote add origin 복사한 링크
```
![스크린샷 2025-01-10 오후 4 41 07](https://github.com/user-attachments/assets/f157dfff-eab1-4ccd-aeaa-5c8903202602)
### 잘 연결되었는지 확인하기 위해 작성된 메모앱 코드들을 깃허브에 푸쉬해보겠습니다.
### 이 때 venv(가상환경) 사용중이신 분들은 아래 .gitignore 추가하는 과정 하나 더 진행해주시고, 아닌 분들은 넘어가주시면 됩니다.
### 가상환경까지 깃허브에 저장할 필요는 없기 때문에 가장 위 폴더에 .gitignore 파일 하나 생성해주시고, venv/ 입력해주세요
![스크린샷 2025-01-10 오후 4 45 48](https://github.com/user-attachments/assets/d3158a7d-afb4-4600-b18d-29c7f5dbecbd)
### 자 이제 아래 명령어들을 순차적으로 실행해 푸쉬를 해보겠습니다. 아래 깃허브 푸쉬 과정은 깃허브 데스크톱 앱을 통해 진행해도 무방합니다.
### add와 .사이에 간격있으니 주의해주세요.
```bash
git add .
```
```bash
git commit -m "initial setting"
```
```bash
git push --set-upstream origin master
```

### 아래와 같이 깃허브 레포지토리에 파일들이 올라왔다면 성공입니다.
![스크린샷 2025-01-10 오후 4 59 58](https://github.com/user-attachments/assets/ca8ff061-268e-4e6e-a202-8647c1fef7a2)

## 2.배포
### cloudtype이라는 사이트를 이용해 배포를 진행해보겠습니다. 구글에 검색해 사이트에 접속해주세요.
![스크린샷 2025-01-10 오후 5 12 21](https://github.com/user-attachments/assets/5f382455-828b-47e3-99ce-0eb7ab7f8ce9)

### 우측 상단의 로그인 클릭 후 깃허브 계정으로 로그인을 클릭해줍니다. 이후 일련의 과정 진행해 로그인해주시면 아래와 같이 빈 시작 화면이 나옵니다.
![스크린샷 2025-01-10 오후 5 14 40](https://github.com/user-attachments/assets/6433e4fc-d55f-4e37-9480-9d4a706bc124)

### 가운데 + 눌러주시고, 팝업에서 Python FastAPI 템플릿 찾아줍니다.
![스크린샷 2025-01-10 오후 5 15 23](https://github.com/user-attachments/assets/73901d9b-a122-4775-98aa-075f574af747)

### 선택해주시면 아래와 같은 화면이 나오는데, 계정 연결 누르셔서 모든 레포지토리 선택하시고 확인 눌러주세요.
![스크린샷 2025-01-10 오후 5 16 27](https://github.com/user-attachments/assets/5e54459a-311b-4cab-bf93-565bb5cae076)

### 그러면 아래와 같은 화면 나오게되는데, 아까 만들어둔 레포지토리 선택해주시면 됩니다.
![스크린샷 2025-01-10 오후 5 18 00](https://github.com/user-attachments/assets/caf12f2d-b0b7-409a-811c-2cebb0753da7)

### 그러면 설정들이 자동으로 선택되는데 특별히 손 대실 부분은 없고, 결제수단을 등록해주셔야합니다. 
### 이후에 직접 유료버전으로 업그레이드 하지 않으시면 실제로 결제가 일어나진 않으니 걱정 안하셔도 됩니다.

### 이제 배포하기를 누르기 전에 메모앱에서 어떤 패키지가 필요한지 배포환경에게 알려주는 파일이 필요한데, VSCode에서 해당 파일 하나만 추가하고 배포하겠습니다.
### 최상단 폴더에 requirements.txt 파일 만들어 주시고 첫 줄에 fastapi, 두 번째 줄에 uvicorn 써주시고 저장해주세요.
![스크린샷 2025-01-10 오후 5 24 19](https://github.com/user-attachments/assets/659fc350-7c0c-4031-a0fb-7dfd41e9168f)

### 다시 아래 과정 하나씩 따라서 깃허브에 푸쉬해줍니다. 역시 깃허브 데스크톱 앱으로 진행하셔도 무방합니다.
```bash
git add .
```
```bash
git commit -m "add: requirements"
```
```bash
git push
```

![스크린샷 2025-01-10 오후 5 27 47](https://github.com/user-attachments/assets/5e2ccb17-f9c5-4302-a8c9-1f3404a88e7d)


### 이제 다시 cloudtype가서 배포하기 누르겠습니다. 아래 같은 화면 나오면 눌러서 상세정보로 들어가주세요.
![스크린샷 2025-01-10 오후 5 29 05](https://github.com/user-attachments/assets/b8692835-96ac-429d-b750-a59d2b2da305)

### 실행중으로 바뀌면 배포가 완료된 것입니다. 연결 탭에서 생성된 링크 누르시면 배포된 메모앱을 확인할 수 있습니다!
![스크린샷 2025-01-10 오후 5 30 34](https://github.com/user-attachments/assets/ad72953d-a935-4e2a-b55e-6d7f2de5c465)
![스크린샷 2025-01-10 오후 5 31 54](https://github.com/user-attachments/assets/ec1cb7b9-7ee3-4056-b713-f4928be771ca)

## 끝


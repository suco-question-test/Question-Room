# Mac에서 fastapi 및 uvicorn 설치

## fastapi 설치
![스크린샷 2025-01-10 오후 3 23 09](https://github.com/user-attachments/assets/bbd872ac-e222-4675-b2ba-10ef94fc95d9)
### 강의에서 나온대로 입력했는데 설치가 안되시는 Mac 유저분들! 
### Mac에서는 pip 대신에 pip3 명령어를 사용해주시면 됩니다.
![스크린샷 2025-01-10 오후 3 26 02](https://github.com/user-attachments/assets/a4d9c9d7-b0de-4a66-a73d-1c17391dca6e)
### 만약 pip3 명령어로 설치하려 할 때 위와 같은 에러가 나온다면 python을 Homebrew를 사용해 설치하신 경우입니다.
### Homebrew는 Python 환경을 관리하는 데 있어, 시스템 전역 설치로 인해 발생할 수 있는 충돌을 방지하기 위해 일부 보호 장치를 두기 때문에, 프로젝트 내에 가상환경을 만들어 필요한 패키지들을 설치하면 됩니다.


### 먼저 가상환경을 생성해주세요.
```bash
python3 -m venv venv
```
![스크린샷 2025-01-10 오후 3 54 50](https://github.com/user-attachments/assets/230ae6c6-9218-42b7-a5c6-f4de7ba490f5)
### 위와 같이 파일 탐색기에 venv폴더가 생성되면 성공입니다.


### 다음으로 가상환경을 활성화해주세요.
```bash
source venv/bin/activate
```
![스크린샷 2025-01-10 오후 4 02 16](https://github.com/user-attachments/assets/9975f0e5-7692-4220-9869-a1b01eefc9a2)
### 터미널 앞에 (venv)가 붙으면 성공입니다.


### 이 상태에서 fastapi 다운받아주시면 됩니다.
```bash
pip3 install fastapi
```

## uvicorn 설치
### uvicorn의 경우도 pip3명령어 사용해주시면 되는데, 강의와 같이 입력하시면
![스크린샷 2025-01-10 오후 4 13 22](https://github.com/user-attachments/assets/f47b9799-2c3e-41e6-b6e7-b03f04a199e9)
### 위와 같은 에러가 발생할 수 있습니다. uvicorn[standard] 부분 ''으로 감싸주세요.
```bash
pip3 install 'uvicorn[standard]'
```


## 끝

# jetson_manualdrive

# 설명

https://github.com/lsy0727/jetson_manualdrive/blob/dfe323ca7b526d774ec02bb711856946b7cfb226/main.cpp#L17-L29

jetson CSI카메라는 리눅스 드라이버에서 지원하지 않기 때문에 gstreamer명령어를 이용해 영상을 읽음.

src = 카메라를 초기화 하는 명령어 저장

-> 프레임, 영상 크기 등 정보 기입

VideoCapture 생성자의 인자로 gstreamer 명령어를 전달함.

https://github.com/lsy0727/jetson_manualdrive/blob/52596a943339e3536f341ed4680d3c1a8777592f/main.cpp#L31-L41

dst1 = gstreamer를 이용해 네트워크로 전송하는 명령어 저장(203.234.58.164 / 포트 : 8001)

-> 호스트의 주소와 포트번호를 기입

VideoWriter 생성자에 gstreamer 명령어 전달

https://github.com/lsy0727/jetson_manualdrive/blob/26285cca4589451b0f37bc9691614383c325d9ed/main.cpp#L43C5-L43C105



# 실행결과

https://www.youtube.com/watch?v=qNhwtKrqa1w

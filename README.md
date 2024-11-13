# jetson_manualdrive

# 설명

https://github.com/lsy0727/jetson_manualdrive/blob/20cffaf82f2f3381af0baf75fda3ffc6b98c0041/main.cpp#L17-L22

jetson CSI카메라는 리눅스 드라이버에서 지원하지 않기 때문에 gstreamer명령어를 이용해 영상을 읽음.

src = 카메라를 초기화 하는 명령어 저장

-> 프레임, 영상 크기 등 정보 기입

VideoCapture 생성자의 인자로 gstreamer 명령어를 전달함.



# 실행결과

https://www.youtube.com/watch?v=qNhwtKrqa1w

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

https://github.com/lsy0727/jetson_manualdrive/blob/6e715355ae32116cb5c08b2e3f7bc88b6011f675/main.cpp#L43

저장할 비디오파일 설정

파일이름 : manualdrive.mp4

VideoWriter::fourcc('X','2','6','4') : 비디오코덱-H.264, 비디오 압축 방식중 하나로 .mp4 파일 형식에서 자주 사용됨.

30 : 프레임

Size : 해상도

true : 컬러로 저장 (false이면 흑백으로 저장)

https://github.com/lsy0727/jetson_manualdrive/blob/8031e931f6d5d93e7ca159282d97dd4a3a3c544b/main.cpp#L61

영상 저장

https://github.com/lsy0727/jetson_manualdrive/blob/757e887b08abb12bcebe801e86ed4ea1d529261f/main.cpp#L64-L77

키보드로부터 키를 입력받으면 해당 동작을 수행함

https://github.com/lsy0727/jetson_manualdrive/blob/b791b68207945361e982473cfde1110bd4a185fb/main.cpp#L79-L84

급가속, 급감속을 방지하기위해 속도를 5단위로 제어함

https://github.com/lsy0727/jetson_manualdrive/blob/ee19055aafda2f547f4c75e561b3e2e32201d914/main.cpp#L87

ctrl+c입력시 프로그램 종료함

https://github.com/lsy0727/jetson_manualdrive/blob/79a2fef1cd0bb8ce4019ebcff390818620e14cea/main.cpp#L93

프로그램 종료시에 장치를 닫음

# 실행결과

https://www.youtube.com/watch?v=qNhwtKrqa1w

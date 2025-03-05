1번 문제
이미지 불러오기 및 그레이스케일 변환(opencv1_1.py)

설명
- OpenCV를 사용하여 이미지를 불러오고 화면에 출력.
- 원본 이미지와 그레이스케일로 변환된 이미지를 나란히 표시.

요구사항
- cv.imread()를 사용하여 이미지 로드.
- cv.cvtColor() 함수를 사용해 이미지를 그레이스케일로 변환.
- np.hstack() 함수를 이용해 원본 이미지와 그레이스케일 이미지를 가로로 연결하여 출력.
- cv.imshow()와 cv.waitKey()를 사용해 결과를 화면에 표시하고, 아무 키나 누르면 창이 닫히도록 할 것.

힌트
- OpenCV는 이미지를 BGR 형식으로 읽음.
- 그레이스케일 변환시 cv.COLOR_BGR2GRAY 사용.

2번 문제
웹캠 영상에서 에지 검출(opencv1_2.py)

설명
- 웹캠을 사용하여 실시간 비디오 스트림을 가져온다.
- 각 프레임에서 Canny Edge Detection을 적용하여 에지를 검출하고 원본 영상과 함께 출력.

요구사항
- cv.VideoCapture()를 사용해 웹캠 영상을 로드.
- 각 프레임을 그레이스케일로 변환한 후, cv.Canny() 함수를 사용해 에지 검출 수행.
- 원본 영상과 에지 검출 영상을 가로로 연결하여 화면에 출력.
- q 키를 누르면 영상 창이 종료.

힌트
- cv.Canny() 함수는 에지 검출에 사용되며, 하한/상한 임계값을 인자로 받음.
- cv.destroyAllWindows()를 사용해 창을 닫음.

3번 문제
마우스로 영역 선택 및 ROI(관심영역) 추출(opencv1_3.py)

설명
- 이미지를 불러오고 사용자가 마우스로 클릭하고 드래그하여 관심영역(ROI)을 선택.
- 선택한 영역만 따로 저장하거나 표시.

요구사항
- 이미지를 불러오고 화면에 출력.
- cv.setMouseCallback()을 사용하여 마우스 이벤트를 처리.
- 사용자가 클릭한 시작점에서 드래그하여 사각형을 그리며 영역을 선택.
- 마우스를 놓으면 해당 영역을 잘라내서 별도의 창에 출력.
- r 키를 누르면 영역 선택을 리셋하고 처음부터 다시 선택.
- s 키를 누르면 선택한 영역을 이미지 파일로 저장.

힌트
- cv.rectangle() 함수로 드래그 중인 영역을시각화.
- ROI 추출은 numpy 슬라이싱을 사용.
- cv.imwrite()를 사용하여 이미지를 저장.

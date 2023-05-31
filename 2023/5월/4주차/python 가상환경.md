파이썬 가상환경 -> 프로젝트별로 라이브러리, 파이썬버전 관리해주는 기능

가상환경을 사용하지 않고 그냥 라이브러리를 설치하면 
AppData\Local\Programs\Python\Python39\Lib\site-packages 에 설치된다


파이썬 가상환경 만들기
python -m venv 폴더이름

가상환경 진입하기
cmd에서 venv안에/Scripts폴더에서 activate
가상환경 나가기
deactivate
-> 배치파일로 편하게 진입가능


vscode 에서 파이썬 인터프리터 설정하기
F1 or Ctrl+Shift+P 누르고 Python Select Interpreter 입력하고 선택하기

가상환경폴더/Scripts/python.exe선택하거나
AppData\Local\Programs\Python\Python39\python.exe 선택하기

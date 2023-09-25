form태그 안에있는 버튼은 submit동작을 한다
form태그 안에있지 않은 버튼은 아무일도 하지 않는다

---
파이썬

가상환경 만들기 
python -m venv myproject

가상환경 진입하기
myproject/Scripts 에서 activate

가상환경 나가기
deactivate

pip은 파이썬 라이브러리를 설치하고 관리해 주는 파이썬 도구

플라스크에서 프로젝트는 하나의 웹사이트

플라스크 프로젝트 -> 한개의 웹사이트 생성, 한개의 애플리케이션이 존재함
플라스크 프로젝트 여러개 가능

pybo.py 와 pybo/__init__.py는 동일한 pybo 모듈이다.
create_app은 플라스크 내부에서 정의된 함수명이다.



---
## 파이썬 클래스

```python
class FourCal:
    # self에는 함수를 호출한 객체 자신이 들어간다
    # 자바스크립트랑 비슷?하네
    def __init__(self, first, second):
        self.first = first
        self.second = second
        
    def add(self):
        result = self.first+self.second
        return result
        
    def min(self):
        result = self.first-self.second
        return result
        
    def mul(self):
        result = self.first*self.second
        return result
        
    def div(self):
        result = self.first/self.second
        return result

  

# 클래스 상속
class PlusCal(FourCal):
    def exp(self):
        result = self.first ** self.second
        return result

# 메소드 오버라이딩
    def div(self):
        if self.second==0 :
            print("0으로 나눌수없습니다")
            return 0
        else:
            return self.first / self.second
  
a = PlusCal(4,0)

# a.first = 4이 실행된다, first변수가 생기면서 이때 값이 저장된다


print("a객체에 변수 추가하기??")
a.asdf = 3;
print(a.asdf)

# 오버로딩은 같은 이름의 함수를 매개변수를 다르게 해서 추가로 정의하는것
# 오버라이딩은 상속받은 자식클래스가 부모 클래스의 함수를 재정의하는것 (가려버린다, 무효화시킨다)
```

클래스는 붕어빵틀
객체는 붕어빵
만들어진 붕어빵은 서로에게 영향을 끼치지 않는다

## 객체와 instance의 차이
a 객체는 붕어빵 클래스(설계도)의 인스턴스이다
-> 인스턴스는 특정 객체가 어떤 클래스의 객체인지를 설명할때 사용한다
a는 인스턴스보다 a는 객체
a는 붕어빵클래스의 객체 보다 a는 붕어빵클래스의 인스턴스
라는 표현이 더 잘어울린다

클래스를 만들때는 객체중심으로 어떻게 동작하게 할건지 구상하면서 만들자

클래스 내부의 함수 = 메서드

파이썬에서 클래스의 메소드에서 첫번째 매개변수 self에는 함수를 호출한 자기자신 객체가 들어간다


setData같은 함수를 만들기 보다 생성자를 이용하자
생성자 = 객체가 생성될때 자동으로 호출되는 메서드
\_\_init__은 생성자!!

클래스변수  
인스턴스변수
// 자바 static은 클래스소속, non static은 인스턴스 소속
클래스 변수는 클래스로 만든 모든 객체에서 공유가능

자바스크립트처럼(?) 객체에 직접 객체변수와 값을 추가할수있다 

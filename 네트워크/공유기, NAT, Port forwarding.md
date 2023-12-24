공유기 = home router = 저용량의 라우터 + wireless access point

게이트 웨이 = 다른 네트워크로 나가기 위한 문, 가정에서는 공유기가 게이트웨이 역할을 한다

공유기는 isp로부터 받은 공인ip주소, default gateway ip주소(사설) 두 가지를 갖는다


사설 ip주소 -> default 게이트 웨이 , 공유기에 연결된 각 장치들이 사설 ip주소를 사용한다
외부에서는 사설ip주소로 해당 장치에 접근할 수 없다
라우터를 통해서 접근한 후 해당 특정 장치에 접근할 수 있도록 port forwarding을 한다
ex) 대표번호로 전화한 다음에 몇번을 눌러 내부 특정부서에 전화하기

리눅스에서
ip addr 로 자신이 쓰는 사설 ip확인 가능
ipconfig
```
curl ipinfo.io/ip // 공인 ip확인, 해당 사이트에서 HTML 전달해줌
```


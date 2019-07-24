[TOC]

# 8ython

##  키워드





### Errors and Exceptions



 EOL 오류(따옴표 오류)  End Of Line



OOP:  Object-Oriented Programming

객체지향프로그래밍



''형태화시킨것을 다룬다''는 목적을 위한 프로그래밍의 한 형태



- class

: 같은 종류의 집단에 속하는 attribute와 behavior을 정의한 것이다.



- instance

: 클래스의 instance/entity

객체는 자신 고유의 attribute를 가지며 클래스에서 정의된 method를 수행

클래스에 정의된 행위를 공유함으로써 메모리를 경제적으로 사용



- attribute

: class/instance가 가지고 있는 value



- method

: class/instance가 할 수 있는 methods





추상화

: Class가 가지는 공통적 특성을 만드는 것



캡슐화

: 외부적으로 바꿀 수 없도록 제한하는 것



상속

: 부모로부터 자식이 특정 method를 상속받는 것



다형성



```python
# Class = 설계도 정의

class TestClass(): 
    '''
    This is TestClass
    '''
    name = 'TestClass'

```



```python
# Instance 생성

# tc class 생성
tc = TestClass()
```



```python
# 생성된 Instance handling

method 사용
instance명.method()

attribute 값 확인
instance명.attribute명
```



self는 instance 객체 자기 자신을 가르킨다.






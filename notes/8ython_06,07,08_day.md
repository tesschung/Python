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





####  OOP advanced



**차이**

클래스 변수(붕어빵 틀)

: 인스턴스가 접근해서 가져간다.

인스턴스 변수(붕어빵)







## 인스턴스 메서드 / 클래스 메서드 / 스태틱(정적) 메서드

#### 인스턴스 메서드

인스턴스가 사용하는 메서드

- 정의 위에 어떠한 데코레이터도 없으면, 자동으로 인스턴스 메서드





#### 클래스 메서드

클래스가 사용하는 메서드

- 정의 위에 `@classmethod` 데코레이터를 사용
- **첫 번째 인자로 클래스(cls) 를 받도록 정의**
- **자동으로 클래스 객체가 cls**



```python
class MyClass:
    @classmethod
    def class_method_name(cls, arg1, arg2, ...):
        ...
```



#### 스태틱(정적) 메서드

클래스 안에서 정의가 되지만, 클래스나 인스턴스와 관계없는 일을 할때 사용하는 메서드

- 클래스가 사용할 메서드
- 정의 위에 `@staticmethod` 데코레이터를 사용
- 묵시적인 첫 번째 인자를 받지 않습니다. 즉, 인자 정의는 자유롭게 합니다.
- **어떠한 인자도 자동으로 넘어가지 않습니다.**





### 연산자 오버로딩(중복 정의)

```python
+  __add__   
-  __sub__
*  __mul__
<  __lt__
<= __le__
== __eq__
!= __ne__
>= __ge__
>  __gt__
```


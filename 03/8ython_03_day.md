[TOC]

# 8ython

##  키워드

함수 function

![built_in](C:\Users\student\development\8ython\03\03\built_in.png)

키워드 인자(Keyword Arguments)로 기본 값(Default Argument Values)을 설정할 수 있다.함수에서 키워드 인자는 항상 마지막에 선언된다

개수가 정해지지 않은 임의의 인자를 받기 위해서는 가변인자('*') 사용

*args





mutable: Set Dictionary List

immutable: Tuple String Range



함수에서는 다음과 같이 두가지 방법인,

-positional

-keyword

로 매개변수 지정





정의되지 않은 인자들 처리하기

**kwargs 사용법 익히기

**LEGB Rule**

Local scope -> Enclosed scope -> Global scope -> Built-in scope



**팩토리얼**계산

```python
'''
5에 대한 팩토리얼 계산은 아래와 같이 이뤄진다.
1*2*3*4*5 = 120
'''

def fact(n):
    result = 1
    while n > 1: 
        result = result * n # 처음 들어온 5는 5 * 1이다. 
        n -= 1 # 5에서 -1을 하고, 하나씩뺀 값들을 result에 담긴 값과 곱하면서 result를 반환한다.
    return result
        
fact(5)
```



#### [**재귀함수**](https://gomguard.tistory.com/111): 함수 내부에서 자기자신을 호출하는 함수

**재귀함수 예제 - 팩토리얼**

```python
def factorial(n):
    if n <= 1: # n이 1이하인 경우, 반환값을 준다.
        return # return value는 None으로 종료된다. 
    factorial(n - 1) #처음실행시 if에 들어가지 않아서 n에서 -, trigger
    print('이제 돌아왔어요.', n)
    
factorial(10)


def factorial(n):
    if n <= 1: #5는 1보다 크므로 False, 다음 실행
        return n
    else:
        return n * factorial(n - 1) 
        
factorial(5)
```

![img](https://t1.daumcdn.net/cfile/tistory/99C4D0405A3C724401)

**재귀함수 예제 - 카운트다운**

```python
def countdown(number):
    if number == 0:
        return number # base-case
    else:
        print(number)
        return countdown(number - 1)

print(countdown(10))
```

```python
10
9
8
7
6
5
4
3
2
1
0
```

![img](https://t1.daumcdn.net/cfile/tistory/994BBE4C5A3C78D317)

**재귀함수 예제 - 구구단출력**

```python
def multi_table(number, fixed_number=2):
    if number == 0:
        print('end')
    else:
        print(f'{fixed_number} * {number} = {fixed_number*number}')
        return multi_table(number - 1)

multi_table(9)
```

```python
2 * 9 = 18
2 * 8 = 16
2 * 7 = 14
2 * 6 = 12
2 * 5 = 10
2 * 4 = 8
2 * 3 = 6
2 * 2 = 4
2 * 1 = 2
end
```

반대로 출력

```python
# 반환값이 사라져서 출력 = base case를 지우고
# 함수로 재귀되었던 값을 출력
def multi_table2(number, fixed_number=2):
    if number == 0:
        print('0으로 돌아왔습니다.')
    else:
        multi_table2(number - 1)
        print(f'{fixed_number} * {number} = {fixed_number*number}')

multi_table2(9)
```

```python
0으로 돌아왔습니다.
2 * 1 = 2
2 * 2 = 4
2 * 3 = 6
2 * 4 = 8
2 * 5 = 10
2 * 6 = 12
2 * 7 = 14
2 * 8 = 16
2 * 9 = 18
```

![img](https://t1.daumcdn.net/cfile/tistory/991EB7475A3C6F152B)

- base case를 통해 함수에서 빠져나오도록 설정한다.



#### **피보나치수열**: 앞의 두자리를 계속 더해 다음값을 만들어나가는 수열

[https://shoark7.github.io/programming/algorithm/%ED%94%BC%EB%B3%B4%EB%82%98%EC%B9%98-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%EC%9D%84-%ED%95%B4%EA%B2%B0%ED%95%98%EB%8A%94-5%EA%B0%80%EC%A7%80-%EB%B0%A9%EB%B2%95.html](https://shoark7.github.io/programming/algorithm/피보나치-알고리즘을-해결하는-5가지-방법.html)

**단순한 단조 증가(monotonically increasing) 수열로 0번째 항은 0, 1번째 항은 1, 그 외 항은 전번, 전전번 항의 합으로 표현

![1563416978136](C:\Users\student\AppData\Roaming\Typora\typora-user-images\1563416978136.png)



```python
# [1, 1] 부터 쌓아가도록 만든다.
# (n-1)+(n-2)가 3번째부터의 수이다.
def fib(number):
    if number == 0 or number == 1:
        return 1
    else:
        result = fib(number - 1) + fib(number - 2)
        return result

print(fib(10))
```



#### 하노이탑




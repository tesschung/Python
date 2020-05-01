# Pythonic

https://www.python.org/dev/peps/pep-0008/





(1) Use 4 spaces per indentation level

```python
foo = long_function_name(var_one, var_two,
                         var_three, var_four)
```



(2) Limit all lines to a maximum of 79 characters.



(3) 연산자 위치

```python
# easy to match operators with operands
income = (gross_wages
          + taxable_interest
          + (dividends - qualified_dividends)
          - ira_deduction
          - student_loan_interest)
# 연산자가 함께 내려간다.
```



(4) Avoid extraneous whitespace in the following situations:

불필요한 공백은 지양한다.

```python
# Correct:
spam(ham[1], {eggs: 2})
# Wrong:
spam( ham[ 1 ], { eggs: 2 } )

# Correct:
foo = (0,)
# Wrong:
bar = (0, )

# Correct:
if x == 4: print x, y; x, y = y, x
# Wrong:
if x == 4 : print x , y ; x , y = y , x
    
# Correct:
ham[1:9], ham[1:9:3], ham[:9:3], ham[1::3], ham[1:9:]
ham[lower:upper], ham[lower:upper:], ham[lower::step]
ham[lower+offset : upper+offset]
ham[: upper_fn(x) : step_fn(x)], ham[:: step_fn(x)]
ham[lower + offset : upper + offset]
# Wrong:
ham[lower + offset:upper + offset]
ham[1: 9], ham[1 :9], ham[1:9 :3]
ham[lower : : upper]
ham[ : upper]

# Correct:
spam(1)
# Wrong:
spam (1)

# Correct:
dct['key'] = lst[index]
# Wrong:
dct ['key'] = lst [index]

# Correct:
x = 1
y = 2
long_variable = 3
# Wrong:
x             = 1
y             = 2
long_variable = 3

# = 의 양옆에 공백을 지양한다.
# Correct:
def complex(real, imag=0.0):
    return magic(r=real, i=imag)
# Wrong:
def complex(real, imag = 0.0):
    return magic(r = real, i = imag)
```



(5) 연산자의 경우 우선순위에 따라 공백이 이뤄진다.

```python
# Correct:
i = i + 1
submitted += 1
x = x*2 - 1
hypot2 = x*x + y*y
c = (a+b) * (a-b)
# Wrong:
i=i+1
submitted +=1
x = x * 2 - 1
hypot2 = x * x + y * y
c = (a + b) * (a - b)
```



(6) 되도록이면 같은 라인에 작성하지 않는다.

```python
# Correct:
if foo == 'blah':
    do_blah_thing()
do_one()
do_two()
do_three()
```

Rather not:

```python
# Wrong:
if foo == 'blah': do_blah_thing()
do_one(); do_two(); do_three()
```





(7) 함수/변수의 이름은 snake_case

```python
(good) def python_function_name(arg1, arg2):

    
(bad) def PythonFunctionName(arg1, arg2):
(bad) def pythonFunctionName(arg1, arg2):
```
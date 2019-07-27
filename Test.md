아리스토텔레스의 체 외우기

01 1

02 1

03 1

04 

07 

08

dict.get('key') 과 dict['key'] 차이
dict.remove('key') 와 dict.discard('key')의 차이



a.remove(x), a.pop(x), a.index(x), count(x)
중에 x가 의미하는 것이 다른것은?





boolean과 integer는 더할 수 있을까요?
print(True + 3) # True는 1로 인식되어진다.



append랑 extend차이

append - 리스트에 요소 추가



x = [1, 2, 3]

x.append([4, 5]) -> append의 object를 통째로 맨 뒤에 추가



결과 :

[1, 2, 3, [4, 5]]



extend - 리스트에 같은 배열로 추가(확장)

x = [1, 2, 3]

x.extend([4, 5]) - extend의 object 의 엘레멘트들을 추가

결과 :

[1, 2, 3, 4, 5]



list.sort()와 sorted(list)
list.reverse()와 reversed(list)





immutable: string tuple range

mutable: list set dictionary

**sequence**(ordered): string list tuple range

Unordered : set dictionary



0 False

1 True



LEGB

Local scope

Enclosed scope

Global scope

Built-in scope

'apple'.find('c'). -1

'apple'.index('c') error
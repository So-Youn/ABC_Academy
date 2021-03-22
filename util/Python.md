# Python

## 기초

* 변수

  * 특수문자, 공백 X
  * 시작을 숫자로 X

* 정수로 구성된 정수형과 소수점이 있는 실수형 - `float`

  * 변수나 데이터 형 `type()`

  ```markdown
  문자 : 'a' 'b' 'c'
  문자열 : 'abc' '안녕하세요'
  불 : True, False
  ```

* 숫자 연산

  ```python
  y = 10/5 # 2.0 (수식은 실수로 리턴)
  x = 7//3 # 2 (소숫점 이하 절삭)
  z = 2 ** 3 # 8 거듭제곱
  ```

## 문자열

* `len` : 문자열 길이

* `+` : 문자열 두개 연결

* `str()` : 숫자일 경우 String 변환

  ```python
  eng = 80
  result = '영어점수' + str(eng) + '점'
  ```

* 문자열 포맷팅

  * `%` 를 이용해 문자가 여러 개일때 좀 더 간결하게 표현 가능

    | 포맷기호 | 데이터 형                          |
    | -------- | ---------------------------------- |
    | `%d`     | 정수형 숫자                        |
    | `%s`     | 문자열                             |
    | `%f`     | 실수형 숫자(6자리)                 |
    | `%05d`   | 정수형 5자리, 남는 부분 0으로 채움 |
    | `%.2f`   | 소수점 둘째 자리의 실수형          |

    ```python
    name = '박보검'
    a = '나는 %s입니다.' %name
    
    age = 30
    a = '나이는 %d' % age
    
    year = 2021
    month = 1
    day = 7
    a = '%d-%02d-%02d'%(year,month,day) # 2021-01-07
    ```

* 문자열 메소드

  * 문자열에 특화되어 문자열 자료형을 다양하게 처리 가능

  ```python
  str.format() # 문자열 포매팅
  str.count() # 문자열 갯수 세기
  str.find() # 문자열 내부 특정 문자열 찾기
  str.upper() # 대문자 변환
  str.lower() # 소문자 변환
  str.replace() # 문자열 내부 특정 문자열 바꾸기
  str.split() # 문자열 분리
  str.isspace() # 문자열 공백 체크
  ```

  ```python
  name = '홍길동'
  age = 30
  eyesight = 1.0
  
  a = '이름:{}'.format(name)
  b = '나이: {}세'.format(age)
  c = '시력: {}'.format(eyesight)
  print(name.count('홍'))
  print('이름: {}, 나이:{}'.format(name,age))
  
  print(name,age,eyesight, sep='/') # sep='/' 중간 구분자 삽입
  
  print(name, end=' ')
  print(age) # 홍길동 30
  ```

  ## 리스트

  * 리스트명 = [데이터,데이터,데이터,...]
  * 리스트명  = list(range(시작값,종료값,증가))
  * 2차원_리스트명=[[데이터,데이터], [데이터,데이터], ...., [데이터,데이터]]

  ```python
  append(x) # 요소 추가
  sort() # 정렬
  reverse() # 역순
  index(x) # x위치값 변환
  insert(a,b) # a번째 위치에 b추가
  remove(x) # 리스트에서 첫번째로 나오는 x 반환
  pop(x) # 만 마지막 요소 반환 후 삭제
  count(x) # 리스트 내 'x' 갯수 반환
  ```

  ```python
  # 확장
  list.append(요소)
  list.insert(index,요소)
  list1.extend(list2)
  list1+list2
  # 삭제
  del list[2] # 특정 인덱스의 요소 삭제
  
  a = [10,20,30,40]
  x = a.index(30)
  print(X) # 2
  # pop -index , remove - 요소
  a.pop(x)
  print(x) # [10,20,40]
  
  a.remove(40) # [10,20]
  
  a.clear() #  초기화
  ```

  ```python
  # 리스트 정렬
  list = [-7,1,5,8]
  list.sort()
  list.sort(reverse = True)
  ```

  

## 튜플

* 리스트와 유사
* 튜플에서 리스트의 대괄호`[]` 대신 `()` 사용
* 튜플에서는 리스트와 달리 수정 / 추가 불가

```python
menu = ('coffee', 'milk', 'tea')
menu[1] = 'cola' XXXXXXX
# 튜플의 병합
tuple3 = tuple1 + tuple2
# 튜플 자체를 삭제
del tuple1
```

```mark
1. 튜플은 반복 처리 시 리스트에 비해 근소하게나마 빠르다
2. 튜플은 요소를 변경할 수 없는 특성으로 인해 딕셔너리의 키로 이용 가능
3. 보안을 요하는 데이터를 보호하는 장점
4. 리스트에 변경이 없는 경우라면 튜플 사용!
```

## 딕셔너리

* 사전이 단어와 뜻으로 구성되듯, `key`와 `value`의 쌍으로 구성

  * `key` : `value`

  ```python
  members = {'name':'안지영', 'age':30, 'email':'~'}
  print(members['name'])
  ```

  

## 집합

* **중복을 허용하지 않으며**, **순서가 없는** 자료 구조
  * print 사용해서 출력하면 기존 자료구조와 다르게 출력된다.
* 집합에 관련된 것을 쉽게 처리하기 위해 만든 자료형
* 집합은 `{}` 사용해서 만든다
* 중복 제거를 위해 사용된다.

```python
set1 = set([1,2,3])
print(set1) # {1,2,3}

set2 = set("Hello")
print(set2) {'H','e','l','o'}

# 값 x 추가
add(x)
# 여러 개의 값을 추가 할 때 사용, x 는 리스트
update(x)
# x 요소 제거
remove(x)
```

| 구분   | 키워드                  |
| ------ | ----------------------- |
| 합집합 | `|` 또는 `union`        |
| 교집합 | `&` 또는 `intersection` |
| 차집합 | `-` 또는 `difference`   |



## 리스트, 튜플,딕셔너리,셋 차이

| 리스트       | 순서대로 정리된 항목들을 담는 자료 구조                      |
| ------------ | ------------------------------------------------------------ |
| **튜플**     | 리스트와 비슷하지만 수정이 불가<br />비정적인 객체 담는데 사용 |
| **딕셔너리** | key와 value로 구성되는 자료 구조                             |
| **집합**     | 중복 허용 X, 순서 X                                          |


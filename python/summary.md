# Summary
Python summary

## 목차
1. [사전 지식](#사전-지식)
2. [사칙연산](#사칙연산)
3. [자료형](#자료형)
    - [숫자](#숫자)
    - 문자열
    - 리스트
4. 변수
5. 문자열
6. 리스트
    - 기초
    - 활용
    - 표현식
    - 2차원 리스트
7. 튜플
8. 출력
9. 입력
10. 조건문
11. 반복문
    - 반복문 for
    - 반복문 while
12. [함수](#함수)

## 사전 지식


## 사칙연산
>더하기 `+`, 빼기 `-`, 곱하기 `*`, 나누기 `/`, 몫 `//`

계산기에 입력할 때 처럼 숫자와 기호를 입력하면 결과값이 출력된다.   
```python
>>> 3 + 5
>>> 10 - 7
>>> 8 * 6
>>> 10 / 3 # 3.3333...
>>> 10 // 3 # 3
```

## 자료형

### 숫자
정수, 실수, 복소수 등

### 문자열
문자 표현


## 변수


## 문자열


## 리스트
리스트 소개 및 활용

### 소개
- 한번에 여러 값을 처리, 저장할 경우 사용
- 여러 값을 나열된 순서대로 저장
- 각 항목을 가져올 때의 번호(인덱스)는 0부터 시작
- 타입이 다른 값들 넣어도 됨

```python
변수명 = [값1, 값2, 값3, ...]
변수명 = list() # 빈 리스트 생성하여 할당
items = [
    'one',
    'two',
    3,
    [ 1, 2, 3, 4 ]
]
```
- 변수 생성
    ```python
    # 1. 숫자값
    nums = [1, 2, 3, 4]
    nums[1:3]   # [2, 3]

    # 2. 문자열
    strs = ['apple', 'melon']

    # 3. 두 리스트 합하여 새로운 리스트 생성
    combineList = nums + strs
    ```

- 항목 변경
    ```python
    nums = [1, 2, 3, 4]

    nums[2] = 5     # [1, 2, 5, 4]
    nums[0] = 0     # [0, 2, 5, 4]
    ```

- 각 요소 방문
    ```python
    nums = [1, 2, 3, 4]

    # 1. 절댓값
    for i in range(4) :
        num = nums[i]
        실행문1
        실행문2

    # 2. len()
    for i in range( len(nums) ) :
        num = nums[i]
        실행문1
        실행문2

    # 3. 리스트
    for num in nums :
        실행문1
        실행문2
    ```

- 특정값 포함 여부
    ```python
    nums = [1, 2, 3, 4]

    if 2 in nums :
        print('2 존재함')
    ```

- 문자열을 특정 구분자 기준으로 분리한 리스트 변환
    ```python
    wordsStr = 'apple-ball-camera'
    wordsList = wordsStr.split('-')    # ['apple', 'ball', 'camera']
    ```

- 리스트 복사
    |일반 변수|리스트 변수|
    |:---:|:---:|
    |변수 값 복사하여 할당|변수 주소 할당|
    |call by value|call by reference|
    |`num2 = num1 # 값 다름`|`num2 = num1 # 값 같음(주소 공유)`|

    ```python
    num1 = [1, 2, 3, 4]
    num2 = num1.copy()
    ```

### 활용
리스트 메소드
>- 객체 Object
>    - 물건, 사물, 대상
>    - 고유한 특징을 가지는 데이터를 저장한 속성 Attribute + 속성으로 조작하는 행위인 메소드 Method
>    - ex. button
>        |속성 Attribute|메소드 Method|
>        |:---:|:---:|
>        |크기, 색, 글자, ...|클릭한다, 더블클릭한다, ...|
>- 클래스 Class
>    - 객체가 가지고 있는 속성, 메소드 정의
>    - 객체를 만들기 위한 설계도
- 항목 추가
    |함수|설명|
    |:---:|:---:|
    |`append(value)`|맨 마지막에 추가|
    |`insert(index, value)`|특정 위치에 추가|
    |`extend(list)`|맨 마지막에 리스트 추가|

    ```python
    num = list()            # []
    num.append(5)           # [5]
    num.append('test')      # [5, 'test']
    num.insert(0, 10)       # [10, 5, 'test']
    num.extend([20, 30])    # [10, 5, 'test', 20, 30]
    ```

- 항목 삭제
    |함수|설명|
    |:---:|:---:|
    |`pop(index)`|특정 위치 값 삭제, 값 없으면 맨 마지막 값 삭제|
    |`remove(value)`|특정 값 중 첫번째 값 삭제|
    |`clear()`|전체 삭제|
    ```python
    data = [10, 5, 'test', 20, 30]
    data.pop(1)     # [10, 'test', 20, 30]
    data.remove(20) # [10, 'test', 30]
    data.clear()    # []
    ```

- 항목 검색
    |함수|설명|
    |:---:|:---:|
    |`index(value, [,start, end])`|특정 범위에서 값 찾으면 인덱스 리턴, 없으면 에러|
    |`count(value)`|특정 값이 리스트에 존재하는 개수|
    ```python
    fruits = ['melon', 'strawberry', 'melon']
    fruits.index('strawberry')  # 1
    fruits.index('melon')       # 0
    fruits.index('melon', 1)    # 2
    fruits.count('melon')       # 2
    ```

- 정렬   
    [sort() 더 알아보기(공식 doc)](https://docs.python.org/ko/3/library/stdtypes.html?highlight=sort#list.sort)
    |함수|설명|
    |:---:|:---:|
    |`sort()`|리스트 항목들 오름차순/내림차순으로 정렬, 원본 변경(오름차순시 알파벳은 대문자 먼저)|
    |`reverse()`|리스트 항목들 역순으로 변경(크기에 따른 정렬X)|
    ```python
    nums = [1, 5, 3, 8, 15, 7]
    chars = ['M', 'e', 'l', 'o', 'n', 'm']

    # 1. 오름차순
    nums.sort()     # [1, 3, 5, 7, 8, 15]
    chars.sort()    # ['M', 'e', 'l', 'm', 'n', 'o']

    # 2. 내림차순
    nums.sort(reverse = True)       # [15, 8, 7, 5, 3, 1]
    chars.sort(reverse = True)      # ['o', 'n', 'm', 'l', 'e', 'M']

    # 3. 역순
    nums.reverse()      # [7, 15, 8, 3, 5, 1]
    chars.reverse()     # ['m', 'n', 'o', 'l', 'e', 'M']

    # 4. 대소문자 구분X
    chars.sort(key = str.lower)     # ['e', 'l', 'M', 'm', 'n', 'o']
    ```

- 집계함수 : 파이썬 내장 함수
    |함수|설명|
    |:---:|:---:|
    |`min(list)`|리스트 항목들 중 가장 작은 값|
    |`max(list)`|리스트 항목들 중 가장 큰 값|
    |`sum(list)`|리스트 항목들의 합|
    |`len(list)`|리스트 항목 개수|
    |`map(fn, list)`|리스트 각 항목에 특정 함수 적용하여 결과 반환, list로 casting 필요|
    |`sorted(list, reverse=True/False)`|원본 변경하지 않고 정렬한 리스트 결과 반환|
    ```python
    num = ['10', '20', '30', '40']
    strToNum = list( map(int, num) )    # 각 항목을 숫자형으로 변환
    ```


### 표현식
리스트 생성

### 2차원 리스트
2차원 리스트 소개


## 튜플
튜플, 딕셔너리


## 출력
화면에 보여주기
```python
print('화면에 출력')
```


## 입력
변수에 데이터 입력
```python
usrData = input('입력 : ')
```


## 조건문
조건에 따라 선택적인 명령을 실행한다.
```python
if 조건 :
    실행문
elif 조건 :
    실행문
else :
    실행문
```

### 조건문에서의 연산자
- 비교 연산
- 논리 연산


## 반복문
같은 패턴의 명령을 반복해서 실행한다.

### 반복문 for
```python
for 변수 in 반복범위 :
    실행문1
    실행문2
    ...
```
- 반복범위 : 숫자, 문자열, 리스트, ... 가능하다!
- range(start = 0, end, step = 1)   
반복 범위 지정  
start, step 생략 가능  
    |값|기본값|
    |:---:|:---:|
    |start|0|
    |step|1|
    ```python
    range(5)        # 0, 1, 2, 3, 4
    range(1, 5, 2)  # 1, 3 (1부터 5 전까지 2만큼 증가)
    ```
- 예시
    ```python
    # ex1. 숫자
    for i in range(3) :
        print('%d번째 루프' %i)
    # 0번째 루프
    # 1번째 루프
    # 2번째 루프

    # ex2. 문자열
    for ch in 'abcd' :
        print(ch)
    # a
    # b
    # c
    # d

    # ex3. 리스트
    for item in ['월', '화', '수', '목'] :
        print(item)
    # 월
    # 화
    # 수
    # 목
    ```

### 반복문 while
```python
while 조건문 :
    실행문1
    실행문2
    if 나갈조건 :
        break
    ...
```


## 함수
특정한 기능을 수행하는 명령어들의 집합을 묶어놓은 것이다.
```python
def 함수명([매개변수1, 매개변수2, ...]) :
    실행문1
    실행문2
    ...
    [return 결과값1, 결과값2, ...]
```
- 위치 인수 vs. 키워드 인수
    ```python
    # 아래와 같은 함수가 있을 경우
    def intro(name, age) :
        실행문...
    ```

    |위치 인수|키워드 인수|
    |:---:|:---:|
    |매개변수 순서 기준|매개변수 명 기준|
    |`intro('josh', 28)`|`intro(age=28, name='josh')`|





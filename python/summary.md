# Summary
Python summary

## 사전 지식



## 사칙연산 : 더하기 `+`, 빼기 `-`, 곱하기 `*`, 나누기 `/`, 몫 `//`
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

### 리스트

## 변수

## 문자열

## 리스트

## 출력 : 화면에 보여주기
```python
print()
```

## 입력 : 변수에 데이터 입력

## 조건문


## 반복문
같은 패턴의 명령을 반복해서 실행

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
start의 default: 0  
step의 default: 1
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





##### Q1. 다음 코드의 결과값은 무엇일까?


```python
a = "Life is too short, you need python"

if "wife" in a: print("wife")
elif "python" in a and "you" not in a: print("python")
elif "shirt" not in a: print("shirt")
elif "need" in a: print("need")
else: print("none")
```

    shirt
    

##### "wife"는 a 문자열 안에 없으므로 False
##### "python"은 a 문자열 안에 있으나 and조건으로 연결된 "you"는 a 문자열에 있으므로 False
##### "shirt"는 a 문자열에 없으므로 True
##### "need"는 a 문자열에 있으므로 True
##### 가장 먼저 True인 "shirt"가 출력됨.

##### Q2. while문을 사용해 1부터 1000까지의 자연수 중 3의 배수의 합을 구해 보자.


```python
sum = 0 # 합을 담을 변수
i = 1 # 증가
while i <= 1000:
    if i % 3 == 0:
        sum += i
    i += 1

print(sum)   
```

    166833
    

##### Q3. while문을 사용하여 다음과 같이 별(*)을 표시하는 프로그램을 작성해 보자.


```python
*
**
***
****
*****
```


```python
i = 0  # 증가
while True:
    i += 1  # 1씩 증가
    if i > 5:
        break # i값이 5보다 크면 break 
    print(i*"*") # i만큼 "*"출력
```

    *
    **
    ***
    ****
    *****
    

##### Q4. for문을 사용해 1부터 100까지의 숫자를 출력해 보자.


```python
for one in range (1,101):
    print(one)
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    11
    12
    13
    14
    15
    16
    17
    18
    19
    20
    21
    22
    23
    24
    25
    26
    27
    28
    29
    30
    31
    32
    33
    34
    35
    36
    37
    38
    39
    40
    41
    42
    43
    44
    45
    46
    47
    48
    49
    50
    51
    52
    53
    54
    55
    56
    57
    58
    59
    60
    61
    62
    63
    64
    65
    66
    67
    68
    69
    70
    71
    72
    73
    74
    75
    76
    77
    78
    79
    80
    81
    82
    83
    84
    85
    86
    87
    88
    89
    90
    91
    92
    93
    94
    95
    96
    97
    98
    99
    100
    

##### Q5. A 학급에 총 10명의 학생이 있다. 이 학생들의 중간고사 점수는 다음과 같다.
##### for문을 사용하여  A학급의 평균 점수를 구해 보자.


```python
class_a = [70, 60, 55, 75, 95, 90, 80, 80, 85, 100]
```


```python
total = 0
for one in class_a:
    total += one

avg = total/len(class_a)
print("A학급의 평균점수는 {}입니다.".format(avg))
```

    A학급의 평균점수는 79.0입니다.
    

##### Q6. 리스트 중에서 홀수에만 2를 곱하여 저장하는 다음 코드가 있다.
##### 아래 코드를 리스트 내포(list comprehension)를 사용하여 표현해 보자.


```python
numbers = [1, 2, 3, 4, 5]
result = []
for n in numbers:
    if n % 2 == 1:
        result.append(n*2)
        print(result)
```

    [2]
    [2, 6]
    [2, 6, 10]
    


```python
numbers = [1, 2, 3, 4, 5]
result = [n*2 for n in numbers if n % 2 == 1]
print(result)           
# 보충
```

    [2, 6, 10]
    


```python
참조) 점프 투 파이썬 https://wikidocs.net/42526
```

# 멀티캠퍼스_TIL



## Python 문법 

### Unit 04. 기본 문법

#### 세미콜론

```python
print('hello') ; print('world')
```

세미콜론으로 코드를 여러 줄 작성 가능 

#### 주석 

- # 
- ''' ''' 

#### 들여쓰기 



### Unit 05. 숫자 계산

#### 몫과 나머지 

```python
divmod(5,2) #몫과 나머지 함께 구하기 
```

#### 진수 

```python	
# 진수, 8진수, 16진수 

# 2진수 : 숫자 앞에 0b 붙임 
print(0b110)

# 8진수 : 숫자 앞에 0o을 붙임
print(0o10)

#16진수 : 숫자 앞에 0x 또는 0X 붙이며 0~9, A~F 까지 사용 

print(0xF)

```

#### 복소수 

```python
# complex 사용 
complex(1.2, 1.3)
```





### Unit 06. 변수와 입력

#### 변수 삭제하기 

`del 변수명`

 

### Unit 07. 출력 방법 

#### 줄바꿈 

`\n`



#### 출력 마지막 

``` python
print(1, end = '')
print(2, end ='')
print(3)
```



### Unit 10. 리스트와 튜플 사용하기

#### 리스트와 튜플 언패킹 

``` python
x = [1,2,3]
a, b, c = x 
print(a, b, c)

x = (4, 5, 6)
a, b, c = x 
print(a, b, c)
```



### Unit 12. 딕셔너리 

#### 딕셔너리 생성

```python
lux = {'he' : 490, 'ma' : 334, 'me' : 550, 'ar' :18.72 }
lux2 = dict(zip(['health', 'mana', 'melee', 'armor'], [490, 334, 550, 18.72])) 
lux3 = dict([('health', 490), ('mana', 334), ('melee', 550), ('armor', 18.72)])
lux4 = dict({'health': 490, 'mana': 334, 'melee': 550, 'armor': 18.72}) 
```





### Unit 22. 리스트와 (튜플) 응용하기

#### 리스트 합치기 

`extend(합칠 리스트)`



#### 리스트 요소 추가 

`insert(인덱스, 요소)`



#### 리스트 요소 삭제 

`pop(인덱스)` 빈 상태이면 마지막 요소만 삭제하고 반환 

`del 리스트[인덱스]`



#### 리스트 특정 값 

`remove(값)` 특정 값 삭제 

`index(값)` 특정 값 인덱스 반환 

`count(값)` 특정 값 개수 반환 



#### 리스트 순서 

`reverse()` 순서 뒤집기 

`sort()` 순서 정렬 

`sorted(리스트)` 순서 정렬 



#### 인덱스와 값 같이 출력 

```python
# 인덱스랑 같이 출력하기 

for index, value in enumerate(a) :
    print(index, value)
    

# 인덱스를 1부터 시작하게 해주려면?? 
for index, value in enumerate(a, start = 1) :
    print(index, value)
    
```



#### 리스트 표현식 

``` python
# 리스트 표현식 사용하기 
a = [i for i in range(10)]
print(a)


# 리스트 표현식에서 if 조건문 사용하기 
a = [i for i in range(10) if i%2 == 0]
print(a)

# for 문과 if 조건문을 여러 번 사용하기 
a = [i*j for j in range(2,10) for i in range(1, 10)]
print(a)
```



### Unit 23. 2차원 리스트 사용하기 

#### 2차원 리스트 출력 

``` python
a = [[10, 20], [30, 40], [50, 60]]
for x, y in a : 
    print(x,y)
```



#### for 문으로 2차원 리스트 생성 

```python
a = []
for i in range(10) : 
    line = []
    for j in range(3) : 
        line.append(j) 
    a.append(line)

print(a)


# 표현식으로 생성 
a = [[0 for j in range(3)] for i in range(4)]
print(a)
```



#### 심사문제 : 정규 표현식 

``` python
import re # 정규 표현식 모듈 
text = '''
the grown-ups' response, this time, was to advise me to lay aside my drawings of boa constrictors, whether from the inside or the outside, and devote myself instead to geography, history, arithmetic, and grammar. That is why, at the, age of six, I gave up what might have been a magnificent career as a painter. I had been disheartened by the failure of my Drawing Number One and my Drawing Number Two. Grown-ups never understand anything by themselves, and it is tiresome for children to be always and forever explaining things to the.
'''
text = re.sub("[\'-.,\n]",'', text) #'.,\n은 전부 공백으로 바꾸라는 것 
text 
```





### Unit 24. 문자열 사용하기 

#### 문자열 리스트 연결하기 

``` python
' '.join(['a', 'p','l'])
```

#### 공백, 특수문자 제거하기 

`strip('.,')`

#### 문자열 정리하기 

`.ljust()` 좌측 정렬

#### 서식 지정자 

``` python
# %s string 
'I am %s.' % 'hakyoung' 

# %d number 
'I am %d years old' % 25

# %f 소수점 
'%.4f' % 2.3

# 서식 지정자로 문자열 정렬하기 
# 문자 길이 설정 
'%10s' % 'python'

# 여러 개 같이 사용
'Today is %d %s' % (3, 'April')
```

#### 문자열 포매팅 

``` python
lan = 'python'
ver = 3.6 

f'Hello, {lan}, {ver}'

# format 메서드로 문자열 정렬하기 
'{0:<10}'.format('python') # 왼쪽 정렬 10글자 
```





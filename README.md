# TIL (Today I Learned)
--- 
## [Python] 

#### REPL
1. Read : (코드를) 읽어서
2. Eval : (읽은 코드를) 평가(실행)하고
3. Print : (실행한 결과를) 출력하는
4. Loop : 루프 (반복) 

#### PowerShell
- **pwd**(Print Working Directory) : 현재 디렉토리(폴더)를 출력함.
- **ls**(List Segments) : 현재 폴더 내용물 출력.
- **cd**(Change Directory) : 다른 폴더로 이동.(**cd 이동할폴더명**)
  - **cd ..** : 상위 폴더로 이동. 
- **cp**(Copy) : 파일을 다른 이름으로 복사.(**cp 복사할원본파일명 복사해서만들새파일명**)
- **rm**(Remove) : 파일 삭제.(**rm 삭제할파일명**)휴지통 없이 바로 삭제되니 주의!!! 
- Tip) 파일이름을 두세글자만 쓰고 **Tab** 키를 누르면 자동완성됨 
- **python 파일명.py** : 실행 

#### if, elif, else
```py
if 조건식:
    실행할 코드
elif 조건식:
    실행할 코드
else:
    실행할 코드
```

#### 함수
- 함수는 코드의 덩어리에 이름을 붙인 것.
- 우리는 새 함수를 만들 수 있다.
- print는 미리 만들어진 함수이다.
- 함수는 한 번 만들고 나면, 그 안은 잊어버려도 좋다.
  - 우리는 한 번도 print의 안을 고민한 적이 없다.
- 매개변수를 이용하면 값을 전달받는 함수를 만들 수 있다. 
```py
def 함수명():
    내용
함수명()
```
```py
def 함수명(파라미터):
    내용
    return 반환값
print(함수명(실행인자))
```
-> 내용이 출력됨. 

- **매개변수(parameter)** : 함수 정의에서 사용하는 이름
- **실행인자(argument)** : 실행할 때 넘기는 값
  - => 양 쪽의 갯수는 일치. 여러개일 때는 쉼표로 구분. 
- 함수의 **return**
  - 함수는 return을 이용해 값을 돌려줄 수 있다.
  - 함수를 사용하는 것은 함수 안의 코드를 모두 실행한 뒤, 이 함수의 자리에 return에 있는 값을 넣은 것과 같다.
  - 여러 값을 반환하려면, return 뒤에 여러 값을 쉼표로 나누어 넣는다.

#### 사용자 입력
- 사용자의 키보드 입력을 return하는 함수(print 기능을 내장하고 있음.)
```py
input('text')
```
와
```py
print('text', end = '')
input()
```
는 같은 결과를 냄.
- Ctrl + C 로 프로그램 즉시 종료 가능. 

#### 리스트 
- **.append**
```py
list.append(16)
```
- **in**
```py
n = 10
if n in list:
  print("{}은 있어".format(n))
```
- **del**
```py
del list[4]
```
- **.remove**: 같은 값이 여러개 있는 경우, 가장 먼저 나오는 값 하나만 지워짐.
```py
list.remove(4)
```

#### for 반복문 
##### for in list
: 순회할 리스트가 정해져 있을 때 
```py
list = ['a','b','c','d','e']
for alpha in list:
  print(alpha)
```

##### for in range
: 순회할 횟수가 정해져 있을 때(또는 1씩 증가하는 숫자가 필요할 때) 
```py
for i in range(5): # [0,1,2,3,4]
  print(i)
```
```py
names = ['철수','영희','바둑이','귀도','비단뱀']

for i in range(len(names))): # len(): 리스트의 길이(원소의 개수)
  name = names[i]
  print('{}번: {}'.format(i+1, name))

# 결과:
# 1번: 철수
# 2번: 영희
# 3번: 바둑이
# 4번: 귀도
# 5번: 비단뱀 
```

#### 모듈(Module)
- 미리 만들어진 코드를 가져와 쓰는 방법
- **import <모듈이름>**
- 사용: **<모듈이름>.<모듈 안의 구성요소>**
```py
import math # 수학과 관련된 기능
math.pi
import random # 랜덤과 관련된 기능
random.choise()
import urllib.request # url을 넣으면 페이지 내용을 돌려주는 기능 
```
- 모듈을 만들 수도 있음.(모듈 파일과 그 모듈을 사용하는 파일이 같은 폴더에 있어야 함.)

#### 검색하기
- 검색은 항상 **구글**에서!
- '파이썬3' or 'python3' + 궁금한 키워드
- 안나오면 영어로 검색 

#### 문서찾기
- 검색예시> **python3 검색내용 generation site:python.org**
  - 'generation': 프로그래밍에서 값을 생성한다는 의미.
  - 'site:': 해당 사이트의 페이지만 모아서 보여주는 구글의 기능
  - python.org: 공식 문서 사이트(필요한 내용을 둘러보고 싶을 때, 파이썬 내장 모듈과 함수의 정보가 필요할 때)
  - 구글 또는 stackoverflow.com(문제의 구체적인 해결 방법이 알고 싶을 때)

#### 딕셔너리
- 여러 값을 저장해놓고 필요한 값을 꺼내 쓰는 기능
- 이름표(key)를 이용해 값(value)를 꺼내 사용
```py
딕셔너리명 = {
    'key1':'value1',
    'key2':'value2',
    }
```
##### 딕셔너리 수정하기
- 값 수정
```py
dict['one'] = 11
```
- 값 추가
```py
dict['three'] = 3
```
- 값 삭제
```py
del(dict['one'])
dict.pop('two')
```

#### 튜플을 이용한 변수의 packing, unpacking
- 하나의 변수에 여러개의 변수 대입 가능.
```py
x, y = y, x
```
- 함수의 return 값으로 여러 값을 전달 할 수 있다. 
  - a[0], a[1] == *a
  
#### 자료형 다루기
- **type(객체)**: 자료형 확인 
- **isinstance(객체, 자료형)**: 어떤 객체가 특정 자료형(클래스)의 인스턴스인지 확인할 때 사용하는 내장 함수(상속관계 고려)

#### 클래스
- **class 클래스명():**
- 클래스와 인스턴스를 이용하면 데이터와 코드를 사람이 이해하기 쉽게 포장할 수 있다.
- 클래스에 함수를 넣을 수 있다. 
- **모델링**
```py
class Human():

def create_human(name, weight):
  person = Human()
  person.name = name
  person.weight = weight
  return person

Human.create = create_human

person = Human.create("철수", 60.5)

def eat(person):
  person.weight += 0.1
  print("{}가 먹어서 {}kg이 되었습니다".format(person.name, person.weight))

def walk(person):
  person.weight -= 0.1
  print("{}가 걸어서 {}kg이 되었습니다".format(person.name, person.weight))

Human.eat = eat
Human.walk = walk

person.walk()
person.eat()
person.walk()

# 결과:
# 철수가 걸어서 60.4kg이 되었습니다
# 철수가 먹어서 60.5kg이 되었습니다
# 철수가 걸어서 60.4kg이 되었습니다
```

#### 메소드
클래스 안에 정의된 함수.
클래스에 묶여서 클래스의 인스턴스와 관계되는 일을 하는 함수를 말한다. 
```py
class Human():

  def create(name, weight):
    person = Human()
    person.name = name
    person.weight = weight
    return person

  def eat(self):
    self.weight += 0.1
    print("{}가 먹어서 {}kg이 되었습니다".format(self.name, self.weight))

  def walk(self):
    self.weight -= 0.1
    print("{}가 걸어서 {}kg이 되었습니다".format(self.name, self.weight))

  def speak(self, message):
    print(message)

person = Human.create("철수", 60.5)

person.speak("안녕하세요")

# 결과:
# 안녕하세요 
```

#### 특수한 메소드 
- **_ _ init _ _**(초기화 함수): 인스턴스를 만들 때 실행되는 함수
- **_ _ str _ _**(문자열화 함수): 인스턴스 자체를 출력할 때의 형식을 지정해주는 함수 
```py
class Human():

  def __init__(self): # 초기화 함수
    self.name = name
    self.weight = weight

  def __str__(self): # 문자열화 함수 
    return "{} (몸무게 {}kg)".format(self.name, self.weight)

  def eat(self):
    self.weight += 0.1
    print("{}가 먹어서 {}kg이 되었습니다".format(self.name, self.weight))

  def walk(self):
    self.weight -= 0.1
    print("{}가 걸어서 {}kg이 되었습니다".format(self.name, self.weight))

person = Human("사람", 60.5) 

print(person.name)
print(person.weight)

print(person)

# 결과:
# 사람
# 60.5 

# 사람(몸무게 60.5kg)
```

#### 상속
```py
class Animal(): # 부모클래스
  def walk(self):
    print("걷는다")

  def eat(self):
    print("먹는다")

class Human(Animal): # 자식클래스

  def wave(self):
    print("손을 흔든다")

class Dog(Animal): # 자식클래스 

  def wag(self):
    print("꼬리를 흔든다")

person = Human()
person.walk()
person.eat()
person.wave()

dog = Dog()
dog.walk()
dog.eat()
dog.wag()

# 결과:
# 걷는다
# 먹는다
# 손을 흔든다
# 걷는다
# 먹는다
# 꼬리를 흔든다 
```

#### 단순 오버라이드
사람이나 강아지의 greet 메소드를 "부모의 greet 메소드를 오버라이드했다(덮어썼다)"고 할 수 있음 
```py
class Animal(): # 부모클래스
  def walk(self):
    print("걷는다")

  def eat(self):
    print("먹는다")

  def greet(self):
    print("인사한다")

class Cow(Animal): # 자식클래스(소)
    '''소'''
    
class Human(Animal): # 자식클래스(사람)
  
  def wave(self):
    print("손을 흔든다")

  def greet(self):
    self.wave()

class Dog(Animal): # 자식클래스(강아지)

  def wag(self):
    print("꼬리를 흔든다")

  def greet(self):
    self.wag() 

cow = Cow()
cow.greet() 

person = Human()
person.greet()

dog = Dog()
dog.greet()

# 결과:
# 인사한다
# 손을 흔든다
# 꼬리를 흔든다
```

#### List comprehension
```py
areas = []
for i in range(1, 11):
    if i%2 == 0:
        areas += [i*i]
print("areas:", areas)

areas2 = [i*i for i in range(1, 11) if i%2 == 0]
print("areas2:", areas2)

# 결과:
# areas: [4, 16, 36, 64, 100]
# areas2: [4, 16, 36, 64, 100]
```
- for문 중첩시키기 
```py
# 15*15인 바둑판의 각 좌표를 튜플로 만들어서 값으로 가지는 리스트
print([(x, y) for x in range(15) for y in range(15)])
```

#### Dictionary comprehension
```py
students = ['태연','진우','정현','하늘','성진']
students_dict = {"{}번".format(number + 1): name for number, name in enumerate(students)}

print(students_dict)

# 결과:
# {'1번': '태연', '2번': '진우', '3번': '정현', '4번': '하늘', '5번': '성진'}
```
- zip
```py
students = ['태연','진우','정현','하늘','성진']
scores = [85,92,78,90,100]

for x, y in zip(students, scores):
    print(x,y)

score_dict = {student : score for student, score in zip(students, scores)}
print(score_dict)

# 결과:
# 태연 85
# 진우 92
# 정현 78
# 하늘 90
# 성진 100
# {'태연': 85, '진우': 92, '정현': 78, '하늘': 90, '성진': 100}
```
<img width="560" height="332" alt="스크린샷 2025-07-16 160119" src="https://github.com/user-attachments/assets/8234e8ca-c803-4d05-be00-caa8a7f51a2c" />




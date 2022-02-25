# python build-in function

| Function      | Description                                                            |
| ------------- | ---------------------------------------------------------------------- |
| abs()         | 將所有數字回傳絕對值                                                   |
| all()         | 檢查可迭代對象中的所有項目是否為真，回傳布林值                         |
| any()         | 檢查可迭代對象中的任一項目是否為真，回傳布林值                         |
| ascii()       | 用轉譯字符替換非 ascii 字符，回傳可讀物件                              |
| bin()         | 將整數轉成二進位                                                       |
| bool()        | 返回指定對象的布林值                                                   |
| bytearray()   |                                                                        |
| bytes()       |                                                                        |
| callable()    | 檢查指定的 object 是否可調用，返回布林值的                             |
| chr()         | 返回表示指定 unicode 的字符                                            |
| classmethod() | 將方法轉換為類方法                                                     |
| compile()     |                                                                        |
| complex()     | 指定實數和虛數返回複數                                                 |
| delattr()     | 刪除指定對象的指定屬性                                                 |
| dict()        | 建立字典                                                               |
| dir()         | 返回指定對象的所有屬性和方法，不帶值。                                 |
| divmod()      | 返回參數 1 除以參數 2 時的商和余數                                     |
| enumerate()   | 將一個可遍歷的數據對象(如列表、元組或字符串)組合為一個索引序列         |
| eval()        | 用來執行一個字符串表達式，並返回表達式的值                             |
| exec()        | 執行指定的 Python code，相比於 eval，exec 可執行更複雜的 Python code。 |
| filter()      | 排除可迭代對像中的項目，返回非排除的項目                               |
| float()       | 將指定的值轉換為浮點數                                                 |
| format()      | 填入格式以及指定的值，格式化指定的值                                   |
| frozenset()   | 返回一個凍結的集合，凍結後集合不能再新增或刪除任何元素                 |
| getattr()     | 從指定對象返回指定屬性的值                                             |
| globals()     | 以字典形式返回當前位置的全部全局變量                                   |
| hasattr()     | 檢查指定的對象是否具有指定的屬性，返回布林值                           |
|    hash()           |    返回指定對象的哈希值             |
|       help()        |   執行內置幫助系統              |
|     hex()          |     將數字轉換為十六進制            |
|     id()          |       返回對象的 id(記憶體位置)          |
|     input()          |              允許用戶輸入   |
|    int()           |     將任何型態轉為整數            |
|   isinstance()            |    檢查指定對象是否屬於指定類型，返回布林值             |
|    issubclass()           |     檢查指定的類是否為指定對象的子類，返回布林值            |
|      iter()         |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
|               |                 |
- abs()

```python
x = abs(-7.25)
print(x) # 7.25
```

- all()

```python
mylist = [True, True, True]
x = all(mylist)
print(x) # True
```

- any()

```python

mylist = [False, True, False]
x = any(mylist)
print(x) # True
```

- ascii()

```python
x = ascii("My name is Ståle")
print(x)
# 'My name is St\e5le'
```

- bin()

```python
x = bin(36)
print(x) # 0b100100
```

- bool()

```python
x = bool(1)
print(x) # True
```

- bytearray()
- bytes
- callable()

```python
def x():
  a = 5

print(callable(x)) # True
```

- chr()

```python
x = chr(97)
print(x) # a
```

- classmethod()
- compile()
- complex()

```python
x = complex(3, 5)
print(x) # (3+5j)
```

- delattr()

```python
class Person:
  name = "John"
  age = 36
  country = "Norway"

delattr(Person, 'age')
```

- dict()

```python
x = dict(name = "John", age = 36, country = "Norway")

print(x)
# {'name': 'John', 'age': 36, 'country': 'Norway'}
```

- dir()

```python
class Person:
  name = "John"
  age = 36
  country = "Norway"

print(dir(Person))
# ['__class__', '__delattr__', '__dict__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__le__', '__lt__', '__module__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', '__weakref__', 'age', 'country', 'name']
```

- divmod()

```python
x = divmod(5, 2)

print(x) # (2, 1)
```

- enumerate()

```python
x = ('apple', 'banana', 'cherry')
y = enumerate(x)

print(list(y))
# [(0, 'apple'), (1, 'banana'), (2, 'cherry')]
```

- eval()

```python
x = 'print(55)'
eval(x) # 55
```

- exec()

```python
x = 'name = "John"\nprint(name)'
exec(x) # John
```

- filter()

```python
ages = [5, 12, 17, 18, 24, 32]

def myFunc(x):
  if x < 18:
    return False
  else:
    return True

adults = filter(myFunc, ages)

for x in adults:
  print(x)

# output
# 18
# 24
# 32
```

- float()

```python
x = float(3)
print(x) # 3.0
```

- format()

```python
x = format(255, 'x')
print(x) # ff
```

- frozen()

```python
mylist = ['apple', 'banana', 'cherry']
x = frozenset(mylist)
print(x)
```

- getattr()

```python
class Person:
  name = "John"
  age = 36
  country = "Norway"

x = getattr(Person, 'age')

print(x) # 36
```

- globals()

```python
x = globals()
print(x['__name__']) # __main__
```

- hasattr()

```python
class Person:
  name = "John"
  age = 36
  country = "Norway"

x = hasattr(Person, 'age')
print(x) # True
```

- hash()
- help()
- hex()

```python
x = hex(255)
print(x) # 0xff
```
- id()

```python
x = 5
y = id(x)
print(y) # 9756352
```

- input()

```python
print('Enter your name:') 
x = input() # 輸入 alan
print('Hello, ' + x) # Hello alan
```

- int()

```python
x = int(3.5)
print(x) # 3
```

- isinstance()

```python
x = isinstance(5, int)
print(x) # True

x = isinstance("Hello", (float, int, str, list, dict, tuple))
print(x) # True

class myObj:
  name = "John"

y = myObj()

x = isinstance(y, myObj)

print(x) # True
```
> issubclass()

- issubclass()

```python
class myAge:
  age = 36

class myObj(myAge):
  name = "John"
  age = myAge

x = issubclass(myObj, myAge)
```
> isinstance()
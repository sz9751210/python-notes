# python 基礎

## Python 基本語法

- python 語法的後綴名是以.py 結尾

### python 執行方式

- 使用交互介面執行
- 使用 python test.py 命令執行
- 使用./test.py 執行

### python 標示符

- 以單下劃線開頭的屬性，表示是類的私有屬性(包括方法，變量)。如:`_foo`表示不能直接訪問的類屬性。
- 以雙下劃線開頭的 `__foo` 代表類的私有成員；
- 以雙下劃線開頭和結尾的 `__foo__` 代表 Python 里特殊方法專用的標識，如 `__init__()` 代表類的構造函數。

### 換行縮進

- python 不使用{}來控制 code 範圍，而使用縮進來控制。一般都使用四個空格做縮進(PEP8規定)。

```python
#!/usr/bin/python
# -*- coding: UTF-8 -*-

print "hello world";

if True:
    print("Answer:");
    print("true");
else:
    print("Answer:");
    # 沒有嚴格縮進，在執行時會報錯
  print("false");
```

### python 引號

- Python 可以使用引號`(')`、雙引號`(")`、三引號`( ''' 或 """ )` 來表示字符串。
- 三引號(""")可以由多行組成，是編寫多行文本的快捷語法，常用於文檔字符串。

```python
# 單引號以及雙引號
'This is a string'
"This is a string"

# 引號包含引號
"We call it 'Dog'...... " # 雙引號內可包含單引號
'We call it "Dog"...... ' # 單引號內可包含雙引號

# 三雙引號可直接換行
"""haha,
this is a dog."""

# 三單引號需要換行符
'''haha, \
this is a dog.'''
```

### python 注釋

- python 中單行註釋採用`#`開頭
- python 中多行註釋使用三個單引號`(''')`或三個雙引號`(""")`
- 多行註釋通常用來為 Python 文件、模塊、類或者函數等添加版權或者功能描述信息。

```python
# 單行
# 註釋內容

# 多行
'''(""")
使用 3 個單引號分別作為註釋的開頭和結尾 可以一次性註釋多行內容 這裡面的內容全部是註釋內容
'''(""")
```

### Python 空行

- 函數之間或 class 的方法之間用空行分隔，表示一段新的代碼的開始。class 和函數入口之間也用一行空行分隔，以突出函數入口的開始。

### 多個語句組成的代碼組

- 縮進相同的一組語句構成一個代碼塊，我們稱之代碼組。
- 子句: 像 if、while、def 和 class 這樣的複合語句，首行以關鍵字開始，以冒號( : )結束，該行之後的一行或多行代碼構成代碼組。

```python
if expression:
    suite
elif expression:
    suite
else:
    suite
```

## python 變量類型

- 變量可以指定不同的數據類型，這些變量可以存儲整數，小數或字符。

### python 變量賦值

- 變量賦值不需要聲明類型，變數的資料型別將根據分配給它的值的型別自動來定義。
- 每個變量在使用前必須賦值，變量賦值以後該變量才會被創建
- 不可以取保留字
- 只能由大小寫字母、數字、 \_ 、 中文組成變數名稱
- 英文字母大小寫視為不同的變數名稱

```python
counter = 100 # 賦值整型變量
miles = 1000.0 # 浮點型
name = "alan" # 字符串
print(count),
print(miles),
print(name);
```

- 多變量賦值，變數之間用`，`分隔

```python
# 2 被分配給 x，4.124 被分配給 y，字串 Python 被分配給 z。
x, y, z = 2, 4.124, "Python"

# 三個變數都是Blue
x = y = z = "Blue"
```

- 刪除變數

```python
del x
```

### python 資料型態

- 數值型態：
  - int
  - float
  - bool
- 字串型態：
  - str
  - chr
- 容器型態：
  - list
  - dict
  - tuple

### Python 基本的純量類型

- 整數（int）
- 浮點數（float）
- 文字（str）
- 布林（bool）
- None（NoneType）

#### 整數和浮點數

- 整數與浮點數使用數學運算符號進行運算
- 會搭配運算符號進行運算
  - `+` 、 `-` 、 `*` 、 `/` ：加減乘除
  - `**` ：次方
  - `%` ：回傳餘數
  - `//` ：回傳商數

#### 字串

- 我們使用成雙的單引號 '' 或成對的雙引號 "" 來建立文字類型
- 如果建立的字串有包含不成對的引號，則需要使用跳脫字元`\`來完成宣告

##### python 格式化字串

- %-formatting

```python
print("I am %s.%s"%("Alan","wang"))

# output
I am Alan.wang
```

- str.format()（Python 2.6+）

```python
# 基本使用
s = 'I am {first_name} {middle_name}. {last_name}'
print(s.format(first_name='Monkey', middle_name='D', last_name='Luffy'))

# output
I am Monkey D. Luffy

# 調整輸出樣式：^(居中）、<（向左對齊）、>（向右對齊）
print('{:^10s}'.format('a')) # ^：居中對齊，10：寬度為10，s：以string輸出

# output
    a

# 以 {:,} 的方式以逗號分隔數字
print('{:,}'.format(100000000))

# output
100,000,000
```

- f-string（Python 3.6+）

```python
# variables
first_name = "Monkey"
middle_name = "D"
last_name = "Luffy"
# f-string
f"I am {first_name} {middle_name}. {last_name}"
# Output: "I am Monkey D. Luffy"
```

#### 布林

- 進行判斷條件或者資料篩選的時候會需要仰賴布林（bool），布林只有 True 與 False 這兩個值。

```python
print(type(True))
print(type(False))
```

- Python（或者絕大多數的程式語言）對於英文的大小寫是敏感的（case-sensitive），像是 True 會被識別為布林，但是 TRUE 或者 true 則會被視作物件名稱。

```python

# recognized as bool
print(type(True))
print(type(False))
# recognized as object names
print(type(true))
print(type(TRUE))
print(type(false))
print(type(FALSE))
```

- True 跟數值 1 相等； False 跟數值 0 相等。如果在數值運算中納入了布林不會產生任何問題。

```python
print(True == 1) # output：True
print(False == 0) # output：True
print(1 + True) # output：2
print(1 + False) # output：1
```

##### 判斷條件簡介

- `== 、 !=`：等於以及不等於
- `> 、 >= 、 < 、 <=`：大於、大於等於、小於以及小於等於
- `is 、 is not`：是否為相同的值與類型
- `and 、 or`：交集與聯集
- `not`：非
- `in` ：是否存在於

#### None

- None 是所謂的無值，或者可以用 NA 值（Not Available）或 NaN 值（Not a Number）去體會它
- None 是無回傳值函數中的預設輸出值、也是搜索特徵函數找不到情況下的預設輸出值

```python
# 宣告了一個只有 pass 保留字內容的 hello_world() 函數，這就是一個所謂的無回傳值函數

def hello_world():
  pass

print(hello_world()) # output：None
print(type(hello_world())) # output：<class 'NoneType'>
```

#### 判斷純量類型的函數

- 使用 isinstance(x, classinfo) 函數判斷純量類型，其中 x 輸入物件名稱、 classinfo 輸入類型名稱。

```python

# 判斷是否為整數
print(isinstance(87, int)) # output：True
print(isinstance("87", int)) # output：False
# 判斷是否為浮點數
print(isinstance(87.0, float)) # output：True
print(isinstance(87, float)) # output：False
# 判斷是否為文字
print(isinstance("True", str)) # output：True
print(isinstance(True, str)) # output：False
# 判斷是否為布林
print(isinstance(False, bool)) # output：True
print(isinstance("False", bool)) # output：False
# 判斷是否為 None
print(isinstance(None, type(None))) # output：True
print(isinstance("None", type(None))) # output：False
```

### 使用 type()函數回傳純量類型

```python
my_int = 87
my_float = 8.7
my_str = "Hello Python"
bool_true = True
bool_false = False
none_type = None

print(type(my_int))
print(type(my_float))
print(type(my_str))
print(type(bool_true))
print(type(bool_false))
print(type(none_type))

# output
## <class 'int'>
## <class 'float'>
## <class 'str'>
## <class 'bool'>
## <class 'bool'>
## <class 'NoneType'>
```

### python 類型轉換

#### 純量轉換

使用與目標轉換類型同名的函數轉換純量類型。

- `int()`：轉換純量為整數類型
- `float()`：轉換純量為浮點數類型
- `bool()`：轉換純量為布林類型，除了 0 以外的數字都是`True`
- `str()`：轉換純量為文字類型

```python
# 轉換成整數
print(int(8.7))
print(int(True))
print(int(False))
print(int("87"))

# output
8
1
0
87

# 轉換成浮點數
print(float(87))
print(float(True))
print(float(False))
print(float("87"))

# output
87.0
1.0
0.0
87.0

# 轉換成布林
print(bool(0))
print(bool(0.0))
print(bool(1))
print(bool(1.0))
print(bool(8.7))
print(bool(-8.7))

# output
False
False
True
True
True
True

# 轉換成字串
print(str(87))
print(str(87.0))
print(str(True))
print(str(False))

# output
87
87.0
True
False
```

### python 運算符

- 算數運算符

> x=5, y=2

| 運算符 | 名稱   | 範例          |
| ------ | ------ | ------------- |
| +      | 加法   | x + y = 7     |
| -      | 減法   | x - y = 3     |
| \*     | 乘法   | x \* y = 10   |
| /      | 除法   | x / y = 2.5   |
| %      | 取餘數 | x % y = 1     |
| \*\*   | 指數   | x \*\* y = 25 |
| //     | 取整除 | x // y = 2    |

> `+` 與 `*` 也可用於字串 (string) ， `+` 用於字串相接， `*` 用於複製字串

```python
a = "a"
b = a + "b" # 字串連接， b 會等於 "ab"
c = a * 3   # 字串重複三倍， c 會等於 "aaa"
```

- 賦值運算符

> x = 5 = 0101 , 3 = 0011

| 運算符 | 名稱       | 範例                     | 解答                                      |
| ------ | ---------- | ------------------------ | ----------------------------------------- |
| =      | 賦值       | x = 5                    | x = 5                                     |
| +=     | 加法賦值   | x += 3 ---> x = x + 3    | x = 8                                     |
| -=     | 減法賦值   | x -= 3 ---> x = x - 3    | x = 2                                     |
| \*=    | 乘法賦值   | x \* = 3 ---> x = x \* 3 | x = 15                                    |
| /=     | 除法賦值   | x /= 3 ---> x = x / 3    | x = 1.666...                              |
| %=     | 取餘賦值   | x %= 3 ---> x = x % 3    | x = 2                                     |
| //=    | 取整除賦值 | x //= 3 ---> x = x // 3  | x = 1                                     |
| \*\*=  | 指數賦值   | x **= 3 ---> x = x ** 3  | x = 125                                   |
| &=     | AND 賦值   | x &= 3 ---> x = x & 3    | x = 1 = 0001                              |
| \|=    | OR 賦值    | x \|= 3 ---> x = x \| 3  | x = 7 = 0111                              |
| ^=     | XOR 賦值   | x ^= 3 ---> x = x ^ 3    | x = 6 = 0110                              |
| >>=    | 右移賦值   | x >>= 3 ---> x = x >> 3  | x = 0 = 0000 = 5 \* 1/2\*\*3 = 5/8        |
| <<=    | 左移賦值   | x <<= 3 ---> x = x << 3  | x = 40 = 0010 1000 = 5 \* 2\*\*3 = 5 \* 8 |

- 比較運算符

| 運算符 | 名稱     | 範例   |
| ------ | -------- | ------ |
| ==     | 相等     | x == y |
| !=     | 不相等   | x != y |
| >      | 大於     | x > y  |
| <      | 小於     | x < y  |
| >=     | 大於等於 | x >= y |
| <=     | 小於等於 | x <= y |

- 邏輯(布林)運算符

> x = 4

| 運算符 | 名稱                                | 範例                             |
| ------ | ----------------------------------- | -------------------------------- |
| and    | 與運算 - 兩者為 True，返回 True     | x < 5 and x < 10 ---> True       |
| or     | 或運算 - 其中一者為 True，返回 True | x < 5 or x < 4 ---> True         |
| not    | 非運算 - 兩者為 Faluse，返回 True   | not(x < 5 and x < 10) ---> False |

- 身分運算符

| 運算符 | 描述                                                              | 範例       |
| ------ | ----------------------------------------------------------------- | ---------- |
| is     | 如果兩個變量是同一個對象(具有相同的記憶體位置)，則返回 True       | x is y     |
| is not | 如果兩個變量不是同一個對象(不是指向相同的記憶體位置)，則返回 True | x is not y |

- 成員運算符

| 運算符 | 描述                                            | 範例       |
| ------ | ----------------------------------------------- | ---------- |
| in     | 當 in 前面的變數在後面的序列中時，結果為 True   | x in y     |
| not in | 當 in 前面的變數不在後面的序列中時，結果為 True | x not in y |

- 位元運算符

> a = 5

| 運算符 | 名稱                                                                                   | 範例                            |
| ------ | -------------------------------------------------------------------------------------- | ------------------------------- |
| &      | AND(位與操作符) - 當兩側數字在該位上都是 1 的時候，結果該位也為 1，否則為 0            | a & 2 = 0 = 0000                |
| \|     | OR(位或操作符) - 當兩側數字在該位上只要有一個是 1 的時候，結果該位為 1，否則為 0       | a \| 2 = 7 = 0111               |
| ^      | XOR(位異或操作符) - 當兩側數字對應位二進位制相異時(其中一位為 1，另一位為 0)，結果為 1 | a ^ 2 = 7 =                     |
| ~      | NOT(位取反操作符) - 對運算元進行按位取反操作，1 變成 0，0 變成 1                       | ~a = -6 = -(0101 + 1) = -(0110) |
| <<     | 左移操作符 - 將 << 左側的數字左移若干位，右側補 0，左側高位數捨棄                      | a << 2 = 20 = 0001 0100         |
| >>     | 右移操作符 - 將 >> 左側的數字右移若干位，左側補齊 0                                    | a >> 2 = 1 = 0001               |

### python 條件語句與迴圈控制
- 條件語句：當程式流程在進行的過程，需要根據某個條件來決定是否執行接下來的動作時使用。
- 迴圈控制：處理資料時，若是想要重複執行某些相同的步驟時，就會使用到迴圈。
#### 條件語句
- if
    - 若判斷條件成立，則執行底下縮排的敘述內容；反之，則不動作。
```python
if condition:
    statement
```

- if-else
    - 若condition 為真 (True)，則執行 statement1；反之，則執行statement2。
```python
if condition:
    statement1 for True condition
else:
    statement2 for False condition
```


- if-elif-else
    - elif 的個數是沒有限制的，可以依照自己的需求而定。
```python
if condition1:
    statement1 for True Condition1
elif condition2 :
    statement2 for True Condition2
elif condition3 :
    statement3 for True Condition3
else:
    statements for Each Condition False
```


- 巢狀if

```python
ID = input()
year = int(ID[1:3])
if year < 4:
    print("Graduated")
elif year <= 7 and year >= 4:
    if year == 7:
        print("Freshman")
    elif year == 6:
        print("Sophomore")
    elif year == 5:
        print("Junior")
    elif year == 4:
        print("Senior")
else:
    print("Not Registered Yet")
```
#### 迴圈控制
- 單層 for-loop
  - 適用在「已知迴圈數」的問題
  - for和in中間放自訂變數，in後面可接一個序列(ex. list)
  - 迴圈會依序從序列裡取得元素，將元素指派給前面的自訂變數，並執行迴圈裡的內容
  - 通常會跟range()做一個搭配使用

> range(起始值，終止值，遞增(減)值)

```python
for x in sequence:
    # 放要執行的東西

# 迴圈搭配list依序印出內容
sequences = [0, 1,'jason',2.5]
for i in sequences:
    print(i)

# output
0
1
jason
2.5

# 迴圈搭配range()使用
for i in range(3):
    print(i, end=" ")

print() # 換行
for i in range(10,2,-2):
    print(i, end=" ")
# output
0 1 2    
10 8 6 4
```

- 巢狀 for-loop
  - 迴圈裡面又包覆著其他的迴圈。
  - 處理的問題具有重複執行某段敘述的特性，而且這些敘述受到兩個 (或兩個以上) 的變數來分別控制其變化

```python
# 九九乘法表
for i in range(1, 10):
    for j in range(1, 10):
        if j == 9:
            print("\t", i*j) # j == 9時，換行
        else:
            print("\t", i*j, end = '') # j < 9時，不換行
```
- while loops
  - 適用在「無法預知迴圈數」的問題


```python
while test_expression:
    Body of while

# 產生1到10的序列
i = 1
while i <= 10:
    print(i, end=" ")
    i = i + 1
```

- break 和 continue(迴圈不規則結束)
    - break：**中斷迴圈**的執行並跳脫迴圈結構，繼續執行迴圈外的敘述。
    - continue：**不中斷迴圈**；只跳過迴圈內 continue 後面的剩餘敘述，接著繼續執行下一次的迴圈運作。

> 規則的結束方式是當迴圈的判斷條件不再符合時，迴圈自然結束；而不規則的迴圈結束則是在迴圈自然結束前，我們已經得到想要的運算結果，利用強制中斷的方式來結束迴圈。

```python
for i in "Hey Alan":
    if i == "l":
        break
    print(i, end=" ")

print()

for i in "Hey Alan":
    if i == "l":
        continue
    print(i, end=" ")

# output 
H e y   A 
H e y   A a n 
```

### python保留字

- 定義：語言本身的編譯器中已經定義過的單詞，具有特定含義和用途，使用者不能再將這些單詞作為變數名或函數名、類名使用。

| 保留字   | 說明                                                          |
| -------- | ------------------------------------------------------------- |
| and      | 邏輯`與`操作，用於表示式運算                                  |
| as       | 用於轉換資料型別                                              |
| assert   | 用於判斷變數或條件表示式的結果                                |
| async    | 用於啟用非同步操作                                            |
| await    | 用於非同步操作中等待協程返回                                  |
| break    | 中斷迴圈語句的執行                                            |
| class    | 定義類                                                        |
| continue | 繼續執行下一次迴圈                                            |
| def      | 定義函數或方法                                                |
| del      | 刪除變數或序列的值                                            |
| elif     | 條件語句，與 if、else 結合使用                                |
| else     | 條件語句，與 if、else 結合使用；也可用於異常或迴圈語句        |
| except   | 包含捕獲異常後的處理程式碼塊，與 try、finally 結合使用        |
| False    | 含義為`假`的邏輯值                                            |
| finally  | 包含捕獲異常後的始終要呼叫的程式碼塊，與 try、except 結合使用 |
| for      | 迴圈語句                                                      |
| from     | 用於匯入模組，與 import 結合使用                              |
| global   | 用於在函數或其他區域性作用域中使用全域性變數                  |
| if       | 條件語句，與 elif、else 結合使用                              |
| import   | 匯入模組，與 from 結合使用                                    |
| in       | 判斷變數是否在序列中                                          |
| is       | 判斷變數是否為某個類的範例                                    |
| lambda   | 定義匿名函數                                                  |
| None     | 表示一個空物件或是一個特殊的空值                              |
| nonlocal | 用於在函數或其他作用域中使用外層（非全域性）變數              |
| not      | 邏輯`非`操作，用於表示式運算                                  |
| or       | 邏輯`或`操作，用於表示式運算                                  |
| pass     | 空的類、方法或函數的預留位置                                  |
| raise    | 用於丟擲異常                                                  |
| return   | 從函數返回計算結果                                            |
| True     | 含義為`真`的邏輯值                                            |
| try      | 測試執行可能出現異常的程式碼，與 except, finally 結合使用     |
| while    | 迴圈語句                                                      |
| with     | 簡化 Python 的語句                                            |
| yield    | 從函數依次返回值                                              |

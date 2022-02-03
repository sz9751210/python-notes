# python基礎
## Python基本語法
- python語法的後綴名是以.py結尾
### python執行方式
- 使用交互介面執行
- 使用python test.py命令執行
- 使用./test.py執行

### python標示符
- 以單下劃線開頭的屬性，表示是類的私有屬性(包括方法，變量)。如:`_foo`表示不能直接訪問的類屬性。
- 以雙下劃線開頭的 `__foo` 代表類的私有成員；
- 以雙下劃線開頭和結尾的 `__foo__` 代表Python 里特殊方法專用的標識，如 `__init__()` 代表類的構造函數。

### 換行縮進
- python不使用{}來控制code範圍，而使用縮進來控制。一般都使用兩個空格做縮進。
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

### python引號
- Python可以使用引號`(')`、雙引號`(")`、三引號`( ''' 或 """ )` 來表示字符串。
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
### python注釋
- python中單行註釋採用`#`開頭
- python中多行註釋使用三個單引號`(''')`或三個雙引號`(""")`
- 多行註釋通常用來為 Python 文件、模塊、類或者函數等添加版權或者功能描述信息。
```python
# 單行
# 註釋內容

# 多行
'''(""")
使用 3 個單引號分別作為註釋的開頭和結尾 可以一次性註釋多行內容 這裡面的內容全部是註釋內容
'''(""")
```

### Python空行
- 函數之間或class的方法之間用空行分隔，表示一段新的代碼的開始。class和函數入口之間也用一行空行分隔，以突出函數入口的開始。

### 多個語句組成的代碼組
- 縮進相同的一組語句構成一個代碼塊，我們稱之代碼組。
- 子句: 像if、while、def和class這樣的複合語句，首行以關鍵字開始，以冒號( : )結束，該行之後的一行或多行代碼構成代碼組。
```python
if expression: 
   suite 
elif expression:
   suite  
else:
   suite 
```

## python變量類型
- 變量可以指定不同的數據類型，這些變量可以存儲整數，小數或字符。
### python變量賦值
- 變量賦值不需要聲明類型，變數的資料型別將根據分配給它的值的型別自動來定義。
- 每個變量在使用前必須賦值，變量賦值以後該變量才會被創建
```python
counter = 100 # 賦值整型變量
miles = 1000.0 # 浮點型
name = "alan" # 字符串
print(count),
print(miles),
print(name);
```
- 多變量賦值
```python
# 2 被分配給 x，4.124 被分配給 y，字串 Python 被分配給 z。
x, y, z = 2, 4.124, "Python"

# 三個變數都是Blue
x = y = z = "Blue"
```

### python資料型態
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
##### python格式化字串
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
print(True == 1)
print(False == 0)
print(1 + True)
print(1 + False)

# output
True
True
2
1
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

print(hello_world())
print(type(hello_world()))

# output
None
<class 'NoneType'>
```
#### 判斷純量類型的函數
- 使用 isinstance(x, classinfo) 函數判斷純量類型，其中 x 輸入物件名稱、 classinfo 輸入類型名稱。
```python

# 判斷是否為整數
print(isinstance(87, int))
print(isinstance("87", int))
# 判斷是否為浮點數
print(isinstance(87.0, float))
print(isinstance(87, float))
# 判斷是否為文字
print(isinstance("True", str))
print(isinstance(True, str))
# 判斷是否為布林
print(isinstance(False, bool))
print(isinstance("False", bool))
# 判斷是否為 None
print(isinstance(None, type(None)))
print(isinstance("None", type(None)))

# output
True
False

True
False

True
False

True
False

True
False
```

### python基本資料結構
- list
- tuple
- dict
- set
### 使用type()函數回傳類型
#### 回傳純量類型
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
#### 回傳資料結構
```python
player_list = ["Ron Harper", "Michael Jordan", "Scottie Pippen", "Dennis Rodman", "Luc Longley"]
player_tuple = tuple(player_list)
player_dict = {
    "PG": "Ron Harper",
    "SG": "Michael Jordan",
    "SF": "Scottie Pippen",
    "PF": "Dennis Rodman",
    "C": "Luc Longley"
}
player_set = set(player_list)

print(type(player_list))
print(type(player_tuple))
print(type(player_dict))
print(type(player_set))
```
### python類型轉換
#### 純量轉換
使用與目標轉換類型同名的函數轉換純量類型。
- `int()`：轉換純量為整數類型
- `float()`：轉換純量為浮點數類型
- `bool()`：轉換純量為布林類型，除了0以外的數字都是`True`
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
### python運算符
### python條件語句與迴圈控制

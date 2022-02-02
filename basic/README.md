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

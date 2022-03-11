## dict(字典)

- key-value 結構，面對大數據時，不必選擇位置，直接選擇 key
- 建立時使用大括號`{}`儲存資料
- 使用中括號`[key]`表示索引
- 可變動的

### 創建 dict

- 使用大括號建立 dict
```python
test_dict = {'name': 'alan', 'year': 1990}
print(test_dict) # {'name': 'alan', 'year': 1990}
print(type(test_dict)) # <type 'dict'>
```

- 使用python 內建函數`dict()`建立 dict
```python
score = [['jason', 39], ['allen', 25], ['tony', 20]]
dict_score = dict(score)
print(type(score)) # <type 'list'>
print(dict_score) # {'tony': 20, 'allen': 25, 'jason': 39}
print(type(dict_score)) # <type 'dict'>

name = ['jason', 'allen', 'tony']
score = [39, 25, 20]
dict_score = dict(zip(name,score))
print(dict_score) # {'tony': 20, 'allen': 25, 'jason': 39}
```


### 操作 dict



#### 更新 dict

#### 刪除 dict

#### 判斷 dict
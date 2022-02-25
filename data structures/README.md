# python 基本資料結構

- list
- tuple
- dict
- set

## list(列表)

- 可容納不同類型的純量與不同長度的資料結構
- 建立時使用中括號`[]`儲存資料
- 可變動的

### 創建 list

- 使用中括號建立 list

```python
test_list = ["a", 2, 3.5, True]
print(test_list) # ['a', 2, 3.5, True]
print(type(test_list)) # <type 'list'>

```

- 使用 python 內建函數`list()`來創建 list

```python
int_seq = range(10)
print(int_seq) # range(0, 10)
int_list = list(int_seq)
print(int_list) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(type(int_list)) # <class 'list'>

```

### 操作 list

- 索引(indexing)
- 切割(slicing)

```python
索引值介紹
- 位置
左側第一個：list[0]
右側第一個：list[-1]

- 語法
[start:stop:step]
預設值 --> [0,-1,1]

# 取得長度為3的list
list[0:3] -> 會取得 [0],[1],[2]

# 切割出基數的資料
list[::2]

# 資料順序顛倒
list[::-1]
```

#### 更新 list

- list.append(x)：將`x`加入到 list 末端
- list.insert(index, x)：將`x`加入到 list 中指定的索引值位置
- list.copy()：複製 list
- list.extend(x)：將`x`添加到 list 末端，`x`必須為可迭代

```python
list_test = [0, 1, 2]
list_test.append(3)
print(list_test) # [0, 1, 2, 3]
list_test.insert(3, 2.5)
print(list_test) # [0, 1, 2, 2.5, 3]
copy_list = list_test.copy()
print(copy_list) # [0, 1, 2, 2.5, 3]
list_test.extend(copy_list)
print(list_test) # [0, 1, 2, 2.5, 3, 0, 1, 2, 2.5, 3]

```

#### 刪除 list

- list.pop()：將 list 最末端的資料拋出
- del list[index]：將指定的索引值位置資料刪除
- list.clear()：清空 list 所有資料
- list.remove(x)：將`x`第一次出現的地方從此 list 移除

```python
list_test = [0, 1, 2, 3]
test = list_test.pop() # 將pop出來的資料存到test變數
print(test) # 3
del list_test[0]
print(list_test) # [1, 2]
list_test.remove(1)
print(list_test) # [2]
list_test.clear()
print(list_test) # []

```

#### 排序 list

- list.sort()：將 list 的資料預設以遞增排序
- list.reverse()：將 list 的資料顛倒排序

```python
list_test = [0, 4, 2, 3]
list_test.sort()
print(list_test) # [0, 2, 3, 4]
list_test.sort(reverse=True)
print(list_test) # [4, 3, 2, 0]
list_test.reverse()
print(list_test) # [0, 2, 3, 4]
```

#### 查詢 list

- list.count(x)：搜尋`x`在此 list 中出現的次數
- list.index(x)：搜尋`x`在此 list 中第一次出現的位置

## tuple(元組)

- 多數的特性都與 list 相同
- 建立的時候使用小括號`()`將希望儲存的資訊包括起來
- 不可變動
- 當只有要建立一個項目的 tuple 時，要加上`,`才會建立成功

### 創建 tuple

- 使用小括號創建 tuple

```python

test_tuple = ("a", 2, 3.5, True)
print(test_tuple) # ('a', 2, 3.5, True)
print(type(test_tuple)) # <type 'tuple'>

# 單一項目tuple
test_tuple = (1,)
print(test_tuple) (1,)
print(type(test_tuple)) # <type 'tuple'>

# 空tuple
test_tuple = ()
print(type(test_tuple)) # <type 'tuple'>
```

- 使用 python 內建函數`tuple()`創建 tuple

```python

int_seq = range(10)
print(int_seq)
int_tuple = tuple(int_seq)
print(int_tuple)
print(type(int_tuple))
```

### 操作 tuple

- 索引(indexing)
- 切割(slicing)

```python
1. 取得長度
len(tuple)

2. 搭配索引值
- 位置
左側第一個：tuple[0]
右側第一個：tuple[-1]

- 語法
[start:stop:step]
預設值 --> [0,-1,1]

# 取得長度為3的tuple
tuple[0:3] -> 會取得 [0],[1],[2]

# 切割出基數的資料
tuple[::2]

# 資料順序顛倒
tuple[::-1]
```

#### 刪除 tuple

- del tuple：將 tuple 刪除

#### 查詢 tuple

- tuple.count(x)：搜尋`x`在此 tuple 中出現的次數
- tuple.index(x)：搜尋`x`在此 tuple 中第一次出現的位置

```python
test_tuple = (1,2,3,3,4)
print(test_tuple.count(3)) # 2
test_tuple = (1,2,3,3,4)
print(test_tuple.index(3)) # 2
```

## dict(字典)

- key-value 結構，面對大數據時，不必選擇位置，直接選擇 key
- 建立時使用大括號`{}`儲存資料
- 使用中括號`[key]`表示索引
- 可變動的


## set(集合)

- 使用大括號`{}`儲存資料
- 只會儲存獨一的資料，若輸入了重複的資訊，則會只記錄一筆
- 無法使用中括號`[]`做索引或是切割
- 可變動的

### 創建 set

- 使用大括號建立 set 
```python
test_set = {"a", 1, 3.5, True}
print(test_set) # set(['a', 1, 3.5])
print(type(test_set)) # <type 'set'>
```

- 使用python 內建函數`set()`創建 set
```python
int_seq = range(10)
print(int_seq) # [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
int_set = set(int_seq)
print(int_set) # set([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
print(type(int_set)) # <type 'set'>
```

### 操作 set

#### 更新 set

- set.add(x)：將`x`加入到 set 中
- set.copy()：：複製 set
- x.difference(y)：回傳只存在於`x`中而不存在於`y`中的 set，**不會修改`x`**
- x.difference_update(y)：回傳只存在於`x`中而不存在於`y`中的 set，**會修改`x`** 
- x.intersection(y)：回傳共同存在於`x`與`y`中的 set，**不會修改`x`**
- x.intersection_update(y)：回傳共同存在於`x`與`y`中的 set，**會修改`x`**
- x.symmetric_difference(y)：回傳`x`與`y`，但不包含`xy`共有的項目，**不會修改`x`**
- x.symmetric_difference_update(y)：回傳`x`與`y`，但不包含`xy`共有的項目，**會修改`x`**
- x.union(y)：回傳`x`與`y`所有的項目，**不會修改`x`**
- x.update(y)：回傳`x`與`y`所有的項目，**會修改`x`**

#### 刪除 set

- set.remove(x)：將`x`從 set 中移除，資料不存在會報錯
- set.discard(x)：將`x`從 set 中移除，資料不存在不會報錯
- set.pop()：將 set 中隨機一個項目移除
- set.clear()：將 set 中所有資料都移除

#### 判斷 set

- x.isdisjoint(y)：如果`x`中的資料完全與`y`無關，則回傳 True
- x.issubset(y)：如果`x`中的資料被完全包含在`y`，則回傳 True
- x.issuperset(y)：如果`x`中的資料完全包含`y`，則回傳 True

## 共同使用函式(list, tuple, set)

- len()：回傳長度
- sum()：回傳總和
- max()：回傳最大值
- min()：回傳最小值

## 判斷是否在集合中(list, tuple, set)

- in：在集合中
- not in：不在集合中
- 
# 使用 type()函數回傳資料結構

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

# python 類型轉換

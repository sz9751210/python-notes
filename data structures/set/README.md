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

#### 查詢 set

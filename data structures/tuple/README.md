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

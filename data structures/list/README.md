# list(列表)

- 可容納不同類型的純量與不同長度的資料結構
- 建立時使用中括號`[]`儲存資料
- 可變動的
- 有順序的

## 創建 list

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


## 存取 list items

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

## 改變 list items

## 新增 list items

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

## 移除 list items

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



## 排序 list

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

## 複製 list

## join list

## 查詢 list

- list.count(x)：搜尋`x`在此 list 中出現的次數
- list.index(x)：搜尋`x`在此 list 中第一次出現的位置

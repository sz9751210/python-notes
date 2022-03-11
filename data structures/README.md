# python 基本資料結構

- list
- tuple
- dict
- set






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

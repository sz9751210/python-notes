### python基本資料結構
- list
- tuple
- dict
- set

#### list(列表)
##### 創建list
- 可容納不同類型的純量與不同長度的資料結構
- 建立時使用中括號`[]`儲存資料
```python
season = "1995-1996"
team = "Chicago Bulls"
coach = "Phil Jackson"
records = [72, 10]
starting_lineup = ["Ron Harper", "Michael Jordan", "Scottie Pippen", "Dennis Rodman", "Luc Longley"]
won_championship = True

best_chicago_bulls = [season, team, coach, records, starting_lineup, won_championship]
print(best_chicago_bulls)
print(type(best_chicago_bulls))

# output
['1995-1996', 'Chicago Bulls', 'Phil Jackson', [72, 10], ['Ron Harper', 'Michael Jordan', 'Scottie Pippen', 'Dennis Rodman', 'Luc Longley'], True]
<class 'list'>
```
- 使用python內建函數`list()`來創建list
```python
int_seq = range(10)
print(int_seq)
int_list = list(int_seq)
print(int_list)
print(type(int_list))

# output
range(0, 10)
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
<class 'list'>
```
##### 操作list
- 索引(indexing)
- 切割(slicing)
###### 索引操作

#### tuple(元組)
#### dict(字典)
#### set(集合)
### 使用type()函數回傳資料結構
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
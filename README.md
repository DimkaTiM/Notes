# Python3
Мои заметки по питону

Замена  format на f-strings
```python3
world = "world"
log_message = 'Hello {} !'.format(world)
```
Лучше
```python3
world = "world"
log_message = f'Hello {world} !'.format(world)
```

Dict
```python3
a = {"hi" : 70}
b = a.get("Hey", 100) # b = 100
```

Spread 
```python3
a, *b, c = range(5) # a = 0, b = [1, 2, 3], c = 4
```

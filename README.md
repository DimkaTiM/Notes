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


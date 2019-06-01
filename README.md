# Python3
Мои заметки по питону

Замена  format на f-strings
```python3
world = "world"
log_message = 'Hello {} !'.format(world)
# Лучше
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

Мемоизация с помощью lru_cache
```python3
from functools import lru_cache
@lru_cache(maxsize=512)
def fib_memoization(number: int) -> int:
    if number == 0: return 0
    if number == 1: return 1
    
    return fib_memoization(number-1) + fib_memoization(number-2)
start = time.time()
fib_memoization(40)
print(f'Duration: {time.time() - start}s') # # Duration: 6.866455078125e-05s
```
Значение "__var"
```python3
class ManglingTest:
     def __init__(self):
         self.__mangled = 'Привет'
        
     def get_mangled(self):
         return self.__mangled
ManglingTest().get_mangled()
ManglingTest().__mangled # AttributeError: "'ManglingTest' object has no attribute '__mangled'"
# Python3 автоматически не дает доступа к методам, переменным и т.д. начинающимся с __
```

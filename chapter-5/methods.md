
#### Методы строк {#str-methods}

Строки неизменяемы. В связи с этим, все методы строк не изменяют исходную строку, а создают новую. Например:
```python
>>> a = 'hello'
>>> a.upper()
'HELLO'
>>> a
'hello'
```

Значение в переменной `a` не изменилось. Чтобы сохранить значение, нужно его присвоить:
```python
>>> a = 'hello'
>>> b = a.upper()
>>> a
'hello'
>>> b
'HELLO'
```

Если исходное значение больше не нужно, можно его перезаписать, не создавая новую переменную:
```python
>>> a = 'hello'
>>> a = a.upper()
>>> a
'HELLO'
```

##### Неполный список методов {#method-list}

`capitalize` - переводит первый символ строки в верхний регистр
```python
>>> 'hello world'.capitalize()
'Hello world'
```

`center` - размещает исходную строку в центре новой строки длинной в n символов(первый аргумент), заполненной символами указанными во втором аргументе. Другое описание: дополнить длинну строки равномерно до n символов, используя заполнитель, указанные вторым аргументом. Если не указан, второй аргумент равет пробелу
```python
>>> 'hello world'.center(20, '-')
'----hello world-----'
```

`count` - подсчитать количество вхождений подстроки в исходную строку
```python
>>> 'hello world'.count('l')
3
```

`endswith` - проверить, заканчивается ли строка подстрокой
```python
>>> 'hello world'.endswith('!')
False
```

`find` - найти индекс первого вхождения подстроки в строку. Если не найдено - возвращается `-1`
```python
>>> 'hello world'.find('o')
4
```

`format` - [форматирование](#format-new) строки
```python
>>> 'hello {}'.format('world')
'hello world'
```

`index` - аналог `find`. Если не найдено - создает ошибку.
```python
>>> 'hello world'.index('o')
4
```

`isalnum` - проверить, состоит ли вся строка только из буквенно-числовых символов
```python
>>> 'hello123world'.isalnum()
True
```

`isalpha` - проверить, состоит ли вся строка только из буквенных символов
```python
>>> 'hello123world'.isalpha()
False
```

`isdigit` - проверить, состоит ли вся строка только из числовых символов
```python
>>> 'hello123world'.isdigit()
False
```

`islower` - проверить, записаны ли все буквенные символы строки в нижнем регистре
```python
>>> 'hello123world'.islower()
True
```

`isupper` - проверить, записаны ли все буквенные символы строки в верхнем регистре
```python
>>> 'hello123world'.isupper()
False
```

`ljust` - аналог `center`. Дополняет строку символами только справа
```python
>>> 'hello world'.ljust(20, '_')
'hello world_________'
```

`lower` - перевести строку в нижний регистр
```python
>>> 'hello WORLD'.lower()
'hello world'
```

`lstrip` - вырезать все пробельные символы слева
```python
>>> '     hello WORLD     '.lstrip()
'hello WORLD     '
```

`replace` - заменить все фрагменты X на фрагменты Y
```python
>>> '     hello WORLD     '.replace(' ', '-')
'-----hello-WORLD-----'
```

`rfind` - аналог `find`. Ищет самое последнее вхождение
```python
>>> '     hello WORLD     '.rfind('l')
8
```

`rindex` - аналог `index`. Ищет самое последнее вхождение
```python
>>> '     hello WORLD     '.rindex('l')
8
```
`rjust` - аналог `center`. Дополняет строку символами только слева
```python
>>> 'hello'.rjust(20, '?')
'???????????????hello'
```

`rstrip` - вырезать все пробельные символы справа
```python
>>> '   hello    '.rstrip()
'   hello'
```

`startswith` - проверить, начитается ли строка с подстроки
```python
>>> '   hello    '.startswith(' ')
True
```

`strip`  - вырезать все пробельные символы слева и справа
```python
>>> '   hello    '.strip()
'hello'
```

`swapcase` - изменить регистр каждого символа на противоположный
```python
>>> '   hello  wOrLd  '.swapcase()
'   HELLO  WoRlD  '
```

`title` - перевести все слова в нижний регистра, затем первую букву каждого слова - в верхний.
```python
>>> '   hello  wOrLd  '.title()
'   Hello  World  '
```

`upper` - перевести строку в верхний регистр
```python
>>> '   hello  wOrLd  '.upper()
'   HELLO  WORLD  '
```

##### Цепочный вызов {#chains}

Так как вызов метода - это выражение, потому что он возвращает значение. Значит, вызов метода может использоваться в значительном количестве случаев, использования переменной и значения.

```python
>>> a = 'hello'
>>> print(a)
hello
>>> print(a.upper())
HELLO
>>> b = a.upper()
>>> b = a.title().swapcase()
>>> b
'hELLO'
>>> b = a.title().swapcase().replace('L', 'l').swapcase()
>>> b
'HeLLo'
>>> a
'hello'
```

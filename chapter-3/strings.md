<!-- Local IspellDict: ru -->

#### Литералы строк {#literal}

Строки - последовательности символов ограниченные парной комбинацией кавычек(`'`, `"`, `'''`, `"""`).

```python
>>> 'hello'
'hello'
>>> "world"
'world'
>>> '''hello'''
'hello'
>>> """world"""
'world'
```

Строки, ограниченные одной кавычкой не могут содержать переносов. Строки, ограниченные тремя кавычками такого ограничения не имеют.
```python
>>> 'hello
  File "<stdin>", line 1
    'hello
         ^
SyntaxError: EOL while scanning string literal
>>> '''hello
... world
... '''
'hello\nworld\n'
```


#### Экранирование спецсимволов {#escape}

Если есть необходимость вывести внутри строки кавычку того же вида, что и ограничитель, эту кавычку нужно экранировать добавив перед ней обратный слеш(`\`). Для вывода самостоятельного слеша следует использовать `\\`. В силу особенностей работы интерпретатора, нужно использовать функцию `print`, чтобы увидеть реалный результат.

```python
>>> 'hello\'world'
"hello'world"
>>> "hello\"world"
'hello"world'
>>> 'hello\\world'
'hello\\world'
>>> print('hello\\world')
hello\world
```

Также существуют специальные символы, экранирование которых приводит к интересным результатам:

* \n - перенос строки
* \t - табуляция
* \b - смещение на один символ назад
* \r - смещение в начало строки

```python
>>> 'hello\nworld'
'hello\nworld'
>>> print('hello\nworld')
hello
world
>>> print('hello\tworld')
hello	world
>>> print('hello\bworld')
hellworld
>>> print('hello\rworld')
world
```
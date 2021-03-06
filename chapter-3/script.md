# Лекция 3

---

## Видео\#1 - Вводная часть

**Видео - голова**

И снова привет. Надеюсь, цифрами вы уже сыты по горло так что сегодня
я постараюсь обойтись без них, или хотя бы максимально снизить их
полезность. Почему бы тогда не переключиться на что-то столь же, если
даже не более, нужное?

Сегодня мы столкнемся с типом данных, который вполне может быть назван
антонимом чисел. Практически все, что могут числа, тут недоступно. Но,
так же, все, на что числа не способны, тут становится возможным. Это
текст. Или, если использовать правильные термины - строки. Все, что в
реальной жизни мы привыкли описывать словами, фразами, предложениям -
это строки. Даже отдельные буквы - это строки, состоящие из одиночных
символов. В принципе, если символов нет, нечто по прежнему может быть
строкой - строки бывают и пустыми.

Как уже сложилось - начнем с классификации. Строки - это неизменяемые
упорядоченные коллекции. Каждое из этих слов приносит множество
особенностей в тип данных. Неизменяемость гарантирует нам постоянство
стоки, на которую ссылается переменная. Нет, не переживайте, сохранив
строку в переменную, мы по-прежнему можем эту переменную
перезаписать. Сама переменная может измениться. А вот строка нет. Вы
не можете изменить часть текста, слово и даже букву. Если возникает
такая необходимость - создайте новую строку, в которой неугодный
фрагмент будет другим. Так что данное ограничение скорее определяет
формат работы со строкой, чем реально запрещает нам что-то
изменять. Есть у нас некий монолитный механизм, путь это наш
ноутбук. Если бы экран неожиданно сломался - мы бы его попытались бы
заменить. Будь ваш ноутбук строкой - вы бы не смогли это сделать. Но
никто не запрещает вам купить новый ноутбук. Возможно, это будет более
ресурсоемким, но я выбрал неудачный пример. Ценность небольшой строки
в компьютере сравнима скорее не с ценой ноутбука, а с ценой спички.

Коллекции. Тут все достаточно предсказуемо - строка это коллекция из
множества символов. У строки есть длинна, равная количеству ее
символов. Если мы соединим две строки - получим третью, длинна которой
будет равна сумме длин первых двух строк. Все до неприличия логично.

И упорядоченность. Это свойство может характеризовать только
коллекции, точнее, способ организации элементов в них. Для нас это
показатель определенности порядка - мы можем быть уверены, что буквы
не будут переставлены в процессе существования строки и,
следовательно, мы всегда сможем ссылаться на отдельные символы с
помощью их порядковых номеров.

Вроде бы это весь пролог. А теперь вперед, к примерам!

---

> [types](https://drive.google.com/open?id=1dzL3pxpjJIoSLlak9xw0Wf8PlFcbIzjn) - литералы строк

## Видео\#2 - Типы данных: строки

**Скринкаст**

Сначала рассмотрим литералы. Напомню всем. В нашем лексиконе литерал -
это форма записи, которая приводит к созданию значения определенного
типа. Литерал числа - создаст число. Литерал строки - строку и так
далее.

Простейшим литералом строк можно считать кавычки. Давайте попробуем
написать какое-нибудь слово в одинарных кавычках. Это и есть
строка. Вне зависимости от своего содержимого и объема, любая подобная
конструкция превращается в строку. Можно даже ничего не писать между
кавычками. Так же результаты можно присваивать в переменные. Только не
забывайте про кавычки. Те же самые слова без кавычек создадут ошибки -
все, что не имеет кавычек вокруг себя воспринимается в python как
инструкции, операторы, функции и переменные. Если для введенного слова
не существует экземпляра в одном из перечисленных определений -
возникнет ошибка подобная той, которая сейчас видна на экране. А если
определение есть - python использует то, что под ним скрывается. Как,
например функции max и min - существуют и мы видим, что в них
содержится.

Заметьте, функция не выполняется, потому что после нее нет круглых
скобок. Интерпретатор просто выводит хранимые значения на экран. Если
мы попробуем провернуть такой трюк со словом avg, которое теоретически
могло бы хранить функцию рассчитывающую среднее значение на основании
своих аргументов. Но такой функции не существует - мы получаем
ошибку. Теперь, сильно забегая вперед, набросаем каркас подобной
функции и попробуем еще раз... Вроде бы работает. То-есть все, что вы
пишите, без кавычек воспринимается только как часть кода. Это
утверждение справедливо и в обратном направлении - любой корректный
код в кавычкаx становится просто строкой. Попробуем несколько
вариантов...

---

**Видео - голова**

Вроде с этой частью разобрались. Хотя, есть одна особенность - что
произойдет, если мы напишем одиночную кавычку внутри нашей строки? Я
раньше говорил, что все содержимое строки - это просто текст. Но увы,
вам придется смириться с тем, что я буду постоянно врать, иначе любое
объяснение приходилось бы сопровождать бесконечными отсылками и наш
курс растянулся бы на целый год. Тем не менее, любая ложь будет
раскрыта мной же, просто несколько позже. Вот, если хотите
доказательств, переменные. Я говорил, что они хранят в себе значения,
а на самом деле все совсем не так! А как на самом деле - мы узнаем
только в следующей серии. Пожалуй нужно было сделать эту фразу
завершающей - вышло бы очень круто.

Одиночная кавычка внутри строки приводит к неоднозначному
результату. С одной стороны - это просто текст. Но python встречает
первую одиночную кавычку и воспринимает ее сигналом завершения
строки. Далее следует какая-то неизвестная переменная и новая кавычка,
как начало второй строки, которая так и не закончилась.

---

> [escape](https://drive.google.com/open?id=1VENGd_Ykki1_xb8Eg4sb2rDoCzjM3djZ) - экранирование спецсимволов

**Скринкаст**

Вот как это выглядит в реальной жизни....

И, в действительности, это не единственный проблемный
символ. Попробуем добавить перенос в нашу строку. Может быть я хочу
начать новый абзац. Но мы сразу же получаем ошибку. Еще одно из
ограничений строк - переносы в них запрещены. Ладно, вру. Переносы в
строках допустимы, но вот сам python воспринимает видимый конец
строки, как окончание действия. Но закрывающая кавычка в этом
окончании отсутствует, что приводит к ошибке.

Чтобы обойти эти проблемы, в строки была добавлена специальная
возможность экранирования символов. Тут она реализована в форме
добавления префикса перед проблемным символом. Этот префикс лишает
следующий за ним знак особых возможностей.

В нашем случае, экранирующим префиксом считается обратный
слеш. Попробуйте поставить его перед этой злополучной кавычкой. Всегда
бы все так работало. Может оно выглядит не очень изящно, но с этим
нужно смириться. Из-за того, что нашу строку ограничивают одиночные
кавычки, мы обязаны экранировать каждую отдельную обратную кавычку,
которая играет роль простого символа.

А еще одна хорошая новость - экранировать можно целую тучу
символов. Попробуем провернуть этот трюк с переносом строки.  И
никакой ошибки - перенос строки просто исчез. Это поведение стоит
запомнить - интерпретатор абсолютно всегда будет удалять перенос
строки, если он стоит сразу после слеша. Например, мы можем таким
образом расписать суммму чисел на несколько строк... Или даже
присваивание... Так что в этом случае хоть слеш и экранирует следующий
символ, но это не особенность строк, а специфика самого
интерпретатора. Отсюда небольшое отличие. Слеш перед кавычкой просто
не позволял ей прервать строку, но сама кавычка оставалась. В то же
время слеш перед переносом строки полностью его уничтожает.

Касательно других символов, которые можно экранировать и их
поведения. Сразу проверим двойную кавычку. Сама по себе она выводится
обычным образом, но перед ней можно поставить слеш - ничего не
изменится! Пусть это и кажется странным, но слеш перед одиночной и
двойной кавычкой просто заставляет эти символы быть самими собой, даже
если без него было бы то же самое. Чтобы понять эту необходимость,
посмотрите еще раз, как выводится экранированная одиночная
кавычка. Перед ней нет никакого слеша, потому что вокруг нее
интерпретатор ставит двойные кавычки и она вроде бы уже и не
конфликтует с границами строки.

Если мы экранируем двойную кавычку - она так же выводится без слеша,
потому что результирующая строка ограничена одинарными кавычками. А
если мы попытаемся в одной строке экранировать и одиночную, и двойную
кавычку - результат становится немного непредсказуемым. Интерпретатор
не может просто взять и решить, чем же оградить строку, чтобы она не
конфликтовала со своим контентом и просто идет по пути наименьшего
сопротивления и выводит всю строку в одиночных кавычках, плюс -
сохраняет экранирование одного из символов.

Это пока не объясняет необходимость экранировать двойные кавычки, но
уже дает подсказку. Мы видели, как интерпретатор выводит строки,
заключенные в двойные, а не одинарные кавычки. А если мы сами
попробуем так сделать? Да, это будет работать. Главное, чтобы
закрывающая и открывающая кавычки совпадали. Остальные правила такие
же, но тут уже выглядит бессмысленным экранирование одиночной кавычки,
а двойные, как раз, вполне оправданы.

Еще один интересный момент - интерпретатор до последнего избегает
экранирования в своем выводе. Если можно просто поменять форму
ограничителя строки - интерпретатор выберет этот путь. И только если в
строке экранируются как одиночная, так и двойная строка - только тогда
интерпретатор покажет нам слеш перед одной из них. И, как это ни
странно, не имеет значения, какие кавычки использовали мы -
интерпретатор всегда стремится использовать одиночные кавычки вокруг
строки.

---

> [slash](https://drive.google.com/open?id=1sSBjZSlR3HRmQuXHNpA0jLaq2tVsxPFX) - экранирование спецсимволов

**скринкаст**

Еще один странный символ для экранирования - сам обратный слеш. Но
просто подумайте - если вам нужно будет вывести на экран двойную
кавычку, предваренную обратным слешем, как вы это сделаете?
Прямолинейность выйдет вам боком из-за ранее рассмотренных
особенностей.. И нам нужно просто экранировать обратный слеш для
достижения желаемого результата. Кстати, сам интерпретатор сохраняет
экранирование, чтобы избежать двусмысленных ситуаций. В реальности
python видит в этой строке только два символа - слеш и кавычку. Если
вы не желаете больше ломать голову над тем, где правда, а где
экранирование - попытаемся вывести пару примеров с использованием
функции print. Те строки, которые появляются в интерпретаторе,
призваны облегчить разработку, потому они, например, записаны в
кавычках - чтобы вы могли скопировать текст и как есть вставить
обратно в код, получив тот же результат. И, например, если мы
скопируем строку, полученную в результате парного экранирования - мы
все-равно придем к той же строке, пусть и записанной в другой форме.

print же, в свою очередь, выводит данные в красивом виде,
предназначенном для конечного пользователя. Потому все экранирующие
слеши исчезают, ровно как и все служебные символы, включая внешние
кавычки ограничители.

Дальше мы некоторое время будем использовать print, чтобы видеть код
не в программном формате, а в конечном.

---

**Видео**

Следующий символ - старый добрый перенос. Верно, мы можем экранировать
разрыв строки в коде, но это не позволит нам создать текст с
несколькими параграфами. Тут нужно что-то посильнее - реальный перенос
строки. Стоит заметить, что перенос - не абстракция, это настоящий
символ, занимающий пространство, как буква, цифра или пробел. И во
многих языках программирования для визуализации таких вот невидимых
символов, которые на самом деле существуют, решили использовать
экранирование обычных букв. Раз буквы просто так экранировать нет
смысла - значит никто этого делать не будет. А ЗНАЧИТ, мы можем
сделать так, что экранирование букв приведет к специальному
результату. Потому у нас есть серия буквенных символов, слеш перед
которыми станет причиной чего-то, на первый взгляд, неожиданного.

---

> [newline](https://drive.google.com/open?id=1SG4VHps8jEdIHuUlhLsyu0fQP6cYRzGR) - экранирование спецсимволов

**Скринкаст**

Первый из них и самый распространенный - \n. Он означает перенос
строки. Посмотрите, как мы можем его использовать...  Что? Удивляетесь
тому, что он по прежнему выглядит, как буква со слешем? Я же говорил,
что нам нужно использовать print, чтобы увидеть правду. Исправляем
ситуации и обнаруживаем строку, разбитую на две линии. В русском языке
с этим проблемы - на деле у нас строка на двух строках. Сама строка -
это текст, но в силу своего типа данных, правильное имя ей -
строка. Написана она на двух линиях, но это звучит чересчур странно,
потому лучше сказать - на двух строках. А вот если мы скомбинируем две
части этого утверждения... В общем, постарайтесь не запутаться, когда
я постоянно буду использовать слово строка в разном контексте.

При комбинировании нескольких групп \n мы получаем ожидаемые длинные
переносы. Если есть желание добавить второму параграфу небольшой
отступ - не забудьте добавить пробелы.

---

> [tab](https://drive.google.com/open?id=1-cjM0BSI4Mpe2Ck8TavXkAeXA-sJYbum) - экранирование спецсимволов

Вторым символом этой группы станет табуляция - \t. Она ведет себя
совсем как обычный символ табуляции, просто экранированную
последовательность чуть проще отличить от обычных пробелов...

Третий символ - backspace. Точнее, он себя так ведет - это \b. Каждое
появление этого символа заставит исчезнуть ближайший символ,
предшествующий последовательности. Давайте проверим парочку
вариантов...

И последний. На самом деле их еще достаточно много, но остальные
символы вряд ли представляют какой-либо интерес. \r - возвращение в
начало строки. Его поведение очень необычно. Мы не затираем
существующие символы строки, а просто телепортируемся в ее начало. Вот
что странно - новые символы будут накладываться вместо уже
существующих, а не отодвигать их вправо. И еще несколько примеров...

---

> [tripple quotes](https://drive.google.com/open?id=1pORGTG1x8EzIk9NW-cr1WMddMQl0OwGk) - экранирование спецсимволов

Еще одним вариантом литералов строк будет использование тройных
кавычек. Такого символа не существует, но нам это не помешает. Мы
просто напишем три одинарные кавычки как открывающую
последовательность и таким же образом ее прервем. Сразу замечу, что
можно использовать и три двойных кавычки, главное следите за
закрывающей парой. Единственное существенное отличие таких строк - они
позволяют добавлять настоящие переносы, которые мы получаем нажатием
на enter. Да \n по-прежнему доступны, но теперь это можно делать
гораздо более удобным образом...

---

## Видео\# - Операторы для работы со строками

**видео - Голова**

Количество строчных операторов значительно меньше, чем у
чисел. Большую часть преобразований вы будете выполнять с помощью
функций, так что сейчас мы очень быстро пробежимся по каждому из них.

---

> [concatenate](https://drive.google.com/open?id=1UQoPCo0IyJe6MpsIqUD2cmJPbuGyujdX) - конкатенация

**Скринкаст**

Как это ни странно - +. Но тут он выступает не в роли сложения, а в
роли оператора конкатенации - оператора объединения строк. Если мы
попытаемся сложить две строки - на выходе получится третья, содержащая
все символы аргументов, в том же порядке. В общем - дико
просто. Посмотрим, что из этого может получиться...

второй оператор - умножение. Умножать строки можно только на целые
числа. Приводит это к повторению исходной строки нужное количество
раз. Эта форма крайне удобна для отрисовки разнообразных узоров в
разделителях при выводе...

проверка на вхождение. Сложно поверить, что это действительно
оператор, потому что он похож на слово. in - бинарный оператор,
который позволяет проверить, входит ли его левый аргумент в правый. А
если на русском - является ли левый фрагмент частью правого. Посмотрим
на него в действии...

---

> [formatting](https://drive.google.com/open?id=1RKaXVMG8Ih0rgU_CXFACe7PkJ6Ok4Jux) - форматирование

**Скринкаст**

И последний, самый сложный оператор - форматирование, или же
подстановка по шаблону. Для этой операции используется символ
процента, как для остатка от деления. Слева находится строка, справа -
множество фрагментов, которые нужно подставить в строку, заключенные в
пару круглых скобок.

В строке должны присутствовать фрагменты, состоящие из знака процента
с последующей буквой показателем типа, например - s. Каждый из таких
фрагментов будет заменен на соответствующий ему по порядковому номеру
элемент из группы справа от оператора. Это значит, что если у вас в
строке трижды встречается %s, то вы должны предоставить три значения
для подстановки в строку.

Попробуем поприветствовать наш язык программирования... Или Геннадия
Антоновича...

В случае единственного шаблона для подстановки, брать аргумент справа
от оператора в скобки вовсе не обязательно, но советую все же делать
это, чтобы не забыть о них в нужный момент. Если вы не добавите скобки
для нескольких аргументов - возникнет ошибка.

Модификатором также могут служить другие буквы. Вот d, например,
удобно использовать для подстановки целых чисел. Если вы попытаетесь
использовать дробные числа при подстановке - они будут преобразованы с
помощью функции int - то-есть преобразованы в целое число. Если вы
попытаетесь передать что-либо совсем непохожее на число - возникнет
ошибка...

Дополнительно вы можете указать минимальное пространство, которое
должен занимать фрагмент. Для этого напишите число между процентом и
модификатором типа в шаблоне. Это приведет к тому, что вокруг значения
будет добавлено необходимое количество пробелов, чтобы в результате
фрагмент занимал либо указанное количество символов, либо
больше. Дополнение происходит только если изначально фрагмент был
недостаточного размера. Урезания фрагментов не происходит в такой
форме никогда. Давайте поэкспериментируем немного с новыми
возможностями...

---

# Видео\#

**Видео - голова**

В целом, можно считать это всеми операторами строк. Остальные
возможности нас пока вряд ли заинтересуют. Хотя я опят вру. Есть еще
один оператор - квадратные скобки. Точно так же, как и круглые скобки

* это окружающий оператор - он оказывает какое-то влияние на свое
  содержимое и каким либо образом взаимодействует со своим
  окружением. Этот оператор позволяет извлекать фрагменты
  строк. Напишите квадратные скобки после строки и поставьте внутри них
  индекс искомого символа. А, мы еще не обсуждали индексы? Индекс, это
  целое число - именно в случае строк, другие типы данных могут быть
  менее привередливы - описывающее отступ искомого символа от начала
  строки. Помедленнее? Представьте нашу строку. Каждый из ее символов
  расположен на своей позиции. Первый, второй, третий. И каждый
  находится на каком-то расстоянии от начала строки. Первый - на
  расстоянии в ноль символов. Второй - в одном символе от начала
  строки. Второй - в двух символах. Тут можно заметить тенденцию -
  отступ всегда на единицу меньше, чем порядковый номер. Так вот эта
  позиция, отступ - она и называется индексом. Многие говорят, что
  индексы - это порядковый номер символа, просто отсчет начинается с
  нуля. Ну а мне больше нравится идея отступов от начала строки.

---

> [index](https://drive.google.com/open?id=14ceVAeLg5l_Feg7jMHL3kP9s9J_qJAw-) - индексы

Попробуем это все на деле...
```
- создаем сроку
- обращаемся к индесу 1 и понимаем , что нужно начинать с нуля
- повторяем правила индексации - начиная с нуля, водим курсором по тексту называя индекс каждой буквы...
- выводим вторую и третью букву.
- переставляем символы задом-наперед

- пытаемся выйти за границы строки. Сначала проверяем десятый символ
- потом одиннадцатый - обрануживаем ошибку и разбираем сообщение об ошибке

- проверяем минус первый символ
- затираем старый код
- догадываемся, что мы выводим буквы с конца
- выводим все слово
- переставляем символы для образования стандартного порядка

- догадываемся, что символ "минус длинна строки" - это первая буква
- проверяем отсутствие индекса в квадратных скобках
- проверяем дробный индекс
- смотрим на сообщение об ошибке
- сравниваем целый и дробный индекс

- пытаемся писать выражения в скобках - сложение, вычитание, скобки, возведение в степень.
- обращаемся к индексу-переменной и получаем ошибку.
- создаем такую переменную
- меняем ее значения

- завершаем повторением. Отрицательные символы - справа налево. Если уйти левее - ошибка.
- положительные символы - слева направо. Выход за границы - ошибка.

- Новость о том, что в отдельных типах данных можно использовать строки в роли индексов.
```

---

А еще с помощью квадратных скобок можно извлекать из строк
срезы. Срез - это фрагмент строки. Как и отдельный символ, но вовсе не
обязательно ограниченный одной буквой. Срез может состоять из двух,
трех, десятка букв. Срез может быть строкой от начала до конца. А
может быть и пустой строкой. В общем срез - это фрагмент произвольной
длинны полученный из оригинальной строки.

---

> [slice](https://drive.google.com/open?id=1fiS4oNkQhmhExi7dPDF46kSm0RT429ml) - индексы
> [slice](https://drive.google.com/open?id=1HbWLMeWAzkuy3vfdzNn_NfjE5vEjZEmK) - индексы

```
- создаем строку
- создаем срез с помощью функции и указанием числового аргумента
- без аргументов - нельзя
- смотрим на срез

- извлекаем срез из строки
- это как индексы, только больше букв
- создаем срезы на месте
- указываем разные аргументы
- выходим за пределы строки
- проверяем дроби

- а теперь срез с нижней границей
- 0
- 1
- 4
- 5
- повышаем верхнюю границу

- срез с шагом в один
- 2
- 3
- 0 - нельзя
- отрицательный - пустая строка - нужно запомнить

- неудобная запись
- синтаксический сахар
- шаг можно не указывать
- и второе двоеточие
- извлекаем 5
- 10
- 1 символ
- много
- убираем второй аргумент
- двоеточие отсавляем
- дергаем первый аргумент
- убираем
- оставляем только одно двоеточие
- добавляем шаг
- оставляем два дваеточия
- расставляем пробелы

- отрицательные границы
- отрицательные индексы

- вся строка с положительным шагом
- отрицательным
- переставляем аргументы
- добавляем отрицательный шаг
- получаем строку задом наперед
```
---

И вот мы добрались до строчных функций. Начнем с преобразования в
строку и из строки. почти все типы могут быть преобразованы в строку
одним из двух способов - функцией repr, либо функцией str. Как и
ранее, для получения правдивых результатов, мы будем использовать
print.

---

> [conv](https://drive.google.com/open?id=1ys3XlhLWoJGvp-ujkmBFLjEnXG2ci4qJ) - преобразование

```
- создаем тестовые переменные
- выводим переменные самостоятельно
- с помощью принта и видим, что принт красивее
- принт использует str

- обнаруживаем, что интерпретатор выводит данные иначе
- смотрим на repr
- сравниваем его с str
- для чисел нет разницы
- для строк она выражается в кавычках и экранированиях

- теперь int
- не меняет целые
- усекает дробную часть
- выдает ошибки для строк

- передаем строку с корректным числом
- но не добавляем в нее текст
- но можно добавлять пробелы
- или переносы

- создаем большое число
- число с ведущим нулем
- нули слева исчезают
- справа - нет
- дробные числа выдают ошибку

- операции, вроде умножения, выдают ошибку
- но можно разбить на фрагменты

- float - делает то же самое, но результатом будет дробь
- значит любая запись дроби сойдет
- нули тоже усекаются
- экспонента сойдет

- пытаемся считать двоичную запись..
- и добавляем второй аргумент
- показываем десятичную систему
- 1 всегда 1
- другие числа - нет. считаем до 7

- восьмеричная система
- проверяем десятку в восьмеричной
- двоичной, 3, 4 и 36ричной
- 37 уже не существует

- проверяем в основании 11 числа 10 и девять.
- добавляем букву а в разных регистрах.
- б недопустима
- но при повышении системы можно
- каждая система добавляет новые буквы

теперь на функции
- создали строку
- сделали ее большую копию
- получили последний символ первой строки
- пытаемсчя угадать последний символ второй строки и сдаемся


- len
- считает строку
- последний индекс - длинна - 1
- расчитываем его прям в квадратных скобках

- пытаемся высчитать центральный символ второй строки
- дробный индекс дает ошибку
- превращаем его с целый

- повторяем эксперимент, но все выражение сразу в квадратных скобках

- max
- из двух чисел выбирает большее
- из строки выбирает больший символ
- не последний, а именно наибольший по алфавиту
- малеькая буква больше большой.
- это всегда правда
- из двух слов max выбирает большее по алфавиту
- слова в верхнем регистре всегда меньше
- длинна строки не важна - важен именно алфавитный порядок

- быстрая проверка min
```

---

И все? Вовсе нет, не думайте, что получится так быстро
отделаться. Ранее я упоминал, что строки выполняют множество
преобразований с помощью функций. Точнее было бы назвать эти штуки не
функциями, а методами, хотя разница не очень существенна, а со
временем мы увидим, что любой метод - это функция, а многие функции
могут стать методами.

Методы - это функции, привязанные к конкретному типу данных. Они не
существуют сами по себе, скорее они содержатся в самом значении
определенного типа. Чтобы использовать метод, нужно обратиться к нему,
поставив точку после значения. Справа от точки находится вызов метода,
который выглядит, как вызов функции.

В данном контексте, точка - это оператор. Поэтому ее можно выделять
пробелами\(но не принято\). Так же к методам можно обращаться не только
из самих значений, но и из переменных. Такой вариант даже более
популярен.

Сегодня мы разберем только один метод для работы со строками - форматирование. Но не переживайте, на следующем занятии я обещаю вам минимум десять новых методов!

---

> [format method](https://drive.google.com/open?id=1sg5Rm-y4sqvk8Oe585Dm3vGrzG8vzzYi) - форматирование

```
- создали строку
- проверяем метод формат в переменной
- и в самой строке
- несколько раз его вызываем с разным количеством аргументов

- добавляем в строку фигурные скобки и подставляем значение
- число
- строку
- знаки вопроса с ошибкой
- без ошибки
- лишние аргументы ничего не ломают
- недостающие - ошибка

- подставляем два числа в пустую строку
- потом два слова
- потом уточняем, что порядок можно контролировать
- добавляем указание индексов в строку
- подставляем отдельную букву в строку с помощью индексов

- проверяем выход за границы
- отрицательные индексы
- срезы
- видим, что только положительные индексы допустимы
- пауза и рассказываем  о возможности контроля способа подстановки
- для чисел нет никакой разницы, но вот строки можно подставлять репром и стром
- по умолчанию идет str

- А еще можно добавить двоеточие, которое ничего не ломает
- после него можно указать тип значения
- это позволяет контролировать то, что подставляют в строку
- причем, преобразования типов не происходит

- а теперь ширина поля
- строки равняются по левому краю, числа - по правому
- если преобразовать числа в строку -все норм
- маленькая ширина не урезает текст.

- Выравниваем два слова на экране
- индексы можно не указывать
- прижимаем слово к левому краю
- к правому
- а теперь числа
- потом выравниваем по центру

- теперь добавляем символ заполнитель

- и усечение
- пишем заведомо большие фрагменты
- добавляем усечение
- делаем то же самое с числом и видим, что нам нужно преобразование в строку

- теперь дробь
- с ней такое прокатит
- но не стоит преобразовывать в целое
- по умолчанию используем экспоненту

- если есть модификатор - можно контролировать форму записи

- создаем пару переменных и показываем, как мы их хотим вывести
- добавляем префикс
- сравниваем формы записи
- добавляем еще одну переменную
- а теперь - несущестующую переменную

- выводим функции
- видим, что функции выводятся как строки

- создаем переменную, в которую присваиваем обычную строку
- не работает - забыли префикс
- добавляем его - заработало

- префикс можно и в верхнем регистре - никакой разницы.
- а еще можно форматировать
```

---

И теперь задание для вас - встаньте  перед зеркалом, похвалите себя и
съешьте что-то вкусное. Потому что весь материал сегодняшнего урока
закончился! Что ж, все заметили, что сегодня кода стало значительно
больше? Увы, это еще не окончательный объем. Мы движемся к тому
времени, когда почти все время урока будет посвящено не моему
прекрасному образу, а происходящему на экране. Объем теории ограничен
и ваша главная задача - научиться ее применять. Старайтесь
экспериментировать как можно больше. Каждый раз, узнавая что-то новое
пытайтесь отразить это на повседневных задачах. Пытайтесь
автоматизировать процессы. В конце концов, пытайтесь включить звук
урока и набирать те элементы, которые я озвучиваю, не глядя на видео
урока. Убедитесь, что вы запомнили правила синтаксиса и хорошо
понимаете причины и следствия вашего кода. Каждый наш маленький шаг не
остается в прошлом. Это не трамплин для написания хорошего кода, а его
фундамент. Вы не разгоняетесь в этих темах, вы должны складывать их в
инвентарь и использовать бесконечное количество раз в будущем. Так что
даже какая-то мелочь, оставшись непонятной, ограничивает ваши
возможности в будущем. Подумайте о том, что вам до сих пор непонятно и
спросите об этом. Если до следующего урока у вас не появится не одного
вопроса - вы плохо стараетесь. Я уверен, что пропустил несколько
маленьких кусочков пазла, что не должно было остаться незамеченным с
вашей стороны. Ну что, пересматривать урок? До встречи на  следующем занятии.

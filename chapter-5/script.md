# Лекция 5

(Говорящая голова)

Рад вас снова тот видеть. Ну как, вы успели попрактиковаться со
строками и условиями с последней нашей встречи? Очень надеюсь что
ответ положительный — сегодня эти навыки Вам будут как нельзя
кстати. Потому что сегодня мы увидим некую альтернативу строкам - не в
плане представления текста , а скорее идеологическую альтернативу
коллекциям множества элементов.  Этой альтернативой является списки —
можно сказать самый общий тип данных объединенных в группу
коллекций. Коллекцией мы будем называть любую группу из множества
элементов . в идеальном случае — однородных элементов , Хотя это не
будет критическим требованием.  Как мы когда-то уже говорили,
коллекции делятся на несколько категорий.  В частности, коллекции
бывают упорядоченными и неупорядоченные. Упорядоченные коллекции мы
уже видели — это строки . Упорядоченность строк выражается в том, что
у каждого отдельного символа есть свой индекс. Индекс символа
постоянен, если вы выполните перестановку символов, тем самым изменив
их индексы, то вы получите совершенно другую строку. В упорядоченных
коллекциях порядок элементов играет ключевую роль . Список также
относится к упорядочным коллекциям. Затем, коллекции бывают
изменяемыми и неизменяемыми. Строки были неизменяемыми , благодаря
чему мы не могли изменить отдельную букву в существующей строке — для
подобной задачи нам пришлось бы создавать новую строку, которая
отличалась бы от оригинала одним символом.  Ладно пожалуй стоит
прервать мои словесные излияния и переключиться на самое интересное —
практическая сторона списков. Начнем, пожалуй, с литералов списков — с
их наиболее простой и удобной формой создания.

(видео конспект)
https://drive.google.com/open?id=1MqmPopl3FwIErThPFCz9WWLouVZCbH65 -
Литералы списков

---

(Говорящая голова)

Касательно работы с отдельными элементами списков. Это одна из
множества деталей за которую я дико люблю Python.  Списки поддерживает
индексы и практически в том же формате что и строки, потому изучив
хорошо индексы в строках, вы без труда сумеете применить их и тут.  Как
мы сейчас увидим мы можем извлекать элементы из списка с помощью
индексов, мы можем использовать и срезы.  Аналогично строкам мы будем
получать ошибки если попытаемся извлечь символ находящийся за
пределами списка , но, с другой стороны, мы можем пользоваться
индексами с отрицательным значением для получения элементов
относительно конца списка. Ну и чтобы это было хоть немного
интересным, мы сумеем модифицировать списки с помощью их индексов ,
что было недоступным в терминологии строк. Перейдем к деталям

(видео конспект)
https://drive.google.com/open?id=1h9f_77R64Y4NJBZQbdFkRIi_b8Q-YvtT -
Индексы

---

(Говорящая голова)

Сравнение списков , пожалуй, весьма предсказуемо . Если проводить
аналогию со строками, то мы можем предположить что величина списка
определяется его содержимым. Сравнивая 2 коллекции мы поочередно
сравниваем элементы на соответствующих позициях — как только в одном
из списков встречается больший элемент, то и весь список считается
большим. Есть ли в обоих списках на одинаковых позициях стоят
одинаковые элементы , то большим считается тот список в котором есть
бонусные элементы. В конце концов, если в 2 списках имеются одинаковые
элементы на одинаковых позиций и длина обоих списков тоже совпадает,
то тогда списки равны. Ну и куда же без рассмотрения этих правил в
интерпретаторе.

(видео конспект)
https://drive.google.com/open?id=1oVv2zLQP9OJCkWOQ9ui3Dz4ZaCdiTJyy -
Равенство

---

(Говорящая голова)

Одним из переходных звеньев между списками и строками можно считать
преобразования одного в другое. Строку можно разбить на множество слов
— мы увидели это на прошлом занятии. Используя метод split мы
определяем символ разделитель и получаем из строки список слов.  А
если имеется метод для разбиения строки на множество слов, то
Обязательно должно существовать и обратная операция — нечто что
позволит нам восстановить исходную строку из множества отдельных
небольших фрагментов. Давайте попытаемся написать код который
подтвердит эту теорию

(видео конспект)
https://drive.google.com/open?id=1HmQdLuvir1v06PY_wcKa6a1A8WjycbXU -
разбиение и соединение

---

(Говорящая голова)

Да, со списками работать достаточно интересно - в них может поместиться
так много всего полезного. Если быть честным то вы можете затолкать в список
практически неограниченное количество данных , разве что вам нужно
учитывать возможности вашего компьютера и попытаться не израсходовать
всю доступную память. После чего вы последовательно будете работать с
каждым элементом списка начиная с самого первого , переходя на 2,
потом на 3 , потом на 4 и так , наверное, до бесконечности . Ах да, Не
забывайте что вы не будете ограничиваться только выводом элементов на
экран — наиболее вероятно, что вы захотите также что-то сделать с
каждым элементом: преобразовать, его сложить с предыдущим значением,
отправить другу по почте — попробуйте придумать десяток других
задач с которыми вы можете столкнуться обрабатывая элементы списка. И
чтобы увидеть проблему, давайте-ка напишем это всё своими ручками ...

(видео конспект)
https://drive.google.com/open?id=1x4NDxJ_pNuhmiKND_lqzuedxKVTMWNp1 -
циклы и while

---

(Говорящая голова)

Инструкция while и If как две родных сестры — обе они начинаются с
ключевого слова определяющего саму операцию, потом следует некое
условие результирующее в правду либо ложь, После чего мы ставим
двоеточие и описываем серию действий , которые необходимо предпринять
в случае успешного выполнения условия. Мы не ограничены в количестве
выполняемых действий — главное соблюдать отступ и в какой-то момент
прервать блок кода вернувшись на изначальный уровень.  И следующие
несколько примеров должны вас убедить в том что обе эти инструкции
почти не различимы

(видео конспект)
https://drive.google.com/open?id=1f0D32jhyWfruZW82xiFZmw5qgaypS3cF -
подробности о while

---

(Говорящая голова)

Сами по себе циклы уже очень удобно, но, как и в условных
конструкциях, возможностей никогда не бывает слишком много. Так что
очень хотелось бы добавить некие инструкции для контроля выполнения
циклов.  Как вы думаете, что можно контролировать в циклах? Если
задуматься, цикл состоит из множества однородных действий . Представим
себя в длинном коридоре с множеством комнат. Следуя циклу, мы должны
открывать двери в эти комнаты, одну за другой. Что мы можем себе
позволить, так это пропустить некоторые двери, Например, если они
закрыты. Или просто они очень скучные и не вызывают у нас
интереса. Также, вероятно, вам может это наскучить и вы захотите
вернуться домой. Таким образом нам нужна некая инструкция для
досрочного прерывания цикла. Только что сказанное в общем-то и
описывает полностью все возможности контроля цикла.

(видео конспект)
https://drive.google.com/open?id=1jNMDhQvWfzSHUUTnYD1dCAo_QHkrS3Oj -
контроль выполнения цикла

---

(Говорящая голова)

Не так уж и много новый информации - запомнить вполне возможно. А вот
действительно ли всё это окажется полезным в реальной жизни? Я
предпочитаю всегда проводить аналогии с реальной жизнью для того чтобы
было проще запомнить. Давайте подумаем, когда нам может пригодиться
перескакивание на следующий шаг цикла? Нууууу, когда я покупаю в
магазине яблоки я их долго перебираю , чтобы найти самые большие
вкусные. Так что цикл выглядит следующим образом: взять яблоко,
повертеть в руках, подумать, положить в пакет, прикинуть вес пакета,
повторить. Но если это самое первое или второе яблока, то рано ещё
уходить и последний шаг с оцениванием веса пакета пока еще лишний.
Иначе, если оценивая яблоко, я решил что но мне не нравятся - все
дальнейшие действия этого шага тоже стоит пропустить и перейти к
началу новой итерации. В конце концов, некоторые яблоки в руки брать
даже не приходится — по ним сразу видно, что они мне не подойдут. Вот
таким образом мы можем использовать переходы на следующий шаг цикла.

Что касается прерывание всего цикла, тут ещё проще. Вот учите вы новую
тему в нашем курсе.  Просмотрели всё видео, выполнили все задачи,
оценили степень понимания.  Если не всё понятно — пересмотреть
урок. Если всё ещё непонятно — пересмотреть урок. И так, возможно, до
бесконечности. Если в какой-то момент всё стало очевидным — прекратить
пересматривать и перейти к следующему уроку. Так что нет никакой
разницы между реальной жизнью и программированием.

(видео конспект)
https://drive.google.com/open?id=1GlLcgHWgR8gbFjVcdTPcwiZ4MWUx8u6A -
примеры использования

---

(Говорящая голова)

А вам интересно для решения каких конкретных задач используются циклы?
Ответить крайне легко — для решения почти любой задачи, в которой
присутствуют множество элементов. Например, поиск элементов в
коллекции, вывод таблицы на экран, чтение файла с текстом. Даже при
воспроизведении этого видео ваш компьютер воспроизводит программу в
которой содержится цикл.  Но мы начнём пробовать с чего-то более
классического. Как насчёт того, чтобы попробовать что-то упорядочить —
и назовем мы наши колдунство сортировкой.

(видео конспект)
https://drive.google.com/open?id=1YKig8_jJ2dvxo7L8vGIJGFMcH639TWYs -
сортировка ---

(Говорящая голова)

Любой практикующий программист, увидев такую реализацию сортировки, до
конца своей жизни будет вас избегать. Она крайне неэффективная,
некрасивая, и выдуманная на лету.  Хотя, нужно быть честным, примерно
так и я решил задачу в которой нужно было что-то отсортировать, когда
впервые с ней столкнулся. А со временем я узнал, что проблема
упорядочивания достаточно распространена и для неё даже существует
множество решений. Называют эти решения алгоритмами сортировки — они
сложные, запутанные, но очень красивые. Нет нет, не подумайте что я
немного странный тип, который восхищается математикой. Просто
попробуйте вбить в Гугле " визуализация алгоритмов сортировки" и
посмотреть первые выданные видео — думаю вы поймёте о чём я
говорю. Учить эти алгоритмы не умея толком программировать — занятия
крайне неблагодарное. Так что давайте просто попробуем реализовать
нечто подобное одному из существующих хороших решений, а именно
сортировку выборкой, но не в полноценном академическом варианте, в
упрощенной форме. А как у вас появится свободное время , обязательно
почитайте про разные алгоритмы.

(видео конспект)
https://drive.google.com/open?id=1hGca3wqszfgwyJQp2LM-DFcnU4HYKDzA -
сортирока выборкой

---

(Говорящая голова)

Кроме того, циклы очень активно используется в уже существующих
возможностях Python. Например, при работе со строками, в тайне от вас,
интерпретатор бегает по отдельным символам строки с безумно
выпученными глазами для того чтобы упростить вам работу. Проверяя
строку на соответствие некому шаблону , изменяя регистр , сравнивая 2
строки между собой — всё это требует использования циклов . Ну, думаю
понять как с помощью цикла интерпретатор получает каждый отдельный
символ строки достаточно просто. А вот как он этот символ сравнивает с
другим символом, или как у этого символа меняется регистр? Если знать
как устроена работа с буквами внутри интерпретатора то, ответ
тоже оказывается крайне простым. В действительности вся ваша
программа, с точки зрения машины, как будто бы и не содержит
букв. Вместо любого символа используется какая-то цифра. Сравнивая две
буквы на равенство, компьютер просто сравнивает величину
чисел. Изменяя регистр компьютер просто прибавляет к числу что-то или
вычитает. И вот как это можно использовать нам...

(видео конспект)
https://drive.google.com/open?id=1s5tTPaerm0SBax0p2kBHMRiyQVUuhSpA -
работа с отдельными символами

---

(Говорящая голова)

Может вы сразу и не поверите но вся работа со строками основывается на
вот этом преобразовании в числa.  Самое смешное, даже настоящeе
преобразование в целое число строки содержащие цифры, происходит с
помощью вот этого промежуточного преобразования. Другими словами, нам
нужно сначала узнать какой цифрой является отдельный символ, Даже если
мы видим что этот символ — единица. Компьютер считает абсолютно
разными значениями символ единицы в виде строки и символ единицы в
виде числа. Поэтому ему нужно как-то определить связь между этими
двумя элементами. Для этого компьютер высчитывает код строки
содержащие единицу, который, к примеру, равен 48 и предполагает в
будущем , что каждый код 48 нужно воспринимать как цифру 1. Запутано,
но только если вы человек, а машине же достаточно легко понять эту
цепочку, до тех пор пока ее можно выразить последовательными
инструкциями.


(видео конспект)
https://drive.google.com/open?id=1leAgpra-1Q6U5FpntF1-VKdBV1AuAbs3 -
преобразование в числа

---

(Говорящая голова)

Вот и закончился очередной день в нашем повествовании. Надеюсь сегодня
вы услышали достаточно новых терминов и у вас будет что погуглить и
прочитать до следующего занятия. Советую не следовать тому циклу
который мы обсудили чуть ранее, с бесконечным пересмотром
занятия. Вместо этого, если что-то непонятно и вам очень хочется это
осилить самостоятельно без помощи окружающих, то попробуйте просто
переключиться сначала на другую тему. Почитайте про алгоритмы, про
распространённые практики и шаблоны программирования. А можно и просто
стороннюю литературу. Ну и разумеется не стоит пренебрегать прогулками
на свежем воздухе. Некоторые темы нужно понимать не пристально глядя
им в глаза а просто повторно перепроходя их спустя некоторое время. Не
торопитесь всё понять сейчас или сегодня, вместо этого повторяйте
материал каждый день и удивляетесь тому насколько очевидным начинает
казаться то что вчера давалась ещё с трудом. Жду вас на следующем
уроке
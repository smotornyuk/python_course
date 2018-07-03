# Лекция 5

(Говорящая голова)

Рад вас снова тот видеть. Ну как, вы успели попрактиковаться со строками и условиями с последней нашей встречи? Очень надеюсь что ответ положительный — сегодня эти навыки Вам будут как нельзя кстати. Потому что сегодня мы увидим некую альтернативу строкам -  Не в плане представления текста , а скорее идеологическую альтернативу коллекциям множества элементов.  Этой альтернативой является списки —  можно сказать самый  общий тип данных  Объединенных в группу коллекций. Коллекцией мы будем называть любую группу из множества элементов . в идеальном случае — однородных элементов , Хотя это не будет критическим требованием.  Как мы когда-то уже говорили, коллекции делятся на несколько категорий.  В частности, коллекции бывают упорядоченными и неупорядоченные. Упорядоченные коллекции мы уже видели — это строки . упорядоченность строк выражается в том, что у каждого отдельного символа есть свой индекс. Индекс символа постоянен, Если вы выполните перестановку символов, тем самым изменив их индексы, то вы получите совершенно другую строку. В упорядоченных коллекциях порядок элементов играет ключевую роль . в списке также относится к порядочным коллекциям. Затем, коллекции было от изменяемыми и неизменяемыми. Строки были неизменяемыми , благодаря чему мы не могли изменить отдельную букву В существующей строки — для подобной задачи нам пришлось бы создавать новую строку, которая отличалась бы от оригинала одним символом.
Ладно пожалуй стоит прервать мои словесные излияния и переключиться на самое интересное — практическая сторона списков. Начнем, пожалуй, с литералов списков — с  их наиболее простой и удобной формой создания.

(видео конспект)
https://drive.google.com/open?id=1MqmPopl3FwIErThPFCz9WWLouVZCbH65 - Литералы списков

---

(Говорящая голова)

Касательно работы с отдельными элементами списков. Это одна из множества деталей за которую я дико люблю  Python.  Списки поддерживает индексы и практически в том же формате что и строки, потому изучив хорошо индексов строках, вы без труда сумеете применить их и тут.  Как мы сейчас увидим мы можем извлекать элементы из списка с помощью индексов, мы можем использовать и срезы.  Аналогично строгом мы будем получать ошибки если попытаемся извлечь символ находящийся за пределами списка , но, с другой стороны,  мы можем пользоваться индексами с отрицательным значением для получения элементов относительно конца списка. Ну и чтобы это было Хоть немного интересным, мы сумеем модифицировать списки с помощью их индексов , что было недоступным в терминологии строк. Перейдем к деталям

(видео конспект)
https://drive.google.com/open?id=1h9f_77R64Y4NJBZQbdFkRIi_b8Q-YvtT - Индексы

---

(Говорящая голова)

Сравнение списков , пожалуй, весьма предсказуемо . Если проводить аналогию со строками, то мы можем предположить что величина списка определяется его содержимым. Сравнивая 2 коллекции мы поочередно сравниваем  элементы на соответствующих позициях — как только в одном из списков встречается больше элемент, то и весь список считается большим. Есть ли в обоих списках на одинаковых позициях стоят одинаковые элементы , то большим считается тот список в котором есть бонусная элементы. В конце концов, если в 2 списках имеются одинаковые элементы на одинаковых позиций и длина обоих списков тоже одинаково, то тогда списки равны. Ну и куда же без рассмотрения  этих правил в  интерпретаторе.

(видео конспект)
https://drive.google.com/open?id=1oVv2zLQP9OJCkWOQ9ui3Dz4ZaCdiTJyy - Равенство

---

(Говорящая голова)

Одним из переходных звеньев между списками и строками можно считать преобразования одного в другое. Трубку можно разбить на множество слов  — мы увидели это на прошлом занятии. Используя метод сплит мы определяем символ разделитель и получаем из строки список слов.  А если имеется метод для разбиения строки на множество слов, то Обязательно должно существовать и обратная операция — Ничто Что позволит нам восстановить исходную строку из множества отдельных небольших фрагментов. Давайте попытаемся написать код который подтвердит эту теорию

(видео конспект)
https://drive.google.com/open?id=1HmQdLuvir1v06PY_wcKa6a1A8WjycbXU - разбиение и соединение

---

(Говорящая голова)

Да, со списками работать достаточно интересно. В них может поместиться так много всего. Если быть честным то вы можете затолкать в список практически неограниченное количество данных , разве что вам нужно учитывать возможности вашего компьютера и  попытаться не израсходовать всю доступную память. После чего вы последовательно будете работать с каждым элементом списка начиная с самого первого , переходя на 2, потом на 3 , потом на 4 и так  , наверное, до бесконечности . Ах да, Не забывайте что вы не будете ограничиваться только выводом элементов на экран — наиболее вероятно, что вы захотите также что-то сделать с каждым элементом: преобразовать, его сложить с предыдущим значением, отправить другу по почте — Попробуйте придумать на скидку 20 других задач с которыми вы можете столкнуться обрабатывая элементы списка. И чтобы увидеть проблему, давайте-ка напишем это всё своими ручками ...

(видео конспект)
https://drive.google.com/open?id=1x4NDxJ_pNuhmiKND_lqzuedxKVTMWNp1 - циклы и while

---

(Говорящая голова)

Инструкция while и If как Две родных сестры — обе они начинаются с ключевого слова определяющего саму операцию, потом следует некое условия результирующее в правду либо ложь, После чего мы ставим двоеточие и описываем серию действий , которые необходимо предпринять в случае успешного выполнения условия. Мы не ограничены в количестве выполняемых действий  — главное соблюдать отступ и в какой-то момент прервать блок кода вернувшись на изначальный уровень.  И следующие несколько примеров должны вас убедить в том что обе эти инструкции почти не различимы

(видео конспект)
https://drive.google.com/open?id=1f0D32jhyWfruZW82xiFZmw5qgaypS3cF - подробности о while

---

(Говорящая голова)

Сами по себе циклы уже очень удобно, но так и в условных конструкциях, возможностей никогда не бывает слишком много. Так что очень хотелось бы добавить некие инструкции для контроля выполнения циклов.  Как вы думаете, что Можно контролировать в циклах. Если задуматься, цикл состоит из множества однородных действий . Представим себя в длинном коридоре с множеством комнат. Следуя циклу, мы должны открывать двери в эти комнаты, одну за другой. Что мы можем себе позволить, так это пропустить некоторые двери, Например, если они закрыты. Или просто они очень скучные и не вызывают у нас интереса. Также, вероятно, вам может это  наскучить и вы захотите вернуться домой. Таким образом нам нужна некая инструкция для досрочного прерывания цикла. Только что сказанное в общем-то и описывает полностью все возможности контроля цикла.

(видео конспект)
https://drive.google.com/open?id=1jNMDhQvWfzSHUUTnYD1dCAo_QHkrS3Oj - контроль выполнения цикла

---

(Говорящая голова)


(видео конспект)
https://drive.google.com/open?id=1GlLcgHWgR8gbFjVcdTPcwiZ4MWUx8u6A - примеры использования

---

(Говорящая голова)


(видео конспект)
https://drive.google.com/open?id=1YKig8_jJ2dvxo7L8vGIJGFMcH639TWYs - сортировка
---

(Говорящая голова)


(видео конспект)
https://drive.google.com/open?id=1hGca3wqszfgwyJQp2LM-DFcnU4HYKDzA - сортирока выборкой

---

(Говорящая голова)


(видео конспект)
https://drive.google.com/open?id=1s5tTPaerm0SBax0p2kBHMRiyQVUuhSpA - работа с отдельными символами

---

(Говорящая голова)


(видео конспект)
https://drive.google.com/open?id=1leAgpra-1Q6U5FpntF1-VKdBV1AuAbs3 - преобразование в числа
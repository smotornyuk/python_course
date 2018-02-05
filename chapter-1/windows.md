#### Начало работы {#begining}
> Первый скринкаст "начало работы"

В стандартном сценарии, сразу после запуска коммандной строки, пользователь оказывается в своей домашней директории.

```
	Z:\home\sergey>
```

#### dir {#dir}
> Второй скринкаст "dir"

Комманда `dir`  без аргументов - отобразить содержимое текущей директории

```
Z:\home\sergey>dir
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:\home\sergey

 1/21/2018   9:01 PM  <DIR>         .
10/15/2017  10:29 AM  <DIR>         ..
 1/10/2018   4:18 PM  <DIR>         Desktop
 1/20/2018   2:18 AM  <DIR>         Downloads
12/16/2017   2:53 PM  <DIR>         Documents
 1/10/2018   5:10 PM  <DIR>         Games
 11/3/2017   9:37 AM  <DIR>         go
 5/19/2017  11:39 PM  <DIR>         Mail
  9/1/2017  12:52 PM  <DIR>         Music
 4/22/2017   2:45 PM  <DIR>         News
 1/14/2018   2:53 PM  <DIR>         Pictures
 1/21/2018   3:51 PM  <DIR>         Projects
 4/22/2017  12:46 PM  <DIR>         Public
 4/22/2017  12:46 PM  <DIR>         Templates
11/27/2017  10:44 AM  <DIR>         Videos
	   0 files                        0 bytes
	  15 directories    152,631,205,888 bytes free
```

#### Аргументы комманд {#arguments}

Аргументы комманд - значения указываемые через пробел после самой комманды. Формат и смысл аргументов может сильно отличаться в зависимости от самой комманды. В случае `dir`, аргумент определяет директорию, чье содержимое будет отображено в результате. Отсутствие аргумента подразумевает текущую директорию(`.`)

```
Z:\home\sergey>dir Projects
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:\home\sergey\Projects

 1/21/2018   3:51 PM  <DIR>         .
 1/21/2018   9:01 PM  <DIR>         ..
 1/11/2018   9:22 PM  <DIR>         base.dev
11/26/2017   8:04 PM  <DIR>         ckan
 1/21/2018   8:50 PM  <DIR>         courses
 10/5/2017   6:18 PM  <DIR>         ds
 9/29/2017  12:06 PM  <DIR>         dsfs
 1/21/2018   3:48 PM  <DIR>         javascript
 1/16/2018  10:34 PM  <DIR>         ncd
 1/14/2018   4:29 PM  <DIR>         python
       0 files                        0 bytes
      10 directories    152,631,205,888 bytes free
```

#### Ссылка на текущую директорию {#current-dir}

Абсолютно в каждой директории есть ссылка на текущее положение. Т.е в любой папке есть элемент, который является самой этой папкой. Обратиться к нему можно с помощью `.`(одна точка)

```
Z:\home\sergey>dir .
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:\home\sergey

 1/21/2018   9:01 PM  <DIR>         .
10/15/2017  10:29 AM  <DIR>         ..
 1/10/2018   4:18 PM  <DIR>         Desktop
12/16/2017   2:53 PM  <DIR>         Documents
 1/20/2018   2:18 AM  <DIR>         Downloads
 1/10/2018   5:10 PM  <DIR>         Games
 11/3/2017   9:37 AM  <DIR>         go
 5/19/2017  11:39 PM  <DIR>         Mail
  9/1/2017  12:52 PM  <DIR>         Music
 4/22/2017   2:45 PM  <DIR>         News
 1/14/2018   2:53 PM  <DIR>         Pictures
 1/21/2018   3:51 PM  <DIR>         Projects
 4/22/2017  12:46 PM  <DIR>         Public
 4/22/2017  12:46 PM  <DIR>         Templates
11/27/2017  10:44 AM  <DIR>         Videos
       0 files                        0 bytes
      15 directories    152,631,205,888 bytes free
```

#### Ссылка на родительскую директорию {#parent-dir}

Также в каждой папке есть ссылка на родительскую директорию - папку, которая содержит текущую папку - `..`(две точки). Для корня файловой системы `..` и `.` указывают на сам корень файловой системы

```
Z:\home\sergey>dir ..
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:\home

10/15/2017  10:29 AM  <DIR>         .
12/10/2017   3:56 PM  <DIR>         ..
10/15/2017  10:29 AM  <DIR>         home
 4/22/2017  11:03 AM  <DIR>         lost+found
 1/21/2018   9:01 PM  <DIR>         sergey
 1/10/2018   4:17 PM  <DIR>         transmission
       0 files                        0 bytes
       6 directories    152,631,205,888 bytes free
```
#### Корень файловой системы {#root}

`\`(обратный слеш) указывает на корень файловой системы. В случае Windows - это сам диск, на котором находится пользователь в момент вызова комманды. Находясь в `C:\Program Files\Prog`, пользователь получит `C:\`, обратившись к корню. В случае `Z:\xxx\yyy` - корнем будет `Z:\`

Стоит заметить, что в корне файловой системы `.` и `..` указывают на текущее положение.

````
Z:\home\sergey>dir \
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:

 1/21/2018   3:50 PM  <DIR>         bin
  1/1/1970   2:00 AM  <DIR>         boot
 4/22/2017   5:05 PM  <DIR>         data
 1/21/2018   3:50 PM  <DIR>         etc
10/15/2017  10:29 AM  <DIR>         home
 1/21/2018   3:50 PM  <DIR>         lib
 1/21/2018   3:50 PM  <DIR>         lib64
 4/22/2017  11:32 AM  <DIR>         lost+found
 3/26/2017  11:57 PM  <DIR>         mnt
 11/8/2017  10:50 AM  <DIR>         opt
 1/20/2018   2:34 AM  <DIR>         root
 1/21/2018   5:08 PM  <DIR>         run
 1/21/2018   3:50 PM  <DIR>         sbin
 3/26/2017  11:57 PM  <DIR>         srv
 1/21/2018   9:00 PM  <DIR>         tmp
 1/21/2018   3:50 PM  <DIR>         usr
 1/20/2018   2:30 AM  <DIR>         var
       0 files                        0 bytes
      17 directories    152,631,205,888 bytes free
```

### Unix {#unix}

#### Терминал в unix системах {#term}
> Третий скринкаст "Unix"

Основная идея остается такой же как и в windows. Ключевые отличия:
* Вместо обратного слеша(`\`) используется обычный(`/`)
* Понятия дисков(разделов `C:`, `D:`, `A:`), как в windows, не существует. Вместо этого используется процесс монтирования разделов. Простыми словами - корнем файловой системы всегда является директория `/`
* Большинство комманд отличается

Комманда `dir`(и схожая комманда `ls`) перечисляет содержимое текущей директории. Для того, чтобы увидеть список подобный результату windows, можно использовать аргумент -l.

Для отображения текущего положения используется комманда `pwd`

```
[sergey@home ~]$ dir
Desktop    Downloads  go    Music  Pictures  Public     Videos
Documents  Games      Mail  News   Projects  Templates
[sergey@home ~]$ ls
Desktop    Downloads  go    Music  Pictures  Public     Videos
Documents  Games      Mail  News   Projects  Templates
[sergey@home ~]$ ls -l
total 60
drwxr-xr-x  2 sergey sergey  4096 Jan 10 16:18 Desktop
drwxr-xr-x  6 sergey sergey  4096 Dec 16 14:53 Documents
drwxr-xr-x  2 sergey sergey 12288 Jan 20 02:18 Downloads
drwx------  9 sergey sergey  4096 Jan 10 17:10 Games
drwxr-xr-x  5 sergey sergey  4096 Nov  3 09:37 go
drwxr-xr-x  4 sergey sergey  4096 May 20  2017 Mail
drwxr-xr-x 11 sergey sergey  4096 Sep  1 13:52 Music
drwxr-xr-x  3 sergey sergey  4096 Apr 22  2017 News
drwxr-xr-x 10 sergey sergey  4096 Jan 14 14:53 Pictures
drwxr-xr-x 10 sergey sergey  4096 Jan 21 15:51 Projects
drwxr-xr-x  2 sergey sergey  4096 Apr 22  2017 Public
drwxr-xr-x  2 sergey sergey  4096 Apr 22  2017 Templates
drwxr-xr-x  5 sergey sergey  4096 Nov 27 10:44 Videos
[sergey@home ~]$ ls -l Projects
total 32
drwxr-xr-x  6 sergey sergey 4096 Jan 11 21:22 base.dev
drwxr-xr-x  9 sergey sergey 4096 Nov 26 20:04 ckan
drwxr-xr-x  6 sergey sergey 4096 Jan 21 20:50 courses
drwxr-xr-x 10 sergey sergey 4096 Oct  5 19:18 ds
drwxr-xr-x  5 sergey sergey 4096 Sep 29 13:06 dsfs
drwxr-xr-x  5 sergey sergey 4096 Jan 21 15:48 javascript
drwxr-xr-x  3 sergey sergey 4096 Jan 16 22:34 ncd
drwxr-xr-x 11 sergey sergey 4096 Jan 14 16:29 python
[sergey@home ~]$ pwd
/home/sergey
[sergey@home ~]$ cd Projects
[sergey@home Projects]$ pwd
/home/sergey/Projects
[sergey@home Projects]$ cd /
[sergey@home /]$ pwd
/
[sergey@home /]$ dir /home/sergey/Projects
base.dev  ckan  courses  ds  dsfs  javascript  ncd  python
[sergey@home /]$ ls -l /home/sergey/Projects
total 32
drwxr-xr-x  6 sergey sergey 4096 Jan 11 21:22 base.dev
drwxr-xr-x  9 sergey sergey 4096 Nov 26 20:04 ckan
drwxr-xr-x  6 sergey sergey 4096 Jan 21 20:50 courses
drwxr-xr-x 10 sergey sergey 4096 Oct  5 19:18 ds
drwxr-xr-x  5 sergey sergey 4096 Sep 29 13:06 dsfs
drwxr-xr-x  5 sergey sergey 4096 Jan 21 15:48 javascript
drwxr-xr-x  3 sergey sergey 4096 Jan 16 22:34 ncd
drwxr-xr-x 11 sergey sergey 4096 Jan 14 16:29 python
[sergey@home /]$
```

> [Дополнительная информация](http://www.linuxcenter.ru/lib/books/shell/) для начинающих пользователей unix систем


#### cd {#cd}
> Четвертый скринкаст "cd"

Комманда `cd` показывает текущее положение(если выполнена без аргументов)

```
Z:\home\sergey>cd
Z:\home\sergey
```

#### Перемещение в соседнюю директорию {#sibling-dir}

Добавляя аргументы, пользователь заставляет командную строку перейти в целевую директорию. Как результат, все дальнейшие комманды(включая комманды без аргументов) будут отталкиваться от нового местоположения

```
Z:\home\sergey>cd Projects

Z:\home\sergey\Projects>dir
Volume in drive Z has no label.
Volume Serial Number is 0000-0000

Directory of Z:\home\sergey\Projects

 1/21/2018   3:51 PM  <DIR>         .
 1/21/2018   9:01 PM  <DIR>         ..
 1/11/2018   9:22 PM  <DIR>         base.dev
11/26/2017   8:04 PM  <DIR>         ckan
 1/21/2018   8:50 PM  <DIR>         courses
 10/5/2017   6:18 PM  <DIR>         ds
 9/29/2017  12:06 PM  <DIR>         dsfs
 1/21/2018   3:48 PM  <DIR>         javascript
 1/16/2018  10:34 PM  <DIR>         ncd
 1/14/2018   4:29 PM  <DIR>         python
       0 files                        0 bytes
      10 directories    152,631,205,888 bytes free
```

#### Сложные пути {#complex-path}

Для ускоренного перемещения можно использовать компоненты пути, разделенные обратным слешем. Комбинации, начинающиеся со слова, отталкиваются от текущего местоположения. Две точки в начале пути означают родительскую директорию. Обратный слеш - заставляет отсчитывать путь от корня файловой системы

```
Z:\home\sergey\Projects>cd courses

Z:\home\sergey\Projects\courses>cd ..

Z:\home\sergey\Projects>cd
Z:\home\sergey\Projects

Z:\home\sergey\Projects>cd ..\..\..

Z:\>cd
Z:
Z:\>cd home\sergey\Projects

Z:\home\sergey\Projects>cd ..\Projects\..\..\sergey\Projects

Z:\home\sergey\Projects>cd .

Z:\home\sergey\Projects>cd .\.\.\.\.

Z:\home\sergey\Projects>cd ..\.\.\.\.\.\Projects

Z:\home\sergey\Projects>
```

> [Введение](http://it-like.ru/kak-zapustit-komandnaya-stroka-windows-7-8-komandyi/) в пользование коммандной строкой и [список комманд](http://ab57.ru/cmdlist.html)

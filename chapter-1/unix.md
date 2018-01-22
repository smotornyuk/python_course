#### Терминал в unix системах {#term}

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

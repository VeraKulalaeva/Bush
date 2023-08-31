# Bush

В представленных заданиях отрабатывается навык использования командной оболочки Bush, позволяющей освоить систему базовых команд для работы с файлами и папками, поиском, настройкой окружения и управления ОС прямо из командной строки

## Часть 1

```bush
1) Зайти в домашнюю директорию
~

2) Определить имя папки, в которой вы находитесь
$ pwd

3) Создать каталог с именем test1
$ mkdir test1

4) Перейти в папку test1
$ cd test1

5) Создать файл 1, 2 и 3 внутри каталога test1
$ touch file1.txt file2.txt file3.txt

6) Проверить содержимое каталога test1
$ ls

7)Перейти в домашнюю директорию
$ cd ..

8)Создать папку test2 внутри домашней директории
$ mkdir test2

9) Удалить папку test2
$ rmdir test2

10)Удалить файл 2 из папки test1
$ cd test1
$ rm file2.txt
$ ls

11)Создать папку в домашней директории test3 и добавить в нее два файла
$ cd ..
$ mkdir test3
$ cd test3
$ touch file_1.txt file_2.txt
$ ls

12) Удалить папку test3
$ cd ..
$ rm -rf test3
$ ls

13) Создать папку test4 в домашней директории
$ mkdir test4

14) Переместить файлы 1 и 3 из папки test1 в папку test4
$ mv test1/file1.txt test4
$ mv test1/file3.txt test4
$ cd test4
$ ls

15) Добавить в файл 1 три строки со словами line
$ echo line >file1.txt
$ echo line >>file1.txt
$ echo line >>file1.txt

16) Посмотреть содержимое файла 1
cat file1.txt

17) Добавьте в файл 3 три строки со словами line
$ echo line >file3.txt
$ echo line >>file3.txt
$ echo line >>file3.txt

18) Просмотрите содержимое двух файлов (1 и 3) сразу
$ cat file1.txt file3.txt

19) Используя один из редакторов замените все строки в файле 1
$ vim file1.txt
$ cat file1.txt

```
## Часть 2

```bush
1) Зайти в домашнюю директорию
~
$ pwd

2) Создать папку test 3
$ mkdir test3
$ git add .

3) Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
$ cd test3
$ touch file4.txt file5.txt file6.txt
$ git add .
$ echo row1 >file4.txt
$ vim file4.txt
$ cat file4.txt
$ git add .

$ cat >file5.txt <<EOF
> row1
> row2
> row3
> row4
> EOF
$ cat file5.txt

$ cat >file6.txt <<EOF
> row1
> row2
> row3
> row4
> EOF
$ cat file6.txt
$ git add .

4)Найдите строку row2 в файле 5
$ grep -i "row2" file5.txt

5) Найдите строку row в папке test3

grep -R "row"

6)Посчитайте сколько строк с содержимым row в файле 6
$ grep -c "row" file6.txt

7)Найдите файл 5 внутри папки test3
$ find . -name "file5.txt"

8) Используя команду find, удалите файл 5
$ find . -name "file5.txt" -delete
$ cd ..
$ ls test3

9) Используя команду echo, добавьте слово test в файл 4
$ echo test >>file4.txt
$ cat file4.txt

10) Замените слово test в файле 4 на fail
$ nano file4.txt
$ cat file4.txt

11) Добавьте в файл 4 слово test так, чтобы сохранилось содержимое
$ echo test >>file4.txt
$ git add .
$ cat file4.txt

12) Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе
$ ps aux

$ tasklist

13) Убейте процесс 666 в консоли
$ kill PID666

14) Узнайте доступность ресурса artsiomrusau.com, используя ping
$ ping  artsiomrusau.com

15) Отправьте 5 пакетов на сайт artsiomrusau.com
$ ping -n 5 artsiomrusau.com

16) Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/
$ curl petstore.swagger.io/v2/pet/findByStatus?status=pending

17) Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/
curl -X POST https://petstore.swagger.io/v2/user --data "userID =15" --data "username =Sunday"    
# bash

Sometimes we need to work with remote servers with no graphic interface. In this case it's important to be able to use bash commands to perform regular actions such as creating, editing, deleting files via CLI. 

## Task 1

##### Working with files and directories
```bash
1. Открыть домашнюю директорию

421@LAPTOP-C008GGKN MINGW64 ~/Desktop
$ cd ..
421@LAPTOP-C008GGKN MINGW64 ~

2. Определить имя папки, в которой вы находитесь

421@LAPTOP-C008GGKN MINGW64 ~
$ pwd
/c/Users/421

3. Создать внутри этой папки каталог с именем test1

421@LAPTOP-C008GGKN MINGW64 ~
$ mkdir test1

4. Перейти в папку test1

421@LAPTOP-C008GGKN MINGW64 ~
$ cd test1
421@LAPTOP-C008GGKN MINGW64 ~/test1

5. Создать файл 1,2 и 3 внутри каталога test1

421@LAPTOP-C008GGKN MINGW64 ~/test1
$ touch 1
421@LAPTOP-C008GGKN MINGW64 ~/test1
$ touch 2
421@LAPTOP-C008GGKN MINGW64 ~/test1
$ touch 3

6. Проверить содержимое каталога test1

421@LAPTOP-C008GGKN MINGW64 ~/test1
$ ls
1  2  3

7. Перейти в домашнюю директорию

421@LAPTOP-C008GGKN MINGW64 ~/test1
$ cd ..
421@LAPTOP-C008GGKN MINGW64 ~


8. Создать папку test2 внутри домашней директории

421@LAPTOP-C008GGKN MINGW64 ~
$ mkdir test2

9. Удалить папку test2

421@LAPTOP-C008GGKN MINGW64 ~
$ rmdir test2

10. Удалить файл 2 из папки test1

421@LAPTOP-C008GGKN MINGW64 ~
$ cd test1
421@LAPTOP-C008GGKN MINGW64 ~/test1
$ rm 2
421@LAPTOP-C008GGKN MINGW64 ~/test1
$ ls
1  3

11. Создать папку в домашней директории test3 и добавить в нее два файла

421@LAPTOP-C008GGKN MINGW64 ~/test1
$ cd ..
421@LAPTOP-C008GGKN MINGW64 ~
$ mkdir test3
421@LAPTOP-C008GGKN MINGW64 ~
$ cd test3
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ touch file1
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ touch file2

12. Удалить папку test3

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ cd ..
421@LAPTOP-C008GGKN MINGW64 ~
$ rm -rf test3

13. Создать папку test4 в домашней директории

421@LAPTOP-C008GGKN MINGW64 ~
$ mkdir test4

14. Переместить файлы 1 и 3 из папки test1 в папку test4

421@LAPTOP-C008GGKN MINGW64 ~
$ mv test1/1 test1/3 test4
421@LAPTOP-C008GGKN MINGW64 ~
$ ls test1
421@LAPTOP-C008GGKN MINGW64 ~
$ ls test4
1  3

15. Добавить в файл 1 три строки со словами line

421@LAPTOP-C008GGKN MINGW64 ~
$ echo line 1 >> 1
421@LAPTOP-C008GGKN MINGW64 ~
$ echo line 2 >> 1
421@LAPTOP-C008GGKN MINGW64 ~
$ echo line 3 >> 1

16. Посмотреть содержимое файла 1

421@LAPTOP-C008GGKN MINGW64 ~
$ cat 1
line 1
line 2
line 3

17. Добавьте в файл 3 три строки со словами line

421@LAPTOP-C008GGKN MINGW64 ~
$ echo 1 line >> 3
421@LAPTOP-C008GGKN MINGW64 ~
$ echo 1 line >> 3
421@LAPTOP-C008GGKN MINGW64 ~
$ echo 1 line >> 3

18. Просмотрите содержимое двух файлов (1 и 3) сразу

421@LAPTOP-C008GGKN MINGW64 ~
$ cat 1 3
line 1
line 2
line 3
1 line
1 line
1 line

19. Используя один из редакторов замените все строки в файле 1

421@LAPTOP-C008GGKN MINGW64 ~
$ nano 1
421@LAPTOP-C008GGKN MINGW64 ~
$ cat 1
changed line 1
changed line 2
changed line 3

nano file3.txt + manual replacement 
```
## Task 2
##### Editing files, checking and killing proccesses, pinging websites
```bash
1. Зайти в домашнюю директорию

421@LAPTOP-C008GGKN MINGW64 ~
$

2. Создать папку test 3

421@LAPTOP-C008GGKN MINGW64 ~
$ mkdir test3

3. Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4

421@LAPTOP-C008GGKN MINGW64 ~
$ cd test3
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ touch 4 5 6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ ls
4  5  6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row1 >> 4
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row2 >> 4
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row3 >> 4
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row4 >> 4
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row1 >> 5
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row2 >> 5
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row3 >> 5
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row4 >> 5
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row1 >> 6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row2 >> 6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row3 >> 6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo row4 >> 6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ cat 4 5 6
row1
row2
row3
row4
row1
row2
row3
row4
row1
row2
row3
row4

4. Найдите строку row2 в файле 5

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ grep -i "row2" 5
row2

5. Найдите строку row в папке test3

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ grep -R "row" .
./4:row1
./4:row2
./4:row3
./4:row4
./5:row1
./5:row2
./5:row3
./5:row4
./6:row1
./6:row2
./6:row3
./6:row4

6. Посчитайте сколько строк с содержимым row в файле 6

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ grep -c "row" 6
4

7. Найдите файл 5 внутри папки test3

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ find 5
5

8. Используя команду find, удалите файл 5

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ ls
4  5  6
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ find 5 -delete
421@LAPTOP-C008GGKN MINGW64 ~/test3
$ ls
4  6

9. Используя команду echo, добавьте слово test в файл 4

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo test >> 4

10. Замените слово test в файле 4 на fail

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ sed -i 's/test/fail/' 4

11. Добавьте в файл 4 слово test так, чтобы сохранилось содержимое

421@LAPTOP-C008GGKN MINGW64 ~/test3
$ echo test >> 4

12. Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе

421@LAPTOP-C008GGKN MINGW64 ~
$ ps aux

13. Убейте процесс 666 в консоли

421@LAPTOP-C008GGKN MINGW64 ~
$ kill 666

14. Узнайте доступность ресурса artsiomrusau.com, используя ping

421@LAPTOP-C008GGKN MINGW64 ~
$ ping artsiomrusau.com

15. Отправьте 5 пакетов на сайт artsiomrusau.com

421@LAPTOP-C008GGKN MINGW64 ~
$ ping -c 5 artsiomrusau.com

16. Используя GET и команду curl, получите информацию о зарегистрированных питомцах на https://petstore.swagger.io/

curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available"

17. Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/

curl -X POST -H "Content-Type: application/json" -d '{
  "id": 667,
  "username": "JerryB",
  "firstName": "Jerry",
  "lastName": "Brown",
  "email": "jerry_brown@mail.ru",
  "password": "jerb123",
  "phone": "89133224558"
}' "https://petstore.swagger.io/v2/user"
```

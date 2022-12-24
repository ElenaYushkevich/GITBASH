Linux terminal (GitBash) commands

1) Посмотреть где я
```bash
pwd
```
2) Создать папку
```bash
mkdir dir1
```
3) Зайти в папку
```bash
cd dir1
```
4) Создать 3 папки
```bash
mkdir dir2 dir3 dir4
```
5) Зайти в любоую папку
```bash
cd dir2
```
6) Создать 5 файлов (3 txt, 2 json)
```bash
touch t1.txt t2.txt t3.txt j1.json j2.json
```
```bash
touch t{1..3}.txt j{4,5}.json
```
7) Создать 3 папки
```bash
mkdir dir5 dir6 dir7
```
8) Вывести список содержимого папки
```bash
ls -la
```
9) Открыть любой txt файл
```bash
cat >> t1.txt
```
или
```bash
vim t1.txt
```
10) написать туда что-нибудь, любой текст.
```bash
row_1
row_2
row_3
```
или
```bash
Буква I и вводим текст, ESC - это для vim
```
11) сохранить и выйти.
```bash
Ctrl+C
```
или
```bash
:wq Enter - это для vim
```
12) Выйти из папки на уровень выше
```bash
cd ..
```
13) переместить любые 2 файла, которые вы создали, в любую другую папку.
```bash
mv dir2/t1.txt dir2/j1.json dir2/dir5/
```
или
```bash
mv t{2,3}.txt dir5/
```
14) скопировать любые 2 файла, которые вы создали, в любую другую папку.
```bash
cp dir2/t2.txt dir2/j2.json dir2/dir6/
```
или
```bash
cp t{1,2}.json dir6/
```
15) Найти файл по имени
```bash
find . -name "t1.txt" -type f
```
16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
```bash
tail -f file.log | grep error
Ctrl+C
```
17) вывести несколько первых строк из текстового файла
```bash
head -2 t1.txt
```
18) вывести несколько последних строк из текстового файла
```bash
tail -2 t1.txt
```
19) просмотреть содержимое длинного файла (команда less) изучите как она работает.
```bash
less file.log - листаем длинный файл с помощью стрелок, выйти Q
```
20) вывести дату и время
```bash
date
```
или
```bash
date +"%d-%m-%Y %H:%M:%S"
```
=========

Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request

```bash
curl http://162.55.220.72:5005/terminal-hw-request
```
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   283  100   283    0     0   3056      0 --:--:-- --:--:-- --:--:--  3109{
  "Intro": "Hello!! This is your the first response from server",
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)",
    "result": [
      "Your_String",
      "Your_number"
    ]
  }
}


```bash
curl "http://162.55.220.72:5005/get_method?name=(Lenchick)&age=(18)"
```

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
script.txt
```bash
#!/bin/bash
cd dir1
mkdir dir2 dir3 dir4
cd dir2
touch t1.txt t2.txt t3.txt j1.json j2.json
mkdir dir5 dir6 dir7
ls -la
mv t1.txt j1.json dir5
```
запускаем командой 
```bash
./script.txt
```

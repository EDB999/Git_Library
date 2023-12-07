# Git_Library
## Библиотека пользования Git, включающая инструкции, подсказки и напоминания.
### Основные команды Git для работы с директориями и файлами, их описание.

1. В командной строке вы всегда находитесь в какой-то папке — просто этого не видно. <br>
Команда: pwd (print working directory — «показать рабочую папку») - узнать, где вы сейчас, с помощью вывода пути к текущей директории (папки). <br>
<br>

2. С помощью терминала вы всегда можете перейти к домашней директории. <br>
Команда: cd (change directory — «сменить директорию») и символ ~ — обозначение домашней директории. <br>
Синтаксис cd - меняет текущую рабочую директорию на ту, которая указана в качестве параметра: [cd] [имя_папки].<br>
Сочетания и фишки: <br>
a) Чтобы вернуться в родительскую директорию — то есть на уровень выше, — вместо названия папки нужно написать две точки: .. (cd ..) ; <br>
b) Чтобы обратиться к текущей директории - вместо названия папки нужно написать одну точку: . (cd .); <br>
c) Чтобы перемещаться сразу через несколько директорий нужно разделить названия директорий с помощью / (Дано условием: $ pwd /projects <br>
Пример: $ cd github/open-source-project). *Примечание - можно указать и полный путь. (Пример: cd /c/Users/newUser/pictures/photo)<br>
*Обратите внимание: если в названии папки есть пробелы, при вводе нужно использовать кавычки. (Пример )<br>
<br>

3. Когда вы открываете папку через графический интерфейс операционной системы, вы сразу видите её содержимое. <br>
Команда: ls (list directory contents — «отобразить/вывести содержимое директории») - В случае с консолью выступает для отображения файлов и папок. <br>
Сочетания и фишки: <br>
a) Чтобы вывести расширенный список, в котором отобразятся все скрытые файлы(. .. и .git) нужно использовать флаг ls-a. <br>
b) Чтобы вывести содержимое домашней директории, вне зависимости от того, что показывается pwd, используется ls ~. <br>
c) Чтобы вывести содержимое родительской директории, вне зависимости от того, что показывается pwd, используется ls .. . <br>

4. Команда: touch - чтобы создать файл, нужно ввести в консоль команду touch («коснуться») с именем файла в качестве параметра.
Синтаксис: touch %ИМЯ_ФАЙЛА%. <br>
(Пример: $ touch my-new-file.txt) <br>
*Обратите внимание: Хорошей практикой при создании файла считается указывать его расширение (в примере — .txt). Это позволит операционной системе выбрать подходящую программу, чтобы открыть файл. <br>

5. Команда: mkdir (make directory — «создать директорию») - позволяет создать директорий через командную строку.
(Пример: $ mkdir new-dir)
Сочетания и фишки:
- Можно создать целую структуру директорий одной командой с помощью флага -p. <br>
(Пример: $ mkdir -p dir1/dir-inside/dir-deeper-inside) <br>
- Можно использовать обе команды вместе с символом домашней директории (~) или родительской директории (..). <br>
(Пример: ~/my-git-projects или touch ../../file.txt) <br>


6. Команда: cp (copy — «копировать») - служит для копирования файлов через командную строку. При копировании можно указать сразу несколько файлов.  <br>
Синтаксис: $ cp что_копируем куда_копируем ИЛИ $ cp что_копируем что_копируем что_копируем куда_копируем) <br>
(Пример: $ cp index.html src/ ИЛИ $ cp index.html style.css script.js src/) <br>
Сочетания и фишки: <br>
- Можно использовать обе команды вместе с символом домашней директории (~) или родительской директории (..). <br>

7. Команда: mv (move - переместить) - позволяет удалить файл в одном месте и создать в другом. <br>
Синтаксис: аналогичен команде cp. <br>
(Пример: $ mv table.csv ./very-important-files) <br>
Обратите внимание: можно копировать или перемещать файлы из разных директорий в одной команде. <br>
(Пример: $ mv ../file.txt cool.png cool-files) <br>

8. Команда: cat (concatenate and print — «объединить и распечатать») - позволяет прочитать файл и выведет(распечатает) в консоли его содержимое. <br>
Синтаксис: $ cat имя_файла <br>
(Пример: $ cat myfile.txt. Будет выведено file-content-1 file-content-2) <br>
!!!Внимание: Команда cat работает только с текстовыми файлами. Вывести этой командой файл другого типа (например, изображение) не получится. <br>

9. Команда: 1) rm (remove - удалить) - позволяет удалить файл.  <br>
Синтаксис: $ rm имя_файла <br>
(Пример: rm example.txt) <br>

2) rmdir (remove directory - удалить директорию) - позволяет удалить директорий(папку) без его содержимого. <br>
Синтаксис: $ rmdir имя_директория <br>
(Пример: rmdir images) <br>
!!!Внимание: если в папке, которую вы пытаетесь стереть, есть какие-то файлы, то командная строка не удалит её и выведет сообщение о том, что папка не пуста(Directory not empty) <br>

3) rm -r (-r recursive - рекурсивно) - позволяет удалить директорий(папку), вместе с его содержимым. Удаление будет последовательно применяться к каждому из элементов в этой папке — пока не сотрёт их все, а затем и директорию. <br>
Синтаксис: $ rm -r имя_директория <br>
(Пример: rm -r images) <br>
!!!Внимание: удаление объектов командами rm и rmdir необратимо — в этом случае файлы и папки не попадают в корзину и исчезают навсегда. <br>

10) Команды в командной строке необязательно вбивать и выполнять по очереди. Их можно указывать не по одной, а сразу списком. Для этого их нужно разделить двумя амперсандами (&&). <br>
(Пример: $ mkdir second-project && cd second-project && touch index.html style.css) <br>

11) У командной строки есть свой собственный буфер(buffer - посредник). В буфере хранятся все команды, которые вызывались до этого. По их списку можно перемещаться. <br>
Чтобы обратиться к последней введённой команде, нажмите на клавиатуре стрелку вверх (↑). Если нажать ещё раз, появится предпоследняя команда; ещё раз — предпредпоследняя; и так далее. <br>
Чтобы вернуться — например, от предпоследней команды к последней, — нажмите стрелку вниз (↓). <br>

12) Если нужно найти какую-нибудь из них, достаточно вспомнить, с каких букв она начинается. Можно набрать их в командной строке и дважды нажать клавишу Tab. Терминал покажет список всех команд, которые начинаются с этих символов. <br>
Tab автоматически дописывает не только команды, но и пути. Терминал заполнит имя автоматически. <br>
*Примачание: если этого не происходит, значит, есть несколько файлов или папок, которые начинаются так же. Нажмите Tab ещё раз, и вы увидите их список. <br>
Есть ещё один способ использовать Tab при навигации в другую директорию. Если ввести cd с названием папки, а затем нажать Tab, в консоль в качестве подсказки выведутся в се возможные пути. <br>
Если вывод будет слишком большой, консоль спросит, нужно ли показать все возможные варианты. <br>
Чтобы подтвердить вывод, нужно нажать y, а чтобы отменить автодополнение — n. <br>

13) Команда: / + [TAB] - позволяет мгновенно перемещаться в ключевые(корневые) папки. Это верхняя в иерархии папка, в которой хранится всё, что есть на вашем жёстком диске. <br>
*Примечание аналогично работает для cd - cd / ИЛИ cd /c(чтобы перейти на соотвествующий диск) <br>

14) Команда: git config -  (configuration — «конфигурация», «настройка») - можно указать любое имя и электронную почту, в совокупности с ключом --global. <br>
Синтаксис: $ git config --global user.name "ваше имя или ник латиницей" <br>
           $ git config --global user.email ваша электронная почта <br>
*Примечание: к git config можно использовать команду cat и --list(вывести список) <br>


### Шпаргалка

#### Навигация

pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке; <br>
ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке; <br>
ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .; <br>
cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project; <br>
cd first-project/html — перейди в папку html, которая находится в папке first-project; <br>
cd .. — перейди на уровень выше, в родительскую папку; <br>
cd ~ — перейди в домашнюю директорию (/Users/Username); <br> 
cd / — перейди в корневую директорию. <br>

#### Работа с файлами и папками. Создание
touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке; <br>
touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел; <br>
mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке. <br>
Копирование и перемещение <br>
cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место; <br>
mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место. <br>

####Чтение
cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt. <br>

####Удаление
rm about.html (от англ. remove, «удалить») — удали файл about.html; <br>
rmdir images (от англ. remove directory, «удалить директорию») — удали папку images; <br>
rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.<br>

#### Полезные возможности
Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (&&). <br>
У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓). <br>
Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. Если файл или папка есть в текущей директории, командная строка допишет путь сама. <br>
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. Останется только нажать Enter. <br>




















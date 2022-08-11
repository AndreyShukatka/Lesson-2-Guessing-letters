# Урок 2 Угадываем буквы
#  Guess
Игра по угадыванию случайного слова по буквам. Имя файла со словами, используемыми в игре хранится в `FILENAME`

# Функция get_rand_word:
Принимает значение `filename` и открывает файл. Возвращает рандомное значение из файла `sowpods.txt` маленькими буквами.

# Функция print_game
Принимает:
1. Список неверно введенных букв
2. Рандомное слово, выданное функцией `get_rand_word`
3. Список отгалданных букв
 
Функция выводит в консоль:
* На первой строке - список неверно введенных букв
* На второй строке - правильно угаданные буквы с их позицией в слове
* На третьей - количество букв в слове символами подчёркивания 
``` 
Wrong  guess: а, я, к
dev  о
______ 
```

# Функция play
Принимает Рандомное слово, выданное функцией `get_rand_word`, которое необходимо угадать пользователю.

Даёт 6 попыток на угадывание буквы, при желании меняется в переменной `attempt`

Функция работает до тех пор, пока у пользователя не закончатся попытки. 

На каждой попытке на экран выводится текущее состояние игры. После производится проверка на победу, если пользователь угадал слово - выводится сообщение о победе `> You win!` и игра заканчивается.

1. У пользователя запрашивается ввод буквы.
2. Проверяется наличие введенной буквы в загаданном слове.
3. Если такая буква есть в слове, то буква помечается программой как угаданная.
4. Буква помечается как использованная.
5. Если буква отсутствует в слове она запоминается как ошибочная и количество попыток уменьшается на 1.
6. После того, как у пользователя заканчиваются попытки на экран выводится состояние игры на момент ее окончания, сообщение о поражении и загаданное слово приведенное к верхнему регистру.

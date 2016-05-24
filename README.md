Задача№1
Необходимо написать общую функции для выборки определенного числа тест-кейсов из файла.
На вход функции подаются 2 параметра: путь к исходному файлу — обязательный параметр, — который содержит таблицу в текстовом виде (разделителями являются табуляция и символ новой строки) и необязательный параметр — количество строк, которые надо выбрать из файла. По умолчанию необходимо выбрать 10 строк. Пример файла:

case One Book Low Book Rating Product Date pairings

5 Hd | STB/Other LT | ST POL Rating L|C|C LM 5

9 Hd LT GTD Rating L|C|C LM 1

7 All All GTD Rating L|C|C | Index LM 3

10 Hd | STB/Other | TTd LT | ST POL Rating L|C|C Expected 1

4 Hd | TTd LT POL Rating L|C|C Expected 5

2 Hd | STB/Other LT | ST POL Rating L|C|C LM 5

3 Hd LT GTD Rating L|C|C LM 1

1 All All GTD Rating L|C|C | Index LM 3

8 Hd | STB/Other | TTd LT | ST POL Rating L|C|C Expected 1

11 Hd | TTd LT POL Rating L|C|C Expected 5


Функция должна делать следующие операции:

Считать содержимое исходного файла
Вырезать заданное число строк из файла случайным образом
Записать выбранные строки в результирующий файл. Путь к этому файлу и его расширение совпадает с путем и расширением исходного файла, а имя формируется как имя исходного фалй + «_res».
Сохранить исходный файл без выбранных строк
Вернуть необходимо путь к результирующему файлу.

Пример вызова функции:
res = select_cases(“C:/Temp/all_pairs.txt”, 5)

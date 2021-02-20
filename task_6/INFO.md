Код блокировки мобильных телефонов не умеют взламывать даже спецслужбы, однако хакерская группировка Анонимусы-80 добралась до исходников операционной системы, и выяснила способ его почти мгновенного взлома.

Оказывается, достаточно лишь посчитать длину линии, рисуемой в процессе взлома кода, после чего округлить её до пятого знака, и нажать пальцем на соответствующие цифры, пропуская нули, как телефон разблокируется.

Раскладка точек блокировки:
6 1 9
5 2 8
4 3 7

Ломаная линия разблокировки представляет собой последовательность цифр от 1 до 9, соответствующих точкам на этой картинке, причем гарантируется, что от точки переход совершается только к её ближайшим соседям (нету перепрыгиваний, например из точки 8 в точку 5).
Расстояние между точками по вертикали или горизонтали считается единичным.

На рисунке представлена такая последовательность: 1 2 3 4 5 6 2 7 8 9

Её длина приблизительно равняется 1 + 1 + 1 + 1 + 1 + 1.41.. + 1.41.. + 1 + 1 = 9.82843
(точность требуется пять цифр после запятой)

Результат: строка "982843"

Если бы результат получился, например, 10.012, то результирующая строка получилась бы "112" (все нули удаляются).

Функция

string PatternUnlock(int N, int [] hits) 

получает параметром N длину массива с кодами разблокировки, а сам массив hits содержит последовательность кодов разблокировки -- номера точек в диапазоне от 1 до 9.
Последовательность задаётся только шагами между соседними точками, программно искать "длинные" пути не нужно.
Серые линии на рисунке -- просто пример возможной траектории.

Возвращает функция строку, как в примере выше. 
.
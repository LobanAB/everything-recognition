# Программа распознавания изображения с веб-камеры.

Распознание лиц(спереди, слева) и глаз.

## Файл run.py

Запускает работу программы. 
Получает каскады из функции 'get_cascades'. 
Запускает видеопоток с веб-камеры. 
В бесконечном цикле берет фрейм, преобразует в цвет в оттенки серого. 
В цикле для каждого каскада высчитываются координаты для каждого прямоугольника(координаты x, y, ширина, высота). 
В цикле для каждого найденного соответствия рисуется прямоугольник. 
Если нажать клавишу `q` программа завершится. 
Запись видео прекращается. 
Закрываются созданные окна.

### is_user_wants_quit

Проверяет, нажал ли пользователь клавишу для завершения программы - `q`.

### show_frame

Показывает кадр с наложенными цветными прямоугольниками.

### draw_square

Рисует прямоугольник нужного цвета на переданном кадре.

### get_cascades

Формирует каскады из заданных в настройке как `"draw": True`.

## Файл config.py

Файл настроек. Задаются отслеживаемые каскады `"draw": True`, задается цвет прямоугольника `"color": (255, 0, 0)` и путь до xml файла с данными по каскаду.
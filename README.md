# WITMOTION BWT901CL
Здесь представлена небольшая работа по считыванию данных с датчика BWT901CL (пока только через USB), их визуализации, а также записи в .csv файл средствами Python.
Вся информация о [датчике](https://github.com/WITMOTION/BWT901CL).

## Состав.
1. Папка func, где лежат используемые функции.
    - create_line.py - создание линий через plotly.
    - formula_for_data - обработка поступающих данных.
    - graph.py - оформление графика.
2. usb_BWT901CL.ipynb - блокнот с программой для подключения датчика через USB.

## Используемые библиотеки.
Используемые библиотеки:
- serial;
- plotly;
- datetime;
- numpy;
- pandas.

### Для запуска на Ubuntu:
Перед запуском скрипта в блокноте узнайте куда подключается датчик: sudo dmesg -wH.
Затем пропишите: sudo chmod a+rw /dev/ttyUSB0, где /dev/ttyUSB0 - результат предыдущей команды (при переподключении датчика придётся вводить эту команду каждый раз. Если Вам это не нужно, введите: sudo usermod -a -G dialout $USER и перезагрузите компьютер).

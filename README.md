# About
Код задачи moving_statics выполняет следующее:
  - Создание или чтение временного ряда из файла
  - Вычисление скользящих статистик для указанных окон
  - Построение и сохранение графиков статистик

## Структура кода

- `create_time_series(file_path, date_col, value_col)` — чтение из файлов csv, xlsx, xls, txt
- `calculation_moving_average(df, window, value_col, new_col=None)` — вычисление скользящего среднего
- `calculation_moving_max(df, window, value_col, new_col=None)` — вычисление скользящего максимума
- `calculation_moving_min(df, window, value_col, new_col=None)` — вычисление скользящего минимума
- `calculation_moving_std(df, window, value_col, new_col=None)` — вычисление скользящего среднего отклонения
- `calculation_statics(df, args)` — вычисление статистик
- `create_new_graphic(df, output_file, format_file, date_col, value_col, new_col)` — создание и сохранение одного графика для конкретной статистики и окна
- `build_graphics(df, output_file, format_file, date_col, value_col, windows, new_cols)` — многократный вызов функции для создания и сохранения графика
- `main()` — основная функция
  
## Зависимости
  pip install pandas matplotlib
  
## Запуск
  python moving_statics.py test.csv -o output --mov-avg "mov_avg" --mov-max "mov_max" --mov-min "mov_min" --mov-std "mov_std" --windows 3 5 7 --format pdf
  
## Вывод программы
  Будет выводить набор графиков от статистик, которые мы указали
  
  Примеры графиков:
<img width="2422" height="1373" alt="image" src="https://github.com/user-attachments/assets/c4b1f3bc-f500-45ba-8ec3-f8b380f4f632" />
<img width="2270" height="1326" alt="image" src="https://github.com/user-attachments/assets/49d648ad-7517-41f2-995d-9e09f6aa5ada" />

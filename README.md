# module13_7_hw
13.7 Практическая работа по курсу Аналитик данных, работа с SQLLite и Python

Мы хотим посмотреть, есть ли сезонность в покупке треков разных жанров.

в папку с данными загрузите файл chinook.db.
Импортируйте необходимые библиотеки и создайте подключение к базе данных.
Напишите запрос, в результате которого получится таблица, содержащая:
данные о чеках (invoice): id, дату;
id покупателя и id всех треков в чеке;
жанр каждого трека: объедините все тяжёлые жанры (Rock, Alternative & Punk, Metal, Alternative, Heavy Metal) в категорию ‘rock’, а остальные жанры — в категорию ‘others’;
стоимость трека.
В таблицу должны попасть данные только по аудиофайлам (нужно проверить media_type) и только за 2020 год. Запрос будет содержать несколько джойнов.
На основе запроса создайте датафрейм с помощью read_sql_query в pandas.
Проверьте датафрейм на пропуски и дубликаты. Если они есть, предположите их происхождение и решите, нужно ли их обрабатывать.
Приведите дату к первому числу каждого месяца (2020-01-01, 2020-02-01 и так далее).
Сгруппируйте данные и с помощью библиотеки seaborn. Постройте графики, чтобы оценить по категориям жанров (‘rock’ и ‘others’) следующие ежемесячные показатели:
общее количество купленных треков,
число чеков,
число покупателей,
общую стоимость треков.
Должно получиться три графика, где на каждом присутствуют обе категории и ежемесячные показатели по ним.
Сделайте выводы по имеющимся данным.

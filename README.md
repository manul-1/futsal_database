# База данных мини-футбольной команды
#### Репозиторий "База данных мини-футбольной команды" содержит ER диаграмму и файл базы данных (БД) и некоторые примеры запросов к БД. Проект включает в себя разработанную БД и телеграм-бот для управления ею. БД создана для личного пользования и содержит информацию о игроках, забитых и пропущенных голах, даты матчей и счет (подробнее на диаграмме). Создание телеграм-бота по большей части принадлежит моему сокоманднику, создание БД и запросы к ней для вычисления в статистики выполнены мной.
## ER-диаграмма
![Alt text](ER.jfif)
## Примеры SQL запросов
#### Лучшие бомбардиры и ассистенты
##### SELECT  who_score, count(*) FROM goal_details GROUP BY who_score ORDER BY count(*) DESC
##### SELECT  who_assist, count(*) FROM goal_details GROUP BY who_assist ORDER BY count(*) DESC
#### Инфомация по вратарям 
##### SELECT goalkeeper, count(*) FROM missed_details GROUP BY goalkeeper ORDER BY count(*) DESC
#### Самые сильные связки
##### SELECT  who_score, who_assist, count(*) FROM goal_details GROUP BY who_score, who_assist ORDER BY count(*) DESC

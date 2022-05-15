# java-filmorate
Таблица User, включает в себя поля cоответствующие классу (name, id, login и т.д),
за исключением списков друзей, т.к SQL не может содержать массивы данных.
Поэтому мы представляем список друзей в качестве отдельной таблицы, где для каждого уникального номера списка хронятся 
идентификаторы добавленных пользователей и статусы  (статусы связанны с таблицей status по полю status_id). 
Данный подход позволяет получить список друзей по уникальному полю friendList_id.

Таблица Фильмов имеет схожую струтуру. Поле LikedList имеет уникальный ключ и содержит
данные об идентификаторе фильма и пользователях, которые отметили данный данный фильм.

![This is an image](https://github.com/Gidrosliv/javafilmorate/blob/add-friends-likes/src/main/resources/SQL.png?raw=true)
https://github.com/Gidrosliv/javafilmorate/blob/add-friends-likes/src/main/resources/SQL.png?raw=true

SELECT *
FROM Film AS f;
— Выводит все поля из таблицы Film;

SELECT *
FROM Film  AS f
WHERE Film_Id =1;
— Выводит все поля у фильма с Id =1;

SELECT *
FROM User;
— Выводит все поля из таблицы User;

SELECT *
FROM FriendList
WHERE user_id=1;
— Выводит всех друзей пользователя c Id =1;

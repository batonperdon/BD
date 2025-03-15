#ЛР 1

1.Выберите из таблицы orders все заказы

SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/ca20e04d-95a3-4b40-87bb-419d6787c6a4)

---------------------------------------------------------------------------
2.Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in

SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery')

![image](https://github.com/user-attachments/assets/99048286-dad3-4850-8ff6-c5a57ae7d22c)

---------------------------------------------------------------------------
3.Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".

![image](https://github.com/user-attachments/assets/b96167ef-2516-4fac-82ac-a31035b1cfd1)

---------------------------------------------------------------------------
4.Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.

![image](https://github.com/user-attachments/assets/ff53b198-fd76-4d41-b382-ff301f5a8470)

---------------------------------------------------------------------------
#ЛР 2

1.Выберите из таблицы orders 3 самых дешевых заказа за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/6bfc8818-b9be-4432-8c40-5371d3d39123)

---------------------------------------------------------------------------
2.Выберите из таблицы orders 2 самых дорогих заказов за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/24de6cc1-563b-459c-adcd-292c9b838752)

---------------------------------------------------------------------------
3.Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

![image](https://github.com/user-attachments/assets/3b834a6f-e473-400a-b3e7-3e5cb2a73ac1)

![image](https://github.com/user-attachments/assets/3327b1cb-c2ea-40f5-9f53-bfc4967a6ada)

---------------------------------------------------------------------------
4.Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

![image](https://github.com/user-attachments/assets/fb1119a0-7bc9-4893-9a5c-1337a2b371bb)

![image](https://github.com/user-attachments/assets/996b06ab-9b75-43e7-9bd7-c89f2c2b9151)

---------------------------------------------------------------------------
5.В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

![image](https://github.com/user-attachments/assets/78fbd6b2-7e74-4d38-9db2-d5eb25b147b6)

![image](https://github.com/user-attachments/assets/e85dc06a-1a3c-4fb1-ac0e-1c0dfb203afa)

---------------------------------------------------------------------------
#Лр 3 

Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.

Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/b0945c0e-85ed-4a2f-89bc-6e9424c32799)

![image](https://github.com/user-attachments/assets/f5b6eff7-8216-45f7-bf00-02e2c8b9a2cc)

---------------------------------------------------------------------------
Создайте таблицу users для хранения информации о пользователях сайта.
В таблице должны быть следующие поля:
id – идентификатор, целое положительное;
email – адрес электронной почты, строка не более 100 символов;
date_joined – дата регистрации (достаточно хранить дату, без времени)
last_activity – дата и время последней активности (с точностью до секунд).

![image](https://github.com/user-attachments/assets/56025db6-09fc-466e-a9f0-0c6eaaa7a018)

Неверное решение:

CREATE TABLE users(
id INT UNSIGNED,
email VARCHAR(100),
date_joined DATE,
last_activity DATETIME
);

INSERT INTO users (id, email, date_joined, last_activity)
VALUES (1, "user1@domain.com", "2014-12-12", "2016-04-08 12:34:54")
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (2, "user2@domain.com", "2014-12-12", "2017-02-13 11:46:53")
INSERT INTO users (id, email, date_joined, last_activity)
VALUES (3, "user3@domain.com", "2014-12-13", "2017-04-04 05:12:07")

Верное решение:
create table users (
id int(10) unsigned,
email varchar (100),
date_joined date,
last_activity datetime
);
insert into users (id, email, date_joined,last_activity)
values
(1,'user1@domain.com', '2014-12-12','2016-04-08 12:34:54'),
(2,'user2@domain.com', '2014-12-12','2017-02-13 11:46:53'),
(3,'user3@domain.com', '2014-12-13','2017-04-04 05:12:07');

![image](https://github.com/user-attachments/assets/a7fa25bd-e186-42c1-beb1-297611249e1e)

---------------------------------------------------------------------------
Создайте таблицу calendar для хранения календаря посетителей.
В таблице должны быть следующие поля:
id – идентификатор записи в календаре, целое положительное;
user_id – идентификатор пользователя, целое положительное;
doctor_id – идентификатор доктора, целое положительное;
visit_date – дата и время визита (точность до секунд).

![image](https://github.com/user-attachments/assets/ad529524-8311-484c-81eb-6ddfd842d12d)

Неверное решение:

Create table calendar (
id int unsigned,
user_id int unsigned,
doctor_id int unsigned,
visit_date datetime);
Insert into calendar (id, user_id, doctor_id, visit_date)
Values (1, 1914 , 1, '2017-04-08 12:00:00'),
(2, 12, 1, '2017-04-08 12:30:00'),
(3, 4641, 2, '2017-04-09 09:00:00'),
(4, 4641, 2,'2017-04-09 09:00:00'),
(5, 15, 2,'2017-04-09 10:00:00')

Верное решение:
Create table calendar (
id int unsigned,
user_id int unsigned,
doctor_id int unsigned,
visit_date datetime);
Insert into calendar (id, user_id, doctor_id, visit_date)
Values 
(1, 1914 , 1, '2017-04-08 12:00:00'),
(2, 12, 1, '2017-04-08 12:30:00'),
(3, 4641, 2, '2017-04-09 09:00:00'),
(4, 784, 1,'2017-04-08 13:00:00'),
(5, 15, 2,'2017-04-09 10:00:00')

VARCHAR (65535) - максимум

![image](https://github.com/user-attachments/assets/a5403a98-4dfa-4c34-bb43-200d2a0616f1)

---------------------------------------------------------------------------
Создайте таблицу users , в которой будут следующие поля:
id — идентификатор, целые положительные числа.
first_name— имя, строки до 50 символов.
last_name — фамилия, строки до 60 символов.
bio — биография, текст до 65000 символов.

![image](https://github.com/user-attachments/assets/df3e70c5-818d-4637-bea4-39d3e67ac866)

Неверное решение:
create table users (
id int (10) unsigned,
first_name varchar (50) unsigned,
last_name varchar (60) unsigned,
bio text
);
INSERT INTO users (id, first_name, last_name, bio)
VALUES
(1,'Антон','Кулик','С отличием окончил 39 лицей.'),
(2,'Сергей','Давыдов',''),
(3,'Дмитрий','Соколов','Профессиональный программист.')

Верное решение:
create table users (
id int (10) unsigned,
first_name varchar (50),
last_name varchar (60),
bio text
);
INSERT INTO users (id, first_name, last_name, bio)
VALUES
(1,'Антон','Кулик','С отличием окончил 39 лицей.'),
(2,'Сергей','Давыдов',''),
(3,'Дмитрий','Соколов','Профессиональный программист.')

![image](https://github.com/user-attachments/assets/29b5a2d4-2a94-4cfa-a1b5-a4f730fc330f)

---------------------------------------------------------------------------


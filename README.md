![image](https://github.com/user-attachments/assets/c184f890-329d-408d-9c20-d6648cbd021e)#ЛР 1
-
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
-
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
-
Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.

Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/b0945c0e-85ed-4a2f-89bc-6e9424c32799)

![image](https://github.com/user-attachments/assets/f5b6eff7-8216-45f7-bf00-02e2c8b9a2cc)

---------------------------------------------------------------------------
#Лр 4
-
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
#Лр 5
-
1.Выберите из таблицы orders 4 самых дорогих заказов за всё время.Данные нужно отсортировать в порядке убывания цены.Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/ea0e31e6-3201-490c-a1b3-417f581fff66)

Решение:
-
SELECT * FROM orders WHERE status != 'cancelled' ORDER BY sum DESC LIMIT 4;

![image](https://github.com/user-attachments/assets/27320489-c61d-4ff7-8cec-62f29dac3ed7)

---------------------------------------------------------------------------
2.Выберите из таблицы products название и цены четырех самых дешевых товаров, которые есть на складе.

![image](https://github.com/user-attachments/assets/264c471a-41a4-45f3-a5b0-0dcd49fbea61)

Решение:
-
SELECT name, price FROM products WHERE count > 0 ORDER BY price ASC LIMIT 4;

![image](https://github.com/user-attachments/assets/46fb572c-98d7-4bae-8b89-9c560bda6f2c)

---------------------------------------------------------------------------
3.Выберите из таблицы orders три последних заказа (по дате date) стоимостью от 3200 рублей и выше.
Данные отсортируйте по дате в обратном порядке.

![image](https://github.com/user-attachments/assets/e6288d03-4a88-4eee-9cbf-00b9cb10ea5e)

Решение:
-
SELECT * FROM orders WHERE sum >= 3200 ORDER BY date DESC LIMIT 3;

![image](https://github.com/user-attachments/assets/d34e49d3-9e90-4c8f-b6f7-4685c88728d2)

---------------------------------------------------------------------------
4.Создайте данную таблицу:

![image](https://github.com/user-attachments/assets/611b54d3-e16b-4a58-8ec4-3d27eaa19f73)

Решение:
-
CREATE TABLE products (
    id INT PRIMARY KEY,
    name VARCHAR(255),
    count INT,
    price DECIMAL(10, 2)
);

INSERT INTO products (id, name, count, price) VALUES
(1, 'Стиральная машина', 5, 10000.00),
(2, 'Холодильник', 0, 10000.00),
(3, 'Микроволновка', 3, 4000.00),
(4, 'Пылесос', 2, 4500.00),
(5, 'Вентилятор', 0, 700.00),
(6, 'Телевизор', 7, 31740.00),
(7, 'Тостер', 2, 2500.00),
(8, 'Принтер', 4, 3000.00),
(9, 'Активные колонки', 1, 2900.00),
(10, 'Ноутбук', 4, 36990.00),
(11, 'Посудомоечная машина', 0, 17800.00),
(12, 'Видеорегистратор', 23, 4000.00),
(13, 'Смартфон', 8, 12300.00),
(14, 'Флешка', 4, 1400.00),
(15, 'Блендер', 0, 5500.00),
(16, 'Газовая плита', 5, 11900.00),
(17, 'Клавиатура', 3, 1800.00);

![image](https://github.com/user-attachments/assets/c53725e2-6b90-4fa4-bbf4-c7f405a94ffd)

![image](https://github.com/user-attachments/assets/0cc73f9a-8e3e-49f2-9b90-4e9cbea71d16)

---------------------------------------------------------------------------
5.Из таблицы ниже сделать выборку на основе задания: Сайт выводит товары по 5 штук. Выберите из таблицы products товары, которые пользователи увидят на 3 странице каталога при сортировке в порядке возрастания цены (price).

![image](https://github.com/user-attachments/assets/3c8c5998-266c-4ba3-bbe0-81e2a9966217)

Решение:
-
SELECT name, price FROM products ORDER BY price ASC LIMIT 5 OFFSET 10;

![image](https://github.com/user-attachments/assets/7bc0b0e6-682c-47e7-8db3-c2da917ce1fe)

---------------------------------------------------------------------------
Создайте таблицу articles для хранения данных о статьях. В таблице должны быть следующие поля:
id — идентификатор, целое положительное, NULL запрещен
name — название статьи, строка до 80 символов.text — текст статьи.
state — статус статьи. Поле из 3 вариантов: draft (черновик), correction (корректура), public (опубликована).Добавьте 3 записи так, чтобы получалась таблица ниже:

Когда можно выбрать 1 вариант - используем ENUM
когда можно выбрать несколько вариантов - используем SET

![image](https://github.com/user-attachments/assets/5f6e5fe4-38e7-4ece-a87a-d86f91b29c18)

Решение:
-
Create table articles (
id int unsigned not null,
name varchar (80),
text text,
state enum('draft', 'correction', 'public')
);
insert into articles (id, name, text, state)
VALUES
(1, 'Новое в Python 3.6', '', 'draft'),
(2, 'Оптимизация SQL запросов', 'При больших объемах данных ...', 'correction'),
(3, 'Транзакции в MySQL', 'По долгу службы мне приходится ...', 'public')

![image](https://github.com/user-attachments/assets/895eef35-cb26-4bc9-aacd-89951f5af8bf)

---------------------------------------------------------------------------
Создайте таблицу rooms для хранения номеров в отеле:

id — идентификатор, целое положительное.
number — номер комнаты, целое положительное. Всего в отеле 107 комнат. NULL запрещен.
beds — количество спальных мест. Выбор из 1+1, 2+1, 2+2. Можно выбрать только один вариант. NULL запрещен.
additional — дополнительные удобства в номере. Можно выбрать несколько вариантов из списка: conditioner, bar, fridge и wifi.
Добавьте 3 записи так, чтобы получалась таблица ниже:

![image](https://github.com/user-attachments/assets/87a873f7-c256-4144-abf4-a134151309c6)

Решение:
-
create table rooms (
id int unsigned not null,
number tinyint unsigned not null,
beds enum('1+1','2+1','2+2') not null,
additional set('conditioner','bar','fridge','wifi')
);
insert into rooms (id,number,beds,additional)
values
(1,10,'1+1','conditioner,bar,wifi'),
(2,12,'2+1',''),
(3,24,'2+2','fridge,bar,wifi')

![image](https://github.com/user-attachments/assets/4ae904fb-6eb2-4f6b-8437-0ffabb920a18)

---------------------------------------------------------------------------
Выберите из таблицы products название, цену и страны всех товаров из России и Белоруссии (в поле country обязательно должна присутствовать или Россия, или Белоруссия).
Выбирайте только товары, у которых задана категория.
Данные отсортируйте по цене в обратном порядке.

Поле country относится к типу SET('RU', 'UA', 'BY', 'KZ') NOT NULL.

![image](https://github.com/user-attachments/assets/afa3f1bb-6560-4ea5-8553-165e951c63df)

Решение:
-
SELECT name,price,country FROM products 
WHERE (find_in_set ('RU',country) OR find_in_set ('BY',country)) AND category_id IS NOT NULL ORDER BY price DESC

![image](https://github.com/user-attachments/assets/c8216f61-dfcd-4fab-bce7-587dd2b356ed)

---------------------------------------------------------------------------
#Лр 6
-
Задание 1.

Создайте таблицу orders для хранения списка заказов:

id — идентификатор, целое положительное.
user_id — идентификатор пользователя, который оформил заказ. Целое положительное, NULL запрещен.
amount — стоимость заказа. Целое положительное число не более 1 млн. NULL запрещен, по умолчанию 0.
created — дата и время создания заказа. NULL запрещен.
state — статус заказа. Выбор из new, cancelled, in_progress, delivered, completed. Можно выбрать только один вариант. NULL запрещен. По умолчанию должен стоять new.
Добавьте 3 записи так, чтобы получалась таблица ниже:

![image](https://github.com/user-attachments/assets/7d0f7aa8-fe53-4147-aaac-c75dd76c366c)

Решение:
-
CREATE TABLE orders (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    user_id INTEGER NOT NULL,
    amount INTEGER NOT NULL DEFAULT 0,
    created DATETIME NOT NULL,
    state ENUM('new', 'cancelled', 'in_progress', 'delivered', 'completed') NOT NULL DEFAULT 'new',
    CHECK (user_id > 0),
    CHECK (amount >= 0 AND amount <= 1000000)
);

INSERT INTO orders (user_id, amount, created) VALUES (56, 5400, '2018-02-01 17:46:59');
INSERT INTO orders (user_id, amount, created) VALUES (90, 249, '2018-02-01 19:13:04');
INSERT INTO orders (user_id, amount, created) VALUES (78, 2200, '2018-02-01 22:43:09');

SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/026e7972-7480-4c90-9b11-284634f31946)

---------------------------------------------------------------------------
2.Создайте таблицу users для хранения списка пользователей сайта: id — идентификатор, целое положительное. first_name — имя, строка до 20 символов. NULL запрещен. last_name — фамилия, строка до 20 символов. NULL запрещен. patronymic — отчество, строка до 20 символов. NULL запрещен, по умолчанию пустая строка. is_active — отметка об активности пользователя. Логическое поле, по умолчанию TRUE. is_superuser — отметка администратора. Логическое поле, по умолчанию FALSE. Добавьте 3 записи так, чтобы получалась таблица

![image](https://github.com/user-attachments/assets/d07e4d5f-0bb0-47ae-a9b9-0016ac228bd8)

Решение:
-
CREATE TABLE users (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    first_name VARCHAR(20) NOT NULL,
    last_name VARCHAR(20) NOT NULL,
    patronymic VARCHAR(20) NOT NULL DEFAULT '',
    is_active BOOLEAN NOT NULL DEFAULT TRUE,
    is_superuser BOOLEAN NOT NULL DEFAULT FALSE,
    CHECK (LENGTH(first_name) <= 20),
    CHECK (LENGTH(last_name) <= 20),
    CHECK (LENGTH(patronymic) <= 20)
);

INSERT INTO users (first_name, last_name, patronymic, is_active, is_superuser)
VALUES ('Дмитрий', 'Иванов', '', TRUE, FALSE);

INSERT INTO users (first_name, last_name, patronymic, is_active, is_superuser)
VALUES ('Анатолий', 'Белый', 'Сергеевич', TRUE, TRUE);

INSERT INTO users (first_name, last_name, is_active, is_superuser)
VALUES ('Андрей', 'Крючков', FALSE, FALSE);

SELECT * FROM users;

![image](https://github.com/user-attachments/assets/229ff61d-f029-4ba0-a6d1-7db4daa3f831)

---------------------------------------------------------------------------
3.Создайте таблицу products для хранения товаров в интернет магазине: id — идентификатор, целое положительное. category_id — категория, целое положительное. Может принимать NULL. По умолчанию NULL. name — название, строка до 100 символов. NULL запрещен. count — количество, целое положительное до 255. NULL запрещен, по умолчанию 0. price — цена типа DECIMAL с 10 знаками, 2 из которых выделены для копеек. NULL запрещен, по умолчанию 0.00. Добавьте 3 записи так, чтобы получалась таблица

Решение:
-
CREATE TABLE products (
    id INTEGER PRIMARY KEY AUTO_INCREMENT,
    category_id INTEGER NULL DEFAULT NULL,
    name VARCHAR(100) NOT NULL,
    count TINYINT UNSIGNED NOT NULL DEFAULT 0,
    price DECIMAL(10, 2) NOT NULL DEFAULT 0.00,
    CHECK (category_id > 0 OR category_id IS NULL),
    CHECK (count >= 0 AND count <= 255),
    CHECK (price >= 0)
);

INSERT INTO products (category_id, name, count, price)
VALUES (1, 'Кружка', 5, 45.90);

INSERT INTO products (category_id, name, count, price)
VALUES (17, 'Фломастеры', 0, 78.00);

INSERT INTO products (name, count, price)
VALUES ('Сникерс', 12, 50.80);

SELECT * FROM products;

![image](https://github.com/user-attachments/assets/c4dcd2d0-66cd-4bd8-8b92-5e716fa4e413)

---------------------------------------------------------------------------

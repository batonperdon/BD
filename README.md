ЛР 1

1.Выберите из таблицы orders все заказы

SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/ca20e04d-95a3-4b40-87bb-419d6787c6a4)

2.Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in

SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery')

![image](https://github.com/user-attachments/assets/99048286-dad3-4850-8ff6-c5a57ae7d22c)

3.Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".

![image](https://github.com/user-attachments/assets/b96167ef-2516-4fac-82ac-a31035b1cfd1)

4.Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.

![image](https://github.com/user-attachments/assets/ff53b198-fd76-4d41-b382-ff301f5a8470)

ЛР 2

1.Выберите из таблицы orders 3 самых дешевых заказа за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/6bfc8818-b9be-4432-8c40-5371d3d39123)

2.Выберите из таблицы orders 2 самых дорогих заказов за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/24de6cc1-563b-459c-adcd-292c9b838752)

3.Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

![image](https://github.com/user-attachments/assets/3b834a6f-e473-400a-b3e7-3e5cb2a73ac1)

![image](https://github.com/user-attachments/assets/3327b1cb-c2ea-40f5-9f53-bfc4967a6ada)

4.Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

![image](https://github.com/user-attachments/assets/fb1119a0-7bc9-4893-9a5c-1337a2b371bb)

![image](https://github.com/user-attachments/assets/996b06ab-9b75-43e7-9bd7-c89f2c2b9151)

5.В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

![image](https://github.com/user-attachments/assets/78fbd6b2-7e74-4d38-9db2-d5eb25b147b6)

![image](https://github.com/user-attachments/assets/e85dc06a-1a3c-4fb1-ac0e-1c0dfb203afa)

Лр 3 

Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.

Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/b0945c0e-85ed-4a2f-89bc-6e9424c32799)

![image](https://github.com/user-attachments/assets/f5b6eff7-8216-45f7-bf00-02e2c8b9a2cc)

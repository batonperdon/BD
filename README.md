ЛР 1

1.Выберите из таблицы orders все заказы

SELECT * FROM orders;

![image](https://github.com/user-attachments/assets/aa1119e5-7744-42a6-b6c0-80b8da4bb268)

2.Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in

SELECT * FROM orders WHERE STATUS IN ('cancelled','in_progress','delivery')

![image](https://github.com/user-attachments/assets/068e07e9-f1b2-431b-84f4-ba5189071ea4)

3.Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".

![image](https://github.com/user-attachments/assets/831bc2ee-60c3-4b1c-a71a-f1561df74ed6)

4.Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count). Вывести нужно только номер (id) и сумму (sum) заказа.

![image](https://github.com/user-attachments/assets/14a43eb6-0c48-40f0-ab6c-7e21ee0dff7c)

ЛР 2

1.Выберите из таблицы orders 3 самых дешевых заказа за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/7f3eca2e-8526-44e0-a5e3-2606e802846d)

2.Выберите из таблицы orders 2 самых дорогих заказов за всё время. Данные нужно отсортировать в порядке убывания цены. Отмененные заказы не учитывайте.

![image](https://github.com/user-attachments/assets/4d798f8c-0612-4a75-bdf4-59462cc69904)

3.Добавьте в таблицу orders данные о новом заказе стоимостью 8000 рублей. В заказе 4 товара (products).

![image](https://github.com/user-attachments/assets/3ec64a53-edbf-460f-9734-17e358ba4f58)

![image](https://github.com/user-attachments/assets/e19367f1-7b96-486e-a31d-6616916ad2ef)

4.Добавьте в таблицу products новый товар — «VR-очки», стоимостью 70000 рублей в количестве (count) 2 штук.

![image](https://github.com/user-attachments/assets/5eae4bb1-3d23-4b11-bfb1-d4afbc19ebd8)

![image](https://github.com/user-attachments/assets/b0e2f4c8-20f4-43ec-a769-99d5f701fce8)

5.В таблицу products внесли данные с ошибкой, вместо "PS5" в наименовании написали IMAC. Исправьте ошибку.

![image](https://github.com/user-attachments/assets/550830b2-ce80-4332-bf6a-6480c247b5ec)

![image](https://github.com/user-attachments/assets/2de688f5-7f6e-4f3d-8cbb-e0f83bbb61a5)

Лр 3 

Создайте таблицу users с полем id типа INT и двумя текстовыми полями, которые будут хранить имя (first_name) и фамилию (last_name). Длина имени и фамилии не превышает 50 символов.

Добавьте в таблицу трех пользователей: Дмитрия Иванова, Анатолия Белого и Дениса Давыдова.

![image](https://github.com/user-attachments/assets/0a9f4874-39fd-42cc-bf65-6ec0bdad6469)

![image](https://github.com/user-attachments/assets/04274f3f-26b3-468e-9eab-e36d55bde99e)

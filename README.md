# goit-rdb-hw-04

## 1. Створіть базу даних для керування бібліотекою книг згідно зі структурою, наведеною нижче. Використовуйте DDL-команди для створення необхідних таблиць та їх зв'язків.

Структура БД

a) Назва схеми — “LibraryManagement”

b) Таблиця "authors":

author_id (INT, автоматично зростаючий PRIMARY KEY)
author_name (VARCHAR)
c) Таблиця "genres":

genre_id (INT, автоматично зростаючий PRIMARY KEY)
genre_name (VARCHAR)
d) Таблиця "books":

book_id (INT, автоматично зростаючий PRIMARY KEY)
title (VARCHAR)
publication_year (YEAR)
author_id (INT, FOREIGN KEY зв'язок з "Authors")
genre_id (INT, FOREIGN KEY зв'язок з "Genres")
e) Таблиця "users":

user_id (INT, автоматично зростаючий PRIMARY KEY)
username (VARCHAR)
email (VARCHAR)
f) Таблиця "borrowed_books":

borrow_id (INT, автоматично зростаючий PRIMARY KEY)
book_id (INT, FOREIGN KEY зв'язок з "Books")
user_id (INT, FOREIGN KEY зв'язок з "Users")
borrow_date (DATE)
return_date (DATE)


![image](https://github.com/user-attachments/assets/94a9a1c8-66c3-4dca-b83d-d282511b6d76)

## 2. Заповніть таблиці простими видуманими тестовими даними. Достатньо одного-двох рядків у кожну таблицю.

![image](https://github.com/user-attachments/assets/cfd6168c-0f74-4d83-a178-c7e1370ea300)

## 3. Перейдіть до бази даних, з якою працювали у темі 3. Напишіть запит за допомогою операторів FROM та INNER JOIN, що об’єднує всі таблиці даних, які ми завантажили з файлів: order_details, orders, customers, products, categories, employees, shippers, suppliers. Для цього ви маєте знайти спільні ключі. Перевірте правильність виконання запиту.

![image](https://github.com/user-attachments/assets/b60db13b-14f7-49d9-a8dc-0d376e82794c)

## 4. Виконайте запити, перелічені нижче:

### 4.1 Визначте, скільки рядків ви отримали (за допомогою оператора COUNT).

![image](https://github.com/user-attachments/assets/4836d6b1-4b24-451a-843b-64c69ee8ed8d)

### 4.2 Змініть декілька операторів INNER на LEFT чи RIGHT. Визначте, що відбувається з кількістю рядків. Чому? Напишіть відповідь у текстовому файлі.

Коли ми використали INNER JOIN для об'єднання всіх таблиць, а потім спробували додати LEFT JOIN, кількість рядків у результаті не змінилася. Це означає, що в нашій базі даних немає жодного замовлення, для якого не було б відповідних даних в інших таблицях. 

Зазвичай, якщо ми замінюємо INNER JOIN на LEFT JOIN, ми очікуємо, що кількість рядків збільшиться, тому що LEFT JOIN покаже всі записи з лівої таблиці, навіть якщо для них немає відповідників у правій. Але в нашому випадку всі замовлення мають повні дані, тому LEFT JOIN не додав жодних додаткових рядків.

![image](https://github.com/user-attachments/assets/90029a2a-b0c5-4af9-af95-02638e40313f)

### 4.3 На основі запита з пункта 3 виконайте наступне: оберіть тільки ті рядки, де employee_id > 3 та ≤ 10.

![image](https://github.com/user-attachments/assets/8198004a-ff33-4bae-8a33-e067252ab97a)

### 4.4 Згрупуйте за іменем категорії, порахуйте кількість рядків у групі, середню кількість товару (кількість товару знаходиться в order_details.quantity).

![image](https://github.com/user-attachments/assets/b134327f-cc7b-46c9-a9a9-ac3a2d462fc9)

### 4.5 Відфільтруйте рядки, де середня кількість товару більша за 21.

![image](https://github.com/user-attachments/assets/f8877e80-5f1e-4867-8b1d-9949b7941f86)


### 4.6 Відсортуйте рядки за спаданням кількості рядків.

![image](https://github.com/user-attachments/assets/862c8383-f8bd-4292-9412-e30fc0cba5f0)


### 4.7 Виведіть на екран (оберіть) чотири рядки з

![image](https://github.com/user-attachments/assets/dc546409-8352-4a32-baed-ef2a494e61d5)



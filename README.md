# LM_Libraries
 Логическая структура БД для создания "Библиотеки"
![LM2](https://github.com/Nastavnik/LM_Libraries/assets/79099352/2ff6ca98-90c3-421d-9d14-9a61bd1ea5ee)

Выбор ключей
PK и FK
1) PK для Books (книги) - books_id bigint
2) PK для Publishers (Издательство) - id bigint
3) PK для readers (читатели) - reader_id bigint
4) PK для employee (сотрудники библиотеки) - id bigint
5) PK для Department (отделы в библиотеки) - id integer 
6) PK для rent_books (аренда книг) - rent_id bigint
7) PK auther_books (авторы книг) - auther_id bigint

FK 
1) в таблице employee (сотрудники библиотеки) - department_id integer (внешний ключ берем из таблицы Department)
2) Books (книги) - id_publisher  bigint (внешний ключ берем из таблицы Publishers)
3) rent_books (аренда книг) - reader_id bigint (внешний ключ берем из таблицы readers)
4) rent_books (аренда книг) - books_id bigint (внешний ключ берем из таблицы Books)
5) rent_books (аренда книг) - employee_id bigint (внешний ключ берем из таблицы employee)
6) books (книги) - auther_id bigint (внешний ключ берем из таблицы auther_books)

Пояснение к связям
1) Издательство может печатать много книг
2) у сотрудника, который оформлял заказ может быть множество заказов
3) Книги могут арендовать множество раз
4) У книг может быть много авторов, поэтому связь между таблицами книги и автора многие ко многим
5) также читатели могут арендовать множество книг
6) в Department могут работать много сотрудников
   ПОЭТОМУ ТУТ СВЯЗИ один ко многим

# LM_Libraries
 Логическая структура БД для создания "Библиотеки"
![LM](https://github.com/Nastavnik/LM_Libraries/assets/79099352/d21ab014-ad16-4325-a89b-54fd088a695e)
Выбор ключей
PK и FK
1) PK для Books (книги) - books_id bigint
2) PK для Publishers (Издательство) - id bigint
3) PK для readers (читатели) - reader_id bigint
4) PK для employee (сотрудники библиотеки) - id bigint
5) PK для Department (отделы в библиотеки) - id integer 
6) PK для rent_books (аренда книг) - rent_id bigint

FK 
1) в таблице employee (сотрудники библиотеки) - department_id integer (внешний ключ берем из таблицы Department)
2) Books (книги) - id_publisher  bigint (внешний ключ берем из таблицы Publishers)
3) rent_books (аренда книг) - reader_id bigint (внешний ключ берем из таблицы readers)
4) rent_books (аренда книг) - books_id bigint (внешний ключ берем из таблицы Books)
5) rent_books (аренда книг) - employee_id bigint (внешний ключ берем из таблицы employee)

Пояснение к связям
1) Издательство может печатать много книг
2) у сотрудника, который офрмлял заказ может быть множество заказов
3) Книги могут арендовать множество раз
4) также читатели могут арендовать множество книг
5) в Department могут работать много сотрудников
   ПОЭТОМУ ТУТ СВЯЗИ один ко многим

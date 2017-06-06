# DataBaseMySql
Project of MySql Database for on-line bookshop

The database consists of 5 main tables (login, customers, orders, books, payments) and 2 additional ones (women, books_it_total) created for triggers. Moreover, there are 10 views for users and 3 more for administrator.

Table login consists of columns: id_customer, login, passwort, priviliges and is connected with table customers using relation 1 to 1.
Table customers  consists of columns: id_customer, firstname, lastname, gender, birthday_date,  city, post_code, street, home_number, province, phone_number, email and is connected with table login using relation 1 to 1 and with table orders using relation 1 to many.
Table books consists of columns: id_book, title, category, description, author_name, author_surname, price, ISBN, publisher, quantity, status_book, publishing_date and is connected with table orders using relation 1 to many.
Table payments consists of columns: id_order, payment_date, amount, payment_status and is connected with table orders using relation 1 to 1.
Table orders consists of columns: id_order, id_customer, id_book, order_date, order_status and is connected with table payments using relation 1 to 1, and connected with tables books and customers using relation 1 to many.

Viwes for users:
1)presenting personal details for specified customer
2)presenting 5 last orders for specified customer
3)presenting 5 last payments for specified customer
4)presenting not paid payments for specified customer
5)presenting all available books
6)presenting books from specified category 'Kulinaria'
7)presenting books lastly published (newcomers)
8)presenting books with keywors 'Java'
9)presenting bestsellers from the beginning of the year
10)presenting bestsellers in current month

Viewers for administrator:
1)presenting all available books from category 'Informatyka'
2)presenting all customers from province ‘mazowieckie’
3)presenting all orders which are open

Triggers for administrator:
1)keeping track how many female buy books
2)keeping track how many books from category 'Informatyka' is available including inserting new books and deleting no longer available books

Additionally, database includes some instructions select: showing sum of payments in April, showing titles of books which was sent in April, showing 3 most expensive books, showing how many books from each category is offered, showing names of all available categories

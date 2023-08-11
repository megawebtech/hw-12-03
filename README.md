 hw-12-03

Домашнее задание к занятию «SQL. Часть 1»    Ярчак Александр

Задание можно выполнить как в любом IDE, так и в командной строке.

Задание 1

Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.


SELECT DISTINCT district FROM address WHERE LEFT(district,1)='K' AND RIGHT(district,1)='a' AND district NOT LIKE '% %';

https://github.com/megawebtech/hw-12-03/blob/master/task1-right.JPG




Задание 2

Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года включительно и стоимость которых превышает 10.00.

SELECT payment_id, payment_date, amount FROM payment WHERE payment_date > '2005-06-15 00:00:00' AND payment_date < '2005-06-18 23:59:59'   AND amount<10.01;

 
https://github.com/megawebtech/hw-12-03/blob/master/task2.JPG


Задание 3

Получите последние пять аренд фильмов.


SELECT payment_id, payment_date, amount FROM payment WHERE payment_date > '2005-06-15 00:00:00' AND payment_date < '2005-06-18' AND amount < '10.01' ORDER BY payment_id DESC LIMIT 5;


https://github.com/megawebtech/hw-12-03/blob/master/task3-1.JPG


Задание 4

Одним запросом получите активных покупателей, имена которых Kelly или Willie.

Сформируйте вывод в результат таким образом:

    все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
    замените буквы 'll' в именах на 'pp'.


SELECT REPLACE(LOWER(first_name),'ll','pp') FROM customer WHERE first_name LIKE 'Kelly' OR first_name LIKE 'Willie';

https://github.com/megawebtech/hw-12-03/blob/master/task%204.JPG


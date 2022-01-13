# Sakila-uzdevumi
Bildes uzdevumi:
1) Uzd = 2
2) Uzd = 3
3) Uzd = 121
4) Uzd = Bija daudz tāpec saskaitīju 66
5) Uzd = arī bija daudz tāpēc saskaitīju 55
6) Uzd = GINA DEGENERES
7) Uzd = ir pieejama
8) Uzd = es nezinu kā
9) Uzd = 115.2720
10) Uzd = Sci-Fi=108.1967; Documentary=108.7500; Children=109.8000; Animation=111.0152; New=111.1270; Action=111.6094; Classics=111.6667; Horror=112.4821; Travel=113.3158; Music=113.6471; Family=114.7826; Comedy=115.8276; Drama=120.8387; Foreign=121.6986; Games=127.8361; Sports=128.2027

Word uzdevumi
1) 1a = SELECT first_name, last_name FROM `actor`
2) 1b = SELECT UPPER(CONCAT(first_name, ' ', last_name))AS `Actor Name` FROM `actor`
3) 2a = SELECT actor_id, first_name, last_name FROM `actor` WHERE first_name = 'Joe'
4) 2b = SELECT * FROM `actor` WHERE last_name like '%GEN%'
5) 2c = SELECT * FROM `actor` WHERE last_name like '%LI%' ORDER BY last_name, first_name
6) 2d = SELECT country_id, country FROM `country` WHERE country IN ('Afghanistan', 'Bangladesh', 'China')
7) 3a = ALTER TABLE `actor` ADD middle_name VARCHAR(45) AFTER first_name
8) 3b = ALTER TABLE `actor` MODIFY middle_name blob
9) 3c = ALTER TABLE `actor` DROP middle_name
10) 4a = SELECT last_name, COUNT(last_name) FROM `actor` GROUP BY last_name
11) 4b =SELECT last_name, COUNT(last_name) FROM `actor` GROUP BY last_name HAVING COUNT(last_name)>1
12) 4c =UPDATE `actor` SET first_name = 'HARPO', last_name = 'WILLIAMS' WHERE first_name = 'GROUCHO'AND last_name = 'WILLIAMS'
13) 4d = nesapratu kas tur jādara
14) 5a = SHOW CREATE TABLE `address`
15) 6a = SELECT first_name, last_name, address FROM `staff` AS s JOIN `address` AS a ON s.address_id = a.address_id
16) 6b = SELECT first_name, last_name, SUM(amount), payment_date FROM `staff` AS s JOIN `payment` AS p ON s.staff_Id=p.staff_id WHERE payment_date LIKE '2005-08%' GROUP BY s.staff_id
17) 6c = SELECT title, COUNT(actor_id) FROM film_actor AS fa INNER JOIN film AS f ON fa.film_id=f.film_id GROUP BY title
18) 6d = SELECT COUNT(i.inventory_id), title FROM inventory AS i INNER JOIN film AS f ON i.film_id=f.film_id WHERE title = 'Hunchback Impossible' GROUP BY f.film_id
19) 6e = SELECT first_name, last_name, sum(amount) FROM payment AS p JOIN customer AS c ON p.customer_id=c.customer_id GROUP BY c.customer_id ORDER BY last_name

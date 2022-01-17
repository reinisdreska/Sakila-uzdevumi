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
20) 7a = SELECT title FROM film AS f JOIN (SELECT language_id FROM language) AS l ON (f.language_id=l.language_id)WHERE title LIKE 'K%' OR title LIKE 'Q%' AND l.language_id = 1
21) 7b = SELECT first_name, last_name FROM film AS f JOIN (SELECT * FROM film_actor) AS fa ON (f.film_id=fa.film_id) JOIN (SELECT * FROM actor) AS a ON (fa.actor_id=a.actor_id) WHERE title = 'Alone Trip'
22) 7c = SELECT first_name, last_name, email FROM customer AS c JOIN address AS a ON c.address_id=a.address_id JOIN city AS ci ON a.city_id=ci.city_id JOIN country AS ca ON ci.country_id=ca.country_id WHERE country = 'canada'
23) 7d = SELECT f.title FROM film AS f JOIN film_category AS fc ON f.film_id=fc.film_id JOIN category AS c ON fc.category_id=c.category_id WHERE c.name='family'
24) 7e = SELECT title, COUNT(f.film_id) FROM film AS f JOIN inventory AS i ON f.film_id=i.film_id JOIN rental AS r ON i.inventory_id=r.inventory_id GROUP BY f.film_id ORDER BY COUNT(f.film_id) DESC
25) 7f = SELECT s.store_id, SUM(amount) FROM store AS s JOIN staff AS st ON s.store_id=st.store_id JOIN payment AS p ON st.staff_id=p.staff_id GROUP BY s.store_id
26) 7g = SELECT s.store_id, c.city, ca.country FROM store AS s JOIN address AS a ON s.address_id=a.address_id JOIN city AS c ON  a.city_id=c.city_id JOIN country AS ca ON c.country_id=ca.country_id
27) 7h = SELECT c.name, SUM(amount) FROM category AS c JOIN film_category AS fc ON c.category_id=fc.category_id JOIN inventory AS i ON fc.film_id=i.film_id JOIN rental AS r ON i.inventory_id=r.inventory_id JOIN payment AS p ON r.rental_id=p.rental_id GROUP BY c.name ORDER BY SUM(amount) DESC
28) 8a = CREATE VIEW sakila.Genres_by_revenue AS SELECT c.name, SUM(amount) FROM category AS c JOIN film_category AS fc ON c.category_id=fc.category_id JOIN inventory AS i ON fc.film_id=i.film_id JOIN rental AS r ON i.inventory_id=r.inventory_id JOIN payment AS p ON r.rental_id=p.rental_id GROUP BY c.name ORDER BY SUM(amount) DESC LIMIT 5
29) 8b = SELECT * FROM sakila.Genres_by_revenue
30) 8c = DROP VIEW sakila.Genres_by_revenue es pieļauju ka tā bet man neatļauj jo command denide for user

Uzdevumi no github
1) 1a = SELECT * FROM actor

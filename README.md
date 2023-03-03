# -ODEV7-SQL
dvdrental sorgu senaryoları çözümleri
Sorgu 1- film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
Çözüm 1- SELECT title, rating FROM film
GROUP BY title, rating
ORDER BY rating;
<img width="517" alt="Ekran Resmi 2023-03-03 17 58 04" src="https://user-images.githubusercontent.com/116847744/222753416-3e05475a-d49d-49bd-a9e2-9e4f8c3781aa.png">

Sorgu 2- film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
Çözüm 2- SELECT replacement_cost, COUNT(replacement_cost) FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50;
<img width="587" alt="Ekran Resmi 2023-03-03 18 07 35" src="https://user-images.githubusercontent.com/116847744/222755130-2a8d9814-5196-409d-88e0-16cb04d30346.png">

Sorgu 3- customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
Çözüm 3- SELECT store_id, COUNT(*) FROM customer
GROUP BY store_id;
<img width="550" alt="Ekran Resmi 2023-03-03 18 11 29" src="https://user-images.githubusercontent.com/116847744/222756050-89826a61-f6cf-45b8-a2f6-982b77ab507c.png">

Sorgu 4- city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
Çözüm 4- SELECT country_id, COUNT(*) FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
<img width="537" alt="Ekran Resmi 2023-03-03 18 16 09" src="https://user-images.githubusercontent.com/116847744/222757112-19f2e0cf-8c7b-41af-98d7-ebb9ad9b455d.png">

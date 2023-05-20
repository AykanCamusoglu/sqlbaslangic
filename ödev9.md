- city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
- customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.
- customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz INNER JOIN sorgusunu yazınız.

### 1
```
SELECT ct.country, c.city 
FROM city c INNER JOIN country ct ON c.country_id = ct.country_id;
```

### 2
```
SELECT payment_id, first_name, last_name
FROM customer INNER JOIN payment ON customer.customer_id = payment.customer_id;
```
### 3
```
SELECT rental_id, first_name, last_name
FROM customer INNER JOIN rental ON customer.customer_id = rental.customer_id;
```
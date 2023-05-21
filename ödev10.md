- city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
- customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
- customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.


### 1
```
SELECT city, country
FROM country co LEFT JOIN city ci ON ci.country_id = co.country_id;
```

### 2
```
SELECT payment_id, first_name, last_name 
FROM payment RIGHT JOIN customer ON payment.customer_id = customer.customer_id;
```


### 3
```
SELECT rental_id, first_name, last_name 
FROM rental RIGHT JOIN customer ON rental.customer_id = customer.customer_id;
```
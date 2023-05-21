- film tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
- film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
- film tablosunda en düşük rental_rate ve en düşün replacement_cost değerlerine sahip filmleri sıralayınız.
- payment tablosunda en fazla sayıda alışveriş yapan müşterileri    (customer) sıralayınız.

### 1
```
SELECT COUNT(*)
FROM film
WHERE rental_rate = (SELECT MAX(rental_rate)
	   				 FROM film);
```

### 2
```
SELECT *
FROM film
WHERE replacement_cost = replacement_cost = (SELECT MIN(replacement_cost)
									 		 FROM film);

```


### 3
```
SELECT *
FROM film
WHERE rental_rate = (SELECT MAX(rental_rate)
	   				 FROM film) AND replacement_cost = (SELECT MIN(replacement_cost)
									 					FROM film);
```

### 4
```
select * from customer
INNER JOIN (select count(*) A, customer_id from payment
group by customer_id
) count_purchases
ON customer.customer_id = count_purchases.customer_id
order by A DESC;

 ```
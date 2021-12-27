# Patika SQL eğitiminin 10. Ödevi


Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştirilmiştir.

- city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.

```sql
SELECT city,country FROM city
LEFT JOIN country city.city_id=country.country_id;
```
- customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.

```sql
SELECT payment_id, first_name, last_name FROM customer
RİGHT JOIN payment customer.customer_id=city.customer_id;
```
- customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.

```sql
SELECT payment_id, first_name, last_name FROM customer
FULL JOIN rental customer.customer_id=rental.rental_id;
```
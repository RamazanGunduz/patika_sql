# Patika SQL eğitiminin 4. Ödevi

- film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
```sql
SELECT DISTINCT replacement_cost FROM film;
```
- film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
```sql
SELECT COUNT(DISTINCT replacement_cost) FROM film;
```
- film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
```sql
SELECT COUNT(replacement_cost) FROM film
WHERE title LIKE 'T%' AND rating in ('G');
```
- country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
```sql
SELECT COUNT(country) FROM country
WHERE country LIKE '_____';
```
- city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
```sql
SELECT COUNT(city) FROM city
WHERE city ILIKE 'R%';
```
# Patika SQL eğitiminin 11. Ödevi


Aşağıdaki sorgu senaryolarını  **dvdrental**  örnek veri tabanı üzerinden gerçekleştiriniz.
 

- **actor**  ve  **customer**  tablolarında bulunan  **first_name**  sütunları için tüm verileri sıralayalım.
```sql
(
SELECT first_name FROM actor)
UNION
(
SELECT first_name FROM customer);
```
-  **actor**  ve  **customer**  tablolarında bulunan  **first_name**  sütunları için kesişen verileri sıralayalım.
```sql
(
SELECT first_name FROM actor)
INTERSECT
(
SELECT first_name FROM customer);
```
-  **actor**  ve  **customer**  tablolarında bulunan  **first_name**  sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
```sql
(
SELECT first_name FROM actor)
EXCEPT
(
SELECT first_name FROM customer);
```
-  İlk 3 sorguyu tekrar eden veriler için de yapalım.
```sql
(
SELECT first_name FROM actor)
EXCEPT ALL
(
SELECT first_name FROM customer);
```
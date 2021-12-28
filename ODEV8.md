# Patika SQL eğitiminin 8. Ödevi

- test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
```sql
CREATE TABLE employee(
	id INTEGER, 
	name VARCHAR(50), 
	birthday DATE, 
	email VARCHAR(100)
);
```
- Oluşturduğumuz employee tablosuna ['Mockaroo'](https://www.mockaroo.com/) servisini kullanarak 50 adet veri ekleyelim.
```sql
insert into employee (id, name, birthday, email) values (80, 'Pierre', '2012-07-10', 'pstevings27@instagram.com');
insert into employee (id, name, birthday, email) values (81, 'Franny', '1984-12-13', 'fwarrior28@java.com');
insert into employee (id, name, birthday, email) values (82, 'Ivy', '1924-02-03', 'iriccardo29@dailymotion.com');
...
...
```
- Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
```sql
UPDATE employee
SET name = 'Cengiz',
	birthday = '1996-02-10',
	email= 'cengiz@cngz.com'
WHERE id = 2;

UPDATE employee
SET name = 'xxx',
	birthday = '1996-02-10',
	email= 'xxx@xxx.com'
WHERE name LIKE '%n';

UPDATE employee
SET name = 'yyyy',
	birthday = '1996-02-10',
	email= 'yyyy@yyyy.com'
WHERE email ILIKE '%@A%;

UPDATE employee
SET name = 'zzzzzz',
	birthday = '1996-02-10',
	email= 'zzzz@zzzz.com'
WHERE id = 21;

UPDATE employee
SET name = 'xyxyxy',
	birthday = '1996-02-10',
	email= 'xyxy@xyxy.com'
WHERE id = 54;
```
- Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
```sql
DELETE FROM employee
WHERE name LIKE 'A%';

DELETE FROM employee
WHERE id = 21;

DELETE FROM employee
ORDER BY birthday
OFFSET 4
LIMIT 5;

DELETE FROM employee
ORDER BY name
LIMIT 7;

DELETE FROM employee
WHERE email ILIKE '%@R%';
```
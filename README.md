# SQL_Assignment_4

## Sorgu Senaryoları

* film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.

```bash
SELECT DISTINCT replacement_cost
FROM film
ORDER BY replacement_cost ASC;
```


* film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?

```bash
SELECT COUNT(DISTINCT replacement_cost)
FROM film;
```

* film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?

```bash
SELECT COUNT(*)
FROM film
WHERE title LIKE 'T%' AND rating = 'G';
```

* country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?

```bash
SELECT COUNT(*)
FROM country
WHERE CHAR_LENGTH(country) = 5;
```

* city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

```bash
SELECT COUNT(*)
FROM city
WHERE RIGHT(city, 1) IN ('R', 'r');
```
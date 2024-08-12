Activity 1

SELECT City, Population 
FROM north_american_cities
WHERE Country = "Canada"
;

-----

SELECT City
FROM north_american_cities
WHERE Country = "United States"
ORDER BY Latitude DESC
;

-----

SELECT City
FROM north_american_cities
WHERE Longitude < -87.629798
ORDER BY Longitude ASC
;

-----

SELECT City
FROM north_american_cities
WHERE Country = "Mexico"
ORDER BY Population DESC
LIMIT 2
;

-----

SELECT City
FROM north_american_cities
WHERE Country = "United States"
ORDER BY Population DESC
LIMIT 2 OFFSET 2
;




---------------

Activity 2

SELECT Director, COUNT() FROM movies GROUP BY Director;

-----

SELECT Director, SUM(Domestic_sales + International_sales) AS Total_sales FROM movies 
LEFT JOIN Boxoffice
ON Id = Movie_id
GROUP BY Director;

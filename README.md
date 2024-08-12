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

---------------

SQLPD



SELECT * 
FROM mailing_list;

-----

A hacked site subscribers' details have surfaced on a darknet forum. Please submit all subscribers' details.

SELECT * 
FROM subscriptions;

-----

An illegal site's servers were seized in a recent operation. Please submit all users last access times, number of posts and family names' details.

SELECT LastAccess, Posts, FamilyName
FROM Users;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records email addresses and given names' details.

SELECT EmailAddress, GivenName
FROM mailing_list;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records number of promotions sent' details. Please make sure there are no duplicates.

SELECT DISTINCT PromotionsSent
FROM mailing_list;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries' details sorted by surnames in ascending order.

SELECT *
FROM mailing_list
ORDER BY Surname ASC;

-----

An illegal site's servers were seized in a recent operation. Please submit all users' details sorted by access times in descending order.

SELECT *
FROM users
ORDER BY AccessTime DESC;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all entries join dates and emails' details sorted by emails in descending order. Please make sure there are no duplicates.

SELECT DISTINCT JoinDate, Email
FROM mailing_list
ORDER BY Email DESC;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit all records join dates, family names and emails' details sorted by family names in ascending order and then by emails in ascending order.

SELECT Joined, FamilyName, Email
FROM mailing_list
ORDER BY FamilyName ASC, Email ASC;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit the top 5 records' details when sorted by join dates in descending order and then by given names in descending order.

SELECT *
FROM mailing_list
ORDER BY JoinDate DESC, GivenName DESC 
LIMIT 5;

-----

A mailing list of an illegal online service was sent to the SQLPD hot-line. Please submit the top 3 entries emails and number of children' details when sorted by number of children in ascending order and then by emails in descending order. Please make sure there are no duplicates.

SELECT DISTINCT Email, Children
FROM mailing_list
ORDER BY Children ASC, Email DESC
LIMIT 3;

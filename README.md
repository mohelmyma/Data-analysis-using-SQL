# Data-analysis-using-SQL
/* Query 1 */
SELECT Genre.Name, COUNT(*) As "songs_number"
FROM Track
JOIN Genre
ON Track.GenreId = Genre.GenreId
WHERE Track.Composer LIKE '%Bill Berry%'
GROUP BY 1


/* Query 2 */
SELECT COUNT(Track.TrackId), Genre.Name AS genre_name
FROM Track
JOIN Genre
ON Track.GenreId = Genre.GenreId
GROUP BY 2


/* Query 3 */

SELECT MediaType.Name, COUNT(MediaType.Name)
FROM Track
JOIN MediaType
ON Track.MediaTypeId = MediaType.MediaTypeId
JOIN Genre
ON Track.GenreId = Genre.GenreId
WHERE(Genre.Name = 'Rock')
GROUP BY MediaType.Name

/* Query 4 */

SELECT  Customer.Country, SUM(Invoice.Total)
FROM Invoice
JOIN Customer
ON Invoice.CustomerId = Customer.CustomerId
GROUP BY 1











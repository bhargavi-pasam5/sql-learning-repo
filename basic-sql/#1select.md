1. Write a solution to find the ids of products that are both low fat and recyclable. Return the result table in any order.

SELECT product_id 
FROM Products 
where low_fats = 'Y' and recyclable = 'Y'


2. Find the names of the customer that are not referred by the customer with id = 2

SELECT name 
from Customer
where referee_id != 2 OR referee_id IS NULL

3. A country is big if:
it has an area of at least three million (i.e., 3000000 km2), or
it has a population of at least twenty-five million (i.e., 25000000).
Write a solution to find the name, population, and area of the big countries.

SELECT name, population , area 
FROM World
where area >= 3000000 OR population >= 25000000

5. Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.
Return the result table in any order.

SELECT tweet_id
FROM Tweets
WHERE length(content)>15;

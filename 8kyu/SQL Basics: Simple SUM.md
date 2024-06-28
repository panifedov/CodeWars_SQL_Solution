# CodeWars SQL Solutions

---

## SQL Basics: Simple SUM

For this challenge you need to create a simple SUM statement that will sum all the ages.

people table schema
id
name
age
select table schema
age_sum (sum of ages)
NOTE: Your solution should use pure SQL. Ruby is used within the test cases to do the actual testing.

NOTE2: You need to use ALIAS for creating age_sum

---

### Given Code

```SQL
compare_with expected do

end

```

---

### Solution

```SQL
SELECT SUM(age) as age_sum
FROM people;

```


[See on CodeWars.com](https://www.codewars.com/kata/57eae65a4321032ce000002d/train/sql)
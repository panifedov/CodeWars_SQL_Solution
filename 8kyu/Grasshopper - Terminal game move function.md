# CodeWars SQL Solutions

---

## Grasshopper - Terminal game move function

Terminal game move function
In this game, the hero moves from left to right. The player rolls the dice and moves the number of spaces indicated by the dice two times.

In SQL, you will be given a table moves with columns position and roll. Return a table which uses the current position of the hero and the roll (1-6) and returns the new position in a column res.

---

``
    move(3, 6) should equal 15
``

### Given Code

```SQL
describe "Basic tests" do
  run_tests [
    [0, 4, 8],
    [3, 6, 15],
    [2, 5, 12]
  ]
end

```

---

### Solution

```SQL
SELECT position + 2 * roll AS res
FROM moves;

```


[See on CodeWars.com](https://www.codewars.com/kata/563a631f7cbbc236cf0000c2/train/sql)
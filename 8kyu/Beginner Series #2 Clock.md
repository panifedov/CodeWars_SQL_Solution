# CodeWars SQL Solutions

---

## Beginner Series #2 Clock

Clock shows h hours, m minutes and s seconds after midnight.

Your task is to write a function which returns the time since midnight in milliseconds.

```
    h = 0
m = 1
s = 1

result = 61000
```

```
    0 <= h <= 23
    0 <= m <= 59
    0 <= s <= 59
```


---

### Given Code

```SQL
DB[:past].multi_insert [
  {h: 0, m: 1, s: 1}, # --> 61000
  {h: 1, m: 1, s: 1}, # --> 3661000
  {h: 0, m: 0, s: 0}, # --> 0
  {h: 1, m: 0, s: 1}, # --> 3601000
  {h: 1, m: 0, s: 0}  # --> 3600000
]

compare_with expected

```

---

### Solution

```SQL
select (3600*h + 60*m + s)*1000 as res
from past;

```

[See on CodeWars.com](https://www.codewars.com/kata/55f9bca8ecaa9eac7100004a/train/sql)
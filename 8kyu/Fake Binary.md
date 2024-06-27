# CodeWars SQL Solutions

---

## Fake Binary

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

Note: input will never be an empty string

---

### Given Code

```SQL
DB[:fakebin].multi_insert([
  {x: "45385593107843568"}, 
  {x: "509321967506747"}, 
  {x: "366058562030849490134388085"},
  {x: "15889923"},
  {x: "800857237867"}
])
  
results = run_sql

describe :columns do
   it "should return 2 columns" do
    expect(results.columns.count).to eq 2
   end
end

describe :column_names do
   it "should match column names" do
     expect(results.columns[0].to_s).to eq "x" 
     expect(results.columns[1].to_s).to eq "res" 
   end
end

compare_with expected do end

```

---

### Solution

```SQL
SELECT x,
    translate(
        translate(x, '01234', '00000'),
        '56789','11111'
      ) AS res
FROM fakebin;

```

[See on CodeWars.com](https://www.codewars.com/kata/57eae65a4321032ce000002d/train/sql)
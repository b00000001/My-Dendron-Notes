---
id: 8fw4xwe5s296cc697g6wdal
title: Algorithms
desc: ''
updated: 1649370703537
created: 1649370299034
---

### Algorithms

```const foo: (n : number) => void = (n) => {
    if (n <= 0) return;
    console.log('bar!');
    return foo(n - 1);
}
```

foo(5)

- The output of this function would be as follows:
  (5) foo(5)
  |
  |
  (4) foo(4)
  |
  |
  (3) foo(3)
  |
  |
  (2) foo(2)
  |
  |
  (1) base case

- Because each function call is determined by the number passed into the recursive function, this function has a time complexity of O(n).

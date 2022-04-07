---
id: 8fw4xwe5s296cc697g6wdal
title: Algorithms
desc: ''
updated: 1649373557406
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
  ```
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
  ```

- Because each function call is determined by the number passed into the recursive function, this function has a time complexity of O(n).
- When we analyze the space complexity of a recursive function, we should include any additional stack space that the function calls take up. When we make a recursive call, we add that to the stack. Since we have (n) different functions calls before we hit our base case, this function has an O(n) space complexity.
---
id: 3s8g4j07a4kgk5w6dml2nwt
title: Fibonacci Study
desc: ''
updated: 1649369595941
created: 1649369052619
---

### Fibonacci Algorithm

```const fib: (n: number) => number = (n) => {
    if (n <= 2) return 1;
    return fib(n - 1) + fib(n - 2);
}
```

Example of recursive function that will calculate the nth position of the fibonacci sequence.

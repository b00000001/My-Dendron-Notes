
### Fibonacci Algorithm

```const fib: (n: number) => number = (n) => {
    if (n <= 2) return 1;
    return fib(n - 1) + fib(n - 2);
}
```

Example of recursive function that will calculate the nth position of the fibonacci sequence.

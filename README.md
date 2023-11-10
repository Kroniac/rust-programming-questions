# rust-programming-questions

---

###### 1. What's the output?

```rust
fn main() {
    let numbers = vec![1, 2, 3, 4, 5];
    for number in numbers.iter() {
        println!("Squared: {}", number * number);
    }
}

main();
```

- A: Squared: 1 Squared: 4 Squared: 9 Squared: 16 Squared: 25
- B: Squared: 1 2 3 4 5
- C: Squared: 1 4 9 16 25
- D: This code will not compile

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The program uses iter() to iterate over each element in the numbers vector, and the map function squares each element. The println! macro then prints the squared values.

</p>
</details>

---

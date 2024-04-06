<div align="center">
    <img src="https://img.icons8.com/external-tal-revivo-bold-tal-revivo/90/external-rust-is-a-multi-paradigm-system-programming-language-logo-bold-tal-revivo.png" alt="external-rust-is-a-multi-paradigm-system-programming-language-logo-bold-tal-revivo"/>
  <h1>Rust Programming Questions</h1>
</div>

<br/>
<p align="center">🚀 Welcome to the Rust Programming Questions repository! Whether you're new to Rust or seeking to deepen your understanding, this collection covers a broad spectrum of topics, from fundamental concepts to advanced techniques. Use these questions to assess your knowledge, prepare for interviews, or simply refresh your skills. Each question is carefully crafted to challenge your grasp of Rust programming principles and features.</p>
<p align="center">💡 Answers are conveniently provided in collapsible sections below each question. Check back regularly for new additions to enhance your proficiency. Best of luck! 🍀</p>
<br/>

---

<br/>
<p align="center">💬 Saying Suggestions and Support 💬</p>
<p align="center">🌟 Have a saying suggestion or feedback to improve this repository? Your input is invaluable! Feel free to share your thoughts, ideas, or questions here. Your support and contributions help make this resource better for everyone. Let's collaborate and make learning Rust programming an enjoyable experience together! 🚀</p>
<br/>

---

#### 1. What's the output?

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

#### 2. What's the output of the following Rust code?

```rust
fn main() {
    let mut numbers = vec![1, 2, 3, 4, 5];
    let mut sum = 0;

    for number in numbers.iter() {
        sum += number;
    }

    println!("Sum: {}", sum);
}

main();
```

-   A: Squared: 1 Squared: 4 Squared: 9 Squared: 16 Squared: 25
-   B: Squared: 1 2 3 4 5
-   C: Squared: 1 4 9 16 25
-   D: This code will not compile

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The program uses iter() to iterate over each element in the numbers vector, and the map function squares each element. The println! macro then prints the squared values.
</p>
</details>

---

#### 3. What will the following code snippet output?

```rust
fn main() {
    let mut x = 5;
    let y = &mut x;
    *y += 1;
    println!("x: {}", x);
}

main();
```

-    A: x: 5
-    B: x: 6
-    C: This code will not compile
-    D: This code will panic at runtime

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The code compiles successfully and prints x: 6. The variable y is a mutable reference to x, allowing it to modify the value of x using the dereference operator *.
</p>
</details>

----

#### 4. What happens when you try to compile the following code?

```rust
fn main() {
    let s1 = String::from("hello");
    let s2 = s1;
    println!("{}", s1);
}

main();
```

-    A: The code compiles and prints "hello" twice.
-    B: The code compiles and prints "hello" once.
-    C: The code fails to compile because s1 is moved to s2.
-    D: The code fails to compile because the String type does not implement the Copy trait.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

The code fails to compile because the String type does not implement the Copy trait, and the assignment let s2 = s1 moves the ownership of the String from s1 to s2. Therefore, s1 is no longer valid after the assignment.
</p>
</details>

---

#### 5. What is the purpose of lifetimes in Rust?

- A: To specify how long references live in memory.
- B: To specify the lifetime of a variable.
- C: To prevent memory leaks.
- D: To specify the scope of a variable.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

Lifetimes in Rust specify how long references live in memory, ensuring that references are always valid and preventing dangling pointers.

</p>
</details>

---

#### 6. What does the `mut` keyword do in Rust?

- A: It creates a new mutable variable.
- B: It marks a variable as immutable.
- C: It specifies that a function can mutate its arguments.
- D: It specifies that a variable can be moved.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `mut` keyword in Rust is used to declare a mutable variable, allowing its value to be changed after it has been initialized.

</p>
</details>

---

#### 7. Which keyword is used in Rust to handle recoverable errors?

- A: `panic!`
- B: `return Err`
- C: `unwrap`
- D: `Result`

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

In Rust, the `Result` type is commonly used to handle recoverable errors. It represents either a success (`Ok`) or a failure (`Err`) and allows for explicit error propagation and handling.

</p>
</details>

---

#### 8. Which of the following statements about concurrency and parallelism in Rust is true?

- A: Rust's standard library provides native support for green threads, allowing lightweight concurrency.
- B: The `std::thread` module in Rust provides high-level abstractions for working with operating system threads.
- C: Rust's `async`/`await` syntax allows for automatic parallelization of code without any additional effort from the programmer.
- D: Rust's `Rayon` crate is primarily used for implementing lock-free data structures in multi-threaded applications.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `std::thread` module in Rust provides high-level abstractions for working with operating system threads, allowing developers to create and manage threads for concurrent execution of code.

</p>
</details>

---

#### 9. Consider the following Rust code:

```rust
enum TrafficLight {
    Red,
    Yellow,
    Green,
}

fn main() {
    let light = TrafficLight::Red;
    
    match light {
        TrafficLight::Red => println!("Stop!"),
        TrafficLight::Yellow => println!("Slow down!"),
        TrafficLight::Green => println!("Go!"),
    }
}

```
What will be printed when this code is executed?

-    A: Stop!
-    B: Slow down!
-    C: Go!
-    D: There will be a compilation error.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The match statement in the code matches the value of the light variable against each variant of the TrafficLight enum. Since light is TrafficLight::Red, the arm corresponding to TrafficLight::Red will be executed, printing Stop!.
</p>
</details>

---

#### 10. Consider the following Rust code:

```rust
trait Drawable {
    fn draw(&self);
}

struct Circle {
    radius: f64,
}

impl Drawable for Circle {
    fn draw(&self) {
        println!("Drawing a circle with radius {}", self.radius);
    }
}

fn main() {
    let c = Circle { radius: 5.0 };
    c.draw();
}

```

What will be printed when this code is executed?

-    A: Drawing a circle with radius 5.0
-    B: Drawing a circle with radius 0.0
-    C: Drawing a circle with radius f64
-    D: Compilation error

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The code defines a trait Drawable with a method draw, and a struct Circle with a field radius. The Circle struct implements the Drawable trait, providing an implementation for the draw method that prints the radius of the circle. In the main function, a Circle object c is created with a radius of 5.0, and the draw method is called on it, printing Drawing a circle with radius 5.0.
</p>
</details>

---

#### 11. Consider the following Rust code:

```rust
use std::fs::File;
use std::io::ErrorKind;

fn open_file(filename: &str) -> Result<File, String> {
    match File::open(filename) {
        Ok(file) => Ok(file),
        Err(error) => match error.kind() {
            ErrorKind::NotFound => Err(String::from("File not found")),
            _ => Err(String::from("Error opening file")),
        },
    }
}

fn main() {
    let result = open_file("nonexistent.txt");
    match result {
        Ok(file) => println!("File opened successfully"),
        Err(message) => println!("Error: {}", message),
    }
}

```

What will be printed when this code is executed?

-    A: File opened successfully
-    B: Error: File not found
-    C: Error opening file
-    D: Compilation error

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The open_file function attempts to open a file specified by the filename parameter. If the file is successfully opened, it returns a Result<File, String> with the File object. If an error occurs, it matches on the error kind: if the error kind is NotFound, it returns an error message indicating that the file was not found. Otherwise, it returns an error message indicating a general file opening error.

In the main function, open_file is called with the filename "nonexistent.txt". Since this file does not exist, the function returns an error with the message "File not found", which is then printed to the console.
</p>
</details>

---

#### 12. Consider the following Rust code:

```rust
fn main() {
    let mut numbers = vec![1, 2, 3, 4, 5];
    let squared_numbers: Vec<i32> = numbers.iter().map(|&x| x * x).collect();
    println!("{:?}", squared_numbers);
}

```

What will be printed when this code is executed?

-    A: [1, 4, 9, 16, 25]
-    B: 1 4 9 16 25
-    C: [1, 2, 3, 4, 5]
-    D: 1, 4, 9, 16, 25

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The map method is used to apply the closure |&x| x * x to each element in the numbers vector. This closure squares each element. The collect method then collects the transformed elements into a new vector squared_numbers. Finally, the println! macro prints the contents of squared_numbers.

Therefore, the output will be [1, 4, 9, 16, 25].
</p>
</details>

---

#### 13. What does the following Rust code snippet accomplish?

```rust
fn main() {
    let x = 5;
    let square = |num| num * num;
    let result = square(x);
    println!("{}", result);
}

```

-    A: It defines a function named square that takes a parameter num and returns the square of that number.
-    B: It defines a closure named square that takes a parameter num and returns the square of that number.
-    C: It defines a trait named square that takes a parameter num and returns the square of that number.
-    D: It defines a macro named square that takes a parameter num and returns the square of that number.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

This code defines a closure named square that takes a parameter num and returns the square of that number. Closures in Rust are similar to functions but have the ability to capture variables from their surrounding environment. In this case, the closure captures the variable x from the main function's scope.
</p>
</details>

---

#### 14. Consider the following Rust code:

```rust
fn main() {
    let mut x = 5;
    let y = &mut x;
    *y += 1;
    println!("{}", x);
}

```

What will be printed when this code is executed?

-    A: 5
-    B: 6
-    C: Error: cannot borrow x as immutable because it is also borrowed as mutable
-    D: Error: cannot borrow y as mutable more than once at a time

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

In Rust, y borrows x mutably, so it can modify the value of x. Therefore, when *y += 1; is executed, x is modified to 6, and this value is printed by println!("{}", x);.
</p>
</details>

---

#### 15. What is a mutable reference in Rust?

- A: A reference that allows the referenced data to be modified
- B: A reference that cannot be modified after it is created
- C: A reference that can be shared across multiple threads
- D: A reference that has a lifetime longer than the data it references

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

A mutable reference in Rust is a reference that allows the referenced data to be modified. It is declared using the `&mut` syntax.

</p>
</details>

---

#### 16. What does the `match` keyword do in Rust?

- A: It defines a new function
- B: It declares a new variable
- C: It performs pattern matching
- D: It allocates memory for a new data structure

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The `match` keyword in Rust is used to perform pattern matching. It allows you to compare a value against a series of patterns and then execute code based on which pattern matches.

</p>
</details>

---

#### 17. What is the purpose of the `#[derive(Debug)]` annotation in Rust?

- A: It enables debugging information to be printed for a data structure
- B: It disables debugging information for a data structure
- C: It defines a new data structure
- D: It allocates memory for a data structure

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

The `#[derive(Debug)]` annotation in Rust automatically implements the `Debug` trait for a data structure, allowing you to print debugging information about instances of that data structure using the `{:?}` format specifier.

</p>
</details>

---

#### 18. What is the difference between `Box<T>` and `Rc<T>` in Rust?

- A: `Box<T>` is used for single ownership and `Rc<T>` is used for reference counting
- B: `Box<T>` is used for reference counting and `Rc<T>` is used for single ownership
- C: Both `Box<T>` and `Rc<T>` are used for single ownership, but `Box<T>` allows borrowing
- D: Both `Box<T>` and `Rc<T>` are used for reference counting, but `Box<T>` does not allow borrowing

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

`Box<T>` is a smart pointer used for single ownership. It allocates memory on the heap and points to it. `Rc<T>` is a reference-counted smart pointer, allowing multiple ownership. It keeps track of the number of references to a value and automatically deallocates memory when the number of references drops to zero.

</p>
</details>

---

#### 19. What is the difference between mutable and immutable references in Rust?

- A: Mutable references allow modification of the data they reference, while immutable references do not
- B: Immutable references allow modification of the data they reference, while mutable references do not
- C: Both mutable and immutable references allow modification of the data they reference
- D: Neither mutable nor immutable references allow modification of the data they reference

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

Mutable references (`&mut`) allow modification of the data they reference, while immutable references (`&`) do not. In Rust, mutable references enforce the concept of exclusive access to data, ensuring memory safety.

</p>
</details>

---

#### 20. What is mutable borrowing in Rust?

- A: Allowing multiple immutable references to a variable
- B: Allowing multiple mutable references to a variable
- C: Allowing only one immutable reference to a variable
- D: Allowing only one mutable reference to a variable

<details><summary><b>Answer</b></summary>
<p>

#### Answer: D

Mutable borrowing in Rust allows only one mutable reference to a variable at a time. This ensures that there are no data races or conflicts when modifying shared data concurrently.

</p>
</details>

---

#### 21. What is the purpose of the `drop` method in Rust?

- A: To free memory allocated on the heap.
- B: To call destructors for resources like files or network connections.
- C: To terminate the program.
- D: To convert a mutable reference to an immutable reference.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The `drop` method in Rust is called when an object goes out of scope, and its purpose is to release resources like memory allocated on the heap or close file handles. This is particularly useful for managing resources that need to be cleaned up explicitly.

</p>
</details>

---

#### 22. What does the following Rust code snippet do?

```rust
fn main() {
    let mut num = 5;
    let result = {
        num += 1;
        num * 2
    };
    println!("Result: {}", result);
}

```

-    A: Adds 1 to num, then multiplies it by 2, and prints the result.
-    B: Multiplies num by 2, adds 1 to the result, and prints it.
-    C: Multiplies num by 2, adds 1 to num, and prints the result.
-    D: Prints 5.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: C

The code block { ... } creates a new scope, and result is assigned the value of the last expression in that scope, which is num * 2. Inside the block, num is incremented by 1, then multiplied by 2, and the result is printed.
</p>
</details>

---

#### 23. Consider the following Rust code snippet:

```rust
fn main() {
    let mut x = 10;
    let y = &mut x;
    *y += 1;
    println!("x: {}", x);
}

```

What will be printed when this code is executed?

-    A: x: 10
-    B: x: 11
-    C: This code will not compile due to a mutable borrowing violation.
-    D: This code will panic at runtime.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

The code will print x: 11. The variable y is a mutable reference to x, so the line *y += 1; increments the value of x by 1. Since x is mutable and was borrowed mutably by y, the change to x is reflected even after y goes out of scope.
</p>
</details>

---

#### 24. What does the following Rust code snippet demonstrate?

```rust
fn main() {
    let numbers = vec![1, 2, 3, 4, 5];
    let doubled_numbers: Vec<_> = numbers.iter().map(|x| x * 2).collect();
    println!("{:?}", doubled_numbers);
}

```

-    A: It creates a new vector containing each number in the numbers vector multiplied by 2.
-    B: It prints each number in the numbers vector multiplied by 2.
-    C: It demonstrates error handling for multiplying numbers in a vector.
-    D: It demonstrates lifetime annotations for vectors.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: A

This code demonstrates the use of iterators and the map function to create a new vector called doubled_numbers where each element is the result of multiplying the corresponding element in the numbers vector by 2.
</p>
</details>

---

#### 25. What is the purpose of the following Rust code snippet?

```rust
fn main() {
    let mut numbers = vec![1, 2, 3, 4, 5];
    numbers.retain(|&x| x % 2 == 0);
    println!("{:?}", numbers);
}

```

-    A: It prints all the numbers in the vector numbers.
-    B: It removes all the odd numbers from the vector numbers.
-    C: It doubles all the numbers in the vector numbers.
-    D: It reverses the order of the numbers in the vector numbers.

<details><summary><b>Answer</b></summary>
<p>

#### Answer: B

This code snippet demonstrates the use of the retain method, which removes all elements from the vector that do not satisfy the predicate specified by the closure. In this case, it removes all odd numbers from the numbers vector, leaving only the even numbers.
</p>
</details>



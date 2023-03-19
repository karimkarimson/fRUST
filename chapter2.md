# Guessing Game
+ We will write a program that generates a random integer between 1 & 100.
+ `cargo new guessing_game`
	`use std::io;
	fn main() {
    		println!("Guess the number!");

    		println!("Please input your guess.");

    		let mut guess = String::new();

    		io::stdin()
        		.read_line(&mut guess)
        		.expect("Failed to read line");

    		println!("You guessed: {guess}");
		}`
+ `use std::io` import the _standard library_ of rust
+ `println!()` is a build in _macro_. Macros are spottable by the !
+ `let` creates a new _variable_
+ `mut` lets a _variable_ be **mutable** 
+ comments start with `//`
+ `String::new()` calls for the _new_ function of _String_ type
> So, the `::`syntax indicates an association between a type and a function
+ `io::stdin()` calls the _stdin_ function associated with the _io_ module
> > what do i call the part before the :: ?
> + you can use not imported modules, for example `std::io::Stdin`
> + `.read_line(&mut guess)` call [read_line](https://doc.rust-lang.org/stable/std/io/struct.Stdin.html#method.read_line)-method
> + **&** symbolises a reference, in this case for the _mutable guess_-variable
> + `.expect("Failed to read line");`finishes the `io::stdin`block which is seen as one line
> > + as a one liner this would look like this:
> > + `io::stdin().read_line(&mut guess).expect("Failed to read line");
> + the read_line() method expects input and therefore a Result, in Rust called **enumeration** or short **enum**
> > _enumerations can have different states, called variants_
> + the **Result** in this case has two variants: `Ok`and `Err`
> + the `Err`variant will contain information about _how_ or _why_ the operation failed
> + so if the operation in this case fails, the program crashes and calls the `expect()`method and prints its insides
> > ** this is an error handling example **
+ `println!("{guess}");`as you notice the curly brackets { } serve as a **placeholder** for a variable

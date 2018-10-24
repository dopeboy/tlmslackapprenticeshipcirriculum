# Lesson 0:  Introduction to Ruby

We'll cover the major differences between Ruby and JavaScript. We'll then get practice writing a simple program in Ruby.

## Major differences between Ruby and JavaScript

### Structural

* Ruby is used to power a lot of web backends using the [Ruby on Rails](https://rubyonrails.org/) framework. JavaScript powers the frontend of all modern web applications. It is supported by every browser in the world making it the most popular programming language. It can also be used in the backend using frameworks like Node.JS.

* Everything is an object in Ruby. In JavaScript, there are primitives (booleans, numbers, strings, etc) and there are objects too.

* Closures are a bit more powerful in Ruby. See [here](https://medium.com/@sihui/what-the-heck-are-code-blocks-procs-lambdas-and-closures-in-ruby-2b0737f08e95) and [here](https://gist.github.com/rsliter/4196824).

### Syntactic

* Variable declaration and initialization: `variable_name = variable_value` [0]

* Accessing a hash/dictionary: [0]

    ```
    var hash_name = { hash_key: hash_value , sechash_key: sechash_value}
    hash_name[:hash_key]
    ```

* No semicolons [0]

* Function definitions: [0]
   
    ```
    def sayhello(name)
        p “Hello” + name.to_s
    end
    ```

## Hello world

1. Head over to [repl.it](https://repl.it/languages/ruby). 
2. Put in `puts 'Hello, world!'`

## Exercise

Let's get a basic handle on Ruby. Use [repl.it](https://repl.it/languages/ruby) to complete these exercises.

1. Write [FizzBuzz](http://wiki.c2.com/?FizzBuzzTest) in Ruby.
2. Write a simple car simulator in Ruby. Follow the object oriented paradigm. Make sure your simulator has:
    * A car object that has a `travel(miles)` function.
    * An engine object that keeps track of gasoline consumed.
    * Four wheel objects that keep track of tire pressure (that might decrease over distance).

    Your `main()` function should instantiate a `Car` object and run the `travel()` function. The user should be able to inquire about the gasoline and tire pressure.

## References & Additional Reading

[0] - https://medium.com/learning-to-code/ruby-vs-javascript-a-quick-comparison-ebd3b63ebc49

[1] - https://medium.com/front-end-hacking/differences-between-ruby-and-javascript-58c580e94570
# Lesson 1:  Introduction to PHP

We'll cover the major differences between javaScript and PHP. We'll then get practice writing a simple program in PHP.

## Major differences between PHP and JavaScript

### Structural

* PHP is used to power web backends. There are several web frameworks for PHP including Laravel, Zend, and Codeigniter. 

* PHP is a multi-threaded language that blocks on I/O operations. JavaScript is a single threaded language based on an event driven model but no blocking I/O.

* There's a more common practice of interleaving presentation with logic in PHP land [1]. This is getting a little more common with JSX but not an inherent practice in JavaScript land.

### Syntactic

* In PHP [0]:

    ```
    $this->turtle   # Instance Property
    $this->bike()   # Method
    $apple          # Variable
    ```
    
* The PHP interpreter will look for an opening `<?php` and closing `?>`.

## Hello world

1. Install the PHP CLI.
2. Make a new directory and place an `index.php` in it with the following contents:

    ```
    <?php 
    echo "hello";
    ?>
    ```
3. Run `php -S localhost:8888` and open [http://localhost:8888/](http://localhost:8888/) in your browser.

## Exercise

Let's get a basic handle on PHP.

1. Write [FizzBuzz](http://wiki.c2.com/?FizzBuzzTest) in PHP.
2. Write a REST API that serves famous quotes. Each quote should have an author associated to it. These quotes can be hardcoded into your PHP file as an associative array. The following endpoints should be supported. Each endpoint below has a sample response.

    ```
    Retrieve every quote
    GET /quotes
    {
        "status": "OK",
        "payload": [
            {
                "author": "Homer Simpson",
                "quote": "Operator! Give me the number for 911!"
            },
            ...
        ]
    }

    Retrieve a random quote
    GET /quotes/random
    {
        "status": "OK",
        "payload": {
            "author": "Eleanor Roosevelt",
            "quote": "Great minds discuss ideas; average minds discuss events; small minds discuss people."
         }
    }

    NOTE: This should fuzzy search against the author and quote fields
    GET /quotes?s=Arthur
    {
        "status": "OK",
        "payload": [
            {
                "author": "Arthur Doyle",
                "quote": "..."
            },
            {
                "author": "...",
                "quote": "Arthur was a fine man..."
            },            
            ...
        ]
    }

    Create a new quote (this doesn't need to persist across a server shutdown)
    POST /quotes
    {
        "status": "OK",
        "payload": {
            "author": "Eleanor Roosevelt",
            "quote": "Great minds discuss ideas; average minds discuss events; small minds discuss people."
         }
    }
    ```

## References & Additional Reading

[0] - https://www.sitepoint.com/php-vs-ruby-lets-all-just-get-along/

[1] - https://www.w3schools.com/php/php_syntax.asp
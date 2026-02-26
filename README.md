# PHP
 
 (1)	What are the differences between echo and print in PHP?
```bash
 echo: Can take multiple parameters (though rarely used this way) and has no return value. It is slightly faster.
 print: Can only take one argument and always returns 1, so it can be used in expressions.
```
(2)	What is PEAR in PHP?
```bash
PEAR stands for PHP Extension and Application Repository. Think of it as a library of reusable PHP components. However, in modern PHP development, it has largely been replaced by Composer.
```
(3)	What is the difference between a session and cookies?
```bash
```
(4)	How do you define a constant in PHP?
```bash
A constant is an identifier for a simple value that cannot change during the script's execution.
•	Example: define("SITE_URL", "https://example.com");

```

(5)	Explain PHP error types.
```bash
•  Notice: Non-critical errors (e.g., using an undefined variable). The script keeps running.
•  Warning: More serious but non-fatal (e.g., include a file that doesn't exist). The script keeps running.
•  Fatal Error: Critical issues (e.g., calling a non-existent function). The script stops immediately.
•  Parse Error: Syntax errors (e.g., a missing semicolon). The script won't run at all.

```
(6)	What is isset()?
```bash
 It checks if a variable is declared and is not null. It returns true or false.
```
(7)	What is empty()?
```bash
 It checks if a variable is "empty." It returns true if the variable is an empty string, 0, null, false, or an empty array.
```
(8)	What is autoload in PHP and why is it important?
```bash
Autoloading allows PHP to automatically load a class file when you try to use that class, so you don't have to write require or include at the top of every single file.
•	Why it's important: It keeps your code clean and organized, especially in large projects.
```
(9)	What is the difference between define and const in PHP?
```bash
define(): Defines constants at runtime. You can use it inside if statements.
const: Defines constants at compile-time. It’s cleaner and used inside Classes, but it can't be used inside conditional blocks.

```
(10)	What is the final keyword?
```bash
When you prefix a class or a method with final, it prevents inheritance.
•	A final class cannot be extended by another class.
•	A final method cannot be overridden by a child class.

```
(11)	What are PHP filters? 
```bash
PHP Filters: These are used to validate (check if it's an email) or sanitize (remove illegal characters) user input.
```
(12)	What is PDO in PHP?
```bash
PDO (PHP Data Objects): A consistent way to connect to various databases. It allows you to switch from MySQL to PostgreSQL without changing much code.
```
(13)	What is SQL Injection? How to prevent it?
```bash
SQL Injection is a security vulnerability where an attacker "injects" malicious SQL code into your query via user input (like a login form) to steal or delete data.
```
 (14) What is Doctrine PHP?
 ```bash
Doctrine is a set of PHP libraries focused on database storage and object mapping. Its most famous component is the ORM (Object-Relational Mapper), which allows you to write database queries using PHP objects instead of raw SQL. It is the default ORM for the Symfony framework.
```
 (15) What are Namespaces in PHP?
  ```bash
Namespaces are a way of encapsulating items. They solve two main problems:

Name Collisions: They allow you to have two classes with the same name (e.g., two User classes) as long as they are in different namespaces.

Organization: They help group related classes together, similar to directories in an operating system.

Example: namespace App\Models;
```
(16) What are the different ORMs in PHP?
  ```bash
An ORM (Object-Relational Mapper) lets you interact with your database using an object-oriented syntax.

Eloquent: Used primarily in Laravel. It uses the "Active Record" pattern.

Doctrine: Used primarily in Symfony. It uses the "Data Mapper" pattern.

Propel: An older, XML-based ORM.

RedBeanPHP: A "zero-config" ORM that creates tables automatically.
```
(17) Sessions vs. Cookies in PHP
  ```bash
Cookies: Stored on the client-side (browser). They are useful for tracking users over long periods (e.g., "Remember Me" checkboxes) but are less secure because users can modify them.

Sessions: Stored on the server-side. The browser only stores a "Session ID." They are more secure and are used to store sensitive data like login status.
```
(18) Throwable $th vs. Exception $e in PHP  
```bash
Exception $e: Only catches standard exceptions (user-defined or logical exceptions).

Throwable $th: This is the interface that both Exception and Error implement. Since PHP 7, using Throwable allows you to catch both internal PHP errors (like TypeError) and standard exceptions in a single block.
```
(19) Exception vs. Error in PHP
  ```bash
Exception: Typically represents "recoverable" problems in the program logic (e.g., a missing file or failed API call).

Error: Typically represents "unrecoverable" or serious engine problems (e.g., TypeError, ParseError, or ArithmeticError).
```
(20) PDO vs. MySQLi in PHP
  ```bash
Feature,PDO,MySQLi
Database Support,"Supports 12 different drivers (MySQL, PostgreSQL, etc.)",Supports only MySQL.
Parameters,"Named parameters (e.g., :id) and positional.",Only positional parameters (?).
Security,Both support Prepared Statements.,Both support Prepared Statements.
Performance,Slightly slower (due to abstraction layer).,Slightly faster for MySQL specifically.

```
(21) Differences between == and ===
  ```bash
== (Equal): Performs Type Juggling. It compares values after converting them to a common type.

Example: 5 == "5" is True.

=== (Identical): No type conversion. It compares both the Value and the Data Type.

Example: 5 === "5" is False.
```

# Laravel
 
 1. What is Object-Oriented Programming (OOP)?
    ```bash
    OOP is a programming paradigm based on the concept of "objects," which can contain data (properties) and code (methods). Instead of writing a long list of instructions (procedural), you organize your code into modular pieces that interact with each other. It rests on four pillars: Encapsulation, Abstraction, Inheritance, and Polymorphism.

    ```
2. Class vs. Object in PHP
   ```bash
    Class: The blueprint or template. It defines what data and behavior a type will have (e.g., a "Car" blueprint).

   Object: An instance of that class. It is the actual "Car" built from the blueprint, living in the computer's memory.
    ```
 3. What are Traits in PHP?
    ```bash
    Traits are a mechanism for code reuse in languages like PHP where multiple inheritance is not supported. A Trait allows you to inject a set of methods into multiple independent classes.

    ```
 4. What are Access Modifiers?
    ```bash
    public: Accessible from anywhere (inside or outside the class).

    protected: Accessible only within the class itself and by inheriting (child) classes.

    private: Accessible only within the class that defined it.
    ```
5. this vs. self in PHP
    ```bash
    $this: Refers to the current object instance. Used to access non-static properties and methods.

    self: Refers to the current class. Used to access static properties, static methods, or constants
    ``` 
6. What are Namespaces?
   ```bash
   Name collisions: They allow you to have two classes named User as long as they are in different namespaces (e.g., App\Models\User vs. App\Auth\User).

   Organization: They help group related classes together logically.
    ```
7. extends vs. implements
   ```bash
   extends: Used for Inheritance. A child class inherits the logic of a parent class.

   implements: Used for Interfaces. A class signs a contract promising to define all methods listed in the interface.

    ```
8. Constructor and Destructor
   ```bash
   __construct(): Runs automatically when a new object is created. Usually used to initialize properties.

   __destruct(): Runs automatically when the object is destroyed or the script ends. Used for cleanup (like closing database connections).

    ```
10. Exception Handling
```bash
Exceptions are used to handle errors gracefully without crashing the script.

throw: Triggers the error.

try: Wraps the code that might fail.

catch: Defines what to do if an error occurs.

finally: Code that runs regardless of whether an error happened (e.g., closing a file).
```
# Laravel

(1)	What is the Middleware in Laravel?
```bash
Middleware acts as a bridge or a "filter" between a request and your application. It intercepts incoming HTTP requests.
Common uses: Checking if a user is authenticated, CORS headers, or logging.
```
(2)	What is Blade in Laravel?
```bash
Blade is Laravel’s powerful templating engine. It allows you to write plain PHP in your templates without the messy syntax. It compiles into plain PHP code and caches it for performance.
```
(3)	Service Container vs Dependency Injection in Laravel ?
```bash
Service Container: A powerful tool for managing class dependencies and performing dependency injection. Think of it as a "big box" where you bind interfaces to concrete classes.

Dependency Injection: The act of "injecting" class dependencies into a class via the constructor or methods. The Container automates this process for you.
```
(4)	What is the Migration in Laravel?
```bash
Migrations are like version control for your database. Instead of sharing SQL dumps, you share migration files that define the table schema in PHP code.
```
(5)	What are seeders & factories in Laravel?
```bash
Factories: Define a "blueprint" for generating fake data (using the Faker library).

Seeders: Use those factories (or manual data) to actually populate the database with records for testing.
```
(6)	What is the route resource in Laravel?
```bash
Route::resource() is a shortcut that creates all the CRUD routes (index, create, store, show, edit, update, destroy) for a controller in a single line of code.
```
(7)	What are Laravel Service Providers?
```bash
The central place of all Laravel application bootstrapping. Your own application, as well as all of Laravel's core services, are bootstrapped via service providers. They "register" things into the Service Container.
```
(8)	 What is Laravel facade?
```bash
Facades provide a "static" interface to classes that are available in the application's service container. For example, Cache::get() is easier to write than resolving the cache service manually.
```
(9)	What are Queues in Laravel?
```bash
Queues allow you to defer the processing of a time-consuming task, such as sending an email, until a later time. This drastically speeds up web requests for the end user.
```
(10)	Queues vs Jobs also schedular in Laravel?
```bash
Job: A specific task (a class) that needs to be done.

Queue: The line/storage where Jobs wait to be processed by a worker.

Scheduler: A tool (replacing individual Cron entries) that allows you to define when tasks or commands should run (e.g., "every Monday at 5 PM").
```
(11)	What is Laravel Caching?
```bash
Storing expensive data (like complex query results) in a fast storage system (like Redis or Memcached) so that subsequent requests don't have to re-process the data.
```
(12)	Explain Request Lifecycle in Laravel ?
```bash
Entry: public/index.php receives the request.

Kernel: The HTTP Kernel loads service providers and middleware.

Routing: The Router directs the request to a controller or closure.

Response: The controller returns a response, which travels back through the middleware to the user.
```
(13)	What is artisan in Laravel?
```bash
Artisan is the Command Line Interface (CLI) included with Laravel. It provides helpful commands for building your app (e.g., php artisan make:controller).
```
(14)	Tell me about multi-tenancy in Laravel?
```bash
An architecture where a single instance of a software application serves multiple customers (tenants). Each tenant's data is isolated from others, either by a separate database or a tenant_id column.
```
(15)	How to debug in Laravel?
```bash
Log Files: Checking storage/logs/laravel.log.

Helper functions: Using dd() (Die and Dump) or dump().

Laravel Telescope: An elegant debug assistant.

Ignition: The default error page that suggests solutions.
```
(16)	What is a RESTful API in Laravel ?
```bash
An API that follows REST principles (Representational State Transfer). In Laravel, this usually means returning JSON responses and using standard HTTP verbs (GET, POST, PUT, DELETE).
```
(17)	What are Laravel Contracts?
```bash
Laravel Contracts are a set of interfaces that define the core services provided by the framework. If you use a Contract instead of a Facade, your code becomes more loosely coupled and easier to test.
```
(18)	What is the difference between query builder & eloquent in Laravel?
```bash
Query Builder: Direct, fluent interface to run database queries. Faster for very large datasets.

Eloquent (ORM): Maps database tables to PHP objects. It is more readable and provides "Active Record" features like relationships, but is slightly slower than raw queries.
```
(19)	Is the CSRF token is fixed for all users in a Laravel project ?
```bash
No. The CSRF token is unique to each user session. It changes when the user logs in/out or when the session expires to ensure security against cross-site request forgery.
```
(20)	How to exclude routes from CSRF protection in Laravel?
```bash
You can add the specific URIs to the $except array in the App\Http\Middleware\VerifyCsrfToken middleware (or bootstrap/app.php in Laravel 11).
```
(21)	How to optimize SQL queries in Laravel application?
```bash
Eager Loading: Use with() to solve the $N+1$ query problem.
Indexing: Ensure database columns used in WHERE clauses are indexed.
Select specific columns: Use select('id', 'name') instead of select *.
```
(22)	How to optimize Laravel application performance?
```bash
php artisan config:cache

php artisan route:cache

php artisan view:cache

Using a fast Cache/Session driver (Redis).
```
(23)	What is Multi-Authentication in Laravel?
```bash
Allows you to have different types of users (e.g., "Admins" and "Customers") logging in via different tables or guards within the same application.
```
(24)	Why we use migrations files in Laravel and did not interact directly with the database?
```bash
Team Collaboration: Everyone has the same DB structure.

History: You can "rollback" changes easily.

Database Agnostic: You can switch from MySQL to PostgreSQL without rewriting your schema code.

```
(25)	What are Polymorphic Relationships in Laravel?
```bash
A relationship where a model can belong to more than one other model on a single association.

Example: A Comment model might belong to both a Post model and a Video model.
```



# Interview-Qstion
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

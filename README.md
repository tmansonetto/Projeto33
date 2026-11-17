# Projeto33 – Streams and File Processing

A Java console exercise that reads employees from a CSV file and processes them with the **Stream API**.

## What it does
1. Asks for the path of a CSV file whose lines look like `name,email,salary`.
2. Loads every line into a list of `Employee` objects.
3. Asks for a salary threshold and prints, sorted alphabetically, the e-mails of everyone who earns more than it.
4. Prints the sum of the salaries of people whose name starts with `M`.

It also includes a small PostgreSQL (JDBC) connectivity check. The credentials are read from the environment variables `DB_USER` and `DB_PASSWORD` (nothing is hard-coded).

## Structure
```
src/application/Program.java    Main program
src/entities/Employee.java      name, email, salary
```

## Concepts practiced
`BufferedReader` / `FileReader`, `filter`, `map`, `sorted`, `reduce`, `Collectors.toList`, try-with-resources.

## Running
Requires JDK 17+. Open in IntelliJ IDEA and run `application.Program`, or compile with `javac` and run with `java`. The PostgreSQL driver (`postgresql-42.7.x.jar`) must be on the classpath.

Sample input:
```
Maria,maria@gmail.com,3200.00
Alex,alex@gmail.com,1900.00
Marco,marco@gmail.com,1700.00
```

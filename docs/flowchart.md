# Flowcharts

Let's Go

```mermaid
---
title: AAP Database Schema
---
classDiagram
    Person <|-- User
    Role --|> User
    class Person {
        +int id
        +string firstname
        +string lastname
        +string email
    }
    class Role {
        +int id
        +int person_id
        +string role
        +string description
    }
    class User {
        +int id
        +int person_id
        +string password
        +uint admin
    }
```
 ---
 # Bar
 ```mermaid
xychart-beta
    title "Sales Revenue"
    x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
    y-axis "Revenue (in $)" 4000 --> 11000
    bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
    line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
 ```
 ---
 # Gantt

 ```mermaid
gantt
    title A Gantt Diagram
    dateFormat YYYY-MM-DD
    section Section
        A task          :a1, 2014-01-01, 30d
        Another task    :after a1, 20d
    section Another
        Task in Another :2014-01-12, 12d
        another task    :24d
 ```
 ---
 
```mermaid
flowchart
    S[Start] --> A;
    A(Enter your email) --> B{Existing User};
    B -->|No| C(Enter name);
    C --> D{Accept Conditions?}
    D -->|No| A
    D -->|Yes| E(Send email with magic link)
```
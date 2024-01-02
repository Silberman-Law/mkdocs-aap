### Database Schema

<!--
https://mermaid.js.org/syntax/classDiagram.html
-->
```mermaid
classDiagram
    person <|-- person_user
    person_role --|> person_user
    roles --|> person_role
    note for roles "Roles defined by name\ndescription"
    class person {
        +int id
        +string firstname
        +string lastname
        +string email
        +datetime createdon
        +id(PK)
        +email(unique)
    }
    class person_role {
        +int id
        +int person_id
        +int role_id
        +datetime createdon
        +id(PK)
        +person_id(FK)
        +role_id(FK)
    }
    class person_user {
        +int id
        +int person_id
        +string password
        +uint admin
        +datetime createdon
        +id(PK)
        +person_id(FK)
    }
    class roles {
        +string id
        +string role
        +string description
        +datetime createdon
        +id(PK)
        +role(unique)
    }
```
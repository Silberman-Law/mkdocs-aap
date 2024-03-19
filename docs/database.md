### Database Schema

<!--
https://mermaid.js.org/syntax/classDiagram.html
-->
```mermaid
classDiagram
    users <|-- user_login
    user_roles --|> user_login
    roles --|> user_roles
    note for roles "Roles defined by\nrole/description"
    templates --|> template_columns
    class users {
        +int id
        +string firstname
        +string lastname
        +string email
        +datetime createdon
        +id(PK)
        +email(unique)
    }
    class user_roles {
        +int id
        +int user_id
        +int role_id
        +datetime createdon
        +id(PK)
        +user_id(FK)
        +role_id(FK)
    }
    class user_login {
        +int id
        +int user_id
        +string password
        +uint admin
        +datetime createdon
        +id(PK)
        +user_id(FK)
    }
    class roles {
        +string id
        +string role
        +string description
        +datetime createdon
        +id(PK)
        +role(unique)
    }
    class templates {
        +int id
        +string name
        +string description
        +int active
        +datetime createdon
        +id(PK)
    }
    class template_columns {
        +int id
        +int template_id
        +string name
        +string description
        +int required
        +int active
        +datetime modifiedon
        +datetime createdon
        +id(PK)
        +template_id(FK)
    }
    class clients {
        +int id
        +string name
        +string description
        +int active
        +datetime createdon
        +id(PK)
    }
```
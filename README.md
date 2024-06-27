# Introduction to Odoo

## Server framework 101

### Architecture

Odoo follows a multitier architecture meaning that the presentation, the
business logic and the data storage are separated.


<p align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Overview_of_a_three-tier_application_vectorVersion.svg" width=500>

</p>

#### Multitier architecture application

```mermaid
sequenceDiagram
    participant C as Client
    participant A as Aplication (Odoo Server)
    participant D as Data Base (PostgreSQL)

    C->>A: Data requests/operations
    A->>D: Queries/Data manipulation
    D-->>A: Data responses
    A-->>C: Response result

    %%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#005eff',
      'primaryTextColor': 'black',
      'primaryBorderColor': '#000',
      'lineColor': '#000000',
      'secondaryColor': '#006100',
      'tertiaryColor': '#fff',
      'fontFamily': ''
    }
  }
}%%

```

### Odoo modules
Odoo modules are the main building blocks of the Odoo application. They are
independent pieces of code that can either add brand new business logic to an
Odoo system or alter an extend existing business logic.

Modules may also be referred to as `addons` and the directories where Odoo
server finds them form the  `addons_path`

#### Compositio of a module

```mermaid
mindmap
  root((Composition 
  of a module))
    An Odoo module can contain:
      Business objects
        Declared as Python classes
        Mapped to database columns via ORM
      Object views
        Define UI display
      Data files
        XML or CSV files declaring model data:
          Views or reports
          Configuration data
          Demonstration data
          And more
      Web controllers
        Handle requests from web browsers
      Static web data
        Images, CSS or JavaScript files
    None of these elements are mandatory

    Some modules may only add data files

    Others may only add business objects

%%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': 'white',
      'primaryTextColor': 'black',
      'primaryBorderColor': '',
      'lineColor': '',
      'secondaryColor': 'yellow',
      'tertiaryColor': 'yellow',
      'fontFamily': ''
    }
  }
}%%
```

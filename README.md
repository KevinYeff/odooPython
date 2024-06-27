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

<iframe style="border:none" width="800" height="450" src="https://whimsical.com/embed/KfWFP5qAr93GTLHMkCR7o4"></iframe>

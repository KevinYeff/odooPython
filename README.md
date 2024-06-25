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

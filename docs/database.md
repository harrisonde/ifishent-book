#Database Design
The following depicts relationships that may exist with the application API. Relationship between tables are established by foreign keys (fk). Auto incremented keys are indicated by "AI." 

## Models

| tasks |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
|  | VARCHAR | **uuid** |
|  | VARCHAR | **name** |
|  | FLOAT | **time_estimate** |
|  | DATETIME | **created_at** |
|  | DATETIME |**updated** |
|  | VARCHAR | **user_id** |
|  | DATETIME | **deleated_at** |
|  | BOOL | **started** |
|  | DATETIME | **due_date** |

| timers |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
|  | VARCHAR | **uuid** |
| | BOOL | **track** |
| | DATETIME | **created_at** |
| | DATETIME | **updated_at** |
| | DATETIME | **expiry** |
| | BOOL | **enabled** |

| users |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
|  | VARCHAR | **uuid** |
| | VARCHAR | **name** |
| |  VARCHAR | **email** |
| |  VARCHAR | **password** |
| |  VARCHAR | **rember_token** |


| password_resets |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
| |  VARCHAR | **email** |
| |  VARCHAR | **token** |
| |  DATETIME | **created_at** |
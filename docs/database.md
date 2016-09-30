#Database Design
The following depicts relationships that may exist with the application API. Relationship between tables are established by foreign keys (fk). Auto incremented keys are indicated by "AI." 

## SQL Tables

| tasks |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
|  | VARCHAR | **name** |
|  | FLOAT | **time_estimate** |
|  FK | VARCHAR | **user_id** |
|  | BOOL | **status** |
|  | DATETIME | **due_date** |
|  | DATETIME | **created_at** |
|  | DATETIME | **deleated_at** |
|  | DATETIME |**updated_at** |

| timers |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
| | BOOL | **track** |
| | DATETIME | **expiry** |
| | DATETIME | **created_at** |
| | DATETIME | **updated_at** |

| users |  | |
| -- | -- | -- |
| PK | TEXT | **uuid** |
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

| audit |  | |
| -- | -- | -- |
| AI, PK | INT | **id** |
| |  DATETIME | **created_at** |
| FK | VARCHAR | **user_uuid** |
||TEXT | **event_type**|
||TEXT | **event_uuid**|

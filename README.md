# Database Modeling - YrkesCo

Database design for a fictional vocational school management system, built as a data engineering exercise.
Covers the full design process - from conceptual ERD to physical PostgreSQL schema — for a school managing students, teachers, courses, and consultants across two cities.


## Stack

PostgreSQL, Docker, DBML


## Docs
- [Project Requirements](docs/project-requirements.md)
- [Conceptual ERD](docs/conceptual-model.md)
- [Logical ERD](docs/logical-model.md)
- [Physical ERD](docs/physical-model.md)
- [Physical model (DBML)](models/physical-model.dbml)
- [PostgreSQL schema](sql/schema.sql)
- [Sample queries](sql/queries.sql)
- [Sample data](sql/seed-data.sql)


## Setup 

```bash
    git clone https://github.com/cactus-commits/database-modeling-postgresql.git
    cp .env.example .env        # add your password
    docker compose up -d
    docker exec -i postgres psql -U postgres -d myh_db < sql/schema.sql
    docker exec -i postgres psql -U postgres -d myh_db < sql/seed-data.sql
```

To explore the database:

```bash
   docker exec -i postgres psql -U postgres -d myh_db < sql/seed-data.sql
```

## What's inside
15 tables in 3NF, with constraints, bridge tables for many-to-many relationships, sample data, and JOIN queries demonstrating the relationships.

_Part of my data engineering studies - first time going through the full ERD → schema → live database workflow._

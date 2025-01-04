# Data Modeling Setup

**Tech Stack**
- Git
- Postgres
- PSQL CLI
- Database management environment (DataGrip, DBeaver, VS Code with extensions, etc.)
- Docker, Docker Compose, and Docker Desktop

**Prerequisites**
- Install and setup docker-desktop

### 1. Run Postgres and PGAdmin in Docker
- clone the repo, open the terminal at Dimensional Data modelling
- Rename the `example.env` to `.env`
- Start the docker using `docker-compose up -d`

- In browser, open localhost:5050, this is where pgadmin is running from the config we gave in `.env` and `docker-compose.yaml`

### 2. Open PgAdmin
1. Right click -> Register server -> give name "Data Modeling"
2. Under connections,
    1. Give the host as container name of postgres which we defined in docker-compose.yaml. In my case it's `postgres`. it's not localhost
    2. username, password same as what we defined in `.env` file
    3. Save the connection.
3. navigate -> schemas -> tables -> actors -> view first 100 rows
4. Our Setup is done.

**Quick Commands**
- To Start containers in detached mode `docker-compose up -d`
- To Stop the containers `docker-compose stop`
- To Remove all stopped containers `docker container prune`


# prompt-eng-python
This Repo is an example to read and answer data from a PostgreSQL database table. This is not a dynamic question and answer prompt but rather answers based on the input present in the python file using 
Open API and python.


### Install Alpine 15 PostgreSQL
  - docker run --name postgres-server -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d postgres:15-alpine
  - docker exec -it imageName bash


### Run Postgresql Docker instance
	- docker run --name postgresql -e POSTGRES_PASSWORD=mysecretpassword -d postgres
 
### Login into Postgres insider Docker.
- psql -U postgres

### SQL
- CREATE TABLE test_user (user_id serial PRIMARY KEY,username VARCHAR ( 50 ) UNIQUE NOT NULL, address VARCHAR ( 300 ) UNIQUE NOT NULL)
- insert into test_user(username, address) values ('Brad', '24 th Street, Chicago, IA');
- insert into test_user(username,address) values ('John', '70th Street, Davenport, IA');

### Docker commands
* docker run -it --rm --network some-network postgres psql -h postgresql -U postgres
* docker run --name docker-server -e POSTGRES_PASSWORD=mysecretpassword -p 5432:5432 -d postgres
* docker run -it --rm --network some-network postgres psql -h postgres -U postgres -e POSTGRES_PASSWORD=mysecretpassword username postgres
* docker run --name postgres-server -e POSTGRES_PASSWORD=mysecretpassword -P 5432:5432 -d postgres:15-alpine

* docker run --name postgres-server -e POSTGRES_PASSWORD=mysecretpassword -e POSTGRES_USER=postgres -p 5432:5432 -d postgres:15-alpine

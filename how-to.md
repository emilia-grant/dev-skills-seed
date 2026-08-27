**Navigate the test db**
- `make test-database-up`
- `psql --username=boundary --host=localhost`
- connect to the test specific database
	- `\l` to list all db's, find the right one
	- `\c boundary_test_1234`
	- `\d` to show all tables
- `select * from the_table;` to show rows in a specific table

**Access the dev database**
- `psql --username=postgress --host=localhost --port=THE_PORT`
	- password is `password`

**Running boundary-local-env basics**
```bash
# Set BOUNDARY_IMAGE and BOUNDARY_LICENSE
# get a clean slate
podman stop $(podman ps -a -q) # Stop all containers
podman system prune # Remove all stopped containers

# Create the db container
podman compose up -d db
# initialize the database with test data
podman compose up db-init
# From the db-init output, copy the initial auth method password

# Run boundary
podman compose up -d boundary
```
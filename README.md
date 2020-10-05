# PostgreSQLdb_backup

<h4> Notes on using shell script </h4>

Manually run Shell script to install docker and initialize PostgreSQL db container with sample tablespace on CentOS

Once the PostgreSQL db container is deployed and initialized on the server. Install PostgreSQL client on the client system to fetch data from the DB -

Installing The Postgres 9.6 Client -

On Red-hat systems, use the following:

$ wget https://download.postgresql.org/pub/repos/yum/9.6/redhat/rhel-7-x86_64/pgdg-redhat-repo-latest.noarch.rpm <br />
$ sudo yum install -y pgdg-redhat-repo-latest.noarch.rpm <br />
$ sudo yum update -y <br />
$ sudo yum autoremove -y postgresql <br />
$ sudo yum install -y postgresql96 <br />

Test connection from Client
Let’s make sure that we can connect to the PostgreSQL server from our development machine by running the following command:

*Note: You’ll need to substitute in your database user’s values for [USERNAME], [PASSWORD], and [SERVER_IP]. <br />

$ psql postgres://[USERNAME]:[PASSWORD]@[SERVER_IP]:80/sample -c "SELECT count(id) FROM employees;"

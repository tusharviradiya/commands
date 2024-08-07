# commands

# postgres

#### installation
sudo apt update
sudo apt install postgresql postgresql-contrib
sudo systemctl start postgresql
sudo systemctl enable postgresql

#### for run postgres
psql -U postgres

#### database related command
create db : CREATE DATABASE monty_monitor;
delete db : DROP DATABASE mydatabase;
database list : \l 
switch database : \c newdatabase
create user : CREATE USER your_username WITH PASSWORD 'your_password';
grant permmistion : GRANT ALL PRIVILEGES ON DATABASE your_database_name TO your_username;
change owner : ALTER DATABASE your_database_name OWNER TO tushar;
login to psql : psql -d <db-name> -U <username> -W
table list of db : \dt

#### dump file 
create dump file : pg_dump -U your_username -F c -b -v -f "path_to_your_dump_file.backup" monty_ohm
import dump file : psql -U postgres -h localhost -d <db_name> < /<location>

#### connect to database direct from terminal
psql -U postgres -d mydatabase
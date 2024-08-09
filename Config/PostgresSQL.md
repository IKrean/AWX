
# ______________________________PostgresSQL______________________________

sudo systemctl status postgresql (checking postgresSQL status)
sudo -i -u postgres (switch on postgres user)
psql (opne console postgres)
\l (list of databases)
\q (exit)
\du (list of roles)
dropdb <name_database> (delete database)
ALTER USER <name_user> WITH PASSWORD '<new_password>'; (change password)
CREATE USER <name_user> WITH PASSWORD '<new_password>'; (create new user)
ALTER USER <name_user> WITH SUPERUSER: (grant superuser rights)
DROP USER <name_user>;
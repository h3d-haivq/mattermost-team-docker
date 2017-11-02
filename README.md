Mattermost Dockerize: Team Edition
---------------------------

This project enables deployment of a Mattermost server in a multi-node production configuration using Docker.

Notes:
 - The default Mattermost edition for this repo is Team Edition
 
You should configure it with following environment variables:
 - MM_USERNAME: database username
 - MM_PASSWORD: database password
 - MM_DBNAME: database name
 
If your database use some custom host and port, it is also possible to configure them :
 - DB_HOST: database host address
 - DB_PORT_NUMBER: database port

If you use a Mattermost configuration file on a different location than the default one (/mattermost/config/config.json) :
 - MM_CONFIG: configuration file location inside the container.

If you choose to use MySQL instead of PostgreSQL, you should set a different datasource and SQL driver :
- DB_PORT_NUMBER : 3306
- MM_SQLSETTINGS_DRIVERNAME : mysql
- MM_SQLSETTINGS_DATASOURCE : MM_USERNAME:MM_PASSWORD@tcp(DB_HOST:DB_PORT_NUMBER)/MM_DBNAME?charset=utf8mb4,utf8&readTimeout=30s&writeTimeout=30s"

Don't forget to replace all entries (beginning by MM_ and DB_) in MM_SQLSETTINGS_DATASOURCE with the real variables values.
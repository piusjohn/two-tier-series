MANUAL DEPLOYMENT (FLASKAPP & MYSQL)

1. INSTALL MYSQL
sudo apt-get update
sudo apt-get install mysql-server


2.CONFIGURE MYSQL 
sudo service mysql start
mysql -u root -p
-- install system dependencies
- sudo apt-get install -y build-essential python3-dev libmysqlclient-dev
- sudo apt-get install -y pkg-config

{CREATE DATABASE myDb;
USE myDb;

CREATE TABLE messages (
    id INT AUTO_INCREMENT PRIMARY KEY,
    message TEXT NOT NULL
);

CREATE USER 'admin'@'localhost' IDENTIFIED BY 'admin';
GRANT ALL PRIVILEGES ON myDb.* TO 'admin'@'localhost';
FLUSH PRIVILEGES;
}
3.install python and Dependencies
sudo apt-get install python3 python3-venv python3-pip
-Create and activate a virtual environment:
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
 pip install Flask flask-mysqldb
4. Configure flask Application
export MYSQL_HOST=localhost
export MYSQL_USER=admin
export MYSQL_PASSWORD=admin
export MYSQL_DB=myDb
5. python app.py

6.http://localhost:5000

# PROJECT-5
CLIENT -SERVER ARCHITECTURE USING MYSQL

1. Create and configure two Linux-based virtual servers (EC2 instances in AWS).
2. On mysql server Linux Server run (sudo apt update -y)
3. On mysql server Linux Server run (sudo spt install mysql-server -y)
4. Run (sudo systemctl enable mysql) to enable the mysql server
5. On mysql client Linux server run (sudo apt update -y ) to update ubuntu
6. On mysql client Linux server run (sudo apt install mysql-client -y) to install the client serveice
7. Input the private I.P of the mysql client linux server on the spaces povided when creating inbound rules for TCP port 3306  on mysql server securoty groups
8. We need to create a database on the the mysql- server,run command (sudo mysql_secure_installation), and set the passsword for root
9.Run (sudo mysql > CREATE USER 'remote_user'@'% IDENTIFIED WITH mysql_native_password BY 'Apple123!'
- mysql > CREATE DATABASE test_db;
- mysql > GRANT ALL ON test_db.* TO 'remote_user'@'%' WITH GRANT OPTION;
- mysql > FLUSH PRIVILEGES
- mysql >exit
10. Configure MySQL server to allow connections from remote hosts
(sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf), Replace ‘127.0.0.1’ to ‘0.0.0.0

11. Restart the mysql Service (sudo systemctl restart mysql)
12. From the mysql-client connect remotely to the mysql server database engine without using ssh (sudo mysql -u remote_user -h private I.P OF sever -p)
13. Check that we successfuly connected and can perfrom queries (Show databases;)

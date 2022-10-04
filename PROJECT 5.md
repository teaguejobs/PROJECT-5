**IMPLEMENT A CLIENT SERVER ARCHITECTURE USING MYSQL DATABASE MANAGEMENT SYSTEM (DBMS)**

- Create and configure two Linux-based virtual servers (EC2 instances in AWS).

- On mysql server Linux Server install MySQL Server software

- On mysql client Linux Server install MySQL Client software.

- MySQL server uses TCP port 3306 by default, so you will have to open it by creating a new entry in ‘Inbound rules’ in ‘mysql server’ Security Groups. For extra security, do not allow all IP addresses to reach your ‘mysql server’ – allow access only to the specific local IP address of your ‘mysql client’.
![tcp](./tcp%203306.PNG)

- Configure MySQL server to allow connections from remote hosts.
Replace ‘127.0.0.1’ to ‘0.0.0.0
![bind ip](./bind%20ip.PNG)

- From mysql client Linux Server connect remotely to mysql server Database Engine without using SSH. 
![remot](./login%20remote.PNG)

- Check that you have successfully connected to a remote MySQL server and can perform SQL queries:
![check](./test%20database.PNG)





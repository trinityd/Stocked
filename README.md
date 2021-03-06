# Stocked

![image](https://user-images.githubusercontent.com/23157710/147143133-84637b86-9846-46dd-b306-095a1a486354.png)


A web-based full stack stock chart and live chat program for Prof. Karra's Software Engineering course at SJSU. 

All updates to master will get automatically built and deployed using Github Actions, but the back end still needs to be ran locally so it's not very useful yet.

Build steps:

1. Install nodejs and npm if you don't already have them

2. In stocked-express-backend directory:
    - npm install
    - npm install -g nodemon
    - Potentially may need to do npm install cors on its own here
    - nodemon socket-server.js 

3. In stocked-client directory:
    - npm install
    - npm start

React page will be on localhost:3000/2021-fall-cs160-pied-piper

Nodemon will be using localhost:5001

4. A local MySQL server must also be running.
    - Follow the steps on the MySQL documentation to install and start MySQL: https://dev.mysql.com/doc/mysql-getting-started/en/
    - Open a terminal window and change directory to /2021-fall-cs160-pied-piper/stocked-express-backend/
    - Run the following command with your MySQL user credentials. Do not include the asterisks *. Put no spaces after the u/p as shown.
        ````
        mysql -u*yourusername* -p*yourpassword*  < build_db.sql
        ````
    - The database should be successfully built, along with a new user with privileges for the database.

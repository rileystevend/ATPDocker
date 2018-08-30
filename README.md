# ATPDocker
containerizing node.js apps with docker and Oracle Autonomous Database

Build docker images configured to run node.js apps on Oracle autonomous Databases.

To build a docker image, 

1. Clone repository to your local machine
2. Provision an Oracle Autonomous Transaction Processing (ATP) database in the Oracle Cloud. Download the credentials zip file
3. Unzip the database credentials zip file wallet_XXXXX.zip in the same folder as your Dockerfile
4. Create db user 'nodeuser' and grant create session
4. Install docker on your local machine if it doesn't exist
5. build Dockerfile - $docker build -t nodeapp .
6. Launch container mapping local port to 3050 -- $docker run -i -p 3050:3050 -t nodeapp
7. Launch browser on local m/c and check out app at http://localhost:3050

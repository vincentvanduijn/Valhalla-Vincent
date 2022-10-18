Project Valhalla
-


Introduction:
-

My final project in the Software Engineering traineeship of Devoteam. In the past months I learned a lot! Now we are combining the knowledge of the different checkpoints into one big project. Special thanks to Jens, my wingman. Kobe, Jesse, my dad and William and the many others who helped me start my journey of software development. 

We are going to access a scaled-up CRUD (create, read, update, delete) REST API microservice via an API gateway and store its data on a MySQL database server. We will have 4 docker images running at the same time. One for the MySQL database, one for the Keycloak security microservice, one for the EUREKA server to enable load-balancing, and the last one for the Spring Cloud API gateway. To easily manage the containers we'll use docker-compose.

Prerequisite:
- 
- You need to have Docker application(Windows, Mac or Linux) installed, please download it from the following URL: https://www.docker.com/products/docker-desktop/
- You need to have a working Java IDE installed on your machine, the code was written in Intelij IDEA Community Edition: https://www.jetbrains.com/idea/download/#section=windows
- You need to have the Java SE development Kit downloaded on your machine, the code was written in Java version 17: https://www.oracle.com/java/technologies/downloads/
- And finally the MySQL Workbench to access our database: https://dev.mysql.com/downloads/workbench/

How to start Valhalla:
-
Once you configured the project on your own device, the following steps are required to start Valhalla. First off, there is an .env.example file in the repository. Change the variables in the file to match the users and passwords you want to use for your version of the Valhalla project. Then remove the .example from the file, so the .env file will remain. 

Now the users and passwords are set, it's time to start the containers. Go to the terminal and run "docker compose up", this should be done in the main Valhalla-Vincent directory.  

After all 4 containers have booted, it's time to check out the different microservices.

- Keycloak - runs on localhost:8180
- EUREKA server - runs on localhost:8761
- Spring Cloud Gateway - runs on localhost:8080

Go to your preferred browser and type in the localhost address. When visiting localhost:8180 you will see the Keycloak admin dashboard. Log in with the chosen credentials from the .env file. You can see the security options after logging in.

When visiting localhost:8761, make sure to check out if the Keycloak and Spring Cloud Gateway are registerd as microservices in the EUREKA server instances board.

Finally, check out localhost:8080 for the Spring Cloud Gateway.



Docker Deployment

We put this application in a Docker container so it can run on any computer.

Getting the Image

You can download our image from Docker Hub. Just run this command:

docker pull david11577/employeetaskmanager-rest:1.0


Running the Application

To start the application in Docker, use this command:

docker run -d -p 8080:8080 --name employee-api david11577/employeetaskmanager-rest:1.0


After it starts, open your web browser and go to http://localhost:8080/swagger-ui.html to use the API.

Building Your Own Image

If you want to build the image yourself instead of downloading it, follow these steps.

First, build the JAR file:

./mvnw clean package -DskipTests


Next, build the Docker image:

docker build -t employeetaskmanager-rest:1.0 .


Then run it:

docker run -d -p 8080:8080 --name employee-api employeetaskmanager-rest:1.0


Stopping the Container

When you want to stop the application, run these commands:

docker stop employee-api
docker rm employee-api

# Simple java web app
This is a starter project for the third laboratory assignment on containerization.

## How to run
You will need [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/downloads/) and [Apache Maven](https://maven.apache.org/install.html) installed in order to compile this project.

Build the project with the following command:

```
mvn clean install
mvn package
```
When you have the project built, you can run it:
```
java -jar target/lab3-0.0.1-SNAPSHOT.jar
```
The server will start on [http://localhost:8080/hello](http://localhost:8080/hello)

You can whrite your name instead of "world":
[http://localhost:8080/hello?myName=your name](http://localhost:8080/hello)
  
When serving a project, press Ctrl+C to sent SIGTERM signal to the running server and bring it down.

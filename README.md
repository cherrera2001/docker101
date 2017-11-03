# docker101
Docker Training

To build the source

    mvn clean install

Copy the jetty-helloworld-webapp-1.0.jar to the /Docker directory

To build the docker image

    docker build -t sample_app .

To run the image in a container

    docker run -p 8080:8080 sample_app

Navigate to http://localhost:8080
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

Create Pod:

    kubectl create -f pod.yml

Forward Port:

     kubectl port-forward jetty-pod 7080:8080

Navigate to:

    http://localhost:7080

Delete the Pod:

    kubectl delete pod/jetty-pod

Create RC:

    kubectl create -f rc.yml

See if they are ready:

    kubectl get rc -o wide

Describe the pods:

    kubectl describe rc

Delete rc:

    kubectl delete replicationcontroller/rc-jetty-test


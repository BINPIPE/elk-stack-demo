Elasticsearch - Logstash - Kibana 
=================================

Building the ELK
---------------------
    $ git clone https://github.com/BINPIPE/elk-stack-demo.git
    $ cd elk-stack-demo

This demo assumes you know how to run Docker.
Run the below command before starting up the ELK cluster-  
```
sysctl -w vm.max_map_count=262144
```

Building the Containers
----------------------
Nothing special if you already have Docker installed:

    $ docker-compose build 

Running Containers with the docker-compose
---------------------
To run these containers:

    $ docker-compose up -d
    
Consuming Rest Service
---------------------
To consume SpringBoot app user service:

    $ curl http://localhost:8080/user/{userid}
    Eg. http://localhost:8080/user/90015

Normally, errors/warnings are logged, so a try a Bad Request status=400 url like http://localhost:8080/user/not-an-userid

To view generated logs on Kibana UI: [http://localhost:5601](http://localhost:5601)







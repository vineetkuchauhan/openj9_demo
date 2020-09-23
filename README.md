# openj9_demo

docker build -t petclinic-openjdk-hotspot .

docker build -t petclinic-openjdk-openj9 .

docker run --name hotspot -p 8080:8080 --rm petclinic-openjdk-hotspot

docker run --name openj9 -p 8089:8080 --rm petclinic-openjdk-openj9

RUN /bin/bash -c 'java -Xscmx50M -Xshareclasses -Xquickstart
        -jar spring-petclinic-2.3.0.BUILD-SNAPSHOT.jar &' ; sleep 20;
        ps aux | grep java | grep petclinic | awk '{print $2}' |
        xargs kill -1
CMD ["java", "-Xscmx50M", "-Xshareclasses", "-Xquickstart", "-jar", "spring-petclinic-2.3.0.BUILD-SNAPSHOT.jar"]

# openj9_demo

docker build -t petclinic-openjdk-hotspot .

docker build -t petclinic-openjdk-openj9 .

docker run --name hotspot -p 8080:8080 --rm petclinic-openjdk-hotspot

docker run --name openj9 -p 8089:8080 --rm petclinic-openjdk-openj9

# openj9_demo

docker build -t petclinic-openjdk-hotspot .

docker build -t petclinic-openjdk-openj9 .

docker run --name hotspot -p 8080:8080 --rm petclinic-openjdk-hotspot

docker run --name openj9 -p 8089:8080 --rm petclinic-openjdk-openj9

x-special/nautilus-clipboard
copy
file:///home/vineet/Pictures/Screenshot%20from%202020-09-23%2009-52-18.png

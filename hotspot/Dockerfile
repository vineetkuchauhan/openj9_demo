FROM adoptopenjdk/openjdk8

RUN apt-get update
RUN apt-get install -y\
	git \
	maven

WORKDIR /tmp

RUN git clone https://github.com/spring-projects/spring-petclinic.git

WORKDIR /tmp/spring-petclinic

RUN mvn install

WORKDIR /tmp/spring-petclinic/target

CMD ["java", "-jar", "spring-petclinic-2.3.0.BUILD-SNAPSHOT.jar"]


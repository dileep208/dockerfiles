FROM maven:3-openjdk-11 as builder
RUN git clone https://github.com/spring-projects/spring-petclinic.git \
	&& cd spring-petclinic \
	&& mvn package

FROM openjdk:11-slim
LABEL Author="Dileep"
COPY --from=builder /spring-petclinic/target/*.jar /spring-petclinic.jar
EXPOSE 8080
CMD ["java", "-jar", "/spring-petclinic.jar"]

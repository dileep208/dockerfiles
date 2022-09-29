FROM openjdk:11-slim
LABEL Author="Dileep"
LABEL Organisation="DileepDevOps"
ARG DOWNLOAD_URL
ADD ${DOWNLOAD_URL} /spring-petclinic.jar
EXPOSE 8080
CMD ["java", "-jar", "/spring-petclinic.jar"]

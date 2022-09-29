FROM maven:3-openjdk-8 as builder
RUN git clone https://github.com/wakaleo/game-of-life.git \
	&& cd game-of-life && mvn package

FROM tomcat:9-jdk8
COPY --from=builder /game-of-life/gameoflife-web/target/*.war /usr/local/tomcat/webapps/gameoflife.war
EXPOSE 8080

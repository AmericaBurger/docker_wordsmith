FROM ubuntu
COPY . .
RUN apt-get update -y && apt-get install maven openjdk-8-jdk -y && mvn verify
EXPOSE 8080
ENTRYPOINT bash -c "cd /target && java -Xmx8m -Xms8m -jar words.jar"
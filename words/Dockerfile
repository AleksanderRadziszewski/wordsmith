FROM maven:3.9.6-eclipse-temurin-8

COPY . /root

WORKDIR /root

RUN mvn verify

CMD java -jar ./target/words.jar


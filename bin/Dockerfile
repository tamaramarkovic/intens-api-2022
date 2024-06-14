# use "eclipse-temurin:8-jdk" as base
FROM eclipse-temurin:8-jdk

# create folder "intens" and use like working directory
WORKDIR /intens

# copy Maven config
COPY .mvn/ .mvn

# copy mvnw and pom.xml
COPY mvnw pom.xml ./

# download dependencies
RUN ./mvnw dependency:go-offline

# copy src
COPY src ./src

# set env port
ENV PORT=8080

# expose port
EXPOSE $PORT

# run app
CMD ["./mvnw", "spring-boot:run"]


FROM maven:3.8.8
WORKDIR /app
COPY pom.xml .
COPY src .
RUN mvn clean package -DskipTests -X
ENV CART_ENDPOINT=cart:8080 \
    DB_HOST=mysql
CMD [ "java", "-jar","shipping.jar"]
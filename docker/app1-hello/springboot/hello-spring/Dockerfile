# Usa una imagen base con Java 21 (JDK completo) de Eclipse Temurin (OpenJDK)
FROM eclipse-temurin:21-jdk

# Define el directorio de trabajo dentro del contenedor como /app
# Si no existe, Docker lo crea automáticamente
WORKDIR /app

# Copia el archivo .jar generado por Maven desde la carpeta target
# y lo renombra como app.jar dentro del contenedor
COPY target/*.jar app.jar

# Indica que la aplicación utiliza el puerto 8080
# (solo es informativo, no abre el puerto por sí mismo)
EXPOSE 8080

# Comando que se ejecuta al iniciar el contenedor
# Ejecuta la aplicación Java empaquetada en app.jar
# Equivale -> java -jar app.jar
CMD ["java","-jar","app.jar"]
# AdmDeLibros

#Libros: localhost:8080/AdministracionLibros/V1.0
#Autores: localhost:8080/AdministracionAutores/V1.0

Generar el War
mvn clean install
java -jar target/administracionlibros-1.0.1.ja

Docker
# Construir la imagen
docker build --tag=administracionlibros:1.0.1 .

# Ejecutar el contenedor
docker run -d --name administracionlibros --rm -p 8080:8080 administracionlibros:1.0.1

#Ver contenedores en ejecución
docker ps

#Detener ejecución de contenedor
docker stop administracionlibros

#Ver imagenes creadas
docker image ls

#Eliminar imagen
docker rmi administracionlibros:1.0.1


#Detener ejecucion del contenedor
docker stop administracionlibros

# Guardar imagen en archivo tar
docker save -o ARTEFACTOS/administracionlibros_1.0.1.tar administracionlibros:1.0.1



# Cargar imagen de archivo tar
docker load -i ARTEFACTOS/administracionlibros_1.0.1.tar

NOTA: Se pueden hacer pruebas del codigo en el ambiente local utilizando postman para los distintos metodos, siempre teniendo en cuenta el idLibro y idAutor asociados

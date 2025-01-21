# Proyecto Biblioteca API

Este proyecto es una aplicación Java para acceder a una biblioteca de libros utilizando una API externa y almacenar los datos obtenidos en una base de datos mediante JPA.

# Tecnologías utilizadas

- Java 17
- Spring Data JPA
- Jakarta Persistence API
- HTTP Client
- Gutendex API

# Descripción de las clases

-Modelo
-Autor
-Clase que representa un autor. Está mapeada a la tabla autores en la base de datos.

# Atributos:

-id: Identificador único del autor.
-nombre: Nombre del autor.
-fechaNacimiento: Año de nacimiento del autor.
-fechaFallecimiento: Año de fallecimiento del autor.
-libros: Lista de libros asociados al autor.

# Libro
-Clase que representa un libro. Está mapeada a la tabla libros en la base de datos.

# Atributos:

id: Identificador único del libro.
titulo: Título del libro.
idioma: Idioma del libro (como enumeración).
numeroDeDescargas: Número de descargas del libro.
autor: Relación con la clase Autor.

# Repositorio
-AutorRepository
Interfaz que extiende JpaRepository para interactuar con la base de datos de autores.

# Métodos personalizados:

obtenerAutorPorNombre(String nombre): Busca un autor por su nombre.

obtenerAutoresVivosEnAnio(int anio): Obtiene autores vivos en un año específico.

# API

PeticionAPI

Clase para realizar peticiones a la API externa Gutendex.

# Método destacado:

obtenerDatos(String titulo): Obtiene datos en formato JSON de un libro específico desde la API de Gutendex.

# Estructura del proyecto

src/main/java/com/alura/literalura/
├── api
│   └── PeticionAPI.java
├── model
│   ├── Autor.java
│   ├── Libro.java
├── repository
│   └── AutorRepository.java

# Instalación y uso

- Clona este repositorio.

- Configura una base de datos compatible con JPA.

- Asegúrate de tener acceso a la API externa de Gutendex.

- Ejecuta el proyecto desde tu entorno de desarrollo favorito.

# Ejemplo de uso

-Para buscar un libro, utiliza la clase PeticionAPI con el método obtenerDatos y procesa los datos obtenidos.
-Crea instancias de Libro y Autor para persistir información en la base de datos mediante JPA.

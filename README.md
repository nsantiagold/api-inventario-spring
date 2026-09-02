# 📦 API REST de Inventario

API REST desarrollada con **Java y Spring Boot** para administrar un inventario de productos. Implementa operaciones CRUD y persistencia en MySQL mediante Spring Data JPA.

## Funcionalidades

- Consultar todos los productos.
- Buscar un producto por su identificador.
- Registrar nuevos productos.
- Actualizar nombre, precio y existencias.
- Eliminar productos.
- Crear y actualizar automáticamente la tabla mediante JPA/Hibernate.

## Tecnologías

- Java 17
- Spring Boot
- Spring Web MVC
- Spring Data JPA
- MySQL
- Maven
- Lombok

## Modelo de producto

| Campo | Tipo | Descripción |
|---|---|---|
| `id` | Long | Identificador generado automáticamente |
| `name` | String | Nombre del producto |
| `price` | Double | Precio del producto |
| `stock` | Integer | Cantidad disponible |

## Endpoints

URL base: `http://localhost:8080/api/products`

| Método | Endpoint | Descripción |
|---|---|---|
| `GET` | `/api/products` | Obtiene todos los productos |
| `GET` | `/api/products/{id}` | Obtiene un producto por ID |
| `POST` | `/api/products` | Registra un producto |
| `PUT` | `/api/products/{id}` | Actualiza un producto |
| `DELETE` | `/api/products/{id}` | Elimina un producto |

### Ejemplo de solicitud

```json
{
  "name": "Teclado mecánico",
  "price": 1299.90,
  "stock": 15
}
```

## Ejecución local

### Requisitos

- Java 17
- MySQL
- Git
- Maven, o utilizar Maven Wrapper incluido en el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/nsantiagold/api-inventario-spring.git
cd api-inventario-spring/demo
```

### 2. Crear la base de datos

```sql
CREATE DATABASE inventario_db;
```

### 3. Configurar la conexión

Actualiza las credenciales locales en `src/main/resources/application.properties`:

```properties
server.port=8080
spring.datasource.url=jdbc:mysql://localhost:3306/inventario_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=TU_USUARIO
spring.datasource.password=TU_CONTRASENA
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

No publiques contraseñas reales ni archivos con credenciales sensibles.

### 4. Ejecutar la aplicación

En Windows:

```powershell
.\mvnw.cmd spring-boot:run
```

En Linux o macOS:

```bash
./mvnw spring-boot:run
```

También puedes ejecutarla desde IntelliJ IDEA utilizando la clase `DemoApplication`.

## Demostración

![Demostración de la API REST](demo/APIGIF.gif)

## Aprendizajes aplicados

Este proyecto permite practicar la creación de controladores REST, el mapeo de entidades con JPA, el uso de repositorios, la conexión con MySQL y la organización de un proyecto Backend con Maven.

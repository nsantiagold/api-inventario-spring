# 📦 API REST de Inventario - Backend (Spring Boot)

API REST desarrollada con **Java** y **Spring Boot** para la gestión de productos, diseñada con operaciones CRUD completas conectada a una base de datos relacional (MySQL).

## 🚀 Tecnologías utilizadas
* **Java** (Versión de tu JDK)
* **Spring Boot** (Web, Data JPA)
* **MySQL**
* **Maven**

## 🔌 Endpoints de la API (Endpoints principales)

| Método     | Endpoint                 | Descripción |
| :--- |       :--- |                   :--- |
| `GET` | `/api/products` | Obtiene la lista completa de productos. |
| `GET` | `/api/products/{id}` | Busca un producto específico por su ID. |
| `POST` | `/api/products` | Crea un nuevo producto. |
| `PUT` | `/api/products/{id}` | Actualiza un producto existente. |
| `DELETE` | `/api/products/{id}` | Elimina un producto por su ID. |

## 🛠️ Cómo ejecutar el proyecto localmente

1. Clona este repositorio:
   ```bash
   git clone [https://github.com/TU_USUARIO/TU_REPOSITORIO.git](https://github.com/TU_USUARIO/TU_REPOSITORIO.git)

2. Configura tu base de datos en src/main/resources/application.properties:
3. 
    spring.datasource.url=jdbc:mysql://localhost:3306/tu_base_de_datos
    spring.datasource.username=tu_usuario
    spring.datasource.password=tu_contraseña

4. Ejecuta la aplicación desde tu IDE favorito (IntelliJ IDEA) o usando Maven:
   
     mvn spring-boot:run

## 🎥 Demostración en funcionamiento

## 🎥 Demostración en funcionamiento

![Demo de la API REST](APIGIF.gif)

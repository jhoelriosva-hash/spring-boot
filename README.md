# Práctica 06 - Framework Spring (Proyecto: avicola)

**Universidad Politécnica Salesiana**  
**Asignatura:** Programación y Plataformas Web  
**Carrera:** Computación  

---

## 📋 Datos del Proyecto (Spring Starter Project)
* **Name:** `avicola`
* **Artifact:** `avicola`
* **Group:** `com.productos`
* **Package:** `com.productos.avicola`
* **Packaging:** `Jar`
* **Java Version:** `17`
* **Dependencias:**
  * `Spring Boot DevTools`
  * `Spring Web`
  * `Thymeleaf`

---

## 📁 Estructura del Proyecto

```text
avicola/
├── pom.xml
└── src/
    ├── main/
    │   ├── java/
    │   │   └── com/productos/avicola/
    │   │       ├── AvicolaApplication.java
    │   │       ├── controllers/
    │   │       │   ├── SaludoController.java
    │   │       │   ├── InformacionController.java
    │   │       │   ├── UsuarioController.java
    │   │       │   └── rest/
    │   │       │       ├── SaludoRestController.java
    │   │       │       └── UsuarioRestController.java
    │   │       └── model/
    │   │           └── Usuario.java
    │   └── resources/
    │       ├── application.properties
    │       ├── static/
    │       └── templates/
    │           ├── saludo.html
    │           ├── informacion.html
    │           └── gestionUsuarios.html
    └── test/
        └── java/
            └── com/productos/avicola/
                └── AvicolaApplicationTests.java
```

---

## 🚀 Endpoints y Rutas de Prueba

Una vez ejecutada la aplicación (`Run As -> Spring Boot App` o `mvn spring-boot:run`):

1. **Saludo Simple (Thymeleaf - Spring MVC):**
   * **URL:** `http://localhost:8080/saludo`
   * **Vista:** `saludo.html`
   * **Resultado:** Muestra `Servidor Activo!!`

2. **Información con Modelo (Thymeleaf - Spring MVC):**
   * **URL:** `http://localhost:8080/informacion`
   * **Vista:** `informacion.html`
   * **Resultado:** Muestra:
     * Datos del Servidor
     * APP Manejo Usuarios
     * localhost

3. **Gestión de Usuarios (MVC con Objeto y Bootstrap):**
   * **URL:** `http://localhost:8080/gestionUsuarios`
   * **Vista:** `gestionUsuarios.html`
   * **Resultado:** Lista estilizada con Bootstrap con los datos de Luis Terán.

4. **API Rest Saludo (RestController):**
   * **URL:** `http://localhost:8080/api/saludo`
   * **Resultado:** JSON:
     ```json
     {"mensaje": "Hola desde Spring Boot!"}
     ```

5. **API Rest Usuarios (RestController con Modelo):**
   * **URL:** `http://localhost:8080/api/v1/usuarios`
   * **Resultado:** JSON:
     ```json
     {
       "Usuario": {
         "id": 1,
         "perfil": 2,
         "ecivil": 1,
         "nombre": "Luis Teran",
         "cedula": "1714032587",
         "correo": "lteran@gmail.com",
         "clave": "lteran"
       }
     }
     ```

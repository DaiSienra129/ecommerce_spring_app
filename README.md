# 🛍 eCommerce Spring Boot API  

## 📌 Descripción  

Este proyecto es una API backend desarrollada en **Java con Spring Boot** para un sistema web de comercio electrónico. Permite la gestión de productos, usuarios, autenticación mediante **JWT**, carritos de compra y pedidos. Utiliza una base de datos **PostgreSQL** y se ejecuta en contenedores **Docker** para facilitar su despliegue.

El sistema se encuentra documentado mediante **Swagger UI** y actualmente no posee un frontend web incorporado, aunque está preparado para integrarse con uno en el futuro.

> 🔒 Este proyecto fue realizado de forma individual por **Daiana Sienra** como trabajo práctico de la materia **Programación Avanzada 2**. No se autoriza su uso ni distribución sin consentimiento.

---

## 🛠 Tecnologías  

- **Java 17** (Spring Boot)  
- **PostgreSQL**  
- **Hibernate ORM**  
- **JWT** (JSON Web Tokens para autenticación)  
- **Jakarta Validation** (validación de datos de entrada)  
- **Maven** (gestión de dependencias)  
- **Docker & Docker Compose** (contenedorización)  

---

## 🏛 Arquitectura  

La aplicación sigue el patrón **MVC (Modelo-Vista-Controlador)**, lo que permite una clara separación entre la lógica de negocio, los datos y la interfaz.

- **Modelos** persistidos con Hibernate.  
- **Controladores REST** para exposición de endpoints.  
- **Servicios** que contienen la lógica de negocio.  
- **Validaciones** de entrada implementadas con Jakarta Validation.  

---

## 🐳 Ejecución con Docker  

El proyecto incluye un script de configuración que automatiza la instalación y ejecución de todo el entorno.

### 🚀 Inicio rápido  

1. Clonar el repositorio:  
```sh
git clone https://github.com/DaiSienra129/ecommerce_spring_app.git
cd ecommerce_spring_app

```  

2️⃣ Hacer ejecutable el script de instalación:  
```sh
chmod +x setup.sh

```  

3️⃣ Ejecutar el script:  
```sh
./setup.sh
```  

El script:

Verifica e instala Maven, Docker y Docker Compose si es necesario.
Construye la aplicación con Maven.
Levanta los contenedores con docker-compose up --build.
Una vez finalizado, la API estará funcionando dentro de los contenedores Docker.
---

⚙️ Instalación manual

Requisitos
  Java 17
  Maven
  PostgreSQL
  
Pasos
1-**Clonar el repositorio:**
```sh
git clone https://github.com/DaiSienra129/ecommerce_spring_app.git
cd ecommerce_spring_app

```  

2- **Crear la base de datos:**  
```sh
psql -U postgres
CREATE DATABASE ecommerce;
\q
```  

3- **Configurar la conexión en el archivo application.properties:**  
Edit the `src/main/resources/application.properties` file:  
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/ecommerce
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña

```  

4- **Construir el proyecto:**  
```sh
mvn clean install
```  

5- **Ejecutar la aplicación:**  
```sh
mvn spring-boot:run
```  

---

🌐 Uso

Una vez que la aplicación está corriendo, podés acceder a la documentación interactiva desde:
📍 http://localhost:8080/swagger-ui.html

Desde allí podés probar los endpoints disponibles para autenticación, gestión de productos, carritos y pedidos.

---
🧩 Estructura del Proyecto

ecommerce_spring_app/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/daianasie...
│   │   └── resources/
│   │       └── application.properties
├── docker-compose.yml
├── Dockerfile
├── setup.sh
├── pom.xml
└── README.md


---

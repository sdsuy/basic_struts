# Basic Struts2 Web Application

Este proyecto sigue el tutorial oficial de Apache Struts 2:  
📚 [How to create a Struts2 Web Application](https://struts.apache.org/getting-started/how-to-create-a-struts2-web-application)

## 📦 Estructura del proyecto

Proyecto Maven tipo `war` con la siguiente estructura:

```
basic-struts2/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/
│   │   ├── resources/
│   │   └── webapp/
│   │       ├── index.jsp
│   │       └── WEB-INF/
│   │           └── web.xml
```

## ▶️ Ejecutar con Jetty

Asegurate de tener Maven instalado, luego ejecutá:

```bash
mvn jetty:run
```

Esto levanta Jetty en [http://localhost:8080](http://localhost:8080)

## ⚠️ Requisitos previos

- JDK 8 o superior
- Maven 3.6+
- Eclipse (opcional, usado como entorno)
- Java servlet API (es provista por Jetty)

## 🔀 Continuación del proyecto

Este proyecto continúa con el segundo tutorial oficial:  
📚 [Hello World using Struts2](https://struts.apache.org/getting-started/hello-world-using-struts2)

Para seguir el segundo tutorial, crear una nueva rama:

```bash
git checkout -b struts2-hello-world
```

Desde esa rama se implementará el `HelloWorldAction`, vistas JSP y la configuración de `struts.xml`.

---

© Apache Struts Documentation — adaptado al flujo Eclipse + Maven + Jetty.

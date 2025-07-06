# Basic Struts2 Web Application

Este proyecto sigue los **tutoriales oficiales de Apache Struts 2**:

1. 📚 [How to create a Struts2 Web Application](https://struts.apache.org/getting-started/how-to-create-a-struts2-web-application)
2. 📚 [Hello World using Struts2](https://struts.apache.org/getting-started/hello-world-using-struts2)

---

## 📦 Estructura del proyecto

Proyecto Maven tipo `war` con la siguiente estructura:

```
basic-struts2/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/org/apache/struts/helloworld/action/HelloWorldAction.java
│   │   ├── java/org/apache/struts/helloworld/model/MessageStore.java
│   │   ├── resources/struts.xml
│   │   ├── resources/log4j2.xml
│   │   └── webapp/
│   │       ├── index.jsp
│   │       ├── HelloWorld.jsp
│   │       └── WEB-INF/web.xml
```

---

## ▶️ Ejecutar con Jetty

Asegurate de tener Maven instalado, luego ejecutá:

```bash
mvn jetty:run
```

Esto levanta Jetty en [http://localhost:8080](http://localhost:8080)

Accedé a la acción:

```
http://localhost:8080/hello
```

---

## ✅ Segunda parte: Hello World Action

Se agregó una clase `HelloWorldAction` y la vista `hello.jsp`. Esto permite enviar un formulario con tu nombre y recibir una respuesta dinámica.

---

## ⚙️ ¿Cómo funciona el código?

1. El navegador solicita la URL: `http://localhost:8080/hello.action`
2. El servidor redirige la petición a `StrutsPrepareAndExecuteFilter`, según está configurado en `web.xml`.
3. Este filtro busca en el archivo `struts.xml` una acción llamada `hello`, y encuentra que se corresponde con la clase `HelloWorldAction`.
4. El framework instancia esa clase y ejecuta el método `execute()`.
5. El método retorna `SUCCESS`, y Struts consulta el `struts.xml` para saber qué vista debe renderizarse cuando se retorna `success`.
6. Se carga `hello.jsp`.
7. La página JSP puede usar etiquetas Struts como `<s:property>` para acceder a datos del `Action`.
8. El servidor genera una respuesta HTML completa y la envía al navegador.

---

## 📌 Qué recordar

- Las clases `Action` procesan formularios HTML y devuelven un resultado como `SUCCESS`, `ERROR` o `INPUT`.
- El archivo `struts.xml` define qué hacer en cada caso (mostrar una página, redirigir a otra acción, etc.).
- Las páginas `.jsp` usan etiquetas Struts (`<s:...>`) para mostrar datos dinámicos enviados por el `Action`.

---

## 🔀 Siguiente paso

Este proyecto puede extenderse con más acciones, validaciones, o integración con bases de datos.

---

© Apache Struts Documentation — adaptado al flujo Eclipse + Maven + Jetty.

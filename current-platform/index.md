---
currentMenu: current_platform
---

# Plataforma Actual de PUF Travel
Actualmente se conforma por dos principales proyectos, un proyecto para toda la interfaz WEB y otro para el API. Procederemos a detallar de cada uno lo siguiente:

<i class="fa fa-network-wired"></i> Tecnología (Technology)<br />
<i class="fab fa-symfony"></i> Framework<br />
<i class="fa fa-hand-peace"></i> Buenas prácticas (Best Practices)<br />
<i class="fa fa-code"></i> Coding Style <br />
<i class="fa fa-swatchbook"></i> Patrones de Diseño (Design Patterns)<br />
<i class="fa fa-box-open"></i> Arquitectura de Software (Software Architecture)<br />
<i class="fa fa-project-diagram"></i> Infraestructura (Infrastructure)<br />
<i class="fab fa-git"></i> Git Flow Development (Flujo de Desarrollo GIT)

<br />

### WEB
<hr />

#### Tecnologías:
- **Lenguaje:** PHP 7.3.x
- **Base de Datos:** MySQL 5.7
- **Sistema de Colas:** Beanstalkd
- **Cache:** Memcached
- **Frontend:** Vue.js, Stylus, CSS

#### Framework:
- Laravael v5.7 + Vue.js

### Buenas Prácticas:
- Escasas, de hecho no se implementan las buenas prácticas oficiales del Framework.

### Coding Style:
- Inexistente, no hay reglas de identación, no se respetan espaciados entre metodos, entre muchos otros errores más.

### Patrones de Diseño (Design Patterns):
- Se utilizan los por defecto del Framework.

### Arquitectura de Software (Software Architecture):
- Se utiliza la por defecto del Framework.

### Infraestructura (Infrastructure):
- Se utiliza una instancia de AWS para el despliegue del proyecto.

### Git Flow Development (Flujo de Desarrollo GIT):
- Ninguno, no se implementa en lo absoluto un GIT Flow para garantizar consistencia en los repositorios de código y sobre todo brindar seguridad en cada release y poder facilmente hacer reverts en producción. No hay control de versiones en el código.

<br />
### API
<hr />

#### Tecnologías:
- **Lenguaje:** PHP 7.3.x
- **Base de Datos:** MySQL 5.7
- **Sistema de Colas:** Beanstalkd
- **Cache:** Memcached

#### Framework:
- Laravael v5.7 + Apiato.io

### Buenas Prácticas:
- Escasas, de hecho no se implementan las buenas prácticas oficiales del Framework. Se implementan las de un tercero --> Apiato.io

### Coding Style:
- Inexistente, no hay reglas de identación, no se respetan espaciados entre metodos, entre muchos otros errores más.

### Patrones de Diseño (Design Patterns):
- Se utilizan los propuestos por un tercero --> Apiato.io

### Arquitectura de Software (Software Architecture):
- Se utiliza la por defecto del Framework más los propuestos por un tercero --> Apiato.io

### Infraestructura (Infrastructure):
- Se utiliza una instancia de AWS para el despliegue del proyecto.

### Git Flow Development (Flujo de Desarrollo GIT):
- Ninguno, no se implementa en lo absoluto un GIT Flow para garantizar consistencia en los repositorios de código y sobre todo brindar seguridad en cada release y poder facilmente hacer reverts en producción. No hay control de versiones en el código.

### Diagrama de la Infrastructura y Arquitectura de Software Actual
<br />
![](/assets/images/diagrams/current_architecture.png)
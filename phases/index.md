---
currentMenu: phases
---

## DEFINICIÓN DE REFACTORING RECOMENDADO

Luego de la revisión exhaustiva de la plataforma actual, en específico del proyecto para la web (frontend) y el proyecto para el API (Backend) se recomienda realizar un refactoring de ambos proyectos. Un refactoring se refiere a la reescritura de un software desde cero pero manteniendo el know-how actual y lógicas de negocio existentes.

En principio lo deseable de este refactoring para cada proyecto se detalla a continuación:
<br/><br/>
- **CARGAR WEB DIRECTAMENTE DESDE EL MOTOR DE VUE.JS**: Para el proyecto de la web, se recomienda que la carga de la SPA (Single Page Application), en este caso, elaborada con el framework de Javascript Vue.js, se haga con el motor directamente de Vue.js y no desde una plantilla de Laravel, esto ayudaría significativamente en el rendimiento y optimización de la web.
<br/><br/>
- **ELIMINAR API EN PROYECTO WEB**: Actualmente existe un API dentro del proyecto WEB en Laravel para servir al frontend de rutas internas las cuales posteriormente realizan autenticación contra el proyecto del API y redirigen nuevamente una petición al API para extraer los datos finales. No logro entender el porque se usaron 2 API para la definición de la arquitectura de Software. El API es la pieza fundamental que provee de los datos y validaciones necesarias al frontend. En este caso, el API se dividio en dos proyectos monolíticos lo cual no tiene sentido. Si se estuviese tratando de un API dividido en microservicios, la cosa sería diferente ya que por la naturaleza de este concepto, cada microservicio cumplirá una única responsabilidad. Para eliminar el API existente en el proyecto web, basta con eliminar la llamada al API interno y hacerlo sobre el API principal.
<br/><br/>
- **REFACTORIZAR EL API**: El API actual esta escrito usando el framework **Laravel** con una capa por encima llamada **Apiato.io**. Para este punto recomiendo realizar una reescritura de cada endpoint o ruta del API en un proyecto mas robusto, usando el framework **Symfony** en su última versión e implementando internamente una **arquitectura hexagonal** en conjunto con **Domain Driven Design (DDD)**, lo cual garantiza un desacople de la lógica de dominio y negocio, del framework propiamente permitiendo a futuro que si es requerido migrar a otro framework, el trabajo se haga de forma simple y rápida.
<br/><br/>
- **IMPLEMENTAR GIT FLOW**: Es necesario establecer un git flow para todo el proceso de desarrollo lo cual permita manejar versionamiento de software mediante los tags de git para poder desplegar en función de versiones y poder mantener un punto de comparación entre los cambios de la versión en producción y los cambios nuevos a implementar, de modo que si algo falla, se pueda o bien hacer un hotfix o en su defecto volver fácilmente a una versión anterior. Actualmente como se viene trabajando, es prácticamente imposible.
<br/><br/>

Para los refactoring previamente definidos, se establecen las siguientes fases:

## FASE I:
- IMPLEMENTAR GIT FLOW
- REFACTORIZAR EL API

## FASE II:
- ELIMINAR API EN PROYECTO WEB

## FASE III:
- CARGAR WEB DIRECTAMENTE DESDE EL MOTOR DE VUE.JS
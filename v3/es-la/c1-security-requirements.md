---

layout: col-document
tags: OWASP Top Ten Controles Proactivos 2018, C1
document: OWASP Top Ten Controles Proactivos 2018
order: 5

---

# C1: Definir Requisitos de Seguridad 

## Descripción

Un requisito de seguridad es una declaración de la funcionalidad de seguridad necesaria que garantiza que se satisfaga una de las muchas propiedades de seguridad diferentes del software. Los requisitos de seguridad se derivan de los estándares de la industria, las leyes aplicables y un historial de vulnerabilidades pasadas. Los requisitos de seguridad definen nuevas características o adiciones a las características existentes para resolver un problema de seguridad específico o eliminar una vulnerabilidad potencial.

Los requisitos de seguridad proporcionan una base para la funcionalidad de seguridad examinada de una aplicación. En lugar de crear un enfoque personalizado de seguridad para cada aplicación, los requisitos de seguridad estándar permiten a los desarrolladores reutilizar la definición de controles de seguridad y mejores prácticas. Esos mismos requisitos de seguridad examinados brindan soluciones para problemas de seguridad que ocurrieron en el pasado. Los requisitos existen para evitar repetir fallas de seguridad del pasado.

### El OWASP ASVS

El [Estándar de Verificación de Seguridad en Aplicaciones (ASVS, por sus siglas en inglés)](https://owasp.org/www-project-application-security-verification-standard/) es un catálogo existente de requisitos de seguridad y criterios de verificación. OWASP ASVS puede ser una fuente de requisitos de seguridad detallados para los equipos de desarrollo.

Los requisitos de seguridad se clasifican en diferentes categorías según una función de seguridad de orden superior compartida. Por ejemplo, el ASVS contiene categorías como autenticación, control de acceso, manejo/registro de errores y servicios web. Cada categoría contiene una colección de requisitos que representan las mejores prácticas para esa categoría redactadas como declaraciones verificables.

### Aumento de los requisitos con historias de usuarios y casos de uso indebido

Los requisitos de ASVS son declaraciones básicas verificables que se pueden ampliar con historias de usuarios y casos de uso indebido. La ventaja de una historia de usuario o un caso de uso indebido es que vincula la aplicación exactamente con lo que el usuario o atacante le hace al sistema, en lugar de describir lo que el sistema ofrece al usuario.

Este es un ejemplo de cómo expandir un requisito de ASVS 3.0.1. De la sección "Requisitos de verificación de autenticación" de ASVS 3.0.1, el requisito 2.19 se centra en las contraseñas por defecto.

    2.19 Verifique que no haya contraseñas por defecto en uso para el marco de trabajo de la aplicación o cualquier componente utilizado por la aplicación (como "admin/contraseña").

Este requisito contiene una acción para verificar que no existan contraseñas predeterminadas y también lleva consigo la guía de que no se deben usar contraseñas predeterminadas dentro de la aplicación.

Una historia de usuario se centra en la perspectiva del usuario, administrador o atacante del sistema y describe la funcionalidad en función de lo que el usuario quiere que el sistema haga por él. Una historia de usuario toma la forma de "Como usuario, puedo hacer a, b y c".

    Como usuario, puedo ingresar mi nombre de usuario y contraseña para acceder a la aplicación.
    Como usuario, puedo ingresar una contraseña larga que tenga un máximo de 1023 caracteres.

Cuando la historia se centra en el atacante y sus acciones, se habla de un caso de uso indebido.

    Como atacante, puedo ingresar un nombre de usuario y una contraseña predeterminados para obtener acceso.

Esta historia contiene el mismo mensaje que el requisito tradicional de ASVS, con detalles adicionales del usuario o del atacante para ayudar a que el requisito sea más verificable.

## Implementación

El uso exitoso de los requisitos de seguridad implica cuatro pasos. El proceso incluye descubrir/seleccionar, documentar, implementar y luego confirmar la implementación correcta de nuevas funciones y funciones de seguridad dentro de una aplicación.

### Descubrimiento y Selección

El proceso comienza con el descubrimiento y la selección de los requisitos de seguridad. En esta fase, el desarrollador comprende los requisitos de seguridad de una fuente estándar como ASVS y elige qué requisitos incluir para una versión determinada de una aplicación. El objetivo del descubrimiento y la selección es elegir una cantidad manejable de requisitos de seguridad para esta versión o sprint, y luego continuar iterando para cada sprint, agregando más funciones de seguridad con el tiempo.

### Investigación y Documentación

Durante la investigación y la documentación, el desarrollador revisa la aplicación existente con respecto al nuevo conjunto de requisitos de seguridad para determinar si la aplicación actualmente cumple con el requisito o si se requiere algún desarrollo. Esta investigación culmina con la documentación de los resultados de la revisión.

### Implementación

Una vez que se determina la necesidad de desarrollo, el desarrollador ahora debe modificar la aplicación de alguna manera para agregar la nueva funcionalidad o eliminar una opción insegura. En esta fase, el desarrollador primero determina el diseño requerido para abordar el requisito y luego completa los cambios de código para cumplir con el requisito.

### Prueba

Se deben crear casos de prueba para confirmar la existencia de la nueva funcionalidad o refutar la existencia de una opción previamente insegura.

## Vulnerabilidades Prevenidas

Los requisitos de seguridad definen la funcionalidad de seguridad de una aplicación. Una mejor seguridad incorporada desde el comienzo del ciclo de vida de una aplicación da como resultado la prevención de muchos tipos de vulnerabilidades.

## Referencias

* [Estándar de Verificación de Seguridad en Aplicaciones (ASVS, por sus siglas en inglés)](https://owasp.org/www-project-application-security-verification-standard/)
* [OWASP Estándar de Verificación de Seguridad en Aplicaciones Móviles (MASVS, por sus siglas en inglés)](https://owasp.org/www-project-mobile-security-testing-guide/)
* [OWASP Top Ten](https://owasp.org/Top10/)

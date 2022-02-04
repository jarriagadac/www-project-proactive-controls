---

layout: col-document
tags: OWASP Top Ten Controles Proactivos 2018, C2
document: OWASP Top Ten Controles Proactivos 2018
order: 6

---
# C2: Aprovechar la Seguridad de Frameworks y Librerías

## Descripción

Las librerías de codificación segura y los marcos de trabajo de software con seguridad embebida ayudan a los desarrolladores de software a protegerse contra fallas de diseño e implementación relacionadas con la seguridad. Un desarrollador que escribe una aplicación desde cero podría no tener suficiente conocimiento, tiempo o presupuesto para implementar o mantener correctamente las funciones de seguridad. Aprovechar la seguridad en los marcos de trabajo ayuda a lograr los objetivos de seguridad de manera más eficiente y precisa.

## Buenas Prácticas de Implementación

Al incorporar bibliotecas o marcos de trabajo de terceros en su software, es importante tener en cuenta las siguientes buenas prácticas:

1. Use librerías y marcos de trabajo de fuentes confiables que se mantienen activamente y son ampliamente utilizados por muchas aplicaciones.
2. Cree y mantenga un inventario de todas las librerías de terceros.
3. Mantenga actualizadas de forma proactiva las bibliotecas y los componentes. Use una herramienta como [Comprobador de Dependencias de OWASP](https://owasp.org/www-project-dependency-check/) y [Retire.JS](https://retirejs.github.io/retire.js/) para identificar las dependencias del proyecto y comprobar si hay vulnerabilidades conocidas y divulgadas públicamente para todos los códigos de terceros.
4. Reduzca la superficie de ataque encapsulando la biblioteca y exponga solo el comportamiento requerido en su software.

### Vulnerabilidades Prevenidas

Las librerías de codificación segura y los marcos de trabajo de software con seguridad embebida pueden ayudar a prevenir una amplia gama de vulnerabilidades en las aplicaciones web. Es fundamental mantener actualizados estos marcos de trabajo y librerías, tal como se describe en [usar componentes con vulnerabilidades conocidas [Diez Riesgos Principales de 2017] (https://owasp.org/www-project-top-ten/).

## Herramientas

* [Comprobador de Dependencias de OWASP](https://owasp.org/www-project-dependency-check/) - identifica las dependencias del proyecto y verifica las vulnerabilidades divulgadas públicamente
* [Retire.JS](http://retirejs.github.io/retire.js/) escáner para librerías de JavaScript

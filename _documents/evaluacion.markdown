---
title: Evaluación técnica
spdx-id: evaluacion
nickname: Evaluación
redirect_from: /documents/evaluacion
source: 
lang: es

description: Una herramienta digital desarrollada con calidad técnica facilita el mantenimiento y reusabilidad de la misma. Las condiciones necesarias especificadas a continuación sirven como lineamientos generales a la hora de desarrollar código. Las condiciones ideales serán útiles si quieres hacer una evaluación de la calidad del código.  

requirements:
- Crea módulos cortos documentados
- Optimiza las líneas de código
- Crea una arquitectura de componentes ordenada y balanceada
- Evita duplicación de código
- Automatiza los test de cobertura 

expected:
- Ausencia de fallos estructurales
- Menos del 25% de líneas duplicadas
- Menos de 10 problemas críticos
- Más del 50% de clases, interfaces y métodos documentados
- Deuda técnica menor a 30 días
- Cobertura de test más del 25%

sidebar: La evaluación técnica de la herramienta permite mantener la calidad del código y e incrementar sus posibilidades de uso, reutilización y adaptación. 

note: Las herramienta digitales del BID publicadas en Código para el Desarrollo deben cumplir con los requerimientos deseables. (Más información aquí)

links:
- <a href="https://github.com/EL-BID/Codigo-para-el-desarrollo/wiki/sonarqube.org">SonarQube </a>

---

*Las herramienta digitales del BID publicadas en Código para el Desarrollo deben cumplir con los requerimientos deseables. (Más información [aquí](https://el-bid.github.io/guia-de-publicacion/documents/pages/guia/))*

## ¿Qué es la calidad técnica de una herramienta digital?

La calidad técnica de una herramienta digital se establece en la medida en que la escritura del código fuente y la arquitectura de la herramienta digital esté libre de fallos estructurales que puedan bloquear su uso o reutilización y que además faciliten la comprensión en la lectura y modificación del Código Fuente.

## ¿Qué características técnicas principales definen la calidad de una herramienta digital?
las siguientes características son variables que dependen del contexto y el propsósito de la herramienta digital.

* **Flexibilidad**
Deberá ser capaz de funcionar de forma completa y adecuada sin depender de licenciamientos forzosos de ningún tipo de componente adicional.

* **Portabilidad** 
Deberá ser capaz de funcionar de forma completa y adecuada en distintos sistemas operativos, especialmente en aquellos que no implican costos adicionales de licenciamiento y que cuentan con actualizaciones periódicas de seguridad de forma gratuita, por ejemplo: algunas distribuciones de Linux y/o sistemas BSD.

* **Escalabilidad**
Deberá contar con documentación, reportes y/o herramientas que permitan determinar de forma adecuada los costos y consideraciones asociados al escalamiento de la solución.

* **Interoperabilidad**
Deberá contar con al menos un mecanismo que permita la interconexión e interoperabilidad con distintos sistemas existentes y futuros, por ejemplo: API, RPC, SDK, etc.

* **Licenciamiento**
Deberá estar publicada bajo un esquema de licenciamiento que permita su despliegue y utilización en distintos contextos y casos de uso.
para más información sobre el licenciamiento de tu herramienta visita la sección 

## ¿Qué es la integración continua de código?

La integración continua es una práctica de desarrollo de software donde los miembros de un equipo integran su trabajo con frecuencia, por lo general cada persona se integra al menos diariamente, lo que lleva a integraciones múltiples por día. Cada integración se verifica mediante una compilación automatizada (incluida la prueba) para detectar errores de integración lo más rápido posible. 

## ¿Por qué es importante la integración continua de código?

Muchos equipos encuentran que este enfoque conduce a la reducción de problemas de integración significativamente y permite a un equipo desarrollar software cohesivo más rápidamente. 

Para leer más sobre este tema te recomendamos que visites la web de Martin Fowler https://www.martinfowler.com/, quien propuso el modelo.

## ¿Qué herramientas de integración continua de código recomendamos?

Existen muchas herramientas de integración continua, en esta guía te recomendamos dos:

* **Travis CI**
Es un servicio de integración continua alojado y distribuido utilizado para probar proyectos de software alojados en GitHub.
Los proyectos de código abierto se pueden probar sin cargo a través en travis-ci.org y los proyectos privados se pueden probar en travis-ci.com con cargo. 
https://travis-ci.org/

Si lo que quieres es configurar travis en tu proyecto de github, empieza por aquí:
https://docs.travis-ci.com/user/languages

* **Jenkins**
es un software de Integración continua open source escrito en Java. Está basado en el proyecto Hudson y es, dependiendo de la visión, un fork del proyecto o simplemente un cambio de nombre.

Jenkins proporciona integración continua para el desarrollo de software. Es un sistema corriendo en un servidor que es un contenedor de servlets, como Apache Tomcat. Soporta herramientas de control de versiones como CVS, Subversion, Git, Mercurial, Perforce y Clearcase y puede ejecutar proyectos basados en Apache Ant y Apache Maven, así como scripts de shell y programas batch de Windows. 
https://jenkins.io/

en ambos casos se debe configurar los builds, que son los paquetes que necesitas para ejecutar un reporte de calidad técnica.

## ¿Cómo generar reportes de calidad técnica?

A través de un análisis de código estático. Este análisis evalúa la comprensión del código a través del estilo de programación, la arquitectura y la documentación del propio código (líneas de código comentadas). 

**SonarQube** es una de las herramientas que permiten llevar un control de la calidad de código a medida que se desarolla. 


## ¿Qué herramientas existen para evaluar la calidad del código?

Existen muchas herramientas y cada una evalúa métricas distintas. Aquí destacamos dos:
* **Sonaqube** es una herramienta de uso gratuíto. Podrás evaluar la calidad del código a un nivel de detalle muy granular. Te permite identificar exactamente los errores y las líneas de código que puedes mejorar. Para configurar la herramienta es necesario disponer de un repositorio en Github o Bitbucket y que conozcas:
  * Los requisitos del sistema operativo para la compilación (versiones específicas de librerías, software de gestión de paquetes y dependencias, SDKs y compiladores, etc.).
  * Las dependencias propias del proyecto, tanto externas como internas (orden de compilación de sub-módulos, configuración de ubicación de librerías dinámicas, etc.).
  * Los pasos específicos para la compilación del código fuente y ejecución de tests unitarios en caso de que el proyecto disponga de ellos.

* **[Better Code Hub](https://bettercodehub.com/)** también es de uso gratuíto y evalúa de manera más general la calidad del código. La configuración requerida es menos compleja, pero los resultados son más generales que con Sonarqube.   

## ¿Cuáles son las métricas más comunes para evaluar la calidad técnica?

Aunque existen muchas métricas que varían según la herramienta que se usa, la más comunes son:
* **Blocker Issues:**
Número de problemas en la escritura del código con severidad alta. Estos problemas pueden ser operacionales o de seguridad que pueden hacer la herramienta digital inestable en producción.

* **Duplicated lines:**
Número de líneas duplicadas en el código.

* **Critical Issues:**
Número de problemas en la escritura del código con severidad crítica. Estos problema pueden ocasionar comportamientos inesperados de la herramienta en producción sin impactar en la integridad de la herramienta completa.

* **Public documented API:**
Número de clases, funciones y propiedades documentadas.

* **Technical debt:**
Esfuerzo necesario para solucionar todos los problemas en la base del código. Se mide en días de trabajo y es una métrica que calcula el sistema de SonarQube.

* **Technical debt ratio:**
Diferencia entre el coste de desarrollar la herramienta digital y el coste de solucionar sus problemas. 

* **Test coverage:**
Porcentaje del código que ha sido testeado. 

En [esta página](https://docs.sonarqube.org/display/SONAR/Metric+Definitions) podrás encontrar más información de cada uno de los indicadores que utiliza SonarQube. En la [Guía de Publicación](https://el-bid.github.io/guia-de-publicacion/documents/pages/guia/) puedes ver una tabla con el rubro de evaluación usado en el BID.





## ¿Cómo se desarrolla software para que tenga fácil mantenimiento?

Existe mucha documentación sobre cómo desarrollar software. Esta cubre temas que van desde la arquitectura hasta las tecnologías que se usan. En esta guía mencionamos los 10 lineamientos obtenidos del *Software Improvement Group's industry benchmark*, que están definidos en el libro *[Building Maintainable Software, Java Edition - Ten Guidelines for Future-Proof Code](http://shop.oreilly.com/product/0636920049159.do)*

* **Escribir unidades cortas de código**: Las unidades cortas son más fáciles de entender.

* **Escribe unidades simples de código**: Las unidades simples son más fáciles de probar.

* **Escribe el código una vez**: El código duplicado significa errores duplicados y duplicación de cambios.

* **Mantener las interfaces de la unidad pequeñas**: Las unidades con interfaces pequeñas son más fáciles de reutilizar.

* **Distintas responsabilidades separadas en módulos distintos**: Los módulos con una sola responsabilidad son más fáciles de cambiar.

* **Pareja de componentes de arquitectura sin apretar**: Los componentes independientes se pueden mantener aislados.

* **Mantener los componentes de arquitectura equilibrados**: Una arquitectura equilibrada hace que sea más fácil encontrar su camino.

* **Mantenga su base de código pequeña**: Una pequeña base de código requiere menos esfuerzo para mantener.

* **Automatice las pruebas**: Las pruebas automatizadas son repetibles y ayudan a prevenir errores.

* **Escribir código limpio**: "Deja el campamento más limpio de lo que lo encontraste".




## ¿Cuáles son los requerimientos técnicos para publicar herramientas digitales del BID?

Para publicar herramientas digitales del BID en Código para el Desarrollo es necesario que la herramienta cumpla con los requerimientos deseables. Puedes consultar más información en la [Guía de Publicación del BID](https://el-bid.github.io/guia-de-publicacion/documents/pages/guia/).

<style> .ocultar_breadcrumb_ingles{ display:none; } .ocultar_home_ingles{ display:none; } </style>

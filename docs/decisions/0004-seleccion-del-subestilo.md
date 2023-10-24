# Seleccion-del-subestilo

* Status: accepted
* Deciders: Miguel, Sergio
* Date: 2023-10-24

## Context and Problem Statement

En el contexto de nuestro proyecto de desarrollo de software, hemos decidido adoptar un subestilo basado en microservicios para el sistema.

## Decision Drivers

* RF-10 Información del pedido
* RF-05 Permitir realizar pedidos
* RF-06 Establecer intentos para realizar pedidos
* RF-12 Sistema de reporte de incidencias

## Considered Options

* 0004-1 Microservicios
* 0004-2 Cliente-Servidor

## Decision Outcome

Chosen option: "0004-1 Microservicios", because resuelve los problemas dados con la realización de pedidos y el reporte de incidencias

## Pros and Cons of the Options

### 0004-1 Microservicios

Los microservicios son pequeños e independientes, y están acoplados de forma imprecisa.

* Good, because Permite trabajar con diferentes funcionalidades del sistema
* Good, because Un microservicio es autónomo e independiente por lo que resulta más fácil administrar las correcciones de errores
* Good, because Permite escalar horizontalmente los subsistemas que requieren más recursos, sin tener que escalar horizontalmente toda la aplicación
* Bad, because El sistema como un todo es más complejo
* Bad, because La latencia adicional puede constituir un problema

### 0004-2 Cliente-Servidor

Es un modelo de diseño software en el que el cliente interactúa directamente con el servidor.

* Good, because Los servidores pueden implementar medidas de seguridad avanzadas
* Good, because La lógica del negocio y los datos se almacenan y gestionan en un servidor centralizado, como la base de datos del problema
* Bad, because Configurar y mantener los servidores puede ser costoso
* Bad, because La dependecia de la red en esta arquitectura crea varios problemas con la utilización de la aplicación

## Links

* https://learn.microsoft.com/es-es/azure/architecture/guide/architecture-styles/microservices

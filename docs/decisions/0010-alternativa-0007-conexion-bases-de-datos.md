# Alternativa-0007-Conexion-bases-de-datos

* Status: accepted
* Deciders: Miguel
* Date: 2023-11-07

## Context and Problem Statement

Nuestro sistema software debera poder acceder a dos bases de datos, una donde se almacena los datos de los clientes y pagos llamada Clientes y otra donde se almacenan los datos restantes llamada Pedidos.

## Decision Drivers

* RF-01: Migrar la arquitectura a una basada en microservicios
* RF-12: Sistema de reporte de incidencias
* RF-03: Conexión a base de datos

## Considered Options

* 0010-1 Uso de un módulo driver

## Decision Outcome

Chosen option: "0010-1 Uso de un módulo driver", because la implementación de esta decisión garantiza un diseño eficiente y desacoplado para la conexión a las bases de datos SQL con los microservicios.

### Positive Consequences

* Pueden realizarse los demas requisitos
* Los eventos son faciles de enviar.
* La empresa obtiene un sistema flexible que se adapta a los cambios y toma decisiones rápidamente.
* Conocer la situación de inmediato.

### Negative Consequences

* Existirán problemas si los consumidores no reaccionan al evento.

## Pros and Cons of the Options

### 0010-1 Uso de un módulo driver

El módulo driver permite la conexion segura durante el acceso a la base de datos debido al puente que se realiza en el driver. La conexión a este módulo se hará a través del Gestor determinado de cada módulo de servicios, de esta manera, se consiguen realizar consultas a través de los servicios de manera eficaz.

* Good, because Uno de los factores mas importantes es el reporte de incidencias.
* Good, because Es imprescindible para los módulos que necesiten información o envíen información a la base de datos.
* Bad, because Es obligatorio una interaccion entre consumidor y emisor

## Links

* https://www.redhat.com/es/topics/integration/what-is-event-driven-architecture#ventajas

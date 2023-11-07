# Alternativa-0007-Conexion-bases-de-datos

* Status: proposed
* Deciders: Miguel
* Date: 2023-11-07

## Context and Problem Statement

Nuestro sistema software debera poder acceder a dos bases de datos, una donde se almacena los datos de los clientes y pagos llamada Clientes y otra donde se almacenan los datos restantes llamada Pedidos.

## Decision Drivers

* RF-01: Migrar la arquitectura a una basada en microservicios
* RF-12: Sistema de reporte de incidencias
* RF-03 Conexión a bases de datos

## Considered Options

* 0010-1 Patrón Adapter

## Decision Outcome

Chosen option: "0010-1 Patrón Adapter", because la implementación de esta decisión garantiza un diseño eficiente y desacoplado para la conexión a las bases de datos SQL con los microservicios.

### Positive Consequences

* Pueden realizarse los demas requisitos
* Los eventos son fáciles de enviar.
* La empresa obtiene un sistema flexible que se adapta a los cambios y toma decisiones rápidamente.
* Conocer la situación de inmediato.

### Negative Consequences

* Existirán problemas si los consumidores no reaccionan al evento.

## Pros and Cons of the Options

### 0010-1 Patrón Adapter

El patrón de Adapter es útil en situaciones donde se necesita interactuar con sistemas o componentes que tienen interfaces incompatibles.

* Good, because Podemos ocultar los detalles de la implementación de la base de datos a los microservicios, lo que permite cambios futuros en la tecnología de la base de datos sin afectar a los microservicios.
* Good, because La conexión de las bases de datos SQL existentes y los microservicios se puede realizar de manera eficiente y controlada.
* Good, because Cada microservicio que necesita acceder a la base de datos utiliza un adaptador concreto para interactuar con la base de datos.

## Links

* https://www.redhat.com/es/topics/integration/what-is-event-driven-architecture#ventajas

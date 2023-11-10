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

* 0010-1 Uso de un módulo driver

## Decision Outcome

Chosen option: "0010-1 Uso de un módulo driver", because la implementación de esta decisión garantiza un diseño eficiente y desacoplado para la conexión a las bases de datos SQL con los microservicios.

### Positive Consequences

* Pueden realizarse los demas requisitos
* Los eventos son fáciles de enviar.
* La empresa obtiene un sistema flexible que se adapta a los cambios y toma decisiones rápidamente.
* Conocer la situación de inmediato.

### Negative Consequences

* Existirán problemas si los consumidores no reaccionan al evento.

## Pros and Cons of the Options

### 0010-1 Uso de un módulo driver

El módulo driver permite la conexion segura durante el acceso a la base de datos debido al puente que se realiza en el driver. La conexión a este módulo se hará a través del Gestor determinado de cada módulo de servicios, de esta manera, se consiguen realizar consultas a través de los servicios de manera eficaz.

* Good, because La conexión de las bases de datos SQL existentes y los microservicios se puede realizar de manera eficiente y controlada.
* Good, because //Cada microservicio que necesita acceder a la base de datos utiliza un adaptador concreto para interactuar con la base de datos.
* Good, because Al utilizar un driver, se puede implementar una capa de seguridad adicional para proteger la base de datos y prevenir posibles vulnerabilidades.
* Good, because Se puede utilizar un driver que este optimizado para SQL.
* Bad, because Algunos drivers pueden no ser igualmente compatibles con todas las plataformas, lo que podría limitar la portabilidad del software en entornos específicos.

## Links

* https://www.redhat.com/es/topics/integration/what-is-event-driven-architecture#ventajas

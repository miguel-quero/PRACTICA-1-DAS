# Módulo-Estadísticas

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-11-10

## Context and Problem Statement

El módulo de estadísticas proporciona información valiosa sobre el estado de los pedidos y la situación en tiempo real de los camiones y la información de clientes. Por esta razón, se deberá hacer una conexion a la base de datos a traves del driver dado.

## Decision Drivers

* RF-10 Información del pedido
* RF-11 Información del cliente

## Considered Options

* 0012-1-GestorEstadisticas

## Decision Outcome

Chosen option: "0012-1-GestorEstadísticas", because Realiza correctamente la funcionas de software pedidas. Ademas puede ser actualizado constantemente con su conexion a la base de datos directa.

### Positive Consequences

* Las estadisticas se envian despues de recopilar la informacion
* Hay seguridad implementada para las consultas

## Pros and Cons of the Options

### 0012-1-GestorEstadisticas

Se realiza una clase GestorEstadisticas dentro del módulo. Esta clase se encargá de conectarse al driver de las bases de datos para realizar las consultas de clientes y pedidos. Finalmente, se genera un resultado final a través de los datos recibidos.

* Good, because Realiza las funciones necesarias para hacer consultas
* Good, because Realiza las consultas de forma segura
* Good, because Crea un resultado final con la información juntada
* Bad, because Se puede generar trafico si no esta bien optimizado

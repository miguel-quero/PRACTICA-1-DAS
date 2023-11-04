# Arreglo-Patron-Mediator

* Status: proposed
* Deciders: Sergio, Miguel
* Date: 2023-11-04

## Context and Problem Statement

Se halló un fallo en la creacion del patron Mediator que habiamos implementado anteriormente. Para ello, se tendra que solucionar por medio de cambios en el diagrama que hemos creado.

## Decision Drivers

* RF-03 Conexión a bases de datos
* RF-10 Información del cliente
* RF-11 Información del pedido
* RF-13 Comunicación de pedidos

## Considered Options

* 0008-1-Añadir GestorDeEventos

## Decision Outcome

Chosen option: "0008-1-Añadir GestorDeEventos", because Era necesario un arreglo del patron debido a los fallos que habia.

## Pros and Cons of the Options

### 0008-1-Añadir GestorDeEventos

La clase GestorPedidos se moveria al modulo de EventConsumers, su funcionalidad hace de intermediario entre clientes, pedidos, repartos e incidencias. La interfaz GestorPedidos se añade para el funcionamiento del patron Mediator en EventConsumers. En EventChanel la clase de GestorPedidos se sustituye por GestorEventos, que contiene los metodos necesarios para procesar las solicitudes que recibe del modulo de EventProducer y comunicarlas a EventConsumer.

* Good, because Arregla el patron
* Good, because Mejora el rendimiento

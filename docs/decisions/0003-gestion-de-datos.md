# Gestion-de-datos

* Status: accepted
* Deciders: Miguel, Sergio
* Date: 2023-10-24

## Context and Problem Statement

En el contexto de nuestro proyecto de desarrollo de software, hemos decidido agrupar varios requisitos para la gestión de la base de datos. Por esto, hay que escoger un patron Mediator que para que se comunique la clase GestorPedidos con los microservicios disponibles de la aplicación.

## Decision Drivers

* RF-03 Conexión a base de datos
* RF-11 Información del cliente
* RF-10 Información del pedido
* RF-13 Comunicacion de pedidos

## Considered Options

* 0003-1-Mediator
* 0004-2-Proxy

## Decision Outcome

Chosen option: "0003-1-Mediator", because permite realizar los microservicios necesarios para el buen uso del sistema.

## Pros and Cons of the Options

### 0003-1-Mediator

El patron mediator se utilizará para conectar la API con GestorPedidos y con los microservicios. De esta manera es mas seguro realizar los microservicios.

* Good, because GestorPedidos trabajará como un balanceador
* Good, because Los eventos funcionarán a través de GestorPedidos que se comunica con todos los microservicios
* Bad, because La carga en GestorPedidos puede incrementar si no estan bien planteadas las conexiones.

### 0004-2-Proxy

El patron proxy es similar al patron Mediator, pero este sera intermediario de uso de GestorPedidos. Este tambien estara conectado a los microservicios.

* Good, because Permite delegar las acciones de los clientes
* Bad, because El punto del patron es controlar los microservicios, cuando es mas conveniente usar GestorPedidos para que se realicen las acciones en él.
* Bad, because GestorPedidos no controla todos los servicios, por lo que es menos conveninete usar el patron Proxy.

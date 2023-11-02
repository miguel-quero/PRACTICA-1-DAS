# Conexion-bases-de-datos

* Status: proposed
* Deciders: Sergio, Miguel
* Date: 2023-10-31

## Context and Problem Statement

Nuestro sistema software debera poder acceder a dos bases de datos, una donde se almacena los datos de los clientes y pagos llamada Clientes y otra donde se almacenan los datos restantes llamada Pedidos.

## Decision Drivers

* RF-03 Conexion a bases de datos

## Considered Options

* 0007-1-Protocolos HTTP/REST mediante Gateway

## Decision Outcome

Chosen option: "0007-1-Protocolos HTTP/REST mediante Gateway", because Realiza correctamente una conexion entre los servicios y las bases de datos de manera eficaz y segura.

## Pros and Cons of the Options

### 0007-1-Protocolos HTTP/REST mediante Gateway

El cliente pide utilizar los protocolos anteriores para conectar los servicios que proveemos. Mediante una API Gateway se conectaran estos servicios con las bases de datos.

* Good, because Permite realizar los servicios de manera mas sencilla
* Good, because Mayor rapidez y seguridad al tener un Gateway

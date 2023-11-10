# Módulo-Clientes

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-11-10

## Context and Problem Statement

Nuestro sistema software implementará un modulo de clintes. Este modulo se encargará de poder acceder a los datos personales de los clienes a través de la base de datos. Dentro del modulo se pueden encontrar dos clases, GestorClientes y la clase Cliente. La clase GestorCliente se encargrá de realizar los metodos de acceso a datos, mientras que la clase Cliente se encarga de guardar esta informacion conseguida.

## Decision Drivers

* RF-04 Permitir acceso a los datos personales

## Considered Options

* 0011-1-GestorClientes se conecta a la base de datos

## Decision Outcome

Chosen option: "0011-1-GestorClientes se conecta a la base de datos", because Realiza los requisitos pedidos del sistema software de manera eficaz y segura.

### Positive Consequences

* Se pueden realizar consultas sobre la información del cliente.
* Tiene mayor seguridad.

## Pros and Cons of the Options

### 0011-1-GestorClientes se conecta a la base de datos

La conexion de GestorClientes se realiza hacia el modulo driver para la base de datos, de esta manera, el modulo Cliente pude acceder a la información de los clientes y cargarla en una clase Cliente.

* Good, because Permite la conexion correcta a la base de datos.
* Good, because Consigue realizar una conexión segura para realizar consultas.

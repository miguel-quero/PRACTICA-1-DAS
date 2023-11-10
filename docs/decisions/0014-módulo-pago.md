# Módulo-Pago

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-11-10

## Context and Problem Statement

Una empresa decide prestar su servicio para facilitar el pago correspondiente.

## Decision Drivers

* RF-08 Desacoplamiento de funciones
* RF-14 Garantía de seguridad al realizar pagos

## Considered Options

* 0014-1 Inclusión del módulo

## Decision Outcome

Chosen option: "0014-1 Inclusión del módulo", because es un componente que una empresa ha decidido proporcionarnos, y no es posbile modificar su implementación.

### Positive Consequences

* Seguridad en los pagos, ya que la empresa que nos proporciona este módulo tendrá unas medidas de seguridad específicas.
* Menos mantenimiento de los pagos, porque la empresa externa es quien se encarga de ello.

### Negative Consequences

* La dependencia externa de este servicio, porque cualquier incidencia dentro del pago podría afectar a nuestro sistema.
* La experiencia del usuario con la aplicación puede verse afectada si el sistema de pago no es fluido.

## Pros and Cons of the Options

### 0014-1 Inclusión del módulo

Se ha decidido incluir el módulo Pago dentro del módulo Eventconsumer, este estará conectado al módulo Pedidos.

* Good, because Al realizar un pedido, desde el módulo Pedidos se utilizará este módulo Pago.
* Good, because Ningún otro microservicio podrá utilizar el módulo Pago.
* Good, because Es muy sencillo conectar este módulo.

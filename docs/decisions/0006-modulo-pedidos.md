# Modulo-pedidos

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-10-31

## Context and Problem Statement

El módulo pedidos resulta ser sencillo en cuanto a sus requerimientos, tan sólo se tienen que poder realizar pedidos y dar un número de intentos necesarios. Para ello, se creará una clase GestorCompra, clase Pedido y clase Producto. La clase GestorCompra contiene las funcionalidades necesarias para realizar un pedido y comprobar el número de intentos. Esta clase recibe las solicitudes procedentes del módulo EventChannels y se comunica con la base de datos de los pedidos.

## Decision Drivers

* RF-05 Permitir realizar pedidos
* RF-06 Establecer intentos para realizar pedidos

## Considered Options

* 0006-1-Sin patron de comportamiento

## Decision Outcome

Chosen option: "0006-1-Sin patron de comportamiento", because Es una respuesta sencilla para el problema que se plantea. Este es un módulo simple que tiene poco peso en el sistema, por lo que no se encuentra un patrón que no complique demasiado su uso.

## Pros and Cons of the Options

### 0006-1-Sin patron de comportamiento

Al ser un modulo sencillo, se propone utilizar una clase Pedido donde pueda realizar el pedido y contar el numero de intentos. Una vez termine de realizar el pedido, otra clase se ocupará de enviar el pedido a las bases de datos.

* Good, because Mejor simplificar en vez de complicar un diseño
* Good, because Realiza lo que el cliente pide
* Good, because El intermediario para la base de datos da mas seguridad
* Bad, because No tiene un patron que verifique un buen comportamiento

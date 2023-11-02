# Modulo-pedidos

* Status: proposed
* Deciders: Sergio, Miguel
* Date: 2023-10-31

## Context and Problem Statement

El modulo pedidos resulta ser sencillo en cuanto a sus requerimientos, tan solo se tienen que poder realizar pedidos y dar un numero de intentos necesarios.

## Decision Drivers

* RF-05 Permitir realizar pedidos
* RF-06 Numero de intentos para realizar pedidos

## Considered Options

* 0006-1-Sin patron de comportamiento

## Decision Outcome

Chosen option: "0006-1-Sin patron de comportamiento", because Es una respuesta sencilla para el problema que se plantea. Este es un modulo simple que tiene poco peso en el sistema, por lo que no se encuentra un patrón que no complique demasiado su uso.

## Pros and Cons of the Options

### 0006-1-Sin patron de comportamiento

Al ser un modulo sencillo, se propone utilizar una clase Pedido donde pueda realizar el pedido y contar el numero de intentos. Una vez termine de realizar el pedido, otra clase se ocupará de enviar el pedido a las bases de datos.

* Good, because Mejor simplificar en vez de complicar un diseño
* Good, because Realiza lo que el cliente pide
* Good, because El intermediario para la base de datos da mas seguridad
* Bad, because No tiene un patron que verifique un buen comportamiento

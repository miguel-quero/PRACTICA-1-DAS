# Módulo-Incidencias

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-11-10

## Context and Problem Statement

El sistema contará con monitorización que reportará cualquier tipo de incidencias a los gestores de rutas.

## Decision Drivers

* RF-08 Desacoplamiento de funciones.
* RF-12 Sistema de reporte de incidencias.
* RF-13 Comunicación de funcionalidades.

## Considered Options

* 0013-1 Sin patrón de diseño
* 0013-2 Patrón Observer

## Decision Outcome

Chosen option: "0013-1 Sin patrón de diseño", because se puede extrapolar cualquier tipo de incidencia mediante el sensor.

### Positive Consequences

* Se pueden detectar los problemas de una forma temprana y así que las respuestas sean más rápidas.
* Es posible monitorizar de forma constante y continua el rendimiento de la aplicación.

### Negative Consequences

* Es posible que se pueda producir una sobrecarga de datos, porque el sensor puede llegar a generar una gran cantidad de información.

## Pros and Cons of the Options

### 0013-1 Sin patrón de diseño

El módulo de incidencias conectado al GestorPedidos tendrá una clase llamada GestorIncidencias que se encargará de monitorizar todo tipo de problema. Además, para detectar estas incidencias se utilizará una clase Sensor conectada al API Gateway dentro del módulo EventProducer.

* Good, because El Sensor se encargará de detectar cualquier tipo de incidencia y enviarla al GestorIncidencias.

### 0013-2 Patrón Observer

Se decidió también incluir la clase Sensor dentro del módulo de incidencias, junto con un patrón observer.

* Bad, because Tiene bastante complejidad a la hora del desarrollo, si no se gestiona de forma adecuada.

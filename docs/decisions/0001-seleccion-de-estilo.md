# Seleccion-de-Estilo

* Status: accepted
* Deciders: Miguel, Sergio
* Date: 2023-10-23

## Context and Problem Statement

En el contexto de nuestro proyecto de desarrollo de software, hemos decidido adoptar una arquitectura dirigida a eventos para mejorar la modularidad y la escabilidad de nuestro sistema.

## Decision Drivers

* RF-01: Migrar la arquitectura a una basada en microservicios
* RF-12: Sistema de reporte de incidencias

## Considered Options

* 0001-1-Arquitectura dirigida por eventos
* 0001-2-Arquitectura cliente-servidor
* 0001-3-Arquitectura orientada a servicios
* 0001-4-Arquitectura modelo vista controlador

## Decision Outcome

Chosen option: "0001-1-Arquitectura dirigida por eventos", because permite una implementacion completa y sencilla de las tareas que se piden en la aplicacion.

### Positive Consequences

* Pueden realizarse los demas requisitos
* Los eventos son faciles de enviar.
* La empresa obtiene un sistema flexible que se adapta a los cambios y toma decisiones rápidamente.
* Conocer la situación de inmediato.

### Negative Consequences

* Existiran problemas si los consumidores no reaccionan al evento.

## Pros and Cons of the Options

### 0001-1-Arquitectura dirigida por eventos

La arquitecura por eventos tendrá emisores de eventos, consumidores y canales de eventos que nos servirán para realizar las tareas que se piden.

* Good, because Uno de los factores mas importantes es el reporte de incidencias.
* Bad, because Es obligatorio una interaccion entre consumidor y emisor

### 0001-2-Arquitectura cliente-servidor

El modelo cliente-servidor accede a datos de las bases de datos y recibe peticiones asincronas y respuestas de eventos.

* Good, because Es una arquitectura escalable.
* Bad, because Al ser basada en el servidor, crea gran inseguridad en un fallo de este.

### 0001-3-Arquitectura orientada a servicios

La arquitectura orientada a servicios fomenta la creacion de servicios para la integracion de aplicaciones.

* Good, because Es sencillo implementar los servicios que se piden.
* Bad, because Es similar a la arquitectura basada en microservicios ya que son procesos que se comunican con otros a traves de una red para conseguir un objetivo.

### 0001-4-Arquitectura modelo vista controlador

El estilo modelo vista controlador esta diseñado para sistemas interactivos donde existen diferentes vistas para los mismos datos

* Good, because Promueve la interaccion en la aplicación
* Bad, because La aplicacion solo tendrá una interfaz
* Bad, because No hay razon para mostrar de diferentes maneras la misma informacion.

## Links

* https://www.redhat.com/es/topics/integration/what-is-event-driven-architecture#ventajas

# Seleccion-de-la-interfaz

* Status: accepted
* Deciders: Miguel, Sergio
* Date: 2023-10-24

## Context and Problem Statement

En el contexto de nuestro proyecto de desarrollo de software, hemos decidido adoptar una interfaz dividida que permita a los usuarios utilizarla desde PC y móvil.

## Decision Drivers

* RF-02 Interfaz para la aplicación

## Considered Options

* 0002-1 Interfaz Unificada
* 0002-2 Interfaz Dividida

## Decision Outcome

Chosen option: "0002-2 Interfaz Dividida", because permite separar las interfaces para PC y móvil

## Pros and Cons of the Options

### 0002-1 Interfaz Unificada

Una interfaz unificada reducirá el tiempo de creacion de las interfaces.

* Good, because Tiene un menor mantenimiento
* Good, because La creacion es mas sencilla
* Bad, because Se tiene que adaptar a ambos dispositivos

### 0002-2 Interfaz Dividida

Una interfaz dividida permite contar con dos tipos de interfaz especificas para movil o PC
Se crearán dos clases distintas que actuaran de interfaces. Por un lado la interfaz "Movil APP" y por otro "Web APP" que generarán los eventos que se crearan en la aplicación. Las interfaces se comunicaran con la aplicación a traves de un patron API Gateway que se enviara al gestor de pedidos y estara como intermediario entre el productor de eventos y el canal de eventos

* Good, because Crea libertad de creacion de interfaz
* Good, because Elimina dependencias entre ambas
* Good, because Se juntan con un patron API Gateway que da seguridad
* Good, because Permite llegar a un mayor numero de usuarios
* Bad, because Al ser diferentes interfaces, podrian generar errores distintos
* Bad, because Genera doble mantenimiento

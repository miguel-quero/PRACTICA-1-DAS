# Seleccion-Patron-Del-Algoritmo-Optimizacion

* Status: proposed
* Deciders: Sergio, Miguel
* Date: 2023-10-31

## Context and Problem Statement

En nuestro sistema software, habrán dos tipos de algortimos de optimizacion que se seleccionaran en funcion de la demora del camión. Para ello decidimos añadir un modulo Algoritmo donde se escogera el algoritmo necesario en base a las necesidades.

## Decision Drivers

* RF-07 Logística de repartos
* RF-09 Gestión de algortimos

## Considered Options

* 0005-1-Strategy

## Decision Outcome

Chosen option: "0005-1-Strategy", because El patron Strategy soluciona los problemas que se pueden encontrar en la eleccion de algortimo.

## Pros and Cons of the Options

### 0005-1-Strategy

El patron Strategy es un buen candidato para la construcción del modulo ya que permite la eleccion del algoritmo segun el contexto que se utilice.

* Good, because Permite una eleccion sencilla de algoritmos segun la información dada.
* Good, because Añade posibilidad de cambiar de algoritmos durante la ejecucion del programa.
* Good, because Se puede modificar la informacion de manera sencilla para la eleccion de algoritmos.
* Bad, because Si se utiliza un solo algoritmo una mayor cantidad de veces, el patron hace que se complique demasiado el modulo.

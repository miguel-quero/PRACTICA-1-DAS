# Seleccion-Patron-Del-Algoritmo-Optimizacion

* Status: accepted
* Deciders: Sergio, Miguel
* Date: 2023-10-31

## Context and Problem Statement

En nuestro sistema software, habrán dos tipos de algoritmos de optimizacion que se seleccionaran en función de la demora del camión. Para ello decidimos añadir el patrón Strategy en el módulo de rutas donde se escogerá el algoritmo necesario en base a las necesidades. Dentro del módulo de rutas, se tiene una clase GestorAlgoritmos que recibe las solicitudes del módulo EventChannels y llama a la clase Context para elegir que algoritmo a ejecutar. La clase Context  guarda el estado del tráfico en tiempo real y calcula cuál de los dos algoritmos se debería ejecutar en cada momento. Existe una interfaz Strategy, que contiene un método execute que utiliza los dos tipos de algoritmos. También, se creará una clase AlgoritmoRutaA y AlgoritmoRutaB que contienen los métodos de optimización e implementarán la interfaz Strategy.

## Decision Drivers

* RF-07 Logística de repartos
* RF-09 Gestión de algoritmos

## Considered Options

* 0005-1-Strategy

## Decision Outcome

Chosen option: "0005-1-Strategy", because El patron Strategy soluciona los problemas que se pueden encontrar en la eleccion de algortimo.

## Pros and Cons of the Options

### 0005-1-Strategy

El patron Strategy es un buen candidato para la construcción del modulo ya que permite la eleccion del algoritmo segun el contexto que se utilice. Se utiliza una clase GestorAlgoritmos que creará un objeto Context para escoger entre los algoritmos disponibles.

* Good, because Permite una eleccion sencilla de algoritmos segun la información dada.
* Good, because Añade posibilidad de cambiar de algoritmos durante la ejecucion del programa.
* Good, because Se puede modificar la informacion de manera sencilla para la eleccion de algoritmos.
* Bad, because Si se utiliza un solo algoritmo una mayor cantidad de veces, el patron hace que se complique demasiado el modulo.

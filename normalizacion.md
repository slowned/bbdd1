**NORMALIZACION**
  
  * Super conjunto: (nuestro def) es el conjunto de los atributos por 
  los cuales se pueden acceder a los atributos retantes del modelo
  > determinan funcionalmente a todos los restantes atributos de la relacion R
  > Una superclave no necesariamente es minimal

  * Axiomas de Astrong: Permiten inferir nuevas _dependencias funcionales_.
    * Basicos (Reflexion, aumento, transitiviad).
    * Aumento
    * Transitividad
    apartir de los axiomas basicos se deduen (Union, descomposicion, pseudotransitividad)

  * Clave de una relacion:
    * Los tributos {A1. A2,..,An} son la clave de una *R* si cumplen:
      1. {A1. A2,..,An} determinaj funcionalmente a todos los restantes atributos de la relacion *R*.
      1. No existe un subconjunto {A1. A2,..,An} que determine funcionalmente a todos los atributos de *R* 
      _esto implica que una clave es un conjuto minimal_.

  * **Dependencia Multivaluada:** afirma que dos o mas atributos son independientes del resto.
    Como consecuencia de la independencia, se tiene redunaania. Esta redundancia no se elimina
    con las dependencias funcionales.


**COMO GENERAR RELACIONES QUE CUMPLAN CIETAS CONDICIONES DE UN BUEN DISENIO**

  * Descomposicion: es una forma ara eliminar las anomalias de una relacion,
    consister en separar los atributos de una relacion en dos nuevas relaciones;

    > No se de perder Informacion, ni dependencias funcionales.

    * Perdida de informacion.
      Si a un esquema *R*, se lo particiona en dos subesquemas *R1* y *R2* se debe cumplir
      alguna de las siguientes condiciones:
      > *R1* U *R2* es clave en el esquema *R1*
      > *R1* U *R2* es clave en el esquema *R2*

    * Perdida de dependencias funcionales.
      Verrificar que cada una de las dependencias funcionales que alian en el esquema *R*,
      sigan valiendo en alguna e las particiones *Ri*


* **BCNF:** provee un mecanismo para asegurar que las anomalias dejen de estar en
  particionamineto, que no se pieda informacion y, en algunos casos, aseguro que no se
  pierdan dependencias funcionales.

  > Un esquema de relacion esta en *BCNF* si, siempre que una dependencia funcional de la
  > forma *X->A* es valida en *R*, entonces se cumple que, _X es superclave de R_ o bien
  > *X->A* es una dependencia funcional trivial.

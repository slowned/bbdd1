# BBDD1 

* # **Modelos de datos**
  > Proveen una notacion para describir los datos, cuentan con
  > estructura de datos, operaciones y restricciones sobre los
  > datos. 

  * **Modelos logicos**
    > Modelo de datos de alto nivel que provee conceptos cercanos
    > a la manera en la que los usuarios perciben los datos.
    * Basado en objetos ("entidades y relaciones","orientado
      a objetos")
    * Basado en registros ("Modelo Relacional")

    > Estos modelos (logicos) deben ser abstracciones del mundo real,
    > representar el significado de los datos, y ser independiente
    > de los detalles de l implementacion fisica.

    * Elementos del modelo (entidad, relacion, atributos)
      * Entidad: Es una "cosa o concepto" que puede ser identificada y
      distinguible de otra "cosa o concepto"

        > Juan con DNI 1234567.
        > Auto modelo 2018 patente PRI.

      * Relacion: Es una asociacion de entidades

        > Juan con dni 12334567 **es_duenio_de** un auto modelo 2018
        > cuya patente es PRI.

      * Atributo: representa informacion acerca de una entidad o
      una relacion

        > nombre, dni, modelo, patente

        * Dominio de un atributo: conjunto de valores que puede
        romar un atriuto  en particular

          > nombre puede ser una cadena de maximo 50 letras.

    * Rol de una entida en una relacion
      > _esposa_de_
      > juan con dni 123456 esta_casado con Maria cuyo dni es 33456.
      > Esta ultima, tiene el rol de esposa_de.

    * Conjunto de entidades (mismo tipo)

      > El conjunto de todas las personas que poseen un nombre y un
      > dni puede llamarse PERSONA.

      > El conjunto de todos los autos que poseen informacion del
      > modelo y de la patente puede llamarse AUTO.

      _No necesariamente son disjuntos, por ejemplo una entidad 
      **alumno** puede ser una entidad **doncente**_

    * Conjunto de relaciones
      > **ES_DUENIO_DE** es un conjuto de relaciones entre las entidades
      > **PERSONA** y **AUTO**.
      

    > **Los termonos, *entidad* y *conjunto de entidades* seran
    > intercambiables, haciendo abuso del vocabulario.

    > **Los termonos, *relacion* y *conjunto de relaciones* seran
    > intercambiables, haciendo abuso del vocabulario.

   * Restricciones el modelo (Cardinalidad, identificador, grado)
    * **Cardinalidad:** Determina el numero de veces en la que puede
    participar una entidad en una relacion (indica dependencia
    _importancia de la cardinalidad minima_).
      * total o de existencia: participacion obligatoria
      * particial: participacion no obligatoria

      > Tomamos un conjunto binario de relaciones **R** entre dos
      > conjuntos de entidades **A** y **B**, la cardinalidad puede ser.
      * **Uno a uno** 
        Una entidad de **A** puede estar asociada con a lo sumo **una**
        entidad **B** y una entidad **B** puede estar asociada con a lo
        sumo **una** entidad de **A**.

      * **Uno a muchos** 
        Una entidad de **A** esta asociada con **cualquier numero** de 
        entidades en **B**, pero una entidad **B** esta asociada con **a lo
        sumo una** entidad de **A**.

      * **Muchos a muchos**
        Una entidad de **A** esta asociada con **cualquier numero** de entidades
        en **B** y una entidad de **B** esta asociada con **cualquier numero**
        entidades en **A**.

    * **Grado:** Representa el numero maximo de veces que una entidad puede
    estar relacionada con otra.
      > (1,n) -> grado n.
      > (1,1) -> grado 1.

    * **Clave o identificador**

  * **Modelos fisicos**
    > Modelo de datos de alto nivel que provee conceptos que
    > describen detalles de como los datos son almacenados.

  _Estos modelos difieren en los elementos que emplean para
  reprecentatar los datos y Expresividad_

  * ## **Modelo de Entidades y Relaciones**
  * ## **Modelo Relacional(Algebra Relacional)**
* # **Normalizacion**
  * ## Conceptos generales
  * ## Proceso
* # **DBMS Relacional**
  * ## MySQL

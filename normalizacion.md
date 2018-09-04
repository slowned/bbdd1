**NORMALIZACION:**
  llamamos **normalizar** hasta BCNF o 3fn


  ## FORMAS NORMALES
    * *1FN*:
      los atributos de la relacion son simples y atomicos.
    * *2FN*:
      un esquema de relacion R esta en 2fn si para toda dependencia de la forma X->A,
      se cumple que, A depende de manera total de la clave.
  
  * **Super conjunto:** (nuestro def) es el conjunto de los atributos por 
  los cuales se pueden acceder a los atributos retantes del modelo
  > determinan funcionalmente a todos los restantes atributos de la relacion R
  > Una superclave no necesariamente es minimal

  * **Axiomas de Astrong:** Permiten inferir nuevas _dependencias funcionales_.
    * Basicos (Reflexion, aumento, transitiviad).
    * Aumento
    * Transitividad
    apartir de los axiomas basicos se deduen (Union, descomposicion, pseudotransitividad)

  * **Clave de una relacion:**
    * Los tributos {A1. A2,..,An} son la clave de una *R* si cumplen:
      1. {A1. A2,..,An} determinaj funcionalmente a todos los restantes atributos de la relacion *R*.
      2. No existe un subconjunto {A1. A2,..,An} que determine funcionalmente a todos los atributos de *R* 
      _esto implica que una clave es un conjuto minimal_.

  * **Dependencia Multivaluada:** afirma que dos o mas atributos son independientes del resto.
    Como consecuencia de la independencia, se tiene redunaania. Esta redundancia no se elimina
    con las dependencias funcionales.


**COMO GENERAR RELACIONES QUE CUMPLAN CIETAS CONDICIONES DE UN BUEN DISENIO**

  * **Descomposicion:** es una forma para eliminar las anomalias de una relacion,
    consister en separar los atributos de una relacion en dos nuevas relaciones;

    > No se de perder Informacion, ni dependencias funcionales.

    * **Perdida de informacion**.
      Si a un esquema *R*, se lo particiona en dos subesquemas *R1* y *R2* se debe cumplir
      alguna de las siguientes condiciones:
      > *R1* U *R2* es clave en el esquema *R1*
      > *R1* U *R2* es clave en el esquema *R2*

    * **Perdida de dependencias funcionales**.
      Verrificar que cada una de las dependencias funcionales que alian en el esquema *R*,
      sigan valiendo en alguna e las particiones *Ri*


* **BCNF:** provee un mecanismo para asegurar que las anomalias dejen de estar en
  particionamineto, que no se pieda informacion y, en algunos casos, aseguro que no se
  pierdan dependencias funcionales.

  > Un esquema de relacion esta en **BCNF** si, siempre que una dependencia funcional de la
  > forma **X->A** es valida en **R**, entonces se cumple que, **X es superclave de R** o bien
  > **X->A** es una dependencia funcional trivial.

  > Cuando no se puede llevar a **BCNF** poruqe se pierden dependendencias funcionales, entones
  > se lleva al esquema a **3FN** , no que asegura que:
  >   1. no se pierda informacion
  >   1. no se puerdan dependenias funcionales
  >   1. pero no siempre se quitan las anomalias.

* **3FN:** en esquema de relacion **R** esta en**FN** si para toda dependencias de la forma
  _X->A_, se cumple que: 
    1. _X -> A_ es trivial 
    1. _X_ es superclave
    1. _A_ es primo(que orma parte de alguna clave candidata)

    De manera esquemática y simplificada, una vez halladas las
dependencias funcionales y las claves candidatas y habiendo
detectado que no se puede llevar a BCNF
◦ Se construye una tabla por cada dependencia funcional
◦ Si la clave de la tabla original, no está incluida en
ninguna de las tablas del punto anterior, se construye
una tabla con la clave



* **Dependencia Multivaluada** afirma que dos o mas
atributos son independientes del resto. Como consecuencia de la independencia, se tiene
redundancia. Esta redundancia no se elimina con las dependencias funcionales

>    se puede decir que: X -->> Y si dado un valor de
> X, hay un conjunto de valores de Y asociados y
> este conjunto de valores de Y,e Y es independiente de los
> atributos de R-X-Y.

* **Dependencia Multivaluada trivial**
> Una dependencia multivaluada de la forma X->>Y
> que vale en R es trivial si:
>  el conjunto de atributos X,Y son todos los atributos
> del esquema

Direccion no tiene nada que lo identifique
PERSONA (dni, apellido, dirección)
PERSONA1(dni , apellido)
PERSONA2(dni,dirección)
¿Se perdió información?
PERSONA1 U PERSONA2 es clave en el esquema PERSONA1
{dni}
En PERSONA2 VALE LA DEPENDENCIA MULTIVALUADA
DM1) dni ->> dirección



* **Cuarta Forma Normal (4FN)**
> Un esquema está en 4FN cuando:
>  No tiene dependencias multivaluadas
> O bien,
>  Las dependencias multivaluadas que en él valen,
> son triviales.

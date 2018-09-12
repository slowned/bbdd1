# SQL

## DBMS (sistema de manejo de bases de datos)

  Sirve para crear y manejar grandes volumenes de datos, permitiendo persistirlos de manera segura por 
  un largo periodo de tiempo.
    1. Permite recuperar datos ante fallos (dirailidad)
    1. Control de acceso de usuarios (aislamiento)
    1. Acciones sobre los datos que se realizan de manera completa (atomicidad)
    1. Crear bases de datos y sus esquemas (lenguaje de definicion de datos "DDL")
    1. Consultar y modificar datos (lenguaje de consulta y manipulacion "DML")


## A.C.I.D
  * **Atomocidad**, o todos las operaciones se realizan o ninguna se hace.
  * **Consistencia**, la ejecucion asilada de la transaccion, conserva la consistencia de la **BD**
  * **Aislamiento**, Cuando dos o mas transacciones se ejecutan concurrentemente, cada una de ellas ignora al resto
  * **Durabilidad**, cuando termina una transaccion exitosamente los camios quedan en la **BD** aun cuando hayan fallos en el sistema

## Estados de la Transaccion

  * **Activa**, mientras se ejecuta.
  * **Parcialmente comprometida**, despues de ejecutarse la ultia instruccion.
  * **Fallida**, luego de darse cuenta que no puede continuar con la ejecucion normal.
  * **Abortada**, despues de hacer el rollback.
  * **Comprometida** al completarse con exito.

## Store Procedure
  
  Conjunto de sentencias **SQL** que se almacenan en el servidor.
  ```SQL
  CALL nombre_SP
  DROP PROCEDURE IF EXIST nombre_SP

  ```
  * **Acceso homogenio**, se realiza la misma operacion en la ase de datos, puede estar escrita en diferentes lenguajes.
  * **Asegura consistencia de operaciones**, cada ve que se ejecute el **SP** retorna de manera Sconsistente los resultados.
  Puede usarse para no permitir el acceso a tablas directamente.
  * **Ayuda de performance**, disminuye el trafico entre servidor y cliente.
  * **Consultas completas**, es posuble usar estructuras y funciones adicionales para resolver consultas complejas.

  Para crear *store procedures* se necesita de siertos privilegios. 
  1. crear, **CREATE RUTINE**
  1. modificar, **ALTER RUTINE**
  1. ejecutar, **EXECUTE**

  ```SQL
  CREATE PROCEDURE nombre_sp (parametros in-out inout a int) 
  ```

## Cursores
  Permiten guardar valores obtenidos de la ejecucion de una sentencia *SQL*, es posible recorrerlo e ir recuperando los valores almacenados.

  > PRIVILEGIOS
  > DECLARE, OPEN, FETCH, CLOSE

  ```SQL 
  DECLARE nombre_cursor CURSOR for select ... where
    fetch nombre into tablas: 1,2
  ```


## Trigger

  Son disparadores que se pueden usar BEFORE-AFTER-INSERT-DELETE-UPDATE
  ```SQL
  CREATE TRIGGER nombre_trigger B-A I-D-U *TABLA* FOR EACH ROW *CONSULTA*JJO

  ```

  > Privilegios TRIGGER

  En los triggers no se pueden usar *store procedures* ni *transacciones*.

## Vistas
  ```SQL
  CREATE VIEW nombre_vista AS consulta
  ```

  Una ez creada la vista es "congelada" si posteriomente las tablas involucradas en la avista son modificadas no afectan a las vista.
  Tener en cuenta que los nombres de las columnas deen ser unicos, no se pueden asociar triggers a las vistas, y no pueden tener subqueries en el FROM

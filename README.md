# PostgreSQL-fi
Curso PostgreSQL Facultad de Ingenieria

# Clase 1

### Caracteristicas
Resiste a fallas, es de los mas populares, es OPEN SOURCE, 
<br>
es portable,
WAL para evitar perdidas de datos, <br> 
Cumple propiedades ACID: 
<ul>
  <li>   <b>A</b>tomicidad: Es decir, que si alguna de las operaciones falla la transacción es cancelada.</li>
  <li>   <b>C</b>onsistencia: Es decir que sigue unas reglas definidas por el sistema, por ejemplo los tipos de datos son los esperados.</li>
  <li>A<b>I</b>slamiento: Se ejecutan de manera paralela, puede ejecutarse sin ser afectada y sin afectar a las demás transacciones.</li>
  <li><b>D</b>urabilidad: Cuando apaguemos o fallo de la base de datos los datos aparecerán ahí.</li>
</ul>

<p>
    Mayor asignación de memoria de forma predeterminada <br>
    Flexible multiplataforma (windows,linux)<br>
    Colección de base de datos<br>
    y divisiones logicas<br>
</p>
<p>
    Instalación de SQL Manager, VMWare con UNICA Software Linux redHat, powerDesigner,pgAdmin<br>
    Instalación de PostgreSQL en Linux<br>
    Configuración de puertos de PostgreSQL en Linux<br>
    Configuración de puertos de PostgreSQL en Linux<br>
</p>


# Clase 2

<p>
    <b>Power Designer</b>: Creando nuestro diagrama conceptual con entidades<br>
    En las entidades existen propiedades que pueden ser: <br>
    <ul>
        <li>Identificador mandatorio: Obligatorio<br></li>
        <li>Identificador primario: Automaticamente mandatorio (no puede quedar vacios)<br></li>
        <li>Display: Mostrar en pantalla <br></li>
    </ul>
    
</p>
<br>
<p>
    Un poco de teoria...<br>
    <b>SQL: Structured Query Language</b> , Oracle fue el primero en adoptarlo. <br>
    Es un estandar ISO<br>
    Actualmente se trabaja con SQL3<br>
    <b>Tipos de datos en SQL</b> son casi los mismos que en programación. <br>
    <b>Tipos de datos extendidos en SQL</b> (como los son box para planos, inet para direcciones de red) <br>


</p>

### Clasificación de Sentencias SQL

<p>
    <b>Data Definition Language(DDL)</b>: Sirve para modificación de la estructura de los objetos de la base de datos.<br>
    <ul>
        <li><b>CREATE</b></li>
        <li><b>DROP</b></li>
        <li><b>ALTER</b> (modifica)</li>
    </ul>
    <b>Data Manipulation Language(DML):</b> Para manipular datos almacenados en las bases de datos a nivel de FILAS o COLUMNAS. Para modificar, agregar, etc elementos o filas.<br><br>
    <ul>
        <li><b>SELECT</b>: Recupera atributos que se desean en el resultado de una consulta</li>
        <li><b>INSERT</b></li>
        <li><b>UPDATE</b></li>
        <li><b>DELETE</b>: Elimina todos los registros de una tabla</li>
    </ul>
    <b>Data Control Language(DCL):</b>Para funciones de administración que realiza el DBMS, tales como atomicidad y seguridad.<br><br>
    <ul>
        <li><b>COMMIT</b>: Finaliza transacción de la base de datos dentro de un DBMS.</li>
        <li><b>ROLLBACK:</b> Devuelve la base de datos a un estado anterior</li>
        <li><b>GRANT:</b>Permite dar permisos a uno o más usuarios para relizar alguna tarea en específico</li>
        <li><b>REVOKE</b>: Eliminar los permisos.</li>
    </ul>
</p>

<br>

<p>
    Vimos un poco de operadores logicos, el desigual es <b><></b><br><br>
    <b>Comandos para:</b><br>
    Crear una base de datos<br>
    Conectar una base de datos<br>
    Crear una tabla<br>
    Modificar una tabla<br>
    Agregar una columna a una tabla<br>
    Eliminar una columna a una tabla<br>
    Cambiar el nombre a una columna de una tabla<br>
    Cambiar el tipo de dato de una columna de una tabla<br>
    <br>


</p>

# Clase 3

<p>
    <b>DML</b>: Actualizando datos de una tabla, creando nuevas tablas, eliminando registros de las tablas,etc.<br>
    Empezamos a ver qué es un Schema de PostgreSQL <br>
    
</p>

# Clase 4

<p>
    <b>Partición de tablas</b>:Creando tablas hijas , PostgreSQL, en este caso solo puede particionar por <b>rango,lista o hash</b> y por <b>columnas.</b><br>
    Teniamos en este caso una tabla padre con los campos id, nombre, transporte y le especificamos el tipo de particion que sería por lista.<br>
    <ul>
        <li>Create table viajeros_barco partition of viajeros for values in ('barco')<br></li>
        <li>Create table viajeros_carro partition of viajeros for values in ('carro')<br></li>
        <li>Aqui acabamos de crear dos particiones de viajeros de tipo lista</li>
    </ul>
    
</p>
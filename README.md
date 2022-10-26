# Azure-Cloud

Repositorio de DataFactory para proyecto final de Siglo 21 y Softtek.

Instrucciones:

Situación inicial
Te contratan como Arquitecto Cloud para una startup de IT dedicada a la consultoría y asesoría en temáticas orientadas a analítica de datos.  Marcela, project manager de tu equipo, te comparte el pedido de que un cliente de la organización (Tech Consulting Group) necesita realizar un proceso de ETL sobre una base de datos que se encuentra de forma “on - premise” dentro de su compañía.

El pedido de la empresa consiste esencialmente en desarrollar una canalización de datos (pipeline) utilizando diferentes servicios de Azure, los cuales incluyen el almacenamiento, procesamiento y orquestación de datos. Como requerimiento excluyente del proyecto, es necesario que todo el flujo de datos se ejecute sobre la nube de Azure dado que es el proveedor que actualmente posee contratado la organización.


La base de datos a utilizar se llama: dbRetail y se encuentra compuesta por diferentes tablas de negocio como ser: Resulta importante destacar que el formato de la base de datos es de tipo .bacpac.

Con esta implementación, se busca realizar diferentes transformaciones sobre las tablas propuestas para automatizar el proceso de ingesta, transformación y carga de datos (Ver: Sección Transformaciones). Con la aplicación de esta tecnología, Tech Consulting Group, lograra incrementar la productividad de sus procesos, al automatizar una tarea repetitiva que con lleva en la perdida de tiempo valioso para el negocio.

Objetivos
Crearemos una canalización que permita:
● Almacenar la base de datos dentro del motor de Azure SQL.
● Ingestar una tabla desde el servicio de Data Factory.
● Configurar los diferentes Linked Services requeridos para el proyecto.
● Integrar el servicio de Databricks para la realización de un ETL con Data Factory.
● Cargar la tabla transformada dentro de un Data Lake a través del proceso de ETL.

Transformaciones:
1. En la tabla “Categoria” renombrar el campo Categoria a Nombre_Categoria.
2. En la tabla “FactMine” obtener el total de la columna: TotalOreMined.
3. En la tabla “Mine” seleccionar únicamente las columnas: Country, FirstName,LastName y Age.
4. En la tabla “Mine” obtener el total de la columna: TotalWasted agrupado por el atributo Country.
5. En la tabla “Producto” realizar un conteo de la cantidad de productos disponibles utilizando el campo: Cod_Producto.
6. En la tabla “Producto” mostrar de forma descendiente la información ordenada por el campo: Cod_Producto.
7. En la tabla “Subcategoria” realizar un filtro por el Cod_Categoria = 3.
8. En la tabla “VentasInternet” generar una columna llamada Ingresos Netos, que se obtenga de multiplicar los atributos: (Cantidad * PrecioUnitario) – CostoUnitario.
9. En la tabla “VentasInternet” mostrar el promedio y suma total de la columna: Ingresos Netos por Cod_Producto.

Assets
La base de datos a utilizar para el proyecto, podrás encontrarla en el siguiente repositorio de GitHub:
• https://github.com/laylascheli/alkemy_proyecto_aceleracion_practica

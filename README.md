# ETL_Project

Descripcion del proyecto
Projecto de ETL manejado con Spark en lenguaje Python para un caso de estudio de peliculas rentadas, este proyecto tiene como objetivo crear una ETL para el procesamiento de datos desde un archivo Excel
Tenemos como primer paso la extracción de los datos desde el archivo excel Films_2 (3).slsx, seguido de la transformación donde pasamos a en base a un analisis exploratorio de los datos a limpiarlos segun sea requerido, para este caso eliminamos la información irrelevante y aplicamos ciertos filtros para sacar información de negocio, Ademas de eso los datos transformados se dejan almacenados como archivos CVS para ser cargados ya sea a una base de datos o para su analisis

Instalación
Para comenzar con este proyecto, primero se deben instalar las dependencias necesarias para hacerlo sigue estos pasos

1.Clona el repositorio
Descargar el archivo zip con toda la carpeta y modulos del proyecto 

2.Entorno y dependencias
En tu computador personal debes tener python instalado y con su entorno configurado
en este en su terminal de uso instalaras 
"pip install pyspark" para la conexion con Api spark
"pip install pandas" para el manejo de la libreria de pandas
"pip install openpyxl" para la lectura y escritura de archvos excel

Ademas de eso para la utilización de spark ya que esta utiliza de base JAVA debes de instalar JAVA en tu sistema el cual lo encuentras en este link
https://www.oracle.com/es/java/technologies/downloads/#java8
y ademas de eso debes añadir la variables de entorno al path de inicio en la configuracion de tu sistema
para eso te dirijes a Este equipo>Propiedades>Configuracion avanzada del sistema>variables de entorno>
en este punto agregas a las variables de tu usuario la ruta de instalacion de JAVA con el nombre de variable "JAVA_HOME" y en la variable Path de tu entorno agregas esta variable %JAVA_HOME%

Puedes probar si ya tienes java instalado y puesto en las variables de entorno entrando al cmd de tu sistema y colocando "Java -version" y te debe aparecer tu version que instalaste

Decargar todo el archivo Zip y hacer las pruebas pertinentes

Una vez tienes todo el sistema y el repositorio clonado puedes empezar a hacer pruebas si te falta alguna libreria por instalar lo haces de igual manera a como se menciono anteriormente

Como usar el repositorio
el repositorio viene ordenado por modulos estos no deben ejecutarse, el archivo que se debe ejecutar es solamente el main.py de la carpeta del proyecto para que el proceso inicie

El proyecto cuenta con modulo de observabilidad este guarda la información de ejecución del sistema en un documento llamado observabilidad.log, este registra mensajes sobre el progreso y posibles errores en el pipeline el cual puedes verificar si presenta algun posible error o para monitorearlo

Modulos

modules/etl_pipeline.py
Modulo principal que maneja todo el flujo del pipeline.Usa funciones de los otros modulos para la carga,limpieza y transformación de los datos

modules/obsevabilidad.py
Modulo encargado de la configuracion del logger, el cual captura los mensajes y eventos generadors en la ejecución

modules/load_data.py
Contiene las funciones encargadas de la carga de los datos desde el archivo Films_2 (3).xlsx

modules/clean_data.py
Contiene las funciones para aplicar la limpieza de los datos mas que todo numericos

modules/transform_data.py
Modulo en el que se aplican las funciones para transformación de los datos, como la creación de nuevas columnas,agregación de la informacion entre otros

main.py
Archivo que se debe ejecutar para el proceso ETL, maneja todas las funciones de los demas modulos




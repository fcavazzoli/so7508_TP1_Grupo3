# TP_1 2C_2019 GRUPO 3

## DESCRIPCION:
 Grupo formado por:
 
 - Perez Flavio
 - Cavazzoli Federico
 - Emanuel 
 
 En este documento de detallaran los pasos a seguir para instalar correctamente el paquete que esta incluido en el repositorio: `TPGRUPO3.tar.gz`.
 
---
# Indice
 - [Instalacion](#instalacion)
  * [Descarga del contenido:](#descarga-del-contenido-)
    + [Path de descarga.](#path-de-descarga)
  * [Desempaquetar paquete:](#desempaquetar-paquete-)
  * [Instalacion:](#instalacion-)
- [Uso del programa](#uso-del-programa)
  * [Ejecucion:](#ejecucion-)
    + [Log files](#log-files)
  * [Start file](#start-file)
  * [Stop file](#stop-file)

---

# Instalacion

## Descarga del contenido:
 
  Lo primero que se debe hacer es descargar el contenido de este repositorio a un ambiente local.
  
### Path de descarga.

  Precondicion: el usuario debe contar con git instalado en su computadora. De no ser este el caso se puede seguir el tutorial que propiociona la misma empresa GitHub en el siguiente link: 
  https://gist.github.com/derhuerst/1b15ff4652a867391f03
 
  Para esto puede crearse una carpeta en el directorio que el usuario considere mas comodo, usando el comando mkdir
 
 `mkdir [nombre_de_la_carpeta]`
 
  Luego se debe indicar que esta carpeta trabajara con un entorno remoto de git.
  
  `git init`
  
  Para luego descargar todos los archivos del repositorio:
  
  `git clone https://github.com/fedecavazzoli/so7508_TP1_Grupo3.git`

  El repositorio tiene permisos publicos por lo que cualquier persona puede clonar su contenido, los permisos de edicion si resultan ser privados.

## Desempaquetar paquete:

  Una vez clonado el repositorio se podran ver los archivos utilizando el comando `ls`.
  Para descomprimir el instalador basta con correr la instruccion:

  `tar -xzvf TPGRUPO03.tar.gz`

  Esto nos generará una carpeta nueva llamada TPGRUPO03 a la cual debemos ingresar haciendo 

  `cd TPGRUPO03`

  En este punto podemos decir que el paquete ya esta descomprimido en nuestro ambiente de trabajo y estamos posicionados correctamente para ejecutarlo.

## Instalacion:

  Para iniciar la instalacion del programa debe ejecutarse el archivo `install.sh` utilizando el siguiente comando:

  `sh intall.sh`

  A patir de este momento puede seguirse leyendo las intrucciones desde la lina de comando ya que el instalador proporciona la informacion necesaria para el usuario pero de todas maneras seran explicadas a continuacion en este README.md.

  Esto da inicio a la instalacion interactiva del programa. 
  Lo primero que nos preguntará será el nombre que deseamos establecer para el directorio de ejecutables, esto queda a gusto del usuario completamente. Simplemente se debe escribir un nombre

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_EJECUTABLES`

  Luego nos pedira que ingresemos un nombre para el directorio donde se guardaran los archivos maestros del programa, al igual que el paso anterior solo debemos ingresar un nombre en la linea de comandos.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_MAESTROS`

  A continuacion nos será solicitado un nombre para el directorio de los archivos de novedades. Tambien debemos ingresar cualquier nombre deseado por lista de comandos.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES`

  Acto seguido se nos solicitara un nombre para el directorio de novedades aceptadas. El cual se ingresa por linea de comados y es a gusto del usuario.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES_ACEPTADAS` 

  Luego se nos pediraá un nombre para un directorio donde se guarden novedades rechadazas.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES_RECHAZADAS`

  A continuacion se solicitara ingresar un nombre para las novedades procesadas.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES_PROCESADAS`

  Luego se le solicitará al usuario que ingrese un nombre para el directorio donde se guarden los archivos de salida.

  `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES_PROCESADAS`

  Llegado este punto ya el script de instalacion tiene toda la informacion necesaria para relizar la instalación del programa y nos preguntará si deseamos confirmar la instalacion a lo que ingresaremos `s` y el script creará todos los directorios con los permisos correspondietes.

  En el caso de elegir `n` se pregunta si se desea continuar la instalacion, a lo que si se le responde `s` la instalacion se reinicia y se le pregunta al usuario el nombre de los directorios nuevamente.

  Llegado este punto la instalacion ya finalizó.


# Uso del programa
  
  Para utilizar el software el usuario debe dirigirse a la carpeta donde se encuentran los archivos ejecutables.

  A partir de este momento llamaremos `bin` al directorio al que el usuario se le pidio que ingrege un nombre para los archivos ejecutables es decir, cuado el intalador requirió de la informacion `NOMBRE_DESEADO_PARA_EL_DERECTORIO_EJECUTABLES`

  `bin = {NOMBRE_DESEADO_PARA_EL_DERECTORIO_EJECUTABLES}`

## Ejecucion:

  acceder a la carpeta de arcivos ejecutables:

  `cd bin`

  Luego hay que inicializar el ambiente. 
  Para hacerlo basta con hacer el siguiente comando.

  `sh init.sh`

---

### Log files

  Llegado este momento, es necesario aclararle al usuario que cualquier inconveniente durante el uso del programa sera registrado mediante un logger en archivos con nombres pertinentes al tipo de log que se realice. Todos estos archivos pueden ser encontrados en la carpeta config a la cual se accede haciendo:

  `cd config/log` 
  (si es que se esta parado en la carpeta raiz del programa)

---
  Siguiendo con el uso del programa:

  Ahora que el programa se esta corriendo, simplemente hay que darle informacion para procesar. Para hacer esto se deben llevar archivos a la carpeta `NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES` que a partir de ahora llamaremos `novedades` es decir 

  `novedades = {NOMBRE_DESEADO_PARA_EL_DERECTORIO_NOVEDADES}`

  Es posible realizar esto con el comando `cp` que provee el sistema operativo.

  `cp source destination`.

  En nuestro caso, `destination` sera la carpeta ubicada en `TPGRUPO03/novedades` y como archivo fuente podemos tomar como ejemplo, los lotes ubicados en `TPGRUPO03/TP/Lotes\ de\ prueba`. Es decir que el comando completo quedaria de la forma:

  `cp novedades TP/Lotes\ de\ prueba/Lote_XX`
  (en el caso de que el usuario ya este parado en la carpeta TPGRUPO03)

  Luego se debe esperar a que el proceso que esta en ejecucion capte el archivo nuevo que se encuentra  ahora en `novedades` y este lo procesara y lo dejara en la carpeta correspondiente.
  Esto se realiza mientras se hacen los logs correspondientes, por lo que el usuario puede ir a ver en cualquier momento que es lo que pasó durante la ejecución del programa simplemente viendo el logfile.

## Start file

  Una vez iniciada la ejecucion con el archivo `init.sh` podemos ver si esta se encuentra efecticamente funcionando abriendo una nueva terminal y ejecuntando 

  `sh start.sh` en la carpeta `bin`
  
  si el proceso ya existe la consola nos dirá algo del tipo:

  `El proceso ya esta corriendo: PID: XXXX`

## Stop file

  Si se desea interrumpir la ejecucion del proceso se debe llamar a la ejecucion del arichivo `stop.sh` que se encuentra dentro de la carpeta `bin` haciendo

  `sh stop.sh`

  Otra opcion es matar el proceso con un comando que provee el sistema operativo como 

  `kill -p [PID]`.

  Pero se recomienda utilizar `stop.sh` que es un archivo que fue pensado para esta tarea y antes de terminar la ejecucion, escribe los archivos de log de forma correspondiente.


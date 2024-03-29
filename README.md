# TP_1 2C_2019 GRUPO 3

## DESCRIPCION:
 Grupo formado por:
 
 - Perez Flavio
 - Cavazzoli Federico
 - Emanuel 
 
 En este documento de detallaran los pasos a seguir para instalar correctamente el paquete que esta incluido en el repositorio: `TPGRUPO3.tar.gz`.
 
---
# Indice
 - [Requisitos](#requisitos)
 - [Instalación](#instalacion)
  * [Descarga del contenido:](#descarga-del-contenido-)
    + [Path de descarga.](#path-de-descarga)
  * [Desempaquetar paquete:](#desempaquetar-paquete-)
  * [Instalación:](#instalacion-)
- [Uso del programa](#uso-del-programa)
  * [Ejecución:](#ejecucion-)
    + [Log files](#log-files)
  * [Stop file](#stop-file)
  * [Start file](#start-file)

---

# Requisitos/Restricciones

  - Contar como sistema operativo alguna distribucion de linux.
  - Una vez inicializado el ambiente con el comando init.sh, se deben ejecutar los siguientes comandos utilizando la misma 
  terminal. Cambiar de terminal llevaría al usuario a tener que reinicializar el ambiente.
  
# Instalación

## Descarga del contenido:
 
  Lo primero que se debe hacer es descargar el contenido de este repositorio a un ambiente local.
  
### Path de descarga.

  Precondición: el usuario debe contar con git instalado en su computadora. De no ser este el caso se puede seguir el tutorial 
  que proporciona la misma empresa GitHub en el siguiente link: 
  https://gist.github.com/derhuerst/1b15ff4652a867391f03
  
  El usuario debe abrir la terminal en el directorio donde desee trabajar. Para esto debe navegar hasta ese directorio      
  utilizando la interfaz grafica de linux. Luego, hacer click derecho en la pantalla del directorio y seleccionar la opcion 
  'Abrir terminal'. 
  
   Otra opción es teclear CTRL+ALT+T, lo que abrirá una terminal en el directorio home. Abierta la terminal ingresar el   
   comando 
   
   `cd [directorio_de_trabajo]`
   
   siendo [directorio_de_trabajo] el nombre del directorio donde se desee trabajar.
   
  Una vez que tenemos la terminal abierta en el directorio donde deseamos trabajar, continuamos con la descarga
  del repositorio.
 
  Para esto puede crearse una carpeta en el directorio que el usuario considere mas comodo, usando el comando mkdir
 
 `mkdir [nombre_de_la_carpeta]`
 
  Luego se debe indicar que esta carpeta trabajara con un entorno remoto de git.
  
  `git init`
  
  Para luego descargar todos los archivos del repositorio:
  
  `git clone https://github.com/fedecavazzoli/so7508_TP1_Grupo3.git`

  El repositorio tiene permisos públicos por lo que cualquier persona puede clonar su contenido, los permisos de edición si
  resultan ser privados.

 Si el usuario no tuviera instalado git en su computadora, y no se encontrara en condiciones de instalarlo, puede descargar 
 el .zip con el contenido del repositorio desde https://github.com/fedecavazzoli/so7508_TP1_Grupo3.git y descomprimirlo en el    
 directorio donde desee comenzar la instalación.

## Desempaquetar paquete:


  Una vez clonado el repositorio se podrán ver los archivos utilizando el comando `ls`.
  Para descomprimir el instalador basta con correr la instrucción:

  `tar -xzvf TPGRUPO03.tar.gz`

  Esto nos generará una carpeta nueva llamada TPGRUPO03 a la cual debemos ingresar haciendo 

  `cd TPGRUPO03`

  En este punto podemos decir que el paquete ya esta descomprimido en nuestro ambiente de trabajo y estamos posicionados correctamente para ejecutarlo.

## Instalación:

  Para iniciar la instalación del programa debe ejecutarse el archivo `install.sh` utilizando el siguiente comando:

  `sh intall.sh`

  A partir de este momento puede seguirse leyendo las instrucciones desde la linea de comando ya que el instalador proporciona la información necesaria para el usuario pero de todas maneras serán explicadas a continuación en este README.md.

  Esto da inicio a la instalación interactiva del programa. 
  Lo primero que nos preguntará será el nombre que deseamos establecer para el directorio de ejecutables, esto queda a gusto del usuario completamente. Simplemente se debe escribir un nombre

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_EJECUTABLES`

  Luego nos pedirá que ingresemos un nombre para el directorio donde se guardaran los archivos maestros del programa, al igual que el paso anterior solo debemos ingresar un nombre en la linea de comandos.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_MAESTROS`

  A continuación nos será solicitado un nombre para el directorio de los archivos de novedades. También debemos ingresar cualquier nombre deseado por lista de comandos.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES`

  Acto seguido se nos solicitara un nombre para el directorio de novedades aceptadas. El cual se ingresa por linea de comandos y es a gusto del usuario.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES_ACEPTADAS` 

  Luego se nos pedirá un nombre para un directorio donde se guarden novedades rechazadas.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES_RECHAZADAS`

  A continuación se solicitara ingresar un nombre para las novedades procesadas.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES_PROCESADAS`

  Luego se le solicitará al usuario que ingrese un nombre para el directorio donde se guarden los archivos de salida.

  `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_DE_SALIDA`

  Llegado este punto ya el script de instalación tiene toda la información necesaria para realizar la instalación del programa y nos preguntará si deseamos confirmar la instalación a lo que ingresaremos `s` y el script creará todos los directorios con los permisos correspondientes.

  En el caso de elegir `n` se pregunta si se desea continuar la instalación, a lo que si se le responde `s` la instalación se reinicia y se le pregunta al usuario el nombre de los directorios nuevamente.

Llegado este punto la instalación ya finalizó.

Como resultado del proceso de instalación se genera la estructura especificada en el arbol de estructura del Documento de TP, que se encuentra tambien en este repositorio.

Si por alguna razón, se produce algún cambio en la configuracion generada por la instalación, que afecte el correcto funcionamiento del programa, puede correrse nuevamente este comando utilizando la opción -r

`sh install.sh -r` 

# Uso del programa
  
  Para utilizar el software el usuario debe dirigirse a la carpeta donde se encuentran los archivos ejecutables.

  A partir de este momento llamaremos `bin` al directorio al que el usuario se le pidió que ingrese un nombre para los archivos ejecutables es decir, cuando el instalador requirió de la información `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_EJECUTABLES`

  `bin = {NOMBRE_DESEADO_PARA_EL_DIRECTORIO_EJECUTABLES}`

## Ejecución:

  acceder a la carpeta de archivos ejecutables:

  `cd bin`

  Luego hay que inicializar el ambiente. 
  Para hacerlo basta con hacer el siguiente comando.

  `. ./init.sh`
  
  Si el ambiente consigue inicializarse correctamente (esto será registrado en los archivos de log) el proceso init llamará al 
  comando start.sh, que a su vez invocará al comando process.sh, dando comienzo al proceso.
 
  Si el ambiente no logra inicializarse correctamente, el comando init mostrará la razón por la que no pudo inicializar el 
  ambiente.
 
---

### Log files

  Llegado este momento, es necesario aclararle al usuario que cualquier inconveniente durante el uso del programa sera registrado mediante un logger en archivos con nombres pertinentes al tipo de proceso que se realice. Todos estos archivos pueden ser encontrados en la carpeta config a la cual se accede haciendo:

  `cd config/log` 
  (si es que se esta parado en la carpeta raíz del programa)

---
  Siguiendo con el uso del programa:

  Ahora que el programa se esta corriendo, simplemente hay que darle información para procesar. Para hacer esto se deben llevar archivos a la carpeta `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES` que a partir de ahora llamaremos `novedades` es decir 

  `novedades = {NOMBRE_DESEADO_PARA_EL_DIRECTORIO_NOVEDADES}`

  Es posible realizar esto con el comando `cp` que provee el sistema operativo.

  `cp source destination`.

  En nuestro caso, `destination` sera la carpeta ubicada en `TPGRUPO03/novedades` y como archivo fuente podemos tomar como ejemplo, los lotes ubicados en `TPGRUPO03/TP/Lotes\ de\ prueba`. Es decir que el comando completo quedaría de la forma:

  `cp novedades TP/Lotes\ de\ prueba/Lote_XX`
  (en el caso de que el usuario ya este parado en la carpeta TPGRUPO03)

  Luego se debe esperar a que el proceso que esta en ejecución capte el archivo nuevo que se encuentra  ahora en `novedades` y este lo procesara y lo dejara en la carpeta correspondiente.
  Esto se realiza mientras se hacen los logs correspondientes, por lo que el usuario puede ir a ver en cualquier momento que es lo que pasó durante la ejecución del programa simplemente viendo el logfile del proceso deseado.
  
  Además de los logs, si los archivos de novedades procesados contaban con un formato valido (segun lo especificado por el enunciado del TP) y registros para procesar, puede verse la salida de los mismos en los archivos de la carpeta `NOMBRE_DESEADO_PARA_EL_DIRECTORIO_DE_SALIDA`.

## Stop file

  Si se desea interrumpir la ejecución del proceso se debe llamar a la ejecución del archivo `stop.sh` que se encuentra dentro de la carpeta `bin` haciendo

  `sh stop.sh`

  Otra opción es matar el proceso con un comando que provee el sistema operativo como 

  `kill -p [PID]`.

  Pero se recomienda utilizar `stop.sh` que es un archivo que fue pensado para esta tarea y antes de terminar la ejecución, escribe los archivos de log de forma correspondiente.

## Start file

  Una vez iniciada la ejecución con el archivo `init.sh` podemos ver si esta se encuentra efectivamente funcionando abriendo una nueva terminal y ejecutando 

  `sh start.sh` en la carpeta `bin`
  
  si el proceso ya existe la consola nos dirá algo del tipo:

  `El proceso ya esta corriendo: PID: XXXX`

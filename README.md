# MFM

CONFIGURACIÓN INICIAL DE GIT

.git config --global user.name "nombre"
.git config --global user.email "correo electrónico"
.git config --list
  Este comando muestra todas las configuraciones hechas anteriormente.

Archivo ".gitignore"
  Cuando creamos este documento dentro de un repositorio nos permite nombrar dentro de este aquello archivos, carpetas o ficheros que     queremos ignorar, por ende GIT no hará ningun proceso con el.



COMANDOS BÁSICOS DE CMD/UNIX

.cd "nombre del archivo"
  Este comando permite movilizarnos a través de los archivos del computador. Si vamos entrar a una carpeta cuyo archivo esta compuesto     por mas de una palabras es necesario utilizar las comillas, además, es obligatorio outilizar "/" para separar el nombre de las         
  carpetas.

.cd..
  Su uso nos permite devolvernos a la carpeta anterior.

.cls/clear
  Limpia la interfaz de los comandos y respuestas hechas anteriormente.

.dir/ls
  Nos muestra todo los ficheros, archivos o carpetas que hay en la ruta en donde nos encontramos posicionados.

.pwd
  Muestra la ruta en la que nos encontramos posicionados.



COMANDOS BÁSICOS DE GIT
.git init
  Este comando convierte un proyecto, carpeta o ficehero local en un repositorio de GIT.
  
.git add.
  Luego de que un archivo esté modificado es adjuntado o añadido con este comando para hacer parte de la siguiente versión local del       repositorio.
  
.git status.
  Este comando nos permite ver los archivos que tenemos dentro del proyecto y su respectivo estado. No todos los archivos que son         mostrados aquí hacen parte del repositorio, pues esa petición la tenemos que hacer específicamente con el comando anterior. Para         identificar los diferentes estados en los que se pueden encontrar los archivos, GIT muestra los nombres con dos color diferentes y los   divide en tres secciones. La primera son aquellos ficheros que están dentro de nuestro proyecto pero aún no han sido añadidos a         nuestro repositorio local, esto se puede presetar por el hecho de que este fichero lo creamos luego de nuestra última versión y no lo   hemos añadido con el comando "git add" y adjuntado a una versión local con el comando "git commit" o simplemente no queremos que haga   parte del repositorio local (si no queremos ver este fichero al momento de utilizar el comando "git status" podemos agregar su nombre   en el archivo .gitignore) por esto se muestra en color rojo. El segundo tipo de fichero es aquel que ya hace parte de nuestro           repositorio local, lo hemos modificado pero aun no hemos ejecutado el comando "git add" sobre él, puede ser porque aun no esté listo y   por ende no puede ser seleccionado aún para ser parte de la nueva version local, este también en color rojo. El tercer tipo de fichero   es aquel que se muestra en color verde indicando que es un archivo que ha sido modificado, terminado, y está listo para hacer parte     de una nueva version local del poyecto.
  
.git commit -m "Comentario o descripción"
  Al ejecutar este comando se unen todos los archivos que ya han sido modificados, están terminados y pueden hacer parte de la nueva       version local del repositorio.

.git checkout "nombre del archivo"
  Su utilidad nos permite regresar los cambios hecos en un fichero siempre y cuando no hayamos hecho uso del comando "git add".

.git diff "nombre del archivo"
  Identifica y muestra los cambios especificos hechos en un documento en el cual no se ha utilizado el comando "git add".

.git branch
  Nos permite visualizar la rama en la que estamos ubicados. Por defecto GIT nos crea una rama llamada "master" la cual contiene todo el   proyecto tontal local como en la nube.

.git branch "nombre de la nueva rama"
  Una rama alternativa en nuestro proyecto puede ayudarnos a contener una copia de seguridad. Además, con la construcción de varias       ramas, podemos separar el proyecto por grupos de trabajo definidos, que trabajarán en un módulo específico y cuando sea necesario       hacer una integración más ordenada a la rama principal o master.

.git log
  Muestra la información especifica de cada versión local realizada en la rama en la que estamos posicionados. (Salimos de esta           información con la tecla q).
  
.git checkout "nombre de la rama"
  Me permite desplazarme a través de las diferentes ramas.

.git remote add origin "ruta de repositorio en la nube"
  Se usa para indicarle a GIT cual es la ruta en la nube que contendrá todo el repositorio local. Al ubicarlo en un espacio como este,     estamos facilitando el acceso a otros miembros del equipo, los cuales puede clonar, descargar, modificar y volver a adjuntar el         proyecto de manera remota y al tiempo.

.git push -u origin "nombre de la rama"
  Une todos los commit hechos en una rama específica y hace una carga hacia la nube.

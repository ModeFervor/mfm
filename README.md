# Mode Fervor Management

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

[Proyecto individual]

.git clone "URL con la ruta del repositorio"
  Nos permite cloar un repositorio alojado en la nube directamente a un lugar indicado por nosotro en nuestro computador.
  
.git init
  Este comando convierte un proyecto, carpeta o ficehero local en un repositorio de GIT.
  
.git add.
  Luego de que un archivo esté modificado es adjuntado o añadido con este comando para hacer parte de la siguiente versión local del       repositorio.
  
.git status.
  Este comando nos permite ver los archivos que tenemos dentro del proyecto y su respectivo estado. No todos los archivos que son         mostrados aquí hacen parte del repositorio, pues esa petición la tenemos que hacer específicamente con el comando anterior. Para         identificar los diferentes estados en los que se pueden encontrar los archivos, GIT muestra los nombres con dos color diferentes y los   divide en tres secciones. La primera son aquellos ficheros que están dentro de nuestro proyecto pero aún no han sido añadidos a         nuestro repositorio local, esto se puede presetar por el hecho de que este fichero lo creamos luego de nuestra última versión y no lo   hemos añadido con el comando "git add" y adjuntado a una versión local con el comando "git commit" o simplemente no queremos que haga   parte del repositorio local (si no queremos ver este fichero al momento de utilizar el comando "git status" podemos agregar su nombre   en el archivo .gitignore) por esto se muestra en color rojo. El segundo tipo de fichero es aquel que ya hace parte de nuestro           repositorio local, lo hemos modificado pero aun no hemos ejecutado el comando "git add" sobre él, puede ser porque aun no esté listo y   por ende no puede ser seleccionado aún para ser parte de la nueva version local, este también en color rojo. El tercer tipo de fichero   es aquel que se muestra en color verde indicando que es un archivo que ha sido modificado, terminado, y está listo para hacer parte     de una nueva version local del poyecto.
  
.git commit -m "Comentario o descripción"
  Al ejecutar este comando se unen todos los archivos que ya han sido modificados, están terminados y pueden hacer parte de la nueva       version local del repositorio.
  
.git commit --amend -m "comentario nuevo"
  Corrije el comentario de un commit añadido anteriormente a una version del repositorio local.

.git log
  Muestra la información especifica de cada versión local realizada en la rama en la que estamos posicionados. (Salimos de esta           información con la tecla q).

.git log > commit.txt
  Crea un archivo txt con la información de todos los commit generados.

.git checkout "nombre del archivo"
  Su utilidad nos permite regresar los cambios hechos en un fichero siempre y cuando no hayamos hecho uso del comando "git add".
  
.git checkout "código SHA"
  Entre la información que muestra el comando "git log", tenemos un código SHA hexadecimal único que identifica cada uno de los commit     generados en la rama en la que estamos posicionados, al ejecutar entonces esta línea de código podremos viajar en el tiempo,             regresando el proyecto a versiones o commit anteriores. Para regresar al head (último commit generado) simplemente ingresamos el         comando "git checkout master".
  
.git reset --soft "código SHA"
  Cada commit es un punto en la historia del repositorio. Si la última versión generada del proyecto a nivel local no es el resultado     final que esperabamos se puede utlizar este comando, el cual nos regresaria a cualquiera de esos puntos o commit anteriores del         proyecto con la diferencia de que los commit entre el head y al que regresamos, se eliminaran. Se aclara que los ficheros quedan         intactos.
  
.git reset --hard "código SHA"
  Este comando al igual que el anterior borra los commit entre el head y al que nos regresamos, pero a diferencia del anterior,   este     si elimina los ficheros y modificaciones realizadas en el código por lo que nunca más podremos volver a recuperar esa                   información.

.git diff "nombre del archivo"
  Identifica y muestra los cambios específicos hechos en un documento en el cual no se ha utilizado el comando "git add".

.git branch
  Nos permite visualizar la rama en la que estamos ubicados. Por defecto GIT nos crea una rama llamada "master" la cual contiene todo el   proyecto tontal local como en la nube.
  
.git branch -
  Nos permite visualizar la rama en la que estamos ubicados y aquellas que se encuentran ocultas.

.git branch "nombre de la nueva rama"
  Una rama alternativa en nuestro proyecto puede ayudarnos a contener una copia de seguridad. Además, con la construcción de varias       ramas, podemos separar el proyecto por grupos de trabajo definidos, que trabajarán en un módulo específico y cuando sea necesario       hacer una integración más ordenada a la rama principal o master.
  
.git checkout -b "nombre de la rama"
  Además de crear una rama alternativa, también nos posiciona inmediatamente sobre ella.
  
.git branch -D "nombre de la rama"
  Elimina aquella rama que ya no está en uso.
  
.git checkout "nombre de la rama"
  Me permite desplazarme a través de las diferentes ramas.
  
.git merge "nombre de la rama absorvida"
  Si además de la rama principal en la que tenemos contenido el proyecto, creamos otra que será de pruebas, ambas trabajarán con commit   diferentes y estos no se juntaran a menos que lo indiquemos. Primero debemos posicionarnos en la rama que absorverá los cambios o       pruebas de la rama alterna, para este ejemplo será "master" la que hará el proceso y "alterna" es donde haremos las pruebas y           modificaciones terminada y listas para ser adjuntadas a la versión final del proyecto en el rama principal, entonces accionamos el       comando "git checkout master" y luego "git merge alterna".

.git remote add origin "ruta de repositorio en la nube"
  Se usa para indicarle a GIT cual es la ruta en la nube que contendrá todo el repositorio local. Al ubicarlo en un espacio como este,     estamos facilitando el acceso a otros miembros del equipo, los cuales puede clonar, descargar, modificar y volver a adjuntar el         proyecto de manera remota y al tiempo.
  
.git remote -v
  Nos permite ver la conexión entre el repositorio local y el que está en la nube.
  
.git remote remove origin
  Elimina la conexión entre el repositorio local y el que está en la nube.
  
.git push -u origin "nombre de la rama"
  Une todos los commit hechos en una rama específica y hace una carga hacia la nube.
  
.git push -u origin "nombre de la rama" -f
  Fuerza a subir los cambios al repositorio en la nube cuando el número de commit son los mismos pero quizás la información de alguno de   como el comentario adjunto, ha cambio.
  
.git tag -a v1.0 -m "comentario" "código SHA"
  Esta etiqueta es otorgado a un commit con la intención de tener un historial de las versiones del repositorio.
  
.git push origin "versión"
  Este comando nos permite subir al repositorio en la nube el tag otorgado a un commit.
  
.git push origin tags
  Este comando nos permite subir al repositorio en la nube los tags otorgado a los diferentes commit.

[Fin]

[Proyecto compartido]

.Desplazarnos a la pestañas settings que está en el repositorio en GitHub.

.Seleccionar la opción situada al finalizar llamada "transferir".

.Ingresar repositorio y usuario u organización al cual se va a transferir el proyecto.

.Eliminar la conexión existente entre el proyecto y la URL donde se almanenaba el repositorio en la nube anteriormente con el comando "git remote remove origin".

.Crear una nueva conexión utlizando el comando "git remote add origin "URL con la ruta del repositorio"".

  [Pasos para el nuevo integrante]

  .Clonar el repositorio alojado en la nube hacia un espacio indicado por nosotros en el computador local usando el comando "git clone      "URL con la ruta del repositorio"".
  
  [Fin]
  
[Clonar cambios de otro miembro del equipo]
.Antes de hacer cualquier subida al repositorio en la nube de algún nuevo cambios, el sistema GIT valida si no hay algún cambio hecho ya por algún otro miembro del equipo.

.git fetch origin
  Esto hará que los cambios hechos por otro miembro del equipo pasen a una rama oculta llamada origin/master a la cual accederemos para   copiar dichos cambios.
   
.git merge origin/master
  Fusiona los cambios descargados con el comando anterior con nuestro proyecto, de esta manera GIT nos permitirá hacer "push" sin         problema.
   
[Fin]

[Fin]

[Creación de página web con GitHub para proyectos personales]



[Fin]

[Creación de página web con GitHub para proyectos grupales]

.git branch gh-pages
  Nos permitirá crear una nueva rama la cual indicaremos a GitHub que cree una página web bajo sus dominios. "'nombre de la               comunidad.gitgub.io/'nombre del repositorio''".

[Fin]


  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  


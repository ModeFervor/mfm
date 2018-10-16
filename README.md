# Mode Fervor Management

[¿QUÉ ES GIT?]

Sistema de control de versiones manteniendo un historial de cambios en tu código fuente permitiendonos volver a estados anteriores, además permite trabajar en paralelo con otros mienbros del equipo de desarrollo, con el uso de versiones en el tiempo.


[CREAACION DE REPOSITORIOS]






[COMANDO BÁSICOS DE CMD/UNIX]

.cd "nombre del archivo"
  .Este comando permite movilizarnos a través de los archivos del computador. Si vamos entrar a una carpeta cuyo archivo esta compuesto    por mas de una palabras es necesario utilizar las comillas, además, es obligatorio outilizar "/" para separar el nombre de las          carpetas.

.cd..
  .Su uso nos permite devolvernos a la carpeta anterior.

.cls/clear
  .Limpia la interfaz de los comandos y respuestas hechas anteriormente.

.dir/ls
  .Nos muestra todo los ficheros, archivos o carpetas que hay en la ruta en donde nos encontramos posicionados.

.ls -a
  .Nos muestras aquellos ficheros ocultos en la ruta en la que estamos posicionados.
  
.pwd
  .Muestra la ruta en la que nos encontramos posicionados.
  
.mkdir "nombre del aarchivo"
  .Crea una carpeta en la ruta en la que estamos ubicados
  
.rmdir "nombre del archivo"
  .Elimina un fichero en la ruta en la que estamos ubicados


COMANDOS BÁSICOS DE GIT

.git
  Muestra los subcomandos que vienen con git.
  
.git config --global user.name "nombre" 
.git config --global user.email "correo electrónico"
.git config --list
  Este comando muestra todas las configuraciones hechas anteriormente.
Archivo ".gitignore"
  Cuando creamos este documento dentro de un repositorio nos permite nombrar dentro de este aquello archivos, carpetas o ficheros que     queremos ignorar, por ende GIT no hará ningun proceso con el.

[Vocabulario básico ]

[Proyecto individual]

.git rm "nombre del achivo" -f
  Elimina un archivo de la ruta en la que estamos posicionados.
  
.git clone "URL con la ruta del repositorio"
  Nos permite cloar un repositorio alojado en la nube directamente a un lugar indicado por nosotro en nuestro computador.
  
.git init
  Este comando convierte un proyecto, carpeta o ficehero local en un repositorio de GIT.
  
.git status.
  Este comando nos permite ver los archivos que tenemos dentro del proyecto y su respectivo estado. Para identificar los diferentes       estados en los que se pueden encontrar los archivos, GIT muestra los nombres con dos color diferentes. Lo archivos en color rojo son     aquellos que están en modificación y no están listos para ser añadidos al próximo commit. Los verdes son aquellos que sus               modificaciones ya concluyeron y están esperando la indicación para ser agregados a un commit.
  
.git add.
  Luego de que un archivo esté modificado es adjuntado o añadido con este comando para hacer parte de la siguiente versión local del       repositorio.
  
.git commit -m "Comentario o descripción"
  Al ejecutar este comando se unen todos los archivos ubocados en el stage, que ya han sido modificados o aquellos que están en el         tercer estado o pueden hacer parte de la nueva version local del repositorio.
  
.git commit --amend -m "comentario"
  Un commit registra o adjunta uno o varios cambios. Dado el caso de que ejecutemos un commit pero se nos haya olvidado adjuntar un       cambio más, podemos añadir ese cambio no agregado al "stage area" o al segundo estado utilizando este comando. Así GIT lo que hace es   retornar el último commit, adjuntar el nuevo cambio que está en el stage area y volverse a ejecutar ofreciendo también la opción de     cambiar el comentario adjunto.

.git log
  Muestra la información especifica de cada versión local realizada en la rama en la que estamos posicionados. (Salimos de esta           información con la tecla q).

.git log > commit.txt
  Crea un archivo txt con la información de todos los commit generados.

.git diff "nombre del archivo"
  Identifica y muestra los cambios específicos hechos en un documento mientras se encuentre en el stage area

.git checkout "nombre del archivo"
  Su utilidad nos permite regresar los cambios hechos en un fichero que no se encuentre en el stage area.
  
.git checkout "código SHA"
  Entre la información que muestra el comando "git log", tenemos un código SHA hexadecimal único que identifica cada uno de los commit     generados en la rama en la que estamos posicionados, al ejecutar entonces esta línea de código podremos viajar en el tiempo,             regresando el proyecto a versiones o commit anteriores. Para regresar al head (último commit generado) simplemente ingresamos el         comando "git checkout master".

.git reset "código SHA"
  Al ejecutar este comando podremos posicionarnos en el commit correspondiente al código SHA ingresado, borrando solamente las acciones     commit y retirando los archivos de stage area sin modificarlos.
  
.git reset HEAD or HEAD "nombre del archivo"
  Retorna todos los archivos del stage area para que pueda seguir siendo modificado.
  
.git reset --
  Retrona todos los archivos del stage area para que pueda seguir siendo modificado.
  
.git reset "nombre del archivo"
  Retira un archivo del stage area para que pueda seguir siendo modificado.
  
.git reset --soft "código SHA"
  Nos regresa al commit correspondiente al código SHA ingresado, pone los archivos en el stage area y nos señala las modificaciones que     habíamos hecho en el commit 
  
.git reset --hard "código SHA"
  Posiciona el proyecto en la version del commit perteneciente al código SHA ingresado en el comando y borra todos los commit que se       hicier luego de este incluyendo el código hecho en este.
  
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


[Proyecto compartido]

.Desplazarnos a la pestañas settings que está en el repositorio en GitHub.

.Seleccionar la opción situada al finalizar llamada "transferir".

.Ingresar repositorio y usuario u organización al cual se va a transferir el proyecto.

.Eliminar la conexión existente entre el proyecto y la URL donde se almanenaba el repositorio en la nube anteriormente con el comando "git remote remove origin".

.Crear una nueva conexión utlizando el comando "git remote add origin "URL con la ruta del repositorio"".

  [Pasos para el nuevo integrante]

  .Clonar el repositorio alojado en la nube hacia un espacio indicado por nosotros en el computador local usando el comando "git clone      "URL con la ruta del repositorio"".
  
  
[Clonar cambios de otro miembro del equipo]
.Antes de hacer cualquier subida al repositorio en la nube de algún nuevo cambios, el sistema GIT valida si no hay algún cambio hecho ya por algún otro miembro del equipo.

.git fetch origin
  Esto hará que los cambios hechos por otro miembro del equipo pasen a una rama oculta llamada origin/master a la cual accederemos para   copiar dichos cambios.
   
.git merge origin/master
  Fusiona los cambios descargados con el comando anterior con nuestro proyecto, de esta manera GIT nos permitirá hacer "push" sin         problema.


[Creación de página web con GitHub para proyectos personales]




[Creación de página web con GitHub para proyectos grupales]

.git branch gh-pages
  Nos permitirá crear una nueva rama la cual indicaremos a GitHub que cree una página web bajo sus dominios. "'nombre de la               comunidad.gitgub.io/'nombre del repositorio''".

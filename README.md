# Creación y sincronización de repositorio con github

### Alumno: 
Anguiano Ayala Alan
### No. de Matrícula:
 2630292

### Objetivo
 Explicar paso a paso el proceso de creación y sincronización de un repositorio en github, desde la creción del repositorio local hasta su sincronización con el repositorio remoto; explicando también el cómo realizar cambios dentro del repositorio de manera local y remota y como reflejar dichos cambios en ambos repositorios
##### Nota: Importante, en el repositorio remoto saldrán más commits de los que se mencion en la practica, esos commits no aportan nada nuevo y son más un producto de la terquedad del creador de este archivo.

## Descripción del proceso
1. Crear un repositorio local en la computadora del usuario.
2.  Crear los archivos .txt y .md necesarios para la práctica
3. realizar los commits necearios para guardar los archivos
4. Crear un repositorio remoto en github.
5. Sincronizar el repositorio local con el repositorio remoto.
6. Utilizar Push para subir los cambios realizados en el repositorio local al repositorio remoto.
7. verficar que los cambios se reflejen en el repositorio remoto y modificar el archivo nuevamente desde el mismo y verficar dichos cambios en el repositorio local.
8. Utilizar Pull para traer los cambios realizados en el repositorio remoto al repositorio local y evaluar que esten correcto
9. Realizar un commit en el repositorio local y utilizar Push para subir los cambios al repositorio remoto y verificar que se reflejen correctamente.
10. Fin

## Descripción de los archivos enviados

### Datos/Texto .txt:

Dependiendo de qué versión mires este archivo podría llamarse Texto, si ves las versiones más antiguas; ó Datos; si mirás la más actual. contiene la evidencia de los 3 cambios hechos a traves de la práctica así como 2 rick rolls que metí por puro humor rancio.

### READNE.md: 

Contiene todo el texto de la práctica, asi como este mismo recuadro, si estas viendo esto signfica o que eres yo, o que mandé el link correcto y lo estas viendo desde github. en todo caso aqupi se concentran toda la información teórica para replicar la suso dicha práctica

## Comandos Git utilizados

- `git init`: Inicializa un nuevo repositorio Git en el directorio actual.
- `git status`: Muestra el estado actual del repositorio, incluyendo los archivos modificados, agregados o eliminados.
- `git add <archivo>`: Agrega un archivo específico al área de preparación (staging area) para su posterior commit.
- `git add -A`: Agrega todos los archivos en la staging zone al área de preparación.
- `git commit -m "mensaje"`: Crea un commit con los cambios agregados al área de preparación, incluyendo un mensaje descriptivo.
- `git remote add origin <url>`: Agrega un repositorio remoto con el nombre "origin" y la URL especificada.
- `git branch -M main`: Cambia el nombre de la rama actual a "main".
- `git push -u origin main`: Sube los cambios del repositorio local al repositorio remoto.
- `git pull -u origin main`: Trae los cambios del repositorio remoto al repositorio local y los fusiona con la rama actual.

## Proceso de creación y sincronización de repositorio con github
Al entrar en terminal nos desplazamos directamente a la ubicación donde haremos nuestro repositorio local

```bash 
$ cd C \ Usuarios\ Alumno\ Desktop
```
Después creamos la carpeta del repositotio local y entramos en ella agregando desde el explorador de archivos el archivo .md y el .txt

```bash
$ mkdir "Practica_sincronizar_Github"
$ cd Practica_sincronizar_Github
```
Una vez dentro de la carpeta desde terminal inicializamos el repositorio local con git init y hacemos git status par verificar que tanto markdown como el .txt esten en el area de untracked files
```bash 
$ git init
$ git status
```
una vez hecho, adicionalemente utilizamos el comando git branch para cambiar el nombre de la rama principal a "main" 
```bash 
$ git branch main
```
una vez esto asegurado usamos `git add -A` y `git commit` para guardar tanto el archivo markdown con el .txt en la base de datos del repositorio

```bash 
$ git add -A
$ git commit -m "Estos son los archivos mínimos para la práctica"
```
Una vez guardados los cambios crearemos el repositorio remoto dentro de Github. En este repositorio será publico y no contendra ningun README, licencia o .gitignore. Una vez creado el repositorio se copiará el url del mismo para sincronzarlo con el repositorio local.
 
Para poder sincronizarlos utilizaremos el comando `Git remote add origin`, este comando se encargará de establecer la ruta por la cual se estaran mandando los commits hechos de manera local. 

```bash 
$ git remote add origin git@github.com:LinuxFakeuser1/Sincronzacion-de-Github_Anguiano_Ayala_Alan.git
```
Una vez conectados utilizamos el comando `git remote -v` para corroborar que sea el repositorio correcto.
```bash 
$ git remote -v`
```
Una vez nos encarguemos de esto nos colocaremos en el repositorio local y haremos nuestro primer subida de datos a nuestro github con el comando `git push`.
```bash 
$ git push origin main 

# Esto hará que todos los cambios confirmados se suban  por medio de internet a Github, más específicamente a nuestro repositorio.
``` 
Vamos al repositorio en github y confirmamos que esté actualizado con los cambios más recientes y una vez que los identifiquemos volveremos  modificar el archivo Datos/Texto .txt de manera que se indique evidente que dicho cambio se realizó desde git hub
```bash 
$ escribir en Datos.txt, "Esta parte del archivo fue modificada en github" o algo así.
```
Ahora se de debe de descargar esos cambios desde github a el repositorio local de nuestra computadora, para ello emplearemos el comando `git pull` cuya función será la de actualizar nuestra base de datos local actual con la versión del repositorio de github.
```bash 
## En terminal:
$ git pull origin main
# Ya
```
Nos vamos a corroborar desde el repositorio local par ver si los cambios dentro del archivo.txt se aplicaron y si es así procedemos nuevamente a modificar una ultima vez el archivo desde el repositorio local, confirmarlo y subirlo nuevamente a github por medio del comando `git push`
```bash
## Dentro del archivo.txt escribir:
$ "Ahora este es el 2do mensaje hecho desde el repositorio local"
## En terminal:
$ git add -A
$ git commit -m "El cambio hecho despues de descargar los cambios hechos desde github, osease el 3er mensaje hecho"
$ git push origin main
## Finalizamos la subida de confirmaciones
```
Con esto finalizamos los pasos para realizar la práctica.

## ¿Qué aprendí? 

Con esta práctica porfin aterrize los conocimientos necesarios para crear, subir y actualizar repositorios en Github, así como familiarizarme más con los comandos de git y Powershell. En general, aumentó mi agilidad y facilidad en el uso de la terminal y me impulsó a investigar más sobre las dudas que tenía sobre algunos comando como el `git remote` en donde directamente no sabía cómo utilizarlo. 
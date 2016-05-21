

## **Ejercicio 1:**


+ **Crear un repositorio en vuestro GitHub**

El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository
![El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository](https://github.com/annalawrenc/Campusciff/blob/master/screens/NewRepository.jpg)

*No he creado ninguno ahora porque ya tengo uno llamado Campusciff que hice en clase*

El repositorio creado se ve as�:
![El repositorio:](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioCampusciff.jpg)



+ **Clonar repositorio en local**

Ya tengo un repositorio de la clase en local, entonces creo otra carpeta para clonar y me situo en ella.

	cd Ejercicio1-2

Despu�s copio la direccion del repositorio del GitHub para poder clonar usando el protocolo SSH
![direccion del repositorio] (https://github.com/annalawrenc/Campusciff/blob/master/screens/CopiarDireccionSSHgit.jpg?)

Para clonar uso el comando git clone con la direcci�n:

	git clone git@github.com:annalawrenc/Campusciff.git

Sale el mensaje de estar clonando y Git pide mi contrase�a:

	Cloning into 'Campusciff'...
	Enter passphrase for key '/c/Users/ania/.ssh/id_rsa':

Una vez introducida la contrase�a el repositorio se acaba de clonar:

	remote: Counting objects: 6, done.
	remote: Compressing objects: 100% (3/3), done.
	remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0
	Receiving objects: 100% (6/6), done.
	Checking connectivity... done.

En la carpeta Ejercicio1-2 veo que se me ha clonado el repositorio
![repositorio clonado](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioClonado.jpg)



+ **Readme**

A�ado al fichero readme.md los pasos y lo a�ado junto con las capturas de pantalla al area de staging

	cd Campusciff
	git add -A

Veo en git status que los ficheros est�n preparados para commit.

	git status
	On branch master
	Your branch is up-to-date with 'origin/master'.
	Changes to be committed:
	  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
        new file:   screens/0000001_stargard-zentrum_980.jpg
        new file:   screens/CopiarDireccionSSHgit.jpg
        new file:   screens/NewRepository.jpg
        new file:   screens/RepositorioCampusciff.jpg
        new file:   screens/RepositorioClonado.jpg




+ **Commit inicial**

Hago el commit inicial:

	git commit -m "commit inicial"

	[master e0eaff9] commit inicial
	 6 files changed, 39 insertions(+), 1 deletion(-)
 	rewrite README.md (100%)
 	create mode 100644 screens/0000001_stargard-zentrum_980.jpg
 	create mode 100644 screens/CopiarDireccionSSHgit.jpg
 	create mode 100644 screens/NewRepository.jpg
 	create mode 100644 screens/RepositorioCampusciff.jpg
 	create mode 100644 screens/RepositorioClonado.jpg

+ **Push inicial**

Subo el repositorio local a repositorio remoto con el comando git push + direcci�n:

	git push  git@github.com:annalawrenc/Campusciff.git
	
Tengo que introducir contrase�a:
	
	Enter passphrase for key '/c/Users/ania/.ssh/id_rsa':

Una vez introducida la contrase�a prospera el push.

	Counting objects: 12, done.
	Delta compression using up to 8 threads.
	Compressing objects: 100% (12/12), done.
	Writing objects: 100% (12/12), 603.16 KiB | 0 bytes/s, done.
	Total 12 (delta 1), reused 0 (delta 0)
	To git@github.com:annalawrenc/Campusciff.git
	   cb00b5d..f85bc4e  master -> master

Ahora el repositorio remoto contiene los elementos que he subido de local:

![repositorio push inicial](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioPushIni.jpg)

+ **Ignorar archivos**

Creo un archivo de texto privado.txt y una carpeta privada.
	
	mkdir privada
	echo "privado" > privado.txt

![repositorio push inicial](https://github.com/annalawrenc/Campusciff/blob/master/screens/privado.jpg)

Creo un archivo .gitignore y a�ado a la lista privado.txt y carpeta privada.

	echo "privado.txt" > .gitignore

![repositorio push inicial](https://github.com/annalawrenc/Campusciff/blob/master/screens/gitignore.jpg)

A partir de ahora la carpeta privada y el archivo privado.txt van a ser ignorados por Git.


+ **A�adir fichero 1.txt**

Creo un fichero 1.txt y lo a�ado primero a staging y despues a repositorio local.

	git add 1.txt

	git commit -m "commit 1.txt"



+ **Crear el tag v0.1**

A�ado una etiqueta v0.1 al �ltimo commit

	git tag v0.1



+ **Subir el tag v0.1**

Subo los cambios a repositorio remoto:

	git push git@github.com:annalawrenc/Campusciff.git


+ **Cuenta GitHub**

+ Subo una foto

![Foto](https://github.com/annalawrenc/Campusciff/blob/master/screens/PerfilGit.jpg)

+ Poner el doble factor de autentificaci�n en vuestra cuenta de GitHub.

El doble factor de seguridad se pone de la siguiente forma:

![Paso 1](https://github.com/annalawrenc/Campusciff/blob/master/screens/two-factor-aut1.jpg)

![Paso 2](https://github.com/annalawrenc/Campusciff/blob/master/screens/two-factor-aut2.jpg)

![Paso 3](https://github.com/annalawrenc/Campusciff/blob/master/screens/two-factor-aut3.jpg)

![Paso 4](https://github.com/annalawrenc/Campusciff/blob/master/screens/two-factor-aut4.jpg)

*No lo finalizo porque no quiero proporcionar mi m�mero de telefono.*

+ Clave p�blica

Ya tengo clave p�blica:

![Key](https://github.com/annalawrenc/Campusciff/blob/master/screens/publickey.jpg)

+ **Uso social de GitHub** 


+ sigo a mis compa�eros.

![Seguimiento](https://github.com/annalawrenc/Campusciff/blob/master/screens/following.jpg)

+ Pongo estrellas a los compa�eros.

![A�ado estrellas](https://github.com/annalawrenc/Campusciff/blob/master/screens/stars.jpg)


+ Busco repositorios para seguir.

![Busco repositorios](https://github.com/annalawrenc/Campusciff/blob/master/screens/searchreposit.jpg)


+ **Compa�eros de mi clase**


|NOMBRE|GITHUB                             |
|------|----------------------------------:|
|Asier |<https://github.com/asiermatas>    | 
|Juan  |<https://github.com/juangarciaciff>|
|Mark  |<https://github.com/Mark-Wellings> |


+ **Nuevo Colaborador**

A�ado como colaborador al profe: asanzdiego.

![Busco repositorios](https://github.com/annalawrenc/Campusciff/blob/master/screens/colaborador.jpg)

![Busco repositorios](https://github.com/annalawrenc/Campusciff/blob/master/screens/colaboradoradolfo.jpg)


## **Ejercicio 2:**

+ **Crear una rama v0.2**

Creo una nueva rama v0.2 pero no me posiciono en ella.

	git branch v0.2

Ahora me posiciono en la rama con el comando:
	git checkout v0.2

Sale una confirmaci�n que he cambiado de rama:

	Switched to branch 'v0.2'

	ania@DESKTOP-S29Q99K MINGW64 /d/git/Ejercicio1-2/campusciff (v0.2)

+ **A�adir fichero 2.txt**

Una vez posicionada en la rama v0.2 creo un fichero 2.txt.

	echo "2.txt"

Veo que el fichero se ha creado en rama v0.2.

	2.txt

Lo a�ado a staging y hago commit en rama v0.2.

	git add -A
	git commit -m "a�adir 2.txt"


Veo que en la rama master no est� el fichero 2.txt

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRamaMaster.jpg)

En la rama V0.2 si est� el fichero 2.txt

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRamaV2.jpg)
 


+ **Crear rama remota v0.2**

Subo los cambios (inserci�n del fichero 2.txt) a repositorio remoto, creando rama v0.2.

	git checkout v0.2
	git push git@github.com:annalawrenc/Campusciff.git v0.2

Veo que tengo una rama nueva v0.2:

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRama2GitHub.jpg)


+ **Merge directo**

Me posiciono en la master

	git checkout master

Hago un merge de la rama v0.2 en la rama master.

	git merge v0.2

Aparece confirmaci�n:

	Merge made by the 'recursive' strategy.
 	2.txt | 0
 	1 file changed, 0 insertions(+), 0 deletions(-)
 	create mode 100644 2.txt

Ejecuto adem�s:

	git add -A
	git commit -m "merger sin conflicto"
	git push git@github.com:annalawrenc/Campusciff.git

Veo que se han fucionado las ramas y ahora tengo el fichero 2.txt tambi�n en la rama master.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/MasterAfterMerge.jpg)

+ **Merge con conflicto**

Me posisiono en la rama master y pongo "Hola" en el fichero 1.txt.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/1txtHola.jpg)

Despu�s hago un commit de los cambios.
	git add -A
	git commit -m "commit hola"

Me posisiono en la rama v0.2 y pongo "Adios" en el fichero 1.txt en la misma l�nea para crear conflicto.

	git checkout v0.2

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/1txtAdios.jpg)

Despu�s vuelvo a posicionarme en la rama master y hago merge.

	git checkout master
	git merge v0.2

Aparece un mesaje de conflicto:

	Auto-merging 1.txt
	CONFLICT (content): Merge conflict in 1.txt
	Automatic merge failed; fix conflicts and then commit the result.


+ **Listado de ramas**

Saco una lista de ramas fusionadas y sin fusionar

	git branch --merged
	* master

	git branch --no-merged
  	v0.2

*La rama master habia fusionado en clase con "rama" pero ahora no est� fusionada con v0.2*

+ **Arreglar conflicto**


Abro el fichero 1.txt, soluciono el conflicto a mano y guardo fichero.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ConflictoHolaAdios.jpg)
![](https://github.com/annalawrenc/Campusciff/blob/master/screens/SinConflictoHolaAdios.jpg)

	git add -A
	git commit -m "resuelto conflicto"

Aparece mensaje:

	[master e1e3de1] resuelto conflicto


+ **Borrar rama**

Creo un tag v0.2.

	git tag v0.2

Despu�s borro la rama v0.2.


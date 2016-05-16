# Campusciff

## **Ejercicio 1:**


+ **Crear un repositorio en vuestro GitHub**

El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository
![El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository](https://github.com/annalawrenc/Campusciff/blob/master/screens/NewRepository.jpg)

*No he creado ninguno ahora porque ya tengo uno llamado Campusciff que hice en clase*

El repositorio creado se ve así:
![El repositorio:](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioCampusciff.jpg)



+ **Clonar repositorio en local**

Ya tengo un repositorio de la clase en local, entonces creo otra carpeta para clonar y me situo en ella.

	cd Ejercicio1-2

Después copio la direccion del repositorio del GitHub para poder clonar usando el protocolo SSH
![direccion del repositorio] (https://github.com/annalawrenc/Campusciff/blob/master/screens/CopiarDireccionSSHgit.jpg?)

Para clonar uso el comando git clone con la dirección:

	git clone git@github.com:annalawrenc/Campusciff.git

Sale el mensaje de estar clonando y Git pide mi contraseña:

	Cloning into 'Campusciff'...
	Enter passphrase for key '/c/Users/ania/.ssh/id_rsa':

Una vez introducida la contraseña el repositorio se acaba de clonar:

	remote: Counting objects: 6, done.
	remote: Compressing objects: 100% (3/3), done.
	remote: Total 6 (delta 0), reused 3 (delta 0), pack-reused 0
	Receiving objects: 100% (6/6), done.
	Checking connectivity... done.

En la carpeta Ejercicio1-2 veo que se me ha clonado el repositorio
![repositorio clonado](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioClonado.jpg)



+ **Readme**

Añado al fichero readme.md los pasos y lo añado junto con las capturas de pantalla al area de staging

	cd Campusciff
	git add -A

Veo en git status que los ficheros están preparados para commit.

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

Subo el repositorio local a repositorio remoto con el comando git push + dirección:

	git push  git@github.com:annalawrenc/Campusciff.git
	
Tengo que introducir contraseña:
	
	Enter passphrase for key '/c/Users/ania/.ssh/id_rsa':

Una vez introducida la contraseña prospera el push.
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

Creo un archivo .gitignore y añado a la lista privado.txt y carpeta privada.

	echo "privado.txt" > .gitignore

![repositorio push inicial](https://github.com/annalawrenc/Campusciff/blob/master/screens/gitignore.jpg)

A partir de ahora la carpeta privada y el archivo privado.txt van a ser ignorados por Git.


+ **Añadir fichero 1.txt**

Creo un fichero 1.txt y lo añado a repositorio local.

	Changes to be committed:
  	(use "git reset HEAD <file>..." to unstage)

        new file:   1.txt

git commit -m "1.txt sin privados"

A repositorio local sube el fichero 1.txt (y los screenshots), pero no los ficheros privados.


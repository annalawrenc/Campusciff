# Campusciff

## **Ejercicio 1:**


+ *Crear un repositorio en vuestro GitHub*

El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository
![El repositorio se crea desde la cuenta Github, eligiendo Repositories: New Repository](https://github.com/annalawrenc/Campusciff/blob/master/screens/NewRepository.jpg)

*No he creado ninguno ahora porque ya tengo uno llamado Campusciff que hice en clase*

El repositorio creado se ve así:
![El repositorio:](https://github.com/annalawrenc/Campusciff/blob/master/screens/RepositorioCampusciff.jpg)



+ *Clonar repositorio en local*

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



+ *Readme*

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




+ *Commit inicial*

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



## **Ejercicio 2:**

**1. Crear una rama v0.2**

Creo una nueva rama v0.2 pero no me posiciono en ella.

	git branch v0.2

Ahora me posiciono en la rama con el comando:
	git checkout v0.2

Sale una confirmación que he cambiado de rama:

	Switched to branch 'v0.2'

	ania@DESKTOP-S29Q99K MINGW64 /d/git/Ejercicio1-2/campusciff (v0.2)

**2. Añadir fichero 2.txt**

Una vez posicionada en la rama v0.2 creo un fichero 2.txt.

	echo "2.txt"

Veo que el fichero se ha creado en rama v0.2.

	2.txt

Lo añado a staging y hago commit en rama v0.2.

	git add -A
	git commit -m "añadir 2.txt"


Veo que en la rama master no está el fichero 2.txt

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRamaMaster.jpg)

En la rama V0.2 si está el fichero 2.txt

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRamaV2.jpg)
 


**3. Crear rama remota v0.2**

Subo los cambios (inserción del fichero 2.txt) a repositorio remoto, creando rama v0.2.

	git checkout v0.2
	git push git@github.com:annalawrenc/Campusciff.git v0.2

Veo que tengo una rama nueva v0.2:

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerRama2GitHub.jpg)


**4. Merge directo**

Me posiciono en la master

	git checkout master

Hago un merge de la rama v0.2 en la rama master.

	git merge v0.2

Aparece confirmación:

	Merge made by the 'recursive' strategy.
 	2.txt | 0
 	1 file changed, 0 insertions(+), 0 deletions(-)
 	create mode 100644 2.txt

Ejecuto además:

	git add -A
	git commit -m "merger sin conflicto"
	git push git@github.com:annalawrenc/Campusciff.git

Veo que se han fucionado las ramas y ahora tengo el fichero 2.txt también en la rama master.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/MasterAfterMerge.jpg)

**5. Merge con conflicto**

Me posisiono en la rama master y pongo "Hola" en el fichero 1.txt.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/1txtHola.jpg)

Después hago un commit de los cambios.
	git add -A
	git commit -m "commit hola"

Me posisiono en la rama v0.2 y pongo "Adios" en el fichero 1.txt en la misma línea para crear conflicto.

	git checkout v0.2

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/1txtAdios.jpg)

Después vuelvo a posicionarme en la rama master y hago merge.

	git checkout master
	git merge v0.2

Aparece un mesaje de conflicto:

	Auto-merging 1.txt
	CONFLICT (content): Merge conflict in 1.txt
	Automatic merge failed; fix conflicts and then commit the result.


**6. Listado de ramas**

Saco una lista de ramas fusionadas y sin fusionar

	git branch --merged
	* master

	git branch --no-merged
  	v0.2

*La rama master habia fusionado en clase con "rama" pero ahora no está fusionada con v0.2*

**7. Arreglar conflicto**


Abro el fichero 1.txt, soluciono el conflicto a mano y guardo fichero.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ConflictoHolaAdios.jpg)
![](https://github.com/annalawrenc/Campusciff/blob/master/screens/SinConflictoHolaAdios.jpg)

	git add -A
	git commit -m "resuelto conflicto"

Aparece mensaje:

	[master e1e3de1] resuelto conflicto


**8. Borrar rama**

Creo un tag v0.2.

	git tag v0.2

Después borro la rama v0.2.
	
	git push git@github.com:annalawrenc/Campusciff.git --delete 

Aparece mensaje:

	To git@github.com:annalawrenc/Campusciff.git
	 - [deleted]         v0.2

Veo en GitHub que ya no tengo la rama v0.2.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/RamaBorrada.jpg)

**9. Lista de commits**

Hago lista de commits con 

	git log

**10. Crear una organización**

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/OrganizacionCreada.jpg)

**11. Crear equipos**

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/Equipos.jpg)

Invito personas a los equipos de colaboradores y administradores.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/EquipoAdministradores.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/InvitacionesColaboradores.jpg)

**12. Crear index.html**

Preparo una página web y la subo a un repositorio que he creado en la organización.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/crearweb.jpg)

Pongo la dirección de la web en los settings de la organización para que el vínculo aparezca en su perfil.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/linkweb.jpg)

La web se ve de la siguiente forma:

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/verweb.jpg)

**13. Crear pull requests**

Hago fork del repositorio de Alberto, del que no soy colaboradora ni administradora.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ForkAlberto.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ForkeandoAlberto.jpg)

Clono el repositorio a local, hago una rama ForkAnna y modifico index.html en ella. 
Después vuelvo a subir el repositorio a github y hago pull request.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ForkAlbertoSubido.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/PullRequestAlberto.jpg)


Hago segundo fork, de repositoio de Araceli. No se llama github.io pero es el único del que no soy colaboradora ni administradora entre los que tienen repositotio con el index.html.

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/forkAraceli.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ForkModIndexAraceli.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/VerForkAraceli.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/ForkAraceliListo.jpg)

A continuación hago pull request:

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/PullRequestAraceli.jpg)

**13. Aceptar pull requests**

Acepto pull request de Asier:

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/pullrequestasier.jpg)

![](https://github.com/annalawrenc/Campusciff/blob/master/screens/pullrequestasiermerged.jpg)

Solo acepto un pull request porque no me han llegado más pul requests.

# L.-Smith

## Git
### Creación del repositorio
```
git init
```
Crea un repositorio local en un directorio determinado.
```
git clone https://github.com/HDominguezD/L.-Smith.git
```
Crea una copia local del repositorio existente.
### Actualizar el repositorio local
```
git pull
```
Descarga y fusiona los cambios remotos en el repositorio local.
```
git merge branchname
```
Fusiona la rama branchname a la rama actual, en caso de que no se pueda fusionar automáticamente marcará con "<<<<<<< HEAD" los tramos del archivo en conflicto.
### Flujo de trabajo
Un repositorio local esta compuesto por tres "árboles" administrados por git. El primero es el Directorio de trabajo que contiene los archivos, el segundo es el Index que actua como una zona intermedia, y el último es el HEAD que apunta al último commit realizado.

* Añadir archivos a Index
```
git add <filename>
```
Añade el archivo con el nombre file name a Index
```
git add .
```
Añade todos los archivos restantes de la carpeta actual a Index

* Hacer un commit de los archivos en Index y guardarlos en el HEAD local.
```
git commit -m "Mensaje del commit"
```
* Subir el commit al repositorio remoto (Github)
```
git push origin <branchname>
```
Sube los cambios a la rama <branchname>
  
 ### Ramas
 Las ramas se utilizan para poder trabajar de forma simultánea sobre los mismos archivos.
```
git checkout -b branchname
```
Crea una nueva rama y mueve el directorio de trabajo a esta rama, de forma que todos los cambios que realizemos se sobreescribirán solo en esta rama.
```
git checkout branchname
```
Mueve el directorio de trabajo a una rama ya existente.
```
git branch -d branchname
```
Borra una rama ya existente. CUIDADO!!!
```
git push origin branchname
```
Sube una rama al repositorio remoto para que la puedan ver el resto de desarrolladores.

### Otros comandos útiles
```
git diff <source_branch> <target_branch>
```
Sirve para ver las diferencias entre dos ramas.
```
git tag 1.0.0 1b2e1d63ff
```
Sirve para etiquetar versiones, marcandolas con el id del último commit que la implementó.
```
git log
```
Muestra el registro de commits del repositorio.
```
git checkout -- <filename>
```
Borra los cambios en filename para dejarlo igual que estaba en HEAD.
```
git reset --hard origin/branchname
```
Borra todos los cambios locales realizados sobre una rama.

# microsoft_data_science
Curso Introductorio a Ciencia de Datos En  Microsoft Learn.

## GIT.

- Servicio de control de versiones.
- Permite trabajar en equipo.

```git
configurar nombre de usuario y correo electronico de quien realiza commits a git 
git config --global user.name "nombre"  
git config --global user.email "email"
```
para ver si estos datos estan configurados
```git
git config --list
```
- VCS (Version Control System)
- Repositorio: Carpeta donde se almacenan los archivos de un proyecto.
- Commit: Guardar los cambios realizados en el repositorio.
- Branch: Rama de desarrollo.
- Merge: Unir dos ramas.
- Pull Request: Solicitud de integración de una rama a otra.
- Fork: Copia de un repositorio.
- Clone: Descargar un repositorio.
- Push: Subir cambios a un repositorio remoto.
- Pull: Descargar cambios de un repositorio remoto.

- Otro nombre para VCS es Sistema de Administracion de Configuraciones de Software (SCM).
- Tecnicamente el control de versiones(VCS) es solo uno de los procedimientos que implica el SCM, aunque ambos terminos se usan indistintamente.

### Con un VCS se puede:

- Ver todos los cambios realizados en el proyecto y quien los efectuo 
- incluir un mensajes on cada cambio y explicar los motivos 
- Recuperar versiones anteriores del proyecto o de archivos individules 
- Crear ramas, donde los cambios se pueden hacer experimentalmente 
- Adjuntar una etiqueta a una version especifica del proyecto

- Git es un VCS distribuido, lo que significa que cada desarrollador tiene una copia completa del historial de versiones del proyecto, incluyendo todos los archivos y los cambios realizados en cada uno de ellos.

### Terminologia GIT

- Arbol de trabajo (Working Tree): Es el directorio donde se encuentra el proyecto.
- Repositorio (Repository- Repo): Es el directorio donde se almacenan los archivos del proyecto, se encuentra situado en el nivel superior del arbol de trabajo 
- Hash numero generado por una funcion hash que representa el contenido de un archivo u otro objeto.
Git usa hashes de 160 bits de longitud. Una ventaja de que git use hashes es que puede indicar si ese archivo a tenido cambios aplicando una funcion hash y comparando su contenido, si cambiase marca la hora y fecha.

- Objetos : un repositorio git contiene 4 tipos de objetos, cada uno identificado por un hash SHA-1.
    - Blob: Archivos de datos.
    - Tree: Directorios.
    - Commit: Representa un estado del repositorio.
    - Tag: Etiqueta para un commit.


- Commit (confirmar): significa crear un objeto, guardar los cambios realizados , para que otros usuarios puedan verlos.

- Branch (rama): serie con nombre de confirmaciones (commit) vinculadas 
la confirmacion mas reciente de una rama se denomina nivel superior.
La rama predeterminada se crea al iniciar un repositorio y esta se denomina `Main` o `Master`.Las ramas son caracteristicas muy utiles , permiten trabajar a los desarrolladores de manera independiente en ramas y luego integrar los cambios en la rama principal.

- Remoto : referencia con nombre a otro repositorio de Git cuando se crea un repositorio Git crea un remoto denominado `Origin` predeterminado para los envios e incorporacion de cambios.

- Git es el comando pull es el subcomando, el subcomando especifica la operacion a realizar

## Git y GItHub

- Git es un sistema de control de versiones distribuido, mientras que GitHub es un servicio de alojamiento de repositorios Git.

- GitHub ofrece las siguientes caracteristicas.
    - Issues
    - Debates
    - Solicitudes de incorporacion de cambios (Pull Requests)
    - Notificaciones
    - Etiquetas
    - Acciones
    - Forks
    - Proyectos 

### Ejercicio Git.

verificar que tenemos acceso a git en la terminal
```git
git --version
```

configurar nombre de usuario y correo electronico de quien realiza commits a git 
```git
git config --global user.name "nombre"
git config --global user.email "email"
```

para ver si estos datos estan configurados
```git
git config --list
```

### Configuracion del Repositorio Git
- Crear una Carpeta 
```git
mkdir nombre_carpeta
```
- Ir a la carpeta
```git  
cd nombre_carpeta
```
- Inicializar el repositorio
```git
git init --initial-branch=main
o
git init -b main
```
- Para conocer el estado del repositorio
```
git status

esto nos devuelve lo siguiente:

hugo [ ~/Cats ]$ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
hugo [ ~/Cats ]$ 
```

- Para mostrar e estado del arbol de trabajo
```git
git ls -a
```

- Ayuda desde Git 
```git
git help


usage: git [--version] [--help] [-C <path>] [-c name=value]
       [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
       [-p | --paginate | --no-pager] [--no-replace-objects] [--bare]
       [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
       <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Forward-port local commits to the updated upstream head
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

```

- Comando Git Add : `git add` es el comando que se utiliza para indicar a git que empiece a realizar un seguimiento de los cambios en determinaso archivos 

- Comando Git Commit : `git commit` (confirmar) es el comando que se utiliza para confirmar los cambios realizados en los archivos que se estan siguiendo.

- Comando Git Log : `git log` es el comando que se utiliza para ver el historial de confirmaciones (commits) realizadas en el repositorio.

# Introduccion a GitHub

## FLujo de GitHub.
Es un flujo de trabajo ligero  basado en ramas 

### Issues.
Son el elemento en el que se produce la mayor parte de la comunicacion entre los consumidores  y el equipo de desarrollo.Se puede crear una incidencia para analizar una amplia variedad de temas , informes de errores solicitudes de caracteristicas , aclaraciones sobre la documentacion 

### Notificaciones.
GitHub como plataforma te ofrece notificaciones de practicamente todos los eventos que ocurren en tu repositorio 

# Python
- Podemos ejecutar un script de python desde la terminal moviendonos al directorio e invocando el nombre del archivo donde se encuentra nuestro script 

- Cuando el texto tiene una combinación de comillas simples y dobles, puede usar comillas triples para evitar problemas con el intérprete:
    
 

```python
"""We only see about 60% of the Moon's surface, this is known as the "near side"."""
```

#### Metodo `title()`

```python
"temperatures and facts about the moon".title()
'Temperatures And Facts About The Moon'


heading = "temperatures and facts about the moon"
heading.title()
'Temperatures And Facts About The Moon'
```

#### Metodo `split()`

split sin argumentos dividira la cadena en cada espacio que exista en ella 

```python
"temperatures and facts about the moon".split()
['temperatures', 'and', 'facts', 'about', 'the', 'moon']
```

#### Operador `in`
busca si un elemento se encuentra en una lista o cadena de texto

```python
"temperatures" in "temperatures and facts about the moon"   
True
```

#### Metodo `find()`
busca un elemento en una cadena de texto y devuelve la posicion en la que se encuentra
Si no se encuentra la palabra , el metodo find() devuelve -1

```python
"temperatures and facts about the moon".find("facts")
16

"temperatures and facts about the moon".find("hola")
-1
```
#### Formato de cadenas `porcentage %`
```python
mass_percentage = "1/6"
print("On the Moon, you would weigh about %s of your weight on Earth" % mass_percentage)

On the Moon, you would weigh about 1/6 of your weight on Earth
El uso de varios valores cambia la sintaxis, ya que se necesitan paréntesis para rodear las variables que se pasan:
```

#### Metodo `format()`
```python
mass_percentage = "1/6"
print("On the Moon, you would weigh about {} of your weight on Earth".format(mass_percentage))
```

#### `f-strings`
```python
mass_percentage = "1/6"
print(f"On the Moon, you would weigh about {mass_percentage} of your weight on Earth")
```










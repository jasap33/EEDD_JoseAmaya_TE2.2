TAREA EVALUABLE 2.2. TRABAJO CON GIT (Comandos)

Objetivos

Conocer los comandos de git más importantes para trabajar con repositorios locales y remotos.
Conocer el entorno de VS Code para trabajar con git.
Conocer el lenguaje de marcado Markdown y su utilización en el desarrollo de documentación.
Entrega

El documento justificativo de la realización de la tarea se realizará en formato Markdown, el nombre del fichero será readme.md y estará dentro de la carpeta UT2\TE2.2 dentro del repositorio oficial del alumno para la asignatura.

El fichero readme.md debe contener los siguientes apartados:


Cada uno de los puntos de la tarea.
Explicación de los pasos realizados y una imagen/gif justificativo del paso. (las imagenes se guardarán en la carpeta UT2\TE2.2\img).
El nombre de la imagen debe ser el número del punto y subpunto seguido de la extensión correspondiente (.png, .jpg, .gif).
Ejemplo: 01.1.png, 02.5.gif, 03.3.jpg.
Copia este documento como plantilla para la realización de este ejercicio en tu repositorio.

📦 Recursos

📁 GIT

Visualizar conceptos con D3

Taller de introducción a GIT

Guía de supervivencia de GIT

SOS Git

Escrbir en Markdown

Curso de GIT y GITHUB (youtube)

💡 Para obtener la url de un fichero en GIThub y que esta URL pertenezca a un commit específico, desde el navegador, desde el teclado pulsar y y se copia la url con el hash del commit.
📹 GIF

ScreenToGif grabar la pantalla y convertirlo en gif.
➕ Extensiones de VSCode

Git Graph
Markdown All in One
Markdown Emoji
1. Crear repositorio local y subir a GITHUB

Crea una carpeta llamada UT2.2.a.

Inicializa un repositorio local en la carpeta UT2.2.a. ¿Qué comando/s utilizas?

 // git init

Revisa qué rama se ha creado por defecto. ¿Qué comando/s utilizas?

// git branch

Renombrar la rama por defecto a main en caso de que tenga otro nombre. ¿Qué comando/s utilizas?

 // git branch -m nombre_antiguo main
 
Agrega un fichero README.md.

# UT2.2.a

Repositorio de prueba para la tarea 2.2.a
Agrega el fichero README.md al stage area. ¿Qué comando/s utilizas?

 // git add README.md
 
Realiza un commit con el mensaje "Add README". ¿Qué comando/s utilizas?

 // git commit -m "Add README”
 
Agrega otro fichero 01.xml con siguiente texto.

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Quijote</titulo>
        <autor>Miguel de Cervantes</autor>
        <editorial>Editorial Castalia</editorial>
        <fecha>1605</fecha>
        <genero>Novela</genero>
        <precio>20</precio>
    </libro>
</libreria>
Agrega el fichero 01.xml al stage area y realiza el commit "Add file 01.xml" ¿Qué comando/s utilizas?

// git add 01.xml

Agrega una nueva rama llamada y posicionate directamente en ella con el mismo comando fea/wac01. ¿Qué comando/s utilizas? (busca en internet si no lo recuerdas)

// git checkout -b fea/wac01

En qué rama estas ahora mismo? ¿Qué comando/s utilizas?

// git branch

Estando en la rama fea/wac01 agrega un fichero `02.xml, y agrega al área de stage y realiza commit "Add file 02".

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Hobbit</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1937</fecha>
        <genero>Fantasía</genero>
        <precio>15</precio>
    </libro>
</libreria>
Muestra el log utilizando solo una línea por commit con opciones gráficas. ¿Qué comando/s utilizas?

// git log --oneline --graph

Posicionate de nuevo en la rama main, y crea otra rama fea/wac02, posicionandote directamente en ella. Agrega un fichero 03.xml, agrega al área de stage y realiza commit "Add file 03".

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Señor de los Anillos</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1954</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
</libreria>
Posicionate en la rama main y muestra los ficheros que hay en el directorio. ¿Qué comando/s utilizas?

// git checkout main + ls

Realizar un merge de la rama fea/wac01 en la rama main. (Indica los comandos utilizados y explica cada uno de ellos).

// git checkout main + git merge fea/wac01 
git checkout main: Este comando cambia la rama activa a main. Es importante estar en la rama en la que deseas fusionar los cambios antes de ejecutar el comando de merge.
git merge fea/wac01: Este comando combina los cambios de la rama fea/wac01 con la rama main. Git intentará fusionar automáticamente los cambios. Si hay conflictos, te lo notificará para que los resuelvas manualmente.

Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen/gif visualizando los comandos) adjunta la imagen

![](cap1.png)

Elimina la rama fea/wac01 sin posibilidad de recuperación. ¿Qué comando/s utilizas?

// git branch -D fea/wac01

Realiza un merge de la rama fea/wac02 en la rama main.

// git checkout main + git merge fea/wac02

Muestra el estado del repositorio, el log, y los ficheros que hay en el directorio. (Imagen) adjunta la imagen

![](cap2.png)

Vuelve a la rama fea/wac02 y modifica el fichero 03.xml añadiendo un nuevo libro.

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Señor de los Anillos</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1954</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
    <libro>
        <titulo>El Silmarillion</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1977</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
</libreria>
Agrega al área de stage y realiza commit "Update 03 file. Add book El Silmarillion".

Posicionate en la rama main, muestra el estado y muestra el contenido del fichero cat 03.xml. (Imagen visualizando comandos) adjunta la imagen

![](cap3.png)

Realiza un merge de la rama fea/wac02 en la rama main. ¿Qué comando/s utilizas?

// git checkout main + git merge fea/wac02

Muestra el estado del repositorio, y muestra el contenido del fichero 03.xml. (Imagen visualizando comandos) adjunta la imagen

![](cap4.png)

Ahora, en la rama main modifica el fichero 03.xml incluyendo un nuevo libro.

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Señor de los Anillos</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1954</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
    <libro>
        <titulo>El Silmarillion</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1977</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
    <libro>
        <titulo>El Hobbit</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1937</fecha>
        <genero>Fantasía</genero>
        <precio>15</precio>
    </libro>
</libreria>
Agrega al área de stage y realiza commit "Update 03 file. Add book El Hobbit".

Agrega un nuevo fichero 04.xml sobre libros ciencia-ficcion, en la rama main.

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El fin de la eternidad</titulo>
        <autor>Isaac Asimov</autor>
        <editorial>Edhasa</editorial>
        <fecha>1955</fecha>
        <genero>Ciencia ficción</genero>
        <precio>20</precio>
    </libro>
</liberia>
Agrega al área de stage y realiza commit "Add 04 file. Add cienca-ficcion books".

Muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) adjunta la imagen

![](cap5.png)

Vuelve un commit atrás, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) adjunta la imagen

![](cap6.png)

Vuelve al commit anterior, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) adjunta la imagen

![](cap7.png)

Posicionate de nuevo en el último commit, y muestra el estado, log una línea y los ficheros que hay en el directorio. (Imagen visualizando comandos) adjunta la imagen

![](cap8.png)

2. Crear repositorio remoto y subir a GITHUB

Crea un repositorio remoto en GITHUB llamado EEDD_{NombreApellido}_TE2.2 público, vacio, sin nada.

Agrega el repositorio remoto a tu repositorio local. ¿Qué comando/s utilizas?

 // git remote add origin https://github.com/GITHUB_USERNAME/EEDD_{NombreApellido}_TE2.2.git
 
Muestra los repositorios remotos que tienes configurados. ¿Qué comando/s utilizas?

 // git remote -v
 
Sube la rama main al repositorio remoto. ¿Qué comando/s utilizas?

 // git push -u origin main
 
Muestra el log de la rama main con opciones gráficas. ¿Qué comando/s utilizas?

 // git log --oneline --graph
 
Posicionate en la rama fea/wac02 y sube la rama fea/wac02 al repositorio remoto. ¿Qué comando/s utilizas?

 // git checkout fea/wac02 + git push -u origin fea/wac02
 
Ahora desde GITHUB (web) en la rama fea\wac02, modifica el fichero 03.xml añadiendo un nuevo libro.

<?xml version="1.0" encoding="UTF-8"?>
<libreria>
    <libro>
        <titulo>El Señor de los Anillos</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1954</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
    <libro>
        <titulo>El Silmarillion</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1977</fecha>
        <genero>Fantasía</genero>
        <precio>25</precio>
    </libro>
    <libro>
        <titulo>El Hobbit</titulo>
        <autor>J.R.R. Tolkien</autor>
        <editorial>Minotauro</editorial>
        <fecha>1937</fecha>
        <genero>Fantasía</genero>
        <precio>15</precio>
    </libro>
    <libro>
        <titulo>El hombre bicentenario</titulo>
        <autor>Isaac Asimov</autor>
        <editorial>Edhasa</editorial>
        <fecha>1976</fecha>
        <genero>Ciencia ficción</genero>
        <precio>20</precio>
</libreria>
Realiza un commit con el mensaje "Update 03 file. Add book El hombre bicentenario". (Muestra pantallazo de GITHUB con el commit realizado) adjunta la imagen

![](cap9.png)

Ahora obten los cambios sin acualizar el repositorio local (git fetch origin).

// git fetch origin

Muestra un log del repositorio local con opciones gráficas. (Incluye imagen) adjunta la imagen

![](cap10.png)

Ahora actualiza el repositorio local con los cambios del repositorio remoto (git pull origin fea/wac02).

Muestra un log del repositorio local con opciones gráficas. (Incluye imagen) adjunta la imagen

![](cap11.png)

Haz un merge de la rama fea/wac02 en la rama main. Muestra estado, log, y el contenido fichero 03.xml (Incluye imagen) adjunta la imagen

![](cap12.png)

Sube la rama main al repositorio remoto. ¿Qué comando/s utilizas?

// git push -u origin main

Elimina la rama local fea/wac02 sin posibilidad de recuperación. ¿Qué comando/s utilizas?

// git branch -D fea/wac02

Elimina la rama remota fea/wac02 sin posibilidad de recuperación (git push origin --delete fea/wac02).

// git push origin --delete fea/wac02

Muestra desde GITHUB (navegador web) las ramas que tienes el en repositorio remoto. (Incluye imagen) adjunta la imagen

![](cap13.png)


3. Enlace repositorio remoto

Incluye el enlace al repositorio remoto en este punto para que el profesor pueda acceder a él.
 // Enlace al repositorio remoto (en que aparece en la URL del navegador)
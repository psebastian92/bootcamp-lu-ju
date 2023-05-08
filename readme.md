# CLASE 15 - CONFIGURACIÓN INICIAL

<!-- Setear nombre de usuario-->
``` sh
git config --global user.name "Sebastian Muñoz"
```

<!-- Setear email -->
``` sh
git config --global user.email "sebastian.munoz092@gmail.com"

```


<!-- Verificar qué datos se ingresaron -->
``` sh
git config --get-regexp user
```


## CREAR UN REPOSITORIO 
<!-- Iniciar repositorio -->
```sh
git init
```

## Áreas del repositorio de GIT

3 Areas:

 * Working Directory (WD): directorio de trabajo donde se van agregando o quitando archivos durante el desarrollo, de manera temporal/actual.
 * Staging Area (SA): (área de control de cambios). Área temporal, intermedia, donde me guarda las nuevas versiones.
 * Local Repo (LR): es una "caja" donde voy a ir teniendo todas las versiones que vayan surgiendo. 


## El estado de los archivos en el repositorio



## El estado de los archivos (en sí mismos)

* untracked: estado actual de los archivos. Es la "U" que aparece en el "Explorer" de Visual Studio Code.
* unmodified: son archivos que GIT está siguiendo y con respecto al WD, no fueron modificados. 
* modified: son archivos que se encuentran en el Repo (están siendo seguidos por GIT) pero difieren con lo que se encuentra actualmente en el WD.
* staged: archivos que están en el área temporal/intercambio (SA). 

## Saber estado actual de los archivos
``` sh
git status
```

## Pasar de WD a SA 
``` sh
git add <nombre archivo>
ejemplo: git add index.html
```
Agregar todos: git add .

## Pasar de SA a LR
``` sh
git commit -m (comentario de qué hice en este paso. Ej: "agregar" index.html)
```
## Ver la historia de commits
``` sh
git log # historia de commit detallada
git log --oneline  # historia de commit resumida
```

SI LA CONSOLA QUEDA BLOQUEDA, Y NO PUEDO SALIR DEL LISTADO: presiono la tecla "q" de "quit".

## Descartar cambios de archivos modificados
``` sh
git restore "nombre del archivo"
```

## Si quiero ver los cambios que tengo entre el WD y el LR:
``` sh
git diff 
```

# Clase 16

## .gitignore
Este archivo me sirve para ignorar carpetas o archivos que no quiero que sean parte del repositorio. Normalmente va sobre la raíz del proyecto (en este caso, la raíz es lo que tengo dentro de la carpeta GIT-INTRO).

Necesito crear el archivo **.gitignore**: 
``` sh
touch .gitignore
```

## Ayuda de git: subcomando --help
``` sh
git help --
```
Ejemplo: git add help--, o git restore --help

## Agrego a mi repo local la URL del repo remoto
``` sh
git remote add origin https://github.com/psebastian92/bootcamp-lu-ju.git
```

### Visualizar si se agrego o qué URL tengo agregada
``` sh
git remote -v
```


# PRACTICA 01 MODULO 01- EJERCICIO GIT


## ¿Qué comando utilizaste en el paso 11? ¿Por qué?

Utilicé el comando siguiente:
```
git reset --hard HEAD~1
```
Esto lo hice así para poder recuperar en el working copy los archivos originales en el commit inicial, perdiendo así los del segundo commit.


## ¿Que comando utilizaste en el paso 12? ¿Por qué?

Como estaba en el commit inicial y con git log no podía ver el commit anterior, usé el comando siguiente:
```
git reflog
```
Obteniendo así los pasos dados anteriores, con los identificadores de los commits. De esta forma pude obtener el id del commit el cual utilicé para rescatar usando el comando:
```
git reset --hard <id_commit>
```
Utilicé ese comando para restaurar en el working copy el archivo.

<img width="498" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/57bba532-5180-413a-b7fd-f7b9b7e7a7c2">


## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué? 

No sale conflicto porque ha hecho un fast foward 

<img width="680" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/5767983e-ef44-49c9-90d4-bfa3a57ced19">


## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

Si, porque al hacer el merge no fast foward había diferencias entre los git-nuestros.md de la rama *styled* con respecto al archivo git-nuestro.md de la rama *htmlify*.

<img width="673" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/35e8b77c-affc-4e2d-86b9-e5f5d2e7772a">


## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

No ha habido conflicto porque he hecho un fast forward, master se ha movido a la rama styled. 

<img width="833" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/1d7bb4ea-ceca-4257-bddb-799af34dac24">


## ¿Qué comando o comandos utilizaste en el paso 25?
El comando ha sido

´´´
git log --branches --graph --oneline
´´´
<img width="713" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/e4313afb-9c4e-4c2c-8033-2a94521c3155">

También se puede obtener el diagrama en Visual Studio Code con la extension git graph
<img width="826" alt="image" src="https://github.com/inmiti/PRACTICA01_GIT/assets/118215654/d4a7632f-17c6-433b-a65c-5dfbdc0e5c73">


## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí podría porque están alineados, no hay bifurcaciones entre ellos.


## ¿Qué comando o comandos utilizaste en el paso 27?

Para deshacer el merge sin recuperar el working copy:
```
git reset HEAD~1
```

## ¿Qué comando o comandos utilizaste en el paso 28?

Sería git remote, pero en mi versión de git es:
```
git checkout -- git-nuestro.md
```


## ¿Qué comando o comandos utilizaste en el paso 29?

Para eliminar la rama title:
```
git branch -D title
```

## ¿Qué comando o comandos utilizaste en el paso 30?

Para rehacer el merge primero hay que volver a hacer la rama title.
Buscamos el commit al que apuntaba dicha rama:
```
git reflog
```
Obtengo el id del commit: 532e93f y deshago:
```
git reset --hard 532e93f
```

## ¿Qué comando o comandos usaste en el paso 32?
Cojo el id del commit inicial usando:
```
git reflog
```
Me cambio usando:
```
git checkout 3b79e59
```

## ¿Qué comando o comandos usaste en el punto 33?

```
git checkout master
```


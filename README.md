# Propuesta de flujo de trabajo en Gitlab para miembros de algún proyecto.
## Version 0.1

Este documento tiene como objetivo proporcionar pautas para la integración de código limpio y ordenado; escrito por los miembros de la organización Aventura Tech.

>Este repositorio es un trabajo en progreso. De hecho, su primer "Merge Request" podría ser corregir o agregar nuevas directrices a este documento. Para llevar esto a cabo póngase en contacto con el lider del equipo o con el encargado de "DevOps".


<a name="#inicio"></a>
### Inicio

| Indice |  |
|--|--|
| [General Conventions](#general-conventions) | Convenciones generales |
| [Meaningful Commit Messages](#commit-messages) | Mensajes de confirmación significativos |
| [Gitlab Workflow](#gitlab-workflow) | Flujo de Trabajo en Gitlab |


<a name="#general-conventions"></a>
## General Conventions

Todos los repositorios deben contar con:
- Una rama `master`. Copia fiel de lo que haya en producción.
- Una rama `release`. La rama **Release Candidate** (RC), debe estar disponible en el  **staging environment**.
- Una rama `develop`. La rama de la cuál cada desarrollador sacará sus respectivas ramas personalizadas para `feature` y `fix`.
- Se recomienda usar letras minúsculas en los nombres.
- Se recomienda el uso de guiones ( - ).
- Se recomienda usar nombres identificativos. Ej. *feature-login-facebook*


<a name="#commit-messages"></a>
## Meaningful Commit Messages

**Estructura del Mensaje**

El mensaje de los commit debe consistir en 3 diferentes partes 
separadas por una linea en blanco: el titulo, un cuerpo 
opcional y un pie opcional. Algo como lo siguiente:

```Shell
type: subject 

body 

footer
```

El tipo es contenido en el titulo y puede ser de alguno de los siguientes casos:

>`feat:` Una nueva caracteristica\
>`fix:` Se soluciono un bug\
>`docs:` Se realizaron cambios en la documentación\
>`style:` Se aplico formato, comas y puntos faltantes, etc; sin cambios en el código\
>`refactor:` Refactorización del código en producción\
>`test:` Se añadieron pruebas, refactorización de pruebas; sin cambios en el código\
>`chore:` Actualización de tareas de build, configuración del admin, de paquetes; sin cambios en el código

*Subject*

- El titulo consiste en el tipo y asunto del mensaje. 
- No debe tener más de 50 caracteres.
- Debe iniciar con una letra mayuscula y no terminar con un punto.

*Body*

Al escribir el cuerpo (Body), se debe dejar una linea en blanco 
entre el título y el cuerpo, además debemos limitar la longitud 
de cada linea a no más de 72 caracteres.

*Footer*

El pie es opcional al igual que el cuerpo, pero este es usado 
para seguimientos. Ej:

```Shell
Resolves: #b214c5\
Issues: #03
```

<a name="#gitlab-workflow"></a>
## Gitlab Workflow

Las siguientes especificaciones son exclusivas de la plataforma Gitlab. Y serán aquellas por las que nos guiaremos.

**Consideraciones**

| Que debe hacerse | Detalle | Quien lo hace |
|--|--|--|
| [Crear Proyecto](#crear-proyecto) | Aquí se incluye la creación del repositorio y/o<br /> ramas que se necesitarán.<br /> También puede asignar a alguien más. | [Fulano de Tal](@FulanodeTal) |
| [Crear Incidencias](#crear-incidencias) (`Issues`) | En este paso (el cuál también puede asignarse<br /> a otro/a persona) es donde se dan las<br /> asignaciones a los desarrolladores. | - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal) |
| [Merge Requests](#merge-requests) | Una vez recibidas las asignaciones y, que cada<br /> desarrollador haya descargado su copia del<br />proyecto; deberá crear su propio `Merge Request`<br /> para iniciar su trabajo. | - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal]( @FulanodeTal)<br />- [Fulanita de Tal](@FulanitadeTal)<br />- [Pablo E. Pulido](@pulidovpe)<br /> |
| [Aprobar un merge](#aprobar-un-merge) | Esta sección es exclusivamente para el<br /> encargado de revisar el código antes de<br /> hacer el merge. | - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal) |
| [Trabajo en equipo](#trabajo-en-equipo") | Solución de conflictos para cuando se trabaja<br /> en equipo. | - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal]( @FulanodeTal)<br />- [Fulanita de Tal](@FulanitadeTal)<br />- [Pablo E. Pulido](@pulidovpe)<br /> |
| [Fusionar los cambios](#fusionar-los-cambios) | Una vez recibida la aprobación ya se puede<br /> realizar la fusión por consola o en *Gitlab*. | - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br /> - [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal](@FulanodeTal)<br />- [Fulano de Tal]( @FulanodeTal)<br />- [Fulanita de Tal](@FulanitadeTal)<br />- [Pablo E. Pulido](@pulidovpe)<br /> |


<a name="#crear-proyecto"></a>
### Crear Proyecto

![Crear Proyecto](img/crea-proyecto.png "Crear proyecto")


<a name="#crear-incidencias"></a>
### Crear Incidencias

Para crear una incidencia lo primero es ubicarse en el proyecto donde se trabajará. Luego en el lado izquierdo ubicamos (dependiendo del idioma configurado) la opción Incidencia ó, `Issues`.

![Crear Incidencias](img/crea-issue1.png "Crear Incidencias")

Al abrir, nos aparecerá el panel de incidencias, donde ubicado a la derecha podremos crear una nueva.

![Crear Incidencias](img/crea-issue2.png "Crear Incidencias")

![Crear Incidencias](img/crea-issue3.png "Crear Incidencias")

Al momento de llenar el formulario existen otra consideraciones a saber; las cuales deben completarse antes de crear la incidencia:
- `Assignee`, que es a quién se le asignará la incidencia. Se la puede asignar la misma persona que crea la incidencia.
- `Milestones`, que son los hitos. Es decir, la forma de conocer el avance del proyecto, generalmente identificados con una versión (Ej. v0.0.1).
- `Labels`, es decir, las etiquetas que nos informarán acerca del tipo de incidencia.
- `Due date`, o sea, la fecha de vencimiento.

![Crear Incidencias](img/crea-issue4.jpg "Crear Incidencias")

Al crearse, la persona asignada será notificada por la plataforma.


<a name="#merge-requests"></a>
### Merge Requests

El/la desarrollador(a), deberá ubicarse en la incidencia creada y dar click en el menú desplegable situado a la derecha del botón que permite crear los `Merge Request`.
Una vez abierto, lo siguiente es seleccionar el origen; que por defecto es *master*. Este campo debe ser editado y cambiado por *develop*.

![Merge Requests](img/crea-merge-request1.jpg "Merge Requests")

**Aclaración**. Debido a que no estamos usando la versión *GitLab Enterprise Edition*, la `approvals interface` no están disponibles. Por lo tanto, al momento de crear un `merge request` tendrá que agregarse una nota identificativa para la persona que debe revisar y aprobar los cambios.

![Merge Requests](img/crea-merge-request2.jpg "Merge Requests")

De esta forma, la persona etiquetada (y notificada) para revisar el código tendrá una forma de confirmar que lo hizo.\
Otra cosa a tomar en cuenta es la modificación (por parte de la plataforma *Gitlab*) del nombre del `merge request` al crearlo, agregándole un prefijo:<br /> **`WIP: Resolve`**

![Merge Requests](img/crea-merge-request3.jpg "Merge Requests")

`WIP: Resolve` es el acrónimo de Work In Progress. Y es un indicador de *Gitlab* para notificar que se está trabajando actualmente en ese `merge request`. Además, evitará que hagamos **merge** hasta que no quitemos ese prefijo.

Para bajarse la rama creada por este `merge request` y empezar a trabajar en ella, se recomienda usar la consola.

Lo primero es descargarse el proyecto y ubicarse dentro.

```
git clone git@gitlab.com:aventuratech/work-flow.git

cd work-flow
```
Luego bajarse la rama creada por el `merge request`.
```
git pull

git branch 2-guia-para-workflow origin/2-guia-para-workflow
```
ó ...
```
git fetch origin

git checkout -b 2-guia-para-workflow origin/2-guia-para-workflow
```

![Merge Requests](img/crea-merge-request4.jpg "Merge Requests")

Esto les mostrará la información de las ramas remotas. Luego enlazaremos la rama local con la remota.
Sino usaron `git checkout`, no hay que olvidar cambiarse a la rama correspondiente.

```
git checkout 2-guia-para-workflow
```

Una vez hechos los cambios, se recomienda seguir las normas descritas en la sección de [Meaningful Commit Messages](#commit-messages) para detallar la información del *commit* antes de subirlo.


<a name="#aprobar-un-merge"></a>
### Aprobar un merge

Además de una revisión personalizada, quien revisa el código cuenta con herramientas en la plataforma, como *diff*.

![Merge Requests](img/revisa-merge-request1.jpg "Merge Requests")

Mientras hay revisiones, puede existir un diálogo entre quien revisa y quien desarrolla. Para estos casos se recomienda usar la plataforma. De esta forma queda constancia de las decisiones que se van tomando durante el desarrollo.

![Merge Requests](img/revisa-merge-request2.jpg "Merge Requests")

Una vez revisado el código; hay que dar la aprobación en *Gitlab*.
La persona etiquetada, debería marcar el *checklist* que se encuentra bajo el título del `merge request` y dar click en el botón **Resolve WIP status**.
Una vez hecho esto, puede dejar que la fusión la haga el propio desarrollador(a) ó, hacerla por usted mismo. 

![Merge Requests](img/revisa-merge-request3.jpg "Merge Requests")

![Merge Requests](img/revisa-merge-request4.jpg "Merge Requests")


<a name="#trabajo-en-equipo"></a>
### Trabajo en equipo


Al trabajar en equipo, los `merge request` hechos por cada desarrollador pueden ir en diferentes intervalos de tiempo. Todavía más, cuando les llegue el momento de ser aprobados y fusionados.
En estos casos, pueden ocasionar conflictos con los de alguien que aún no sube sus cambios, mostrando mensajes como el siguiente:

Ej.
```Shell
la rama de origen está 2 commits detrás en relación a la rama de destino
```

Para evitar que ocurran estos escenarios, se sugiere que antes de hacer un commit y subir los cambios tomar previsiones, bajando la última versión del repositorio:

```Shell
$ git fetch
```

Se recomienda ejecutar un `git fetch` en lugar de un `git pull` debido a que el fetch sólo recupera todos los datos del proyecto remoto que no tengas todavía, pero no fusiona las ramas sin preguntar como lo hace el pull, que lo hace automáticamente. Hecho esto, tendremos la ultima versión de la rama *develop* y nuestros cambios en el *stage* seguirán intactos.

>En caso de que ya tengamos algún *commit* ejecutado, pero no lo hayamos subido con `git push` porque estabamos trabajando en otro, tenemos la opción de regresar al estado anterior usando un `git reset --soft HEAD~1`. Esto deshará el commit y pondrá nuestros cambios en el *stage*.


Una vez tengamos la versión más actualizada del proyecto en nuestro repositorio *local*; para no perder los cambios que se encuentren en el *stage* (sin haber ejecutado un commit) respaldaremos nuestro trabajo de esta forma:

```Shell
$ git stash
```

>Antes de ejecutar el siguiente comando, es de suponer; que debemos encontrarnos ubicados en nuestra rama de trabajo. Es decir, en la rama que nos generó el `merge request`.


Luego de tomadas las previsiones, podremos fusionar los nuevos cambios de la rama *develop* a nuestra rama de trabajo con el siguiente comando:

```Shell
$ git merge -s recursive -X theirs develop
```

Lo que ha ocurrido; es que hemos hecho la fusión, dándole prioridad a los nuevos cambios de la rama *develop* (`theirs`) para que sobrescriba los nuestros (`ours`) de manera *recursiva*.
Finalmente, después de hacer el merge podremos recuperar nuestros cambios (que aún no estaban *commiteados*). Y estos quedarán listos para agregarlos y subirlos para revisión y posterior fusión.

```Shell
$ git stash apply

$ git add --all

$ git commit -a

$ git push
```


<a name="#fusionar-los-cambios"></a>
### Fusionar los cambios

Existen dos maneras de cerrar el `merge request`. Desde la plataforma de *Gitlab* (lo cual recomendamos) y desde la consola.

Desde *Gitlab*, luego de marcar los *checklist* `Eliminar rama origen` y `Squash commits`. Desde aquí, evitamos hacer un *fast-forward* y eliminamos la rama del repositorio origen.

![Merge Requests](img/cerrar-merge-request1.jpg "Merge Requests")

Y desde la consola, teniendo cuidado de no permitir un *fast-forward* y previniendo así algún conflicto de versiones.
Ya ubicados en la rama correspondiente:

```Shell
$ git fetch origin

$ git checkout origin/develop

$ git merge --no-ff 2-guia-para-workflow
```

Y luego subiendo los cambios a la rama *develop*.

```Shell
$ git push origin develop
```

Para borrar la rama remota:

```Shell
$ git push origin --delete 2-guia-para-workflow
```

#### [Volver a Gitlab Workflow](#gitlab-workflow)

### Manejando las Etiquetas

Una etiqueta sirve para tener un nombre mas fácil de recordar un commit, sirve como un sobrenombre para apuntar hacia ahí.

Para crear una etiqueta con descripción:

```Shell
$ git tag -a nombre_etiqueta -m "mensaje de la etiqueta"
```

Para listar todas las etiquetas en orden alfabético:

```Shell
$ git tag
```


#### [Volver al inicio](#inicio)

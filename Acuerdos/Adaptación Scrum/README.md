# Definición del marco de trabajo

## Marco general de Scrum

Para este mini proyecto utilizaremos el marco de trabajo de scrum pero con algunas adaptaciones a sus ceremonias.

Al comienzo de cada sprint tendremos las ceremonias de **Refinement** y del **Sprint Planning** juntas.
Adaptamos estas dos ceremonias en una sola. Comenzaremos con la **refinement** para poder aclarar y terminar de definir algunas historias del backlog y luego pasaremos a la **planning** donde seleccionaremos las historias que realizaremos en el sprint que comienza.

La ceremonia de **Daily Scrum** la realizaremos 2 días a la semana, Lunes y Jueves.  
El primer Lunes de cada sprint, cancelaremos la **daily** para tener la ceremonia de **refinement** y **planning**.

Y por último tendremos las ceremonias de **Sprint Review** y **Sprint Retrospective**. Estas las llevaremos acabo el último Viernes de cada sprint, comenzaremos con la **review** y luego pasaremos a la **retro**.

## Roles del equipo

En este mini proyecto tendremos tres roles: Product Owner, Scrum Master y Developer, los cuales asignaremos a cada uno de los integrantes del equipo.

| Integrante         | Rol           |
| ------------------ | ------------- |
| Christian Patri    | Scrum Master  |
| Cristian Palma     | Product Owner |
| Federico Alonso    | Developer     |
| Juan Manuel Otegui | Developer     |

## Políticas de trabajo

### Definition of Ready

Una historia de usuario estará lista para poder ser planificada y ejecutada cuando se logre verificar que la misma cumple con los criterios INVEST con el objetivo de asegurar la calidad en la escritura de la historia.

Las características a cumplir son:

 - Independiente
 - Negociable
 - Valiosa
 - Estimable
 - Pequeña
 - Testeable

El proceso para escribir la historia comenzará con una primer idea por parte del product owner en conjunto con el cliente. Luego de que esten escritas todas las historias para abarcar el alcance de este proyecto, en equipo discutiremos una por una para determinar lo siguiente:

 - Estamos de acuerdo en realizar esa historia? (SI/NO)
 - En caso negativo la descartamos
 - En caso afirmativo la discutimos para aclarar mejor la idea.
 - Finalmente verificamos caracteristica por característica (INVEST) si la historia cumple haciendo las correcciones pertinentes.
  - Cuando verificamos lo anterior, entonces la declaramos como pronta para ser planificada y ejecutada.

### Definition of Done 

Se utilizará el proceso de BDD para trabajar con las historias de usuario. Para que una historia la consideremos que este terminada se deberá seguir los siguientes procesos (primero verificación y luego validación con el cliente):

 * Se conversa con el cliente de una de las necesidades del negocio, en nuestro caso seleccionamos una detallada en la letra del presente proyecto.
 * En equipo escribimos en lenguaje natural la narrativa y los escenarios de la historia de usuario.
  * Desarrollaremos uno o varios prototipos para presentarle al cliente 
 *  Verificamos que los prototipos cumplan con las siguientes heurísticas de Nielsen:
  
      1. Visibilidad del estado del sistema
      2. Coincidencia entre el sistema y el mundo real
      3. Dale al usuario el control y la libertad
      4. Consistencia y estándares
      5. Prevención de errores
      6. Reconocer en lugar de recordar
      7. Flexibilidad y eficiencia de uso
      8. Estética y diseño minimalista
      9. Ayuda al usuario a reconocer, diagnosticar y recuperarse de los errores
      10.  Ayuda y documentación

 * Finalmente validamos armando escenarios para hacer validaciones con usuarios de los prototipos creados y obtenemos el feedback. 
 * Si no hay correcciones de parte del usuario declaramos la historia como finalizada.
 * En el caso que haya que hacer correcciones se tendrán que realizar en otro sprint previa planificación y luego repetir este ciclo.
 * Al finalizar un sprint luego de hacer una reunión de equipo para el pull request subir el trabajo a la rama main.

Para la construcción de prototipos utilizaremos https://framer.com/

#### Lista a corroborar

  * Los criterios de aceptación se cumplieron
  * Se verifica el grado de cumplimiento de los prototipos con las 10 heurísticas de nielsen
  * El equipo concuerda (desarrolladores y product owner)
  * Se corrigieron las observaciones que surgieron durante la validación del usuario probando los escenarios.

Si cumple con lo anterior, al final del sprint el equipo subirá los cambios a producción, en nuestro caso al final de la iteración subimos reflejamos los cambios en la rama MAIN.


#### Tamaño del WIP (Work in Progress)

 * El tamaño acordado por el equipo es de 1 tarea por cada integrante.
 * Las tareas estaran estimadas para realizarla en 2 días.

#### Acuerdo para las reuniones del Equipo

 * Hacer 4 daily meetings por sprint distribuidas de la siguiente manera:

 >Primer semana del sprint :  Miércoles 18:00 y Viernes 18:00\
  Segunda  semana del sprint: Lunes 18:00 y Miércoles 18:00

 * Sprint planning:  Primer domingo de la primera semana del sprint.

 * Sprint review y sprint retrospective: último día del sprint (viernes de la segunda semana)


#### Revisiones con pull request:

 * El equipo acordó hacer los pull request al finalizar el sprint luego de las reuniones de sprint review y sprint retrospectiva.
 * Se realizará una reunión especifica para ejecutar esta tarea luego de debatir y hacer intercambio de ideas.
 * La estrategia es que durante un sprint se abre una rama con el nombre del sprint y al finalizar el mismo se efectuará un merge main.


 #### Validaciones de los prototipos:

 * El equipo acordó hacer validaciones de los prototipos creando escenarios.
 * Estas validaciones se podrán realizar durante un sprint para obtener feedback de forma temprana.

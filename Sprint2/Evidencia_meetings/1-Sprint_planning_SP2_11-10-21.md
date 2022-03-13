## Minuta del Spring Planning del Sprint 2 <a name=""></a>

#### Fecha : 11-10-2021
#### Integrantes : 

>Cristian Palma - Product Owner
 Federico Alonso - Desarrollador
 Christian Patri - Scrum Master
 Juan Otegui - Desarrollador

### Objetivo concentro de la iteración

Los objetivos de esta iteración son:

* Aplicar las sugerencias planteadas #issues por el docente.
* Completar las tareas pendientes del sprint 1
* Completar los prototipos y validarlos del 50% del total de épicas del product backlog.

Las épicas a completar en este sprint son:

* Registro e información de usuario
* Login
* Visualizar información relevante de la evolución de la Pandemia en Uruguay
* Interacciones con mi centro asistencial

#### Presentación de las historias de usuario y estimación de puntos de historia

### 01 Registrarse en el sistema
#### Puntos de historia: 3
#### Descripción

> * **Como**: usuario
> * **Quiero**: poder registrarme en el sistema
> * **Para**: acceder a las funcionalidades disponibles para los usuarios registrados

#### Criterios de aceptación 

*Escenario: Registro exitoso de un usuario nuevo*

> * **Dado**: un usuario sin registrarse en el sistema que selecciona la opción "Registrarse"
> * **Cuando**: ingresa: \
         -> CI válida\
         -> Celular válido 
> * **Entonces**: el usuario queda registrado en el sistema

*Escenario: Registro sin éxito de un usuario CI no válida*

> * **Dado**: un usuario sin registrarse en el sistema que selecciona la opción "Registrarse"
> * **Cuando**: ingresa: \ 
        -> CI  no válida\
        -> celular válido (numero ANTEL, CLARO O MOVISTAR de Uruguay)
> * **Entonces**: el sistema lanza un mensaje de error informando que la ci es incorrecta

*Escenario: Registro sin éxito de un usuario celular no válido*

> * **Dado**: un usuario sin registrarse en el sistema que selecciona la opción "Registrarse"
> * **Cuando**: ingresa\ 
    -> CI   válida\
    -> celular NO válido
> * **Entonces**: el sistema lanza un mensaje de error informando que el celular no es válido

*Escenario: Registro sin éxito de un usuario CI ya registrada*

>  * **Dado**: un usuario sin registrarse en el sistema que selecciona la opción "Registrarse"
> * **Cuando**: ingresa\ 
    -> CI   ya registrada en el sistema\
    -> celular NO válido
> * **Entonces**: el sistema lanza un mensaje de error informando que la CI ya se encuentra registrada en el sistema
### 04 Login
#### Puntos de historia: 1
#### Descripción

> * **Como**: un usuario registrado
> * **Quiero**: poder iniciar sesión
> * **Para**: poder utilizar los recursos de la plataforma

#### Criterios de aceptación

*Escenario: Inicio de sesión usuario registrado*

>  * **Dado**: un usuario registrado y  una contraseña correcta
> * **Cuando**: inicia sesión
> * **Entonces**: puede acceder a los recursos que tiene permiso

*Escenario: Inicio de sesión fallido sin bloqueo de usuario*

>  * **Dado**: un usuario registrado y una contraseña incorrecta y sin intentos fallidos para el usuario registrado
> * **Cuando**: inicia sesión
> * **Entonces**: el usuario es notificado de su error y el sistema contabiliza el intento fallido

*Escenario: Inicio de sesión fallido con bloqueo de usuario*

>  * **Dado**: un usuario registrado y una contraseña incorrecta y 2 intentos fallidos para el usuario registrado
> * **Cuando**: inicia sesión
> * **Entonces**: el usuario es notificado de su error y el usuario es bloqueado para acceder al sistema
### 02 Actualizar datos personales
#### Puntos de historia: 3
#### Descripción

> * **Como**: usuario registrado y autenticado
> * **Quiero**: poder cambiar mis datos personales
> * **Para**: tener actualizado dicha información

#### Criterios de aceptación

*Escenario: usuario autenticado actualiza correctamente sus datos*

>  * **Dado**: un usuario correctamente autenticado en el menú de Actualizar datos personales
> * **Cuando**: modifica alguno de los siguientes datos:\
    -> Nombre completo (no vacío)\
    -> Teléfono  (válido)\
    -> Fecha de nacimiento\
    -> Departamento\
    -> Dirección\
    -> Prestador de Salud\
  y oprime el botón "Confirmar"
> * **Entonces**: el sistema actualiza los datos del usuario

*Escenario: usuario autenticado actualiza incorrectamente sus datos*

>  * **Dado**: un usuario correctamente autenticado en el menú de Actualizar datos personales
> * **Cuando**: modifica alguno de los siguientes datos:\
        -> Nombre completo (vacío)\
        -> Teléfono  (no válido)\
        -> Fecha de nacimiento\
        -> Departamento\ 
        -> Dirección\
        -> Prestador de Salud\
        y oprime el botón "Confirmar"
> * **Entonces**: el sistema informa "nombre incorrecto" y  "teléfono incorrecto"  marcando el error en los campos donde fue ingresada la información.
### 03 Actualizar condición de salud personal
#### Puntos de historia: 2
#### Descripción

> * **Como**: usuario autenticado
> * **Quiero**: poder actualizar mi condición de salud
> * **Para**: recibir las notificaciones pertinentes al plan de vacunación que correspondan a mi condición especifica de salud

#### Criterios de aceptación

*Escenario: usuario autenticado actualiza correctamente su condición de salud*

> * **Dado**: un usuario autenticado que se encuentra en el menú "Actualizar condición de salud"
> * **Cuando**: modifica alguna de las siguientes condiciones seleccionando (SI o NO)\
        -> diabetes (SI/NO)\
        -> enfermedad cardiovascular (SI/NO)\ 
        -> inmunodeficiencia congénita o adquirida (SI/NO)\
        -> cáncer (SI/NO)\
        -> VIH (SI/NO)
> * **Entonces**: el sistema actualiza los datos y el usuario visualiza un mensaje "Datos actualizados correctamente"
### 05 Restablecer contraseña
#### Puntos de historia: 1
#### Descripción

> * **Como**: usuario
> * **Quiero**: poder restablecer mi contraseña
> * **Para**: poder ingresar al sistema en el caso que haya olvidado la misma

#### Criterios de aceptación

*Escenario: usuario registrado en el sistema que solicita recuperar la contraseña con éxito*

>  * **Dado**: un usuario registrado no autenticado en el menú de "recuperar la contraseña"
> * **Cuando**: ingresa:\ 
    -> cédula (registrada en el sistema)\
    -> celular (registrado en el sistema)
> * **Entonces**: el sistema envía un sms al usuario con una contraseña nueva.

*Escenario: usuario registrado en el sistema que solicita recuperar la contraseña indicando una CI  o teléfono no válida*

>  * **Dado**: un usuario registrado no autenticado en el menú de "recuperar la contraseña"
> * **Cuando**: ingresa:\ 
    -> cédula (no válida)\
    -> celular  (no válida)
> * **Entonces**: el sistema informa mediante un mensaje de error:  "CI y/o Celular no válido"

*Escenario: usuario solicita recuperar la contraseña indicando datos inexistentes en el sistema.*

>  * **Dado**: un usuario no autenticado en el menú de "recuperar la contraseña"
> * **Cuando**: ingresa:\ 
        -> cédula (inexistente en el sistema)\
        -> celular (inexistentes en el sistema)
> * **Entonces**: el sistema informa mediante un mensaje de error:  "CI y/o Celular no registrados"
### 06 Información relevante para una fecha seleccionada
#### Puntos de historia: 2
#### Descripción

> * **Como**: usuario
> * **Quiero**: poder visualizar la información de la pandemia en Uruguay en una fecha seleccionada
> * **Para**: poder estar informado de la situación sanitaria del país

#### Criterios de aceptación 

*Escenario: usuario selecciona una fecha para ver los datos de la pandemia en Uruguay*

>  * **Dado**: un un usuario autenticado o no autenticado en el menú "Información" pestaña por fecha
> * **Cuando**: el usuario selecciona una fecha
> * **Entonces**: puede visualizar los siguientes datos relevantes de la pandemia:\
    -> Casos nuevos\
    -> Casos totales\
    -> Casos en CTI\
    -> Fallecidos\
    -> Fallecidos totales\
    -> Test realizados\
    -> Porcentaje de test positivos
### 07 Información relevante de la evolución de la pandemia en un período
#### Puntos de historia: 3
#### Descripción

> * **Como**: usuario
> * **Quiero**: poder visualizar la información de la evolución de la pandemia de forma gráfica
> * **Para**: poder comprender de forma rápida la evolución de la pandemia en Uruguay

#### Criterios de aceptación 

*Escenario: usuario visualiza información de la evolución de la pandemia en un periodo seleccionado*

>  * **Dado**: un un usuario autenticado o no autenticado en el menú "Información" pestaña por período
> * **Cuando**: el usuario selecciona una período:\
    -> Últimos 60 días\
    -> Últimos 30 días\
    -> Últimos 14 días\
    -> Todo (desde el 01/03/2020)
> * **Entonces**: puede visualizar los siguientes datos relevantes de la pandemia de forma gráfica:\
    -> evolución de casos nuevos\
    -> evolución de test realizados\
    -> evolución de los casos activos\
    -> evolución de fallecidos\
    -> ocupación CTI

    
### 08 Formulario de síntomas
#### Puntos de historia: 2
#### Descripción

> * **Como**: usuario registrado en el sistema
> * **Quiero**: tener un diagnóstico informando los síntomas que presento
> * **Para**: saber si tengo la posibilidad de estar infectado con COVID-19

#### Criterios de aceptación 

*Escenario: usuario autenticado completa con éxito formulario "tengo síntomas"*
> * **Dado**: un usuario autenticado que selecciona la función "tengo síntomas"
  Y con el centro de salud en estado "confirmado"
> * **Cuando**: completa la información (SI/NO) de los siguientes síntomas:\
        -> tos\
        -> fiebre mayor a 37.8° C\
        -> dificultar al respirar\ 
        -> resfrío\
        -> dolor de garganta\
        -> pérdida de olfato\ 
        -> pérdida del gusto.
> * **Entonces**: la aplicación le envía una notificación al centro de salud del usuario correspondiente con los datos del formulario
  y se le informa al usuario "los datos fueron enviado con éxito, su centro de salud se pondrá en contacto con Ud"
### 09 Formulario para indicar contacto con un caso confirmado
#### Puntos de historia: 3
#### Descripción

> * **Como**: usuario registrado en el sistema
> * **Quiero**: poder informar a mi prestador de salud que tuve contacto con un caso confirmado de COVID-19
> * **Para**: poder coordinar un test que verifique si me encuentro infectado

#### Criterios de aceptación 

*Escenario: usuario autenticado completa con éxito formulario "contacto con un caso confirmado"*

>  * **Dado**: un usuario autenticado que selecciona la función "Tuve contacto con un caso confirmado"
   Y con el centro de salud en estado "confirmado"
> * **Cuando**: completa la información:\
        -> fecha del contacto\
        -> lugar donde fue el contacto (opcional)\
        -> ci del contacto (opcional)\
        -> nombre del contacto (opcional)\
        -> síntomas (SI/NO)  tos, fiebre mayor a 37.8° C, dificultar al respirar, resfrío, dolor de garganta, -> pérdida de olfato, pérdida del gusto. 
> * **Entonces**: la aplicación le envía una notificación al centro de salud del usuario correspondiente con los datos del formulario
  y se le informa al usuario que debe hacer cuarentena hasta realizar TEST PCR
  y  que su centro de salud se pondrá en contacto
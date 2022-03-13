# Prototipo Actualizar datos personales

A continuación se hará un análisis de las heurísticas de Nielsen en referencia al prototipo en cuestión. El puntaje será de 1 a 5 siendo 1 que aplica muy poco y 5 que se ajusta correctamente. En caso de valer 0 es porque no se aplica al prototipo estudiado.

| Heurística | Resumen | Valor | Observaciones |
|------------|---------|-------|---------------|
| Visibilidad del estado del sistema | El sistema debe siempre mantener a los usuarios informados del estado del sistema, con una realimentación apropiada y en un tiempo razonable. | 5 | Se indica claramente lo que se requiere en cada campo a completar, se ilustra con ejemplos de "placeholder". |
| Coincidencia entre el sistema y el mundo real | El sistema debe hablar el lenguaje de los usuarios, con las palabras, las frases y los conceptos familiares, en lugar de que los términos estén orientados al sistema. Utilizar convenciones del mundo real, haciendo que la informacion aparezca en un orden natural y lógico. | 5 | Cumple correctamente. |
| Dale al usuario el control y la libertad | Los usuarios eligen a veces funciones del sistema por error y necesitan a menudo una salida de emergencia claramente marcada, esto es, salir del estado indeseado sin tener que pasar por un diálogo extendido. Es importante disponer de deshacer y rehacer. | 5 | En caso de ingresar por error o no querer continuar con el formulario el usuario puede volver a la pantalla principal. |
| Consistencia y estándares | Los usuarios no deben tener que preguntarse si las diversas palabras, situaciones, o acciones significan la misma cosa. En general siga las normas y convenciones de la plataforma sobre la que se esta implementando el sistema. | 5 | Mantiene el mismo formato de los otros prototipos. |
 Prevención de errores | Es importante prevenir la aparición de errores que mejor que generar buenos mensajes de error. | 2 | Pocos mensajes de error, solamente en el campo Nombre y Teléfono. No se explica a que se debe el error (debería indicar porque es incorrecto el dato ingresado). La fecha de nacimiento permite ingresar datos incorrectos.|
| Reconocer en lugar de recordar | El usuario no deberia tener que recordar la información de una parte de diálogo a la otra. Es mejor mantener objetos, acciones, y las opciones visibles que memorizar. | 2 | El prototipo NO indica que acción se esta realizando, en que pantalla me encuentro, debiendo recordar el usuario a la funcionalidad que ingresó. |
| Flexibilidad y eficiencia de uso | Las instrucciones para el uso del sistema deben ser visibles o fácilmente accesibles siempre que se necesiten. Los aceleradores no vistos por el usuario principiante, mejoran la interacción para el usuario experto de tal manera que el sistema puede servir para usuarios inexpertos y experimentados. Es importante que el sistema permita personalizar acciones frecuentes. | 4 | Al prototipo se accede desde la pantalla de inicio. El sistema no permite personalizar acciones frecuentes. |
| Estética y diseño minimalista | No deben contener la información que sea inaplicable o se necesite raramente. Cada unidad adicional de la información en un diálogo compite con las unidades relevantes de la información y disminuye su visibilidad relativa. | 5 | El diseño sólo contiene la información relevante. |
| Ayuda al usuario a reconocer, diagnosticar y recuperarse de los errores | Que los mensajes de error se deben expresar en un lenguaje claro (no haya codigos extraños), se debe indicar exactamente el problema, y deben ser constructivos. | 2 | No se indica exactamente el problema en caso de error. |
| Ayuda y documentación | Aunque es mejor si el sistema se pueda usar sin documentación, puede ser necesario disponer de ayuda y documentación. Esta ha de ser fácil de buscar, centrada en las tareas del usuario, tener información de las etapas a realizar y que no sea muy extensa. | 1 | No se muestra información de qué puede realizar el usuario en el prototipo. |
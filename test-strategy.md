Fecha: [25/08/2023]
Preparado por: [Christian Alejandro Leon Rabanales]
Proyecto: Juego "Adivina tu Número"

Resumen Ejecutivo
Este documento describe la estrategia de pruebas y corrección empleada para abordar y solventar las deficiencias identificadas en el juego "Adivina tu Número". A través de pasos metódicos y deliberados, se documenta el enfoque adoptado para garantizar la funcionalidad y el cumplimiento de los requisitos.
Objetivos

*Los objetivos principales de esta estrategia son:

    +Identificar y corregir errores en el código del juego "Adivina tu Número".
    +Garantizar que el juego funcione según los requerimientos y especificaciones del enunciado.

*Proceso de Pruebas y Corrección

    -Identificación de Errores
        +Revisión minuciosa del código línea por línea.
        +Detección de errores sintácticos, problemas de anidación de etiquetas HTML y otros aspectos de escritura.
        +Verificación de que todas las etiquetas HTML estén cerradas adecuadamente.

    -Cumplimiento de Requisitos
        +Verificación de la congruencia de la lógica con los requisitos del enunciado.
        +Confirmación de la generación de números aleatorios entre 1 y 100.
        +Aseguramiento de que el juego permita 10 intentos y muestre mensajes apropiados.

    -Validación de Entrada
        +Confirmación de la validación adecuada de la entrada del jugador.
        +Aseguramiento de que solo se permitan números enteros como entrada válida.
        +Verificación de la correcta presentación de alertas en caso de entrada inválida.

    -Corrección de Errores en JavaScript
        +Identificación y corrección de errores de sintaxis.
        +Ajuste de nombres incorrectos de variables y funciones siguiendo las indicaciones proporcionadas.

    -Funcionalidad de Botones y Eventos
        +Verificación de la operatividad de los botones y eventos interactivos.
        +Confirmación de que la función checkGuess() maneje los diversos resultados de manera precisa.

    -Mensajes y Estilos
        +Validación de que los mensajes se muestren de forma adecuada según los resultados del juego.
        +Verificación de la adaptación de los estilos de mensajes de acuerdo con los resultados esperados.

    -Depuración y Pruebas
        +Realización de pruebas exhaustivas en diferentes escenarios de juego.
        +Evaluación de intentos válidos e inválidos, así como aciertos antes y después del último intento.
        +Uso de la consola del navegador para rastrear y depurar errores y mensajes.

*Resultados de la Corrección
Se identificaron y corrigieron los errores identificados en el juego "Adivina tu Número" siguiendo los pasos delineados en esta estrategia. El juego ahora cumple con los requisitos y se espera que funcione de manera coherente con las especificaciones del proyecto.

Siendo estos los cambios realizados:
    -Estilo CSS:
        +Se creó un nuevo estilo .error para resaltar los mensajes de error en rojo.

    -Etiquetas HTML:
        +Cambiada la clase de <p class="lastResult"></p> a <p class="message"></p> para unificar el estilo de los mensajes.

    -Variables y Constantes JavaScript:
        +Corregido el nombre de la constante de ATTEMPS a ATTEMPTS para utilizar nombres consistentes.
        +Cambiado el nombre de la variable lastResult a message para unificar el estilo de los mensajes.

    -Generación de Número Aleatorio:
        +Modificada la generación de números aleatorios en las líneas let randomNumber = Math.floor(Math.random() * 100) + 1; para cumplir con el rango de 1 a 100.

    -Validación de Entrada:
        +Agregada la función displayErrorMessage() para mostrar mensajes de error resaltados en rojo cuando el usuario ingrese un valor no válido.
        +Modificada la función checkGuess() para mostrar el mensaje de error con la función displayErrorMessage() si el usuario no ingresa un número válido.

    -Función checkGuess():
        +Modificada para usar la función displayErrorMessage() en caso de entrada no válida.
        +Actualizado el mensaje de pérdida para mostrar el número correcto: displayMessage('¡Perdiste! El número era ' + randomNumber + '.', 'red');.

    -Función setGameOver():
        +Cambiado el mensaje del botón de reinicio a "Comenzar un nuevo juego".

    -Función resetGame():
        +Modificada la generación de números aleatorios al reiniciar el juego: randomNumber = Math.floor(Math.random() * 100) + 1;.
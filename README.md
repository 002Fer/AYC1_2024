# Manual Técnico
## Proyecto: Calculadora con Funcionalidad de Memoria
## Arquitectura: ARM64
# Fernando Misael Morales Ortiz
## 202001950


## Descripcion

El programa es una calculadora simple implementada en ensamblador ARM64 que permite al usuario realizar operaciones aritméticas básicas como suma, resta, multiplicación y división. También ofrece la opción de operar con memoria, es decir, permite realizar operaciones utilizando valores almacenados en memoria.

El usuario interactúa con el programa a través de un menú de opciones, donde puede seleccionar la operación deseada. El programa convierte la entrada de usuario (en formato ASCII) en números enteros, realiza las operaciones solicitadas, y luego convierte los resultados en cadenas de texto para mostrarlos.

## Organización del Código
## .data (Segmento de Datos)

Contiene cadenas de texto utilizadas para imprimir mensajes en pantalla y para procesar la entrada del usuario.

## .bss (Segmento de Variables Sin Inicializar)

En este segmento se definen los buffers que almacenan la entrada del usuario y los resultados de las operaciones.

## .text (Segmento de Código)

Contiene el código ejecutable del programa, incluidas las macros para entrada/salida, las funciones para conversión de datos y el bucle principal de ejecución.
## atoi (ASCII to Integer)

Convierte una cadena de caracteres (ASCII) que representa un número en formato entero.

    Recorre la cadena carácter por carácter y convierte cada dígito a su valor numérico.
    Gestiona números negativos.
    Utiliza multiplicadores para determinar el valor posicional de cada dígito.

# itoa (Integer to ASCII)

Convierte un número entero en su representación como cadena de caracteres ASCII.

    Convierte el número entero dividiéndolo en sus dígitos y convirtiendo cada uno a su valor ASCII.
    Añade un signo negativo si es necesario.
    Gestiona correctamente números negativos y el caso especial del número cero.
## macros
son secciones que sirven como funiones en este caso se usaron para poder hacer el pedido de una de las opciones del menu 

# _start (Punto de Entrada)

El flujo principal del programa comienza en la etiqueta _start, que contiene los siguientes pasos:

    Mostrar Encabezado y Menú Principal:
        Limpia la pantalla con clear_screen.
        Muestra el encabezado de la universidad y el menú de opciones.

    Leer la Opción del Usuario:
        Usa la macro read para obtener la opción del usuario desde el menú principal.
        Dependiendo de la opción seleccionada, realiza una de las siguientes operaciones: suma, resta, multiplicación, división o salir del programa.

    Operaciones Aritméticas:
        El programa solicita dos operandos al usuario y los convierte a enteros usando la función atoi.
        Ejecuta la operación seleccionada (suma, resta, multiplicación, división).
        Si se selecciona división, verifica si el divisor es cero y, de ser así, muestra un mensaje de error.

    Mostrar Resultados:
        El resultado de la operación se convierte de nuevo a una cadena ASCII usando la función itoa.
        Imprime el resultado en pantalla.
        Espera a que el usuario presione una tecla para continuar o finalizar el programa.
<a href="https://imgbb.com/"><img src="https://i.ibb.co/SJv4xJN/Captura-desde-2024-09-24-17-11-08.png" alt="Captura-desde-2024-09-24-17-11-08" border="0"></a>
![Nombre del Documento](https://i.ibb.co/x2f3n6F/Captura-desde-2024-09-24-16-59-15.png)
![Nombre del Documento](https://i.ibb.co/Rbbcjqn/Captura-desde-2024-09-24-17-06-09.png)
![Nombre del Documento](https://i.ibb.co/j4PwF4H/Captura-desde-2024-09-24-17-07-25.png)
## Pruebas

![Nombre del Documento](https://i.ibb.co/nkpcFQ3/Captura-desde-2024-09-24-17-09-52.png)
![Nombre del Documento](https://i.ibb.co/SJv4xJN/Captura-desde-2024-09-24-17-11-08.png)
![Nombre del Documento](https://i.ibb.co/LvyVpGh/Captura-desde-2024-09-24-17-12-28.png)

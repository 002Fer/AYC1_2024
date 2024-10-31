# ACYE1_A_2S24_202001950

# Manual Técnico
## PROYECTO NO. 2
## Arquitectura: ARM64
# Fernando Misael Morales Ortiz
## 202001950
##
## Descripcion
la aplicación trata sobre hojas de cálculo realizadas en el lenguaje Ensamblador.
Dicho software permitirá manejar datos numéricos por medio de diversas operaciones
matemáticas y lógicas, operando sobre datos puntuales o rangos. Se interactuará con
el programa a través de una interfaz de línea de comandos por la cual se instruirá al
programa sobre las acciones que debe realizar
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

## itoa (Integer to ASCII)

Convierte un número entero en su representación como cadena de caracteres ASCII.

    Convierte el número entero dividiéndolo en sus dígitos y convirtiendo cada uno a su valor ASCII.
    Añade un signo negativo si es necesario.
    Gestiona correctamente números negativos y el caso especial del número cero.
## macros
son secciones que sirven como funiones en este caso se usaron para poder hacer el pedido de una de las opciones del menu 

## import_data/readCSV/openfile
Esta seccion de codigo se encarga de poder cargar un archivo CSV que puede contener cualquier dato y las almacena en los registros para poder ir colocando cada dato en la columna y fila correspondiente

## imprimirCeldas
se encarga de poder imprimier el cuadro que simula la cuadrilla de exel mostrando las columnas y su identificacion ademas de las filas con su numeral correspondiente
## verificarParametro
es la parte central debido a que se encarga de poder ir verificando y leyendo cada parametro que el usuario esta ingresando para luego ir viendo a que etiqueta irse y ejecutar la funcion correspondiente
## verificarComando
en esta parte se va verificando que la plantilla no se sobrepase de los parametros planteados en el proyecto

## verificarASTERISCO
en esta parte se va verificando que al comando guardar le siga el asterisco para poder hacer el guardado del resultado de la operacion y poder almacenarla en alguna de las celdas de la plantilla 
## palabra intermedia
en esta parte se va verificando que en el comando diferencia que tipo es, si es para guardar, hacer alguna operacion, hacer una importacion etc.



# _start (Punto de Entrada)

El flujo principal del programa comienza en la etiqueta _start, que contiene los siguientes pasos:
primero muestra en pantalla los datos personales por un momento hasta que se le de enter y luego:

Va verificando el comando y dependiedo de ese hace una comparacion para ir a la etiqueta correspondiente y si no son iguales va buscando a la que le corresponde 


# Manual De Usuario
## PROYECTO NO. 2
## Arquitectura: ARM64
# Fernando Misael Morales Ortiz
## 202001950

## Inicio del programa
<img src="https://i.ibb.co/0sv5HX6/Captura-desde-2024-10-30-23-46-43.png">

inicialmente muestra datos personales como el nombre de la universidad, facultad, curso, nombre y carnet


## Cuadricula inicial
<img src="https://i.ibb.co/NTjLKQq/Captura-desde-2024-10-30-23-57-58.png">
aca muestra el tablero que inicialmente esta lleno de ceros que despues ira almacenando los valores que el usuario vaya digitando

## Inicio del programa
<img src="https://i.ibb.co/68dNGCN/Captura-desde-2024-10-31-00-00-29.png">
aca muestra el area correspondiente para poder ingresar los comandos 

## Ejemplo de comandos
<img src="https://i.ibb.co/2dzPfQp/Captura-desde-2024-10-31-00-02-32.png">
aca hay unos ejemplos de los comandos que se puede ingresar 

## Ejemplo de el comando Guardar
<img src="https://i.ibb.co/TMbY13D/Captura-desde-2024-10-31-00-04-21.png">
aca hay unos ejemplos de como se ingresa un comando y que se va reflejando automaticamente en la plantilla

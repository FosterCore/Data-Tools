# Comandos de Excel

 * [Atajos de Teclado](#atajos-de-teclado)
 * [Símbolos](#símbolos)
 * [Formulas](#formulas)
 * [Gráficos](#gráficos)

## [Atajos de Teclado](#comandos-de-excel)

 * ``Ctrl + Espacio`` : Seleccionar columna. Para acomodar el texto de toda la tabla es necesario seleccionar todas las columnas completas.
 * ``Shift + Espacio`` : Seleccionar fila.
 * ``Shift + F11`` : Nueva Hoja.
 * ``Ctrl + 1`` : Abre la ventana **Formato de Celdas**.
 * ``Ctrl + +`` : Aumentar fila, columna o celdas  (depende de lo que tengas seleccionado).
 * ``Ctrl + -`` : Elimina fila, columna o celdas  (depende de lo que tengas seleccionado).
 * ``Ctrl + E o Ctrl + Shift + Espacio`` : Selecciona toda una tabla hasta donde terminan sus datos.
 * ``Ctrl + B`` : Abre el cuadro de Buscar y Reemplazar. La opción *Coincidir con el contenido de toa la celda* en caso queramos reemplazar una palabra que contiene espacio ejm: Banda y Banda 16 (queremos cambiar solo las "bandas")
 * ``Ctrl + T`` : Insertar Tabla.
 * ``Ctrl + X`` : Cortar. Al cortar una columna entera podemos insertarla usando `Ctrl + +`.
 * ``Ctrl + Z`` : Deshacer.
 * ``Ctrl + Y`` : Rehacer.
 * ``Ctrl + Click`` : Selecciona o deselecciona convenientemente (Sombreado por separado).
 * ``Ctrl + Shift + 1`` : Convertir a formato numero, con sus separador de miles.
 * ``Ctrl + Shift + 3 o Ctrl + W`` : Convertir a formato fecha.
 * ``Ctrl + Shift + 4`` : Convertir a formato moneda (pesos, soles, dolares...).
 * ``Ctrl + Shift + 5`` : Convertir a formato porcentaje.
 * ``Ctrl + Shift + L`` : Saca el filtro a los encabezados. Los filtros no captan los espacios demás, las tablas dinámicas si las diferencia. La opción *Texto en columnas>De ancho fijo* quita los espacios y unifica con su similar (en caso los datos tenga espacios junto con otro dato no funcionara. Ejm: "Banda 16")
 * ``Ctrl + ,`` : Nos da la fecha actual .
 * ``Ctrl + Shift + .`` : Nos da la hora actual.
 * ``Ctrl + Shift + ↔`` : Desplaza y sombrea hasta la última celda con datos de izquierda a derecha.
 * ``Ctrl + Shift + ↨`` : Desplaza y sombrea hasta la última celda con datos de arriba a abajo.
 * ``Ctrl +av.pag`` : Desplaza hacia la siguiente pestaña (hoja).
 * ``Ctrl +re.pag`` : Desplaza hacia la anterior pestaña (hoja).
 * ``Alt + F11`` : Abre el editor *Visual Basic*
 * ``Alt + W + K`` : Activa o desactiva las líneas de cuadricula.
 * ``Alt + O + V + V`` : Pegado especial sin formato.
 * ``Alt + O + V + T`` : Pegado especial Transponer.
 * ``Alt + Shift + =`` : Auto Suma. Completa auto-suma a todo un cuadro con espacios en blanco al final.
 * ``Alt + Shift + →`` : Agrupa celdas seleccionadas pudiendo mostrarlas u ocultarlas.
 * ``Alt + Shift + ←`` : Desagrupa celdas seleccionadas pudiendo mostrarlas u ocultarlas.
 * ``Archivo>Opciones>Opciones Avanzadas>Opc. de presentación de esta hoja>Mostrar saltos de pagina`` : Quitas las lineas de visualización de saltos de pagina. Se suelen quedar pegadas tras ver la impresión de la pagina.
 * ``Ctrl + F1`` : Ocultar/Mostrar Barra de Inicio y demás herramientas.
 * ``Ctrl + J`` : Rellena hacia abajo, para simular el autocompletado es necesario sombrear incluyendo a la celda con formula hasta las celdas en blanco hacia abajo que querramos.
 * ``Ctrl + Shift + E`` : Relleno rápido e inteligente, rellena celdas en blanco según lo que tengamos seleccionado en la primera celda.

## [Símbolos](#comandos-de-excel)

 * **``+``** :	Suma
 * **``-``** :	Resta. Para suma de negativos: Sumamos los negativos poniendo el símbolo "-" seguido de la función Sum().
 * **``/``** :	Divide
 * **``*``** :	Multiplica
 * **``%``** :	Porcentaje (Divide entre 100). Divide el numero de la celda entre 100 *F19%*
 * **``&``** :	Concatenar. Incluir espacio *+A1&" "&B1*. Concatenar un símbolo con una formula. *">"&Promedio(A1:B2)*
 * **``^``** :	Elevar a
 * **``=``** :	Igual
 * **``>``** :	Mayor que
 * **``<``** :	Menor que
 * **``>=``** :	Mayor o igual que
 * **``<=``** :	Menor o Igual que
 * **``<>``** :	No igual a

Terminología:

 * **``#``** :	Indica espacio para un dígito. Ejm: cualquier numero de 3 dígitos = ###
 * **``?``** :	Indica espacio para una Letra. Ejm: cualquier palabra de 3 letras = ???


## [Formulas](#comandos-de-excel)

### Fechas

 * **``=hoy()``** :	Arroja la fecha actual de hoy.
  
 * **``=si(Arg1,arg_verdad,arg_falso)``** :	Función condicional. Si dejas un argumento vació significa no modificar. Ejm: =SI(E9>=$L$10;"Si descuento";"No descuento"). También podemos añadir función dentro de una función para tener 3 opciones. Si(arg1,arg_verdad,si(arg,arg_verdad,arg_falso))
  
 * **``=Y()``** : Esta función Añade más valores lógicos `and` para aumentar condiciones .Se suele usar junto con la función ``SI()`` para aumentar los valores lógicos por el cual se tenga un arg verdadero y falso. Si(Y(Arg1,Arg2,Arg3),arg_verdad,arg_falso). Es importante respetar el orden e ir llenando la función con los datos de mayor a menor.

 * **``=O()``** : Esta función es de tipo condicional `or` .Se suele usar junto con la función ``si()`` para aumentar los valores lógicos por el cual se tenga un arg verdadero y falso. Si(O(Arg1,Arg2,Arg3),arg_verdad,arg_falso).

 * **``=SI.CONJUNTO(Arg1,arg_verdad1,Arg1,arg_verdad1..)``** :	Es una función ``si()`` mejor ordenada.

 * **``=BuscarV(Celda a buscar,Matriz,Columna de la matriz,Precision exacta o aproximada)``** :	Esta función busca un dato dentro de una matriz indicando en que columna de la matriz esta el dato que queremos que retorne, puede retornar un dato coincidiendo la celda a buscar con un valor exacto o aproximado (Buscara el inmediato inferior).<br>
 En computación el valor 0 = Falso y 1 = Verdadero.<br>
 BuscarV no puede hacer búsquedas hacia la izquierda. Tampoco se puede hacer un arrastre de su formula.
 

 * **``=BuscarH(Celda a buscar,Matriz,Fila de la matriz,Precision exacta o aproximada)``** :	Esta función es igual que `BuscarV()` solo que no le indicamos la búsqueda por columnas sino por filas.

 * **``=SI.error(Valor,ValorSI.ERROR)``** : Esta función se usa para evitar los #N/A (error de excel). En caso de error indicamos que nos devuelva un valor que le indiquemos.
  
 * **``=Sumar.SI(Rango,Criterio,RangodeSuma)``** : Esta función se toma un rango de valores que vamos a indicarle un criterio para sumar nuestro rango de suma (Valores que vamos a sumar). ejem: *Sumar.SI(H:H;"<0";E:E)*

 * **``=Sumar.SI.Conjunto(RangodeSuma,Rango1,Criterio1..., Rango2,Criterio2)``** : Es lo mismo que `Sumar.Si` solo que los criterios van anidados al rango que queremos que dependan. Siempre es bueno fijar todo lo que sea rangos. ejem: *Sumar.SI(H:H;;E:E;"<0";P:P;"Monterrey")*

 * **``=Contar(Valor1,Valor2..,etc)``** : Esta función cuenta solo valores numéricos, lo textos los ignora.

 * **``=Contara(Valor1,Valor2..,etc)``** : Esta función cuenta todo tipo de datos numéricos y textos.

 * **``=Contar.Si(Rango,Criterio)``** : Condicional de contar.

 * **``=Contar.SI.Conjunto(Rango1,Criterio1..., Rango2,Criterio2)``** : Función contar con varias condicionales.

 * **``=Coincidir(Valor Buscado,Matriz,Precision)``** : Esta función nos retorna el numero de posición del dato (indice).En la ``precision`` se suele usar 0 = exacto, 1 = aproximado. Nota: en la criterio ``matriz`` si seleccionamos los títulos esto aumentara en 1 al resultado de la posición de nuestro valor a buscar. Al igual que `BuscarV` si no encuentra un dato devuelve #N/D.

 * **``=indice(Matriz,nºfila,nºcolumna)``** : Esta función retorna un dato tras señalar su posicionamiento en la tabla ( matriz, fila y columna) para lo cual se apoya con el `coincidir` para ellos (fila y columna).<br>
 La ventaja con indice - coincidir es que se puede hacer un arrastre en su formula cosa que no se puede con `BuscarV`

## [Gráficos](#comandos-de-excel)

Se suele poner como Sub-titulo el tipo de gráfico que haces y como titulo la conclusion o análisis de la gráfica.

 * **``G. Barras``** :	Se puede usar para casi todo tipo de contexto. Barras verticales cuando el titulo cabe, Barras Horizontales cuando el titulo no cabe (es grande).
 * **``G. Lineas``** :	Se suele utilizar cuando hay tiempo involucrados, con el fin de ver la evolución de los tiempo (Fechas).
 * **``G. Dispersion``** :	Scatter. Se suele utilizar para hacer comparación entre 2 variables. 
 * **``G. Cascada``** :	Se usa para ver la diferencia entre un tiempo vs otro de sus respectivos items. Ejm: Costos de Julio vs Agosto.



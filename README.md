# lab01- sumador 
Laboratorio 01: Introducción a HDL
Nisefoles Vargas Yepes

1.Sumador de 1 bit.

Para crear nuestro codigo en verilog primero debemos identificar las entradas, salidas y cables necesarios para implementar nuestro sumador de 1 bit. Este funciona muy facil entra A,B,Ci el resultado se muestra en S y el carry (número se "lleva"), si tenemos 1+1+1 el resultado es 1 y lleva 1, pero si se ingresa 1+0+1 el resultado es 0 y el carry es 1. 
Una vez hecho esto vamos a iniciar a crear el código, el primer paso y mas importante es crear un modulo.
El modulo es necesario para crear cualquier código ahí debemos introducir nuestras variables del código y el cuerpo del texto.
En el modulo ingresamos primero las entradas separadas por comas y luego las salidas.
En el cuerpo del modulo debemos crear las entradas y salidas.
Las entradas seran input, que son los datos que nosotros ingresamos a nuestro sistema en este caso numeros de un bit.
Las salidas seran output, que son los datos obtenidos al pasar las entradas en nuestro sistema.
Los cables seran wire estos se utilizan para la conexíon.
![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/sum1bcc_primitive.PNG)
La parte de los operadores lógicos se le asignan los cables y/o datos de entrada y salida, en este caso el orden es al revés primero van las salidas y luego las entradas.

*Podemos verificar que el código corresponde con nuestro modelo mediante el RTL viewer. Esta herramienta la utilizamos para verificar que nuestro código este escrito correctamente, allí vemos las conexiones que hemos realizado

![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/Sumador%20primitive.PNG)

2.Generamos un almacenamiento de 2 bit.
Aplicamos el procedimiento visto en el numeral anterior, sin embargo, esta vez añadimos otra funcion llamada reg.
Este reg permite crear un almacenamiento de el número de bits que deseemos abriendo parentesis cuadrados e ingresando los bits correspondientes en este caso como necesitamos 2 sería [1:0] es decir el bit 1 y el bit 0
Cuando queremos referirnos a una posición simplemente ponemos el número de esta posición entre parentesis.
El reg permite almacenar un dato y posteriormente ser reescrito cuando le damos otro valor.
![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/sum1bcc.PNG) 

3.Hacemos que nuestras entradas cambien cada 200, 400 y 800ns, esto mediante nuestro simulador RTL, obteniendo los siguientes resultados que son los esperados las entradas son sumadas, para comprender mejor nos podemos fijar del 00000 en adelante, vemos que cuando las entradas son 111 la suma es 1 y nuestro carry muestra un 1.

![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/Sumador%201%20bit%20800ns.PNG)

4.Adicionalmente podemos ver un diagrama de nuestro sumador, aquí podemos ver que nuestro diagrama muestra las entradas correspondientes de dos bit, y la salida va con S y Cout como se hizo en el código.

![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/sumador%201%20bit%20diagrama.PNG)


Sumador 4 bits.
Aplicando lo visto en los numerales anteriores lo incorporamos a un nuevo concepto que es instanciación.
Una vez realizados los pasos similar a los efectuados en los numerales anteriores procedemos a la instanciación.
La instanciación consiste en tomar una variable pasada (utilizada en otro modulo) y asignarla a una actual (utilizada en nuestro modulo) este está estructurado de la siguiente manera Sum1bcc(nombre del modulo anterior) nombre de la función actual(s0) (anteriormente usado pero con nombre nuevo)A pasado Xi (actual). Adicionalmente aplicamos el concepto de las posiciones.
![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/sum4bcc.PNG)

EL sumador de 4 bits se ve de la siguiente manera. Vemos que la salida es de 4 bits y las conexiones corresponden con el modelo planteado por el profesor.

![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/Sumador%204%20bits%20diagrama.PNG)

Podemos ver la simulación RTL, el funcionamiento es similar al mostrado en los sumadores anteriores, en este caso la visualización no tiene suficiente zoom para ver los valores de abajo, debemos tener eso en cuenta para las simulaciones posteriores. 

![conex](https://github.com/unal-edigital1-lab/lab00-NisefolesVargas/blob/master/wave%20testbench.PNG)




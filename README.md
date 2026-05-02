
# **FUNDAMENTOS DE LA PROGRAMACION.**
***
## **UNIDAD 1**
***
## DATOS DEL AUTOR

![Imagen](https://www.unl.edu.ec/sites/default/files/inline-images/unl_0_2.png) 

**FACULTAD DE LA ENERGÍA, LAS INDUSTRIAS Y LOS RECURSOS NATURALES NO RENOVABLES**

**CARRERA COMPUTACIÓN**

**Estudiante:** Karen Valenitna Lalangui Lapo 

**Ciclo:** 1er Ciclo 

**Docente:** Ing. Lissette López

**Periódo Académico:** Marzo 2026 - Agosto 2026

***

## CONTENIDOS 
***
**1. ALGORITMO**

![Imagen](https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/Algoritmo.png?raw=true.png)

- **Tipos de datos:**
  - 🔢*Enteros*: Son valores que no tienen punto decimal, pueden ser negativos o positivos, se incluye el 0
  - 📔*Reales*: Valores que tienen punto decimal, se incluye el 0
  - 🏧*Carácter*: Conformados por un solo carácter, van entre comillas dobles, pueden ser letras, números o símbolos, “x”, “3” etc
  - 🔤*Cadenas*: También conocidos como alfanuméricos, la formación de muchos caracteres forma una cadena
  - 🧐*Lógicos*: Determina si algo es verdadero o falso

- **Pseudocodigo:**
  - Es utilizado para entender la estructura de un código. Se caracteriza por utilizar una sintaxis flexible y un lenguaje cercano al natural. Entre las herramientas mas utlizadas para este propósito podemos mencionar a [Pseint](https://pseint.sourceforge.net/).

- **Diagramas de flujo:**
  - Emplea formas para la representación visual del algoritmo.

- **Pruebas de escritorio:**
  - Mediante la pueba de escritorio podemos verificar si la codificación de nuestro código es correcto.

- **¿Qué es un lenguaje de programación?**
  - Los lenguajes de programación permiten a los desarrolladores crear software mediante instrucciones que la computadora puede interpretar. Todo lenguaje de computador entiende lenguaje binario, 1 y 0.
    Los lenguajes de programación pueden dividirse en dos categorías:
    - *Lenguajes compilados:*
      Traduce completamente el código fuente antes de ejecutarlo, generando un archivo ejecutable, por ejemplo: C/c++, Pascal, etc
      
    - *Lenguajes interpretados:*
      Ejecuta el código línea por línea en tiempo real, por ejemplo: Python, JavaScrip, etc.
***
**2. PROGRAMACION POR BLOQUES**
- Es un método utilizado para desarrollar la lógica de programación, se caracteriza por utilizar piezas visules. Analogicamente, es como armar un rompecabezas. Entre las herramientas más utlizadas para este propósito podemos mencionar a [pilas bloques](https://pilasbloques.program.ar/online/#/)

![Programacion por bloques](https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/Programacion%20por%20bloques.png?raw=true.png)

***

## **EJERCICIOS CON ESTRUCTURA SECUENCIAL: LENGUAJE C**
***

**1. Planteamiento del problema:**
- En una concesionaria de vehículos se realizaron tres ventas de vehículos de alta gama a 3 clientes. Cada vehículo cuesta 30000, 29000 y 33000 usd. El gerente desea saber cuál es porcentaje (comisión) que cada vendedor se llevaría, lo que le pagará a cada uno de ellos (considerando el 4% por cada vendedor) y lo que le pagará en conjunto (total).

**2. Analisis del problema:**
- Datos de entrada:
  - Este ejercicio no tiene datos de entrada, ya que nos dan las variables con un valor asignado.

- Proceso:

  **c1** = v1 * porcentaje;

  **c2** = v2 * porcentaje;

  **c3** = v3 * porcentaje;

  **ct** = c1 + c2 + c3;

   - *Donde **c** es comison, y **v** es vehiculo*

- Datos de salida:
  - comision total(ct)

**3. Diseño del algoritmo: Diagrama de flujo y Pseudocodigo**
- Pseudocodigo:
~~~
Algoritmo Ventas
	
	//Variables
	Definir v1, v2, v3 Como Real;
	Definir c1, c2, c3, ct Como Real;
	Definir porcentaje como real; 
	
	// Asignar valores
	v1=30000;
	v2=29000;
	v3=33000;
	porcentaje=0.04;
	
	// Proceso
	c1 = v1 * porcentaje;
    c2 = v2 * porcentaje;
    c3 = v3 * porcentaje;
    ct = c1 + c2 + c3;
	
	//Datos de salida
	Escribir ("Comision 1 es:"), c1;
	Escribir ("Comision 2 es:"), c2;
	Escribir ("Comision 3 es:"), c3;
	Escribir ("Comision total es:"), ct;
	
FinAlgoritmo
~~~

- Diagrama de flujo:
  
![Imagen](https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/Ejercicio_Diagrama%20de%20flujo.png?raw=true)

**4. Codificacion: Código fuente**
~~~
#include <stdio.h>
int main(){

    float v1 = 30000; 
    float v2 = 29000;
    float v3 = 33000;
    float porcentaje = 0.04;
    float c1, c2, c3, ct; 

    c1 = v1 * porcentaje;
    c2 = v2 * porcentaje;
    c3 = v3 * porcentaje;
    ct = c1 + c2 + c3;

    printf("Comision 1 es: %.1f\n", c1);
    printf("Comision 2 es: %.1f\n", c2);
    printf("Comision 3 es: %.1f\n", c3);
    printf("Comision total es: %.1f\n", ct);
    
    return 0; 
}
~~~

**5. Prueba de escritorio:**

![Imagen](https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/Prueba%20de%20escritorio.png?raw=true)

| c1                 |          c2        |        c3           | total |
|--------------------|--------------------|---------------------|-------|
|30000 * (0.04)= 1200|29000 * (0.04)= 1160|33000 * (0.04)= 1320 | 3680  |

***
## PRINCIPALES DIFICULTADES Y REFLEXION CRITICA EN LA PRACTICA DE LOS CONTENIDOS 

**1. Dificultades:**
- Confusión en la interpretación del problema
- Dificultades en identificar variables y el uso de sintaxis en el programa C.

**2. Reflexion critica:**
- Estas difucultades fueron corregidas mediante el analisis de ejercicios prácticos revisados en clase, y la revision de la teoria. Asi mismo, se realizaron diversos ejercicios de práctica para identificar variables y el uso de la sintaxis del programa C.  

  
  
 




   



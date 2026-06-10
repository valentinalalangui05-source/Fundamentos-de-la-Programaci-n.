## **UNIDAD 2**
***

## **CONTENIDOS**
1. [Estructuras condicionales](#estructuras-condicionales)
   - [Tipos de estructuras condicionales](#tipos-de-estructuras-condicionales)
2. [Estructuras repetitivas](#estructuras-repetitivas)
   - [Tipos de estructuras repetitivas](#tipos-de-estructuras-repetitivas)
3. [Ejercicio práctico](#ejercicio-practico)
   - [Planteamiento del problema](planteamiento-del-problema)
   - [Análisis del problema](analisis-del-problema)
   - [Diagrama de flujo](diagrama-de-flujo)
   - [Código fuente](codigo-fuente)
   - [Validacion del problema](validacion-del-problema)
***

## **ESTRUCTURAS CONDICIONALES**
### **Tipos de estructuras condicionales**
#### **1. Condicional simple:**
- Permite ejecutar una acción solamente cuando la condición es verdadera.
  
#### **Pseudocodigo**
```
Algoritmo simple
	
	Si (CONDICION ) Entonces
		instruccion1
		intruccion2
		...
	Fin Si
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/condicion_simple.jpg?raw=true" width="300">

#### **2. Condicional doble:**
- Nos permite elegir entre dos caminos posibles, es decir, evalua dos posibles casos. 
  
#### **Pseudocodigo**
```
Algoritmo doble
	
	Si (CONDICION ) Entonces
		instruccion1
		intruccion2
		...
	si_no
		instruccion1
		intruccion2
		...
	Fin Si
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/condicion_doble.jpg?raw=true" width="500">

#### **3. Condicional multiple:**
- Permite evaluar varias condiciones. 
  
#### **Pseudocodigo**
```
Algoritmo multiple
	Segun variable_numerica Hacer
		opcion_1:
			secuencia_de_acciones_1
		opcion_2:
			secuencia_de_acciones_2
		opcion_3:
			secuencia_de_acciones_3
		De Otro Modo:
			secuencia_de_acciones_dom
	Fin Segun
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/condicion_multiple.jpg?raw=true" width="700">

***

## **ESTRUCTURAS REPETITIVAS**
### **Tipos de estructuras repetitivas**
#### **1. Ciclo mientras(while):**
- Permite repetir un número de lı́neas de código mientras se cumpla una determinada condición.
  
#### **Pseudocodigo**
```
Algoritmo mientras
	Mientras (expresion_logica) Hacer
		secuencia_de_acciones
	Fin Mientras
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/ciclo-while.jpg?raw=true" width="300">

#### **1. Ciclo hacer...mientras(do...while):**
- En ocasiones se necesita que el conjunto de sentencias se ejecuten al menos una vez sea cual sea el valor de la expresión o condición evaluada.
  
#### **Pseudocodigo**
```
Algoritmo dowhile
	Hacer
		secuencia_de_acciones
	mientras(expresion_logica)
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/ciclo-do-while.png?raw=true" width="400">

#### **1. Ciclo para(for):**
- Es adecuado utilizar en un bucle for cuando el desarrollador conoce de antemano la cantidad de iteraciones a ejecuatar.
  
#### **Pseudocodigo**
```
Algoritmo for
	Para (inicializador) Hasta (condicion) [aumento/decremento] Hacer
		secuencia_de_acciones
	Fin Para
FinAlgoritmo
```
#### **Diagrama de flujo**
<img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/ciclo-for.jpg?raw=true" width="300">

***

## **3. EJERCICIO PRACTICO
#### **1. Planteamiento del problema:**

- Una institución educativa necesita un sistema que permita calcular la nota final de un estudiante en las diferentes asignaturas que cursa durante un periodo académico.
  - El programa solicitará al usuario la cantidad de asignaturas que desea evaluar. Para cada asignatura se ingresarán tres calificaciones obtenidas durante el curso(caliificaciones por unidad).
  - El sistema realizará el cálculo del promedio final mediante la suma de las tres notas dividida entre tres.
  - Ademas, el programa contará con validaciones para evitar el ingreso de valores incorrectos, permitiendo únicamente notas dentro del rango establecido de 0 a 10.
  - Una vez calculado el promedio, el sistema determinará si el estudiante aprueba o reprueba la asignatura, considerando como nota mínima de aprobación un promedio igual o mayor a 7.


#### **2. Análisis del problema:**

- **Datos de entrada:**
  - Número de asignaturas que se van a calcular.
  - Contador de asignaturas (se genera en el ciclo).
  - Primera nota de la asignatura.
  - Segunda nota de la asignatura.
  - Tercera nota de la asignatura.

- **Proceso:**
  - Valida que el número de asignaturas sea mayor que 0.
  - Valida que las notas ingresadas sean correctas entre 0 y 10:
  - Deben estar dentro del rango permitido.
  - Calcula el promedio: ***pT= num1+num2+num3 /3*** 
  - Compara el promedio minimo para determinar si el estudante aprobo (minimo 7) o reprobo (menor a 7).

- **Datos de salida:**
  - Nota final por cada asigantura y el mensaje de aprobado i reprobado.
  

#### **3. Diagrama de flujo:**
![Imagen](https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/Ejercicio-practico.png?raw=true)
#### **4. Código fuente:**

```
#include <stdio.h>
int main(){

    float num1, num2, num3, pT;
    int i, eT;

    do{
        printf("Ingrese el numero de asignaturas: ");
        scanf("%d", &eT);
    }while(eT<=0);

    for(i=1; i<=eT; i++ ){
        printf("=================================\n");
        printf("Asigantura %d\n", i);
        printf("=================================\n");

        do{
            printf("Ingresar nota 1: ");
            scanf("%f", &num1);

            if(num1<0 || num1 >10){
                printf("ERROR\n");
            }
        }while(num1<0 || num1 >10);

        do{
            printf("Ingresar nota 2: ");
            scanf("%f", &num2);

            if(num2<0 || num2 >10){
                printf("ERROR\n");
            }
        }while(num2<0 || num2 >10);

        do{
            printf("Ingresar nota 3: ");
            scanf("%f", &num3);

            if(num3<0 || num3 >10){
                printf("ERROR\n");
            }
        }while(num3<0 || num3 >10);

        pT=(num1+num2+num3)/3;
        printf("%.2f\n", pT);

        if(pT>=7){
            printf("Nota aprobada\n");
        }
        if(pT<7){
            printf("Reprobado\n");

        }
    }

    return 0;   
}
```

#### **5. Validacion del problema:**

| **i** | **eT** | **num1** | **num2** | **num3** | **pT** |
|-------|--------|----------|----------|----------|--------|
|   1   |    2   |    10    |    10    |    5     |  8.33  | Aprobado  |
|   2   |        |    7     |     5    |    4     |  5.33  | Reprobado |

![Imagen]()







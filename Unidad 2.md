## **UNIDAD 2**
***

## **CONTENIDOS**
1. [Estructuras condicionales](#estructuras-condicionales)
   - [Tipos de estructuras condicionales](#tipos-de-estructuras-condicionales)

2. [Estructuras repetitivas](#estructuras-repetitivas)
   - [Tipos de estructuras repetitivas](#tipos-de-estructuras-repetitivas)
   - [Estructura en diagrama de flujo](#estructura-en-diagrama-de-flujo-repetitivo)
   - [Estructura en pseudocódigo](#estructura-en-pseudocódigo-repetitivo)
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









# 📚 Unidad 3

> **Objetivo:** Comprender qué es la modularidad, cómo funcionan los parámetros en las funciones y cómo utilizar los diferentes tipos de arreglos en Python.

***

## 📑 Índice

- [1. Modularidad](#1-modularidad)
- [2. Pase de Parámetros](#2-pase-de-parámetros)
  - [2.1 Por Valor](#21-pase-por-valor)
  - [2.2 Por Referencia](#22-pase-por-referencia)
- [3. Arreglos](#3-arreglos)
- [4. Tipos de Arreglos](#4-tipos-de-arreglos)
- [5. Dificultades Encontradas](#5-principales-dificultades)
- [6. Reflexión Crítica](#6-reflexión-crítica)

---

## 1. Modularidad

### 📖 ¿Qué es?

La **modularidad** consiste en dividir un programa en pequeñas partes llamadas **funciones** o **módulos**, donde cada una cumple una tarea específica. Existe una frase llamada **divide y venceras**

### ¿Por qué utilizar modularidad?

| Ventaja | Descripción |
|---------|-------------|
| ♻️ Reutilización | Una función puede utilizarse varias veces. |
| 🛠️ Mantenimiento | Es más fácil corregir errores cuando se trabaja en equipo. |
| 👨‍💻 Trabajo colaborativo | Cada integrante puede desarrollar un módulo diferente. |
| 📚 Legibilidad | El código es más fácil de entender. |

***

### Diagrama

> [!NOTA]
> Como programadores, es fundamental realizar un análisis visual antes de escribir código, ya que nos permite organizar nuestras ideas, comprender mejor el problema y tener una visión clara de la solución que vamos a implementar.

***

## Ejemplo

```
nombre = input("Ingresa tu nombre")

def saludar(nombre):
    print("Hola", nombre)

saludar(nombre)

```

### Resultado

```
Ingresa tu nombre: Karen
Hola karen
```

---

## 2. Pase de Parámetros

Cuando llamamos una función podemos enviar información.

Existen dos formas muy utilizadas para entender este proceso.

---

# 2.1 Pase por Valor

La función trabaja con una **copia** del dato, es decir, se envía el contenido de la variable, peor la varible no se altera. 

### Código

```
x = 20
def sumar(numero):
    numero += 10
    print(numero)

sumar(x)
print(x)
```

### Resultado

```
30
20
```
---


# 2.2 Pase por Referencia

Se envía la dirección de memoria de la variable es decir si dentro de la función se realiza algún cambio pues la variable fuera de la función sufrirá este cambio.

> [!NOTA]
> Si el objeto es mutable (como una lista o un diccionario), sus cambios pueden verse fuera de la función; si es inmutable (como un entero, una cadena o una tupla), las modificaciones dentro de la función no afectan a la variable original.

### Código

```
datos = [10,20,30]

def agregar(lista):
    lista.append(50)
agregar(datos)

print(datos)
```

### Resultado

```
[10,20,30,50]
```

***

# 3. Arreglos

## ¿Qué son?

Un arreglo es una estructura que permite almacenar varios datos bajo una misma variable.

En Python normalmente se utilizan las **listas**.

```
numeros = [5,10,15,20]
```

***

# 4. Tipos de Arreglos

## 🔹 Arreglo Unidimensional

```
colores = ["Rojo","Azul","Verde"]
```
---

## 🔹 Arreglo Bidimensional

```python
matriz = [
    [1,2,3],
    [4,5,6]
]
```
---

## 🔹 Arreglo Tridimensional

```
cubo = [
    [
        [1,2],
        [3,4]
    ],
    [
        [5,6],
        [7,8]
    ]
]
```
---

# 📝 Ejercicio Rápido

¿Puedes adivinar el resultado?

```
lista = [1,2]

def cambiar(x):
    x.append(3)

cambiar(lista)

print(lista)
```

<details>

<summary>✅ Ver respuesta</summary>

```
[1,2,3]
```

Porque las listas son mutables.

</details>

---

## 5. Principales Dificultades

| Problema | Solución |
|----------|----------|
| Confusión entre parámetros | Practicar con funciones pequeñas |
| Errores de índices | Dibujar el arreglo antes de programar |
| Variables locales | Identificar el alcance de cada variable |
| Matrices | Recorrerlas usando ciclos anidados |

---

## 6. Reflexión Crítica

La modularidad permite construir programas más organizados y fáciles de mantener, mientras que los arreglos ofrecen una forma eficiente de almacenar y manipular información.

Durante el aprendizaje, uno de los mayores desafíos es comprender cómo se comportan los parámetros y cómo acceder correctamente a los elementos de los arreglos, especialmente en estructuras multidimensionales. Sin embargo, con la práctica constante, estos conceptos se convierten en herramientas fundamentales para desarrollar aplicaciones más robustas, escalables y fáciles de mantener.

---

# 🎯 Conclusiones

- ✅ La modularidad divide problemas grandes en soluciones pequeñas.
- ✅ Las funciones favorecen la reutilización del código.
- ✅ El paso por valor y por referencia determina cómo se modifican los datos.
- ✅ Los arreglos permiten organizar información de forma eficiente.
- ✅ Dominar estos conceptos facilita el aprendizaje de estructuras de datos y programación orientada a objetos.



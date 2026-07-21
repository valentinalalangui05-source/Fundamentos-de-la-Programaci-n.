# 📚 Unidad 3

> **Objetivo:** Comprender qué es la modularidad, cómo funcionan los parámetros en las funciones y cómo utilizar los diferentes tipos de arreglos en Python/Progrma C.

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

### Ejemplo

```
#include <stdio.h>

void saludar(char nombre[]) {
    printf("Hola %s\n", nombre);
}

int main() {
    char nombre[50];

    printf("Ingresa tu nombre: ");
    scanf("%49s", nombre);

    saludar(nombre);

    return 0;
}

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

## 2.1 Pase por Valor

La función trabaja con una **copia** del dato, es decir, se envía el contenido de la variable, peor la varible no se altera. 

### Código

```
#include <stdio.h>

void sumar(int numero){
    numero += 10;
    printf("%d\n", numero);
}

int main(){
    int x = 20;

    sumar(x);

    printf("%d\n", x);

    return 0;
}
```

### Resultado

```
30
20
```
---


## 2.2 Pase por Referencia

Se envía la dirección de memoria de la variable es decir si dentro de la función se realiza algún cambio pues la variable fuera de la función sufrirá este cambio.
> [!NOTE]
> En Python, los objetos **mutables** (como las listas y los diccionarios) pueden modificarse dentro de una función, y esos cambios se reflejan fuera de ella. En cambio, los objetos **inmutables** (como los enteros, las cadenas y las tuplas) no pueden modificarse; cualquier cambio dentro de la función crea un nuevo objeto, por lo que la variable original permanece sin cambios.

### Código
- Programa C
  
```

#include <stdio.h>

void agregar(int lista[], int *tam)
{
    lista[*tam] = 50;
    (*tam)++;
}

int main()
{
    int datos[10] = {10, 20, 30};
    int tamaño = 3;

    agregar(datos, &tamaño);

    printf("Datos: ");

    for(int i = 0; i < tamaño; i++)
    {
        printf("%d ", datos[i]);
    }

    return 0;
}

```
- Python
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

## 3. Arreglos

### ¿Qué son?

Un arreglo es una estructura que permite almacenar varios datos bajo una misma variable.

```
numeros = [5,10,15,20]
```

***

## 4. Tipos de Arreglos

### Arreglo Unidimensional

```
colores = ["Rojo","Azul","Verde"]
```
---

### Arreglo Bidimensional

```
matriz = [
    [1,2,3],
    [4,5,6]
]
```
---

### Arreglo Tridimensional

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

## 📝 Ejercicio Practico: Funciones 

**Contextualizacion:** 
Una empresa desea calcular el salario semanal de sus empleados. El programa debe utilizar funciones para:

- Leer el nombre del empleado.
- Leer las horas trabajadas.
- Leer el pago por hora.
- Calcular el salario.
- Mostrar toda la información.

Condición:
- Si el empleado trabaja más de 40 horas, las horas adicionales se pagan al 150% del valor de la hora normal.

```
#include <stdio.h>

void leerDatos(char nombre[], float *horas, float *pagoHora);
float calcularSalario(float horas, float pagoHora);
void mostrarDatos(char nombre[], float horas, float pagoHora, float salario);

int main()
{
    char nombre[30];
    float horas, pagoHora, salario;

    leerDatos(nombre, &horas, &pagoHora);

    salario = calcularSalario(horas, pagoHora);

    mostrarDatos(nombre, horas, pagoHora, salario);

    return 0;
}

// Leer datos
void leerDatos(char nombre[], float *horas, float *pagoHora)
{
    printf("Nombre del empleado: ");
    scanf("%s", nombre);

    printf("Horas trabajadas: ");
    scanf("%f", horas);

    printf("Pago por hora: ");
    scanf("%f", pagoHora);
}

// Calcular salario
float calcularSalario(float horas, float pagoHora)
{
    float salario;

    if(horas <= 40)
        salario = horas * pagoHora;
    else
        salario = (40 * pagoHora) + ((horas - 40) * pagoHora * 1.5);

    return salario;
}

// Mostrar resultados
void mostrarDatos(char nombre[], float horas, float pagoHora, float salario)
{
    printf("\n===== REPORTE =====\n");
    printf("Empleado: %s\n", nombre);
    printf("Horas trabajadas: %.2f\n", horas);
    printf("Pago por hora: $%.2f\n", pagoHora);
    printf("Salario total: $%.2f\n", salario);
}
```

<details>
<summary>✅ Ver respuesta</summary>

<br>

<p align="center">
  <img src="https://github.com/valentinalalangui05-source/Fundamentos-de-la-Programaci-n./blob/main/imagenes/Captura%20de%20pantalla%202026-07-21%20121543.png" width="900">
</p>

</details>

---
## 📝 Ejercicio Practico: Arreglos

### 1. Arreglo Unidimensional (1D)

- Guarda las edades de cinco personas.

```c
#include <stdio.h>

int main() {
    int edades[5] = {18, 20, 22, 19, 21};

    printf("Edades:\n");

    for (int i = 0; i < 5; i++) {
        printf("%d\n", edades[i]);
    }

    return 0;
}
```

---

### 2. Arreglo Bidimensional (2D)

- Guarda las ventas de tres días y cuatro productos.

```c
#include <stdio.h>

int main() {
    int ventas[3][4] = {
        {10, 15, 12, 20},
        {8, 18, 14, 16},
        {11, 13, 17, 19}
    };

    printf("Ventas:\n");

    for (int i = 0; i < 3; i++) {
        printf("Día %d: ", i + 1);

        for (int j = 0; j < 4; j++) {
            printf("%d ", ventas[i][j]);
        }

        printf("\n");
    }

    return 0;
}
```

---

### 3. Arreglo Tridimensional (3D)

- Guarda la temperatura de dos ciudades, dos días y tres horarios.

```c
#include <stdio.h>

int main() {
    int temperatura[2][2][3] = {
        {
            {20, 24, 18},
            {21, 25, 19}
        },
        {
            {28, 31, 26},
            {29, 32, 27}
        }
    };

    for (int ciudad = 0; ciudad < 2; ciudad++) {
        printf("Ciudad %d\n", ciudad + 1);

        for (int dia = 0; dia < 2; dia++) {
            printf(" Día %d: ", dia + 1);

            for (int hora = 0; hora < 3; hora++) {
                printf("%d ", temperatura[ciudad][dia][hora]);
            }

            printf("\n");
        }

        printf("\n");
    }

    return 0;
}
```

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


⬅️[Volver a inicio](README.md)



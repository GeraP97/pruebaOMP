# Suma de Arreglos en Paralelo con OpenMP

Este proyecto implementa un programa en C++ que utiliza la librería **OpenMP** para realizar la suma de dos arreglos de forma paralela. El objetivo principal es demostrar cómo el paralelismo puede mejorar el rendimiento al manejar grandes cantidades de datos.

## Descripción

El programa realiza las siguientes operaciones:
1. Crea dos arreglos (`a` y `b`) con **N** elementos.
2. Inicializa los arreglos con valores calculados mediante expresiones matemáticas.
3. Utiliza OpenMP para paralelizar la suma elemento por elemento de los arreglos y almacena el resultado en un tercer arreglo (`c`).
4. Imprime los primeros elementos de los arreglos para verificar que la suma se realizó correctamente.

## Requisitos

- Visual Studio 2022 (o cualquier IDE compatible con OpenMP).
- Compilador con soporte para OpenMP.
- Librerías estándar de C++.

## Configuración del proyecto

1. **Habilitar OpenMP en Visual Studio**:
   - Ve a las propiedades del proyecto.
   - En **Configuración de C/C++ → Todas las opciones**, habilita la opción **Soporte de OpenMP** (`/openmp`).

2. **Compilación**:
   - Asegúrate de que OpenMP esté habilitado antes de compilar.

## Estructura del código

### Función principal

- **Inicialización de arreglos**: Los valores se calculan con fórmulas simples (`a[i] = i * 10`, `b[i] = (i + 3) * 3.7`).
- **Paralelización**: Se utiliza `#pragma omp parallel for` para dividir las iteraciones del bucle de suma entre varios hilos.

### Función auxiliar: `imprimeArreglo`
- Imprime los primeros 10 elementos de un arreglo para verificar los resultados.

## Uso

1. Clona este repositorio:
2. Abre el proyecto en Visual Studio.
3. Configura OpenMP y compila el programa.
4. Ejecuta el programa para ver los resultados.

## Resultados

Al ejecutar el programa, obtendrás una salida similar a esta (para N = 1000):

Sumando Arreglos en Paralelo

Imprimiendo los primeros 10 elementos del arreglo a:
0 - 10 - 20 - 30 - 40 - 50 - 60 - 70 - 80 - 90 -

Imprimiendo los primeros 10 elementos del arreglo b:
11.1 - 14.8 - 18.5 - 22.2 - 25.9 - 29.6 - 33.3 - 37 - 40.7 - 44.4 -

Imprimiendo los primeros 10 elementos del arreglo c:
11.1 - 24.8 - 38.5 - 52.2 - 65.9 - 79.6 - 93.3 - 107 - 120.7 - 134.4 -

Reflexión

La programación paralela con OpenMP permite optimizar tareas intensivas en cálculo, como esta suma de arreglos. Este ejemplo es una introducción al uso de OpenMP para tareas simples, pero puede escalarse a problemas más complejos, como simulaciones científicas o análisis de grandes volúmenes de datos.
